# AI Coding Assistant Prompt Templates

A collection of reusable prompts for working with AI coding assistants (Copilot, Claude Code, etc.). Adapt the bracketed sections `[like this]` to your specific situation.

---

## Table of Contents

1. [Codebase Understanding](#1-codebase-understanding)
2. [Improvement Opportunities](#2-improvement-opportunities)
3. [Writing Tests](#3-writing-tests)
4. [Debugging](#4-debugging)
5. [Code Review](#5-code-review)
6. [Documentation](#6-documentation)
7. [Refactoring](#7-refactoring)

---

## 1. Codebase Understanding

### Analyze a Specific Directory

```
Analyze the [/src/services/billing] directory. I need you to:

1. Map out the key files and their responsibilities
2. Trace how data flows through this module (entry points → processing → outputs)
3. Identify the external dependencies (other internal modules, third-party packages, APIs)
4. Summarize the core business logic in plain English

Context: [This handles invoice generation for recruitment clients. I inherited this code and need to modify it for a new pricing model.]
```

### Onboarding to Unfamiliar Code

```
I'm new to this codebase. Walk me through [/src/core]:

1. What is the main purpose of this module?
2. What are the entry points (where does execution typically start)?
3. What are the key abstractions/classes I need to understand?
4. What would break if I deleted this module?

Context: [I'm taking over maintenance from a colleague who left. No documentation exists.]
```

### Trace a Specific Feature

```
Trace how [user authentication] works in this codebase:

1. Starting from the API endpoint, follow the code path
2. Identify each file/function involved
3. Note where external services are called
4. Highlight any non-obvious logic or gotchas

Context: [I need to add MFA support and want to understand the current flow first.]
```

---

## 2. Improvement Opportunities

### General Code Quality Review

```
Review [/src/services/billing] for improvement opportunities. Focus on:

1. Code duplication that could be consolidated
2. Functions doing too many things (candidates for decomposition)
3. Overly complex logic that could be simplified
4. Error handling gaps or inconsistencies
5. Naming or structure that hurts readability

Prioritise suggestions by impact—what would give the most maintainability benefit for the effort?

Context: [This module rarely changes so major refactors aren't justified, but I want to clean it up before adding new features.]
```

### Performance Review

```
Review [/src/services/data_processor.py] for performance issues:

1. Identify potential bottlenecks (N+1 queries, unnecessary loops, blocking calls)
2. Check for memory inefficiencies (loading large datasets fully into memory, etc.)
3. Look for opportunities to add caching
4. Flag any operations that should be async but aren't

Context: [This processes ~10k records daily. Currently takes 45 minutes, need to get under 10.]
```

### Security Review

```
Review [/src/api/auth] for security concerns:

1. Input validation gaps
2. Authentication/authorization weaknesses
3. Sensitive data exposure (logging, error messages)
4. Injection vulnerabilities (SQL, command, etc.)
5. Dependency vulnerabilities if obvious

Context: [This is an internal tool but will soon be exposed to external clients.]
```

---

## 3. Writing Tests

### Add Tests to Existing Code

```
Write tests for [/src/services/billing/invoice_generator.py]

Cover:
1. Happy path for the main functions
2. Edge cases (empty inputs, null values, boundary conditions)
3. Error handling (what should raise exceptions vs return gracefully)

Use pytest. Match the testing patterns already in /tests if any exist.

Context: [This function calculates prorated charges. Key business rule: partial months round up to full days.]
```

### Bootstrap Tests for Untested Code

```
I need to add tests to [/src/services/billing] which currently has no test coverage.

1. First, identify which files/functions are highest priority to test (most complex, most critical, or most likely to break)
2. Then write tests for the top 3 priorities
3. Use pytest with fixtures where appropriate

Context: [This is a legacy module I inherited. I'm about to modify the pricing logic, so I want tests as a safety net before I touch anything.]
```

### Test-Driven Development (Tests First)

```
I need to implement a function that [validates candidate submissions and returns structured errors].

Write the tests first. Cover:
- Expected inputs and outputs
- Edge cases: [empty submissions, missing required fields, invalid file formats]
- Error conditions: [should return error dict, not raise exceptions]

Don't write the implementation yet—just the tests. I'll implement against them.

Context: [This will be called by the API layer. Invalid submissions should return a structured error dict with field-level messages.]
```

### Review and Improve Existing Tests

```
Review the tests in [/tests/services/test_billing.py]

Identify:
1. Gaps in coverage (what scenarios aren't tested)
2. Brittle tests (too coupled to implementation details)
3. Redundant tests (testing the same thing multiple ways)
4. Missing edge cases

Then suggest specific improvements, prioritised by risk.
```

### Integration/End-to-End Tests

```
Write integration tests for the [invoice generation] workflow:

Entry point: [POST /api/invoices]
Dependencies: [PostgreSQL, Stripe API]

1. Test the full flow from request to database state
2. Mock external services (Stripe) but use a real test database
3. Cover: successful creation, validation failures, payment failures

Context: [We use pytest-docker for spinning up Postgres. Stripe calls should be mocked with responses library.]
```

### Add Tests for a Bug Fix

```
I'm fixing a bug where [invoices show wrong amounts for partial months].

1. First, write a failing test that reproduces the bug
2. The test should capture the exact scenario: [subscription started mid-month, cancelled after 10 days]
3. Expected behaviour: [charge should be prorated to 10/30 of monthly rate]

Context: [Current code charges full month. Don't fix the bug yet, just write the test.]
```

---

## 4. Debugging

### Diagnose a Specific Error

```
I'm getting this error:

[Paste full stack trace here]

1. Explain what's causing this error
2. Trace back to the root cause (not just the immediate trigger)
3. Suggest fixes, ordered by likelihood of being correct

Context: [This started happening after I added the new pricing tier logic. Works fine for existing customers, fails for new signups.]
```

### Debug Unexpected Behaviour

```
[Function/endpoint] is behaving unexpectedly:

Expected: [Invoice total should be $150]
Actual: [Invoice total is $0]

Relevant code is in [/src/services/billing/calculator.py]

1. Identify where the logic diverges from expected
2. Add strategic logging/print statements to narrow down the issue
3. Suggest the fix once identified

Context: [This only happens when discount codes are applied. Full-price invoices work correctly.]
```

### Debug Performance Issue

```
[/src/jobs/daily_report.py] is running slowly (45 mins, should be <10).

1. Profile the code and identify the slowest operations
2. Check for common issues: N+1 queries, unnecessary loops, blocking I/O
3. Suggest optimisations in priority order

Context: [This runs nightly, processes ~10k records, writes to PostgreSQL and sends summary emails.]
```

---

## 5. Code Review

### Review a Specific File/PR

```
Review [/src/services/billing/new_pricing.py] as if you're a senior engineer:

1. Correctness: Will this work as intended? Any logic errors?
2. Edge cases: What inputs might break this?
3. Maintainability: Is this easy to understand and modify later?
4. Performance: Any obvious inefficiencies?
5. Style: Does it follow Python conventions?

Be specific—point to line numbers and suggest concrete changes.

Context: [This is a new pricing module I wrote. First time implementing tiered pricing logic.]
```

### Review for Production Readiness

```
Review [/src/api/webhooks/stripe.py] for production readiness:

1. Error handling: What happens when things fail? Are failures recoverable?
2. Logging: Is there enough to debug issues? Too much noise?
3. Idempotency: Can this safely handle duplicate requests?
4. Timeouts: Are external calls properly bounded?
5. Secrets: Are credentials handled securely?

Context: [This webhook handler processes payment events. Currently works in dev, deploying to prod next week.]
```

---

## 6. Documentation

### Generate Documentation for a Module

```
Write documentation for [/src/services/billing]:

1. Overview: What does this module do, in 2-3 sentences?
2. Key concepts: What domain terms does a reader need to understand?
3. Main functions/classes: Document each public interface with params, returns, and example usage
4. Common patterns: How is this module typically used?

Format as markdown. Aim for helpful, not exhaustive.

Context: [This will go in our internal wiki. Audience is other devs on the team.]
```

### Add Docstrings

```
Add docstrings to all public functions in [/src/services/billing/calculator.py]

Use Google-style docstrings. Include:
- Brief description of what the function does
- Args with types and descriptions
- Returns with type and description
- Raises if any exceptions are raised intentionally

Keep them concise—prioritise clarity over completeness.
```

### Write a README

```
Write a README.md for [/src/services/billing]:

Include:
1. What this module does (one paragraph)
2. Quick start: minimal code to use the main functionality
3. Configuration: environment variables or settings needed
4. Key functions with brief descriptions
5. Common gotchas or FAQs

Context: [This is used by 3 other services in our monorepo. New team members often struggle to understand it.]
```

---

## 7. Refactoring

### Extract a Function/Class

```
The function [process_invoice] in [/src/services/billing/processor.py] is too long (150 lines).

1. Identify logical sections that could be extracted into separate functions
2. Suggest names for the extracted functions
3. Refactor the code, keeping behaviour identical

Context: [This function handles validation, calculation, and persistence all in one. I want to separate concerns.]
```

### Simplify Complex Logic

```
Simplify the logic in [/src/services/billing/discount.py]:

The current implementation has deeply nested conditionals that are hard to follow.

1. Identify the core logic buried in the complexity
2. Refactor to make the logic clearer (early returns, guard clauses, lookup tables, etc.)
3. Ensure behaviour is identical—write tests first if needed

Context: [This handles 5 different discount types. Each type was added by a different person over 2 years.]
```

### Remove Duplication

```
Find and consolidate duplicated code in [/src/services/billing]:

1. Identify patterns that appear in multiple places
2. Propose a shared abstraction (function, class, or module)
3. Refactor to use the shared code

Prioritise duplication that's likely to cause bugs (divergent copies) over cosmetic duplication.

Context: [I've noticed similar validation logic in 3 different files. When I fix a bug in one, I have to remember to fix the others.]
```

### Modernise Legacy Code

```
Modernise [/src/services/billing/legacy_calculator.py]:

Current issues:
- Uses old-style string formatting (% instead of f-strings)
- No type hints
- Uses deprecated libraries [specify if known]

1. Update to modern Python conventions (3.10+)
2. Add type hints to function signatures
3. Replace deprecated patterns

Keep behaviour identical. Flag anything that looks risky to change.

Context: [This was written in 2018 for Python 2.7, hastily ported to 3.x. Still works but hard to maintain.]
```

---

## Tips for Better Results

| Tip | Why It Helps |
|-----|--------------|
| **Specify the file path** | Prevents ambiguity about which code you mean |
| **Include context** | Your constraints shape which suggestions are practical |
| **State your goal** | "I'm adding feature X" vs "I'm debugging" changes the focus |
| **Mention existing patterns** | "Match what's in /tests" keeps consistency |
| **Set boundaries** | "Don't refactor, just identify issues" prevents unwanted changes |
| **Ask for prioritisation** | "Order by impact" makes long lists actionable |

---

## Quick Reference: Context to Include

When asking about code, consider including:

- **Your role**: "I'm the only maintainer" vs "Large team"
- **Timeline**: "Quick fix needed today" vs "Doing it right for long-term"
- **Scale**: "10 users" vs "10k daily requests"
- **Constraints**: "Must run on Python 3.8" or "Can't add new dependencies"
- **Business rules**: Domain knowledge that isn't obvious from code
- **What you've tried**: Prevents suggestions you've already ruled out

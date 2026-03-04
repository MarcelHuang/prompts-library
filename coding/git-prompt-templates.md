# Git Prompt Templates

A reusable reference for generating high-quality commit messages, PR titles, and PR descriptions using an LLM.

---

## Table of Contents

- [Commit Messages](#commit-messages)
- [Pull Request Title & Description](#pull-request-title--description)
- [Code Review Responses](#code-review-responses)
- [Release Notes](#release-notes)
- [Tips for Better Results](#tips-for-better-results)

---

## Commit Messages

### CM-1 — Diff-based (default)

Best for: everyday commits where you paste the raw diff.

```
Given the following git diff, write a concise commit message following the Conventional Commits format (type(scope): short description). Then add 2-3 bullet points explaining *why* the change was made, not just what changed. Be specific — avoid vague language like "fix bug" or "update code".

Diff:
<paste diff here>
```

---

### CM-2 — Plain English to structured message

Best for: when you know what you did but want better wording.

```
I made the following change to my codebase: <describe in plain English what you did>.

Write a commit message in Conventional Commits format. The subject line should be under 72 characters, use imperative mood ("add", "fix", "refactor" — not "added" or "fixes"), and clearly communicate intent. Suggest 3 variations ranked from most to least descriptive.
```

---

### CM-3 — Messy or large commits

Best for: commits that bundle multiple unrelated changes.

```
Here is a git diff of multiple changes bundled into one commit: <paste diff>.

First, tell me if these changes should be split into separate commits and why. If yes, suggest how to split them and write a message for each. If no, write a single cohesive commit message that honestly represents all the changes.
```

---

### CM-4 — Context-aware (for team or work projects)

Best for: professional codebases where audit trails and handoffs matter.

```
Context: <brief description of the project or module being changed>
Change: <what you did>
Reason: <why you did it — ticket, bug, requirement, etc.>

Write a commit message that a new developer joining the project 6 months from now would find genuinely useful when reading git log. Use Conventional Commits format.
```

---

### CM-5 — Quick one-liner

Best for: low-stakes commits where you just need a clean subject line fast.

```
Summarize this change as a single git commit subject line under 72 characters, imperative mood, no period at end, Conventional Commits prefix (feat/fix/refactor/chore/docs/test):

Change: <describe or paste diff>
```

---

### CM-6 — Chore and dependency updates

Best for: lockfile updates, version bumps, config changes with no logic change.

```
I updated the following dependencies / configuration. Write a commit message that clearly communicates what was updated and why, without overstating the significance of the change.

What changed: <e.g., bumped axios from 1.3 to 1.6, updated ESLint config>
Reason: <e.g., security patch, compatibility fix, team standard>

Use chore or build prefix as appropriate. Keep it factual.
```

---

### CM-7 — Reverting a commit

Best for: rollbacks where context of the original change matters.

```
I am reverting a commit. Write a commit message for the revert.

Original commit message: <paste>
Reason for reverting: <why this is being undone — regression, wrong approach, changed requirements>

The message should make it immediately clear this is a revert and why, so it's easy to trace in git log.
```

---

## Pull Request Title & Description

### PR-1 — Standard PR from diff or branch

Best for: most PRs where you have commits and a diff summary ready.

```
Given the following context, write a pull request title and description.

Branch name: <branch name>
Commits (run `git log main..HEAD --oneline`): <paste commit list>
Diff summary (run `git diff main --stat`): <paste stat output>

Title: One line, under 72 characters, imperative mood, describes the change not the implementation.

Description should include:
- **What**: What this PR does
- **Why**: The business or technical reason for the change
- **How**: Brief notes on the approach taken (skip if obvious)
- **Testing**: How this was tested or verified
- **Notes**: Any gotchas, follow-up work, or reviewer guidance

Keep it factual. No filler phrases like "This PR aims to..." or "In this PR we...".
```

---

### PR-2 — Ticket or requirement driven

Best for: PRs that trace back to a specific ticket, story, or business requirement.

```
I'm writing a PR for the following change.

Ticket/requirement: <paste ticket title or requirement>
What I changed: <describe in plain English>
Files touched: <list key files or paste `git diff --stat`>

Write a PR title and description a senior engineer would consider complete. The description should tell the reviewer what to focus on, what decisions were made and why, and what they don't need to worry about.
```

---

### PR-3 — Refactor with no behavior change

Best for: structural cleanups, renames, extractions, and code organisation changes.

```
This PR is a refactor with no functional changes. Here's what changed structurally:

<describe what was reorganised, renamed, extracted, etc.>

Write a PR title and description that:
1. Makes it immediately clear there is no behavior change
2. Explains the motivation (readability, maintainability, prep for future feature, etc.)
3. Tells the reviewer the safest way to verify nothing broke
```

---

### PR-4 — Hotfix

Best for: urgent fixes where the description will be read under pressure.

```
This is a hotfix PR. Write a title and description for it.

Problem: <what was broken and what was the impact>
Root cause: <why it happened>
Fix: <what you changed>
Risk: <any risk introduced by the fix itself>
Rollback plan: <how to undo if this makes things worse>

Be direct and clinical. This will be read under pressure.
```

---

### PR-5 — Solo project / lightweight team

Best for: personal projects or small teams where brevity matters more than ceremony.

```
Write a concise PR title and a 3-5 sentence description for this change:

<describe what you did and why>

No headers, no bullet points. Just a clear title and a short paragraph a future version of me would appreciate reading in git history.
```

---

### PR-6 — Reviewer-focused (complex PR)

Best for: large or nuanced PRs where guiding reviewer attention saves significant back-and-forth.

```
I need to write a PR description that helps the reviewer efficiently review this change.

Change summary: <what the PR does>
Most complex part: <what they should spend the most time on>
Parts that are safe to skim: <what's mechanical or low-risk>
Context they need: <any background that isn't obvious from the code>

Write a description that respects the reviewer's time and guides their attention to what matters.
```

---

### PR-7 — Draft / WIP PR

Best for: PRs opened early to get feedback before the work is complete.

```
I'm opening a draft PR to get early feedback. Write a title and description that makes clear this is a work in progress.

What's done: <what's already implemented>
What's still pending: <what's not done yet>
Specific feedback I want: <what you want reviewers to focus on now>

The title should be prefixed with [WIP] or [Draft]. The description should set expectations clearly so reviewers don't waste time reviewing incomplete parts.
```

---

### PR-8 — Self-review checklist generator

Best for: before you hit "ready for review" on any PR you wrote.

```
I've written a PR and want to self-review it before requesting a code review. Based on the following change, generate a self-review checklist tailored to this specific PR.

Change summary: <describe the PR>
Language/stack: <e.g., Python, FastAPI, PostgreSQL>

The checklist should cover correctness, edge cases, error handling, performance considerations, test coverage, and anything a reviewer would likely push back on.
```

---

## Code Review Responses

### CR-1 — Responding to review comments

Best for: drafting your reply to reviewer feedback professionally.

```
I received the following code review comment and need to respond.

Comment: <paste reviewer's comment>
My code: <paste the relevant snippet>
My intended approach: <explain why you wrote it this way>

Write a response that either:
(a) Agrees and commits to a fix — be specific about what you'll change
(b) Pushes back respectfully — explain the reasoning without being defensive
(c) Asks a clarifying question — if the comment is ambiguous

Keep it concise and professional.
```

---

### CR-2 — Writing a code review

Best for: when you're reviewing someone else's PR and want structured, useful feedback.

```
I am reviewing the following code change. Write a code review with inline comments and a summary.

Diff: <paste diff>
Context: <what this code is supposed to do>

For each comment, label it as one of: [blocker] [suggestion] [nit] [question].
End with a summary paragraph: overall assessment, what's good, what needs addressing before merge.
```

---

## Release Notes

### RN-1 — Release notes from commit log

Best for: generating user-facing or internal release notes from a list of commits.

```
Generate release notes for version <version number> based on the following commit log.

Commits:
<paste `git log vX.X.X..HEAD --oneline`>

Audience: <e.g., internal engineering team / external users / non-technical stakeholders>

Format:
- Group changes by type: New Features, Bug Fixes, Performance, Breaking Changes, Internal
- Use plain language — avoid jargon unless the audience is technical
- Omit chore/refactor commits unless they have meaningful impact
- Flag any breaking changes prominently at the top
```

---

### RN-2 — Changelog entry

Best for: adding a single entry to a CHANGELOG.md in Keep a Changelog format.

```
Write a changelog entry for the following change to add to CHANGELOG.md (Keep a Changelog format).

Version: <e.g., 1.4.2>
Date: <YYYY-MM-DD>
Changes:
- <describe each change>

Use sections: Added, Changed, Deprecated, Removed, Fixed, Security. Only include sections that apply.
```

---

## Tips for Better Results

**Feed intent, not just code.** A diff tells the model what changed. You need to tell it why — that's where the useful message comes from.

**Use Conventional Commits prefixes consistently.** The standard types are: `feat`, `fix`, `refactor`, `chore`, `docs`, `test`, `perf`, `ci`, `build`, `style`, `revert`.

**The scope is optional but useful.** `feat(auth): add OAuth2 login` is more scannable in a log than `feat: add OAuth2 login` when the codebase has multiple modules.

**For PR descriptions, Prompt PR-6 is the most underused.** Explicitly telling a reviewer where to focus attention dramatically reduces review time and back-and-forth.

**Paste `git diff --stat` instead of the full diff** when the diff is too large — the model can infer a lot from file names and change volumes.

**For long-lived projects, prefer CM-4 over CM-1.** The context-aware prompt produces messages that are genuinely useful 6 months later in git blame, not just at merge time.

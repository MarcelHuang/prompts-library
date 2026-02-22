# ACQ AI Onboarding: 14 Prompts for Sales, Marketing & Content

A comprehensive collection of AI prompts for sales optimization, content creation, and marketing automation.

---

## Table of Contents

1. [Sales Script Analysis](#1-sales-script-analysis)
2. [Newsletter Style Analyzer + Generator](#2-newsletter-style-analyzer--new-newsletter-generator)
3. [Failed Call Objection Analyzer](#3-failed-call-objection-analyzer)
4. [Universal Writing Style Analyzer](#4-universal-writing-style-analyzer)
5. [Sales Call → VSL Script Generator](#5-sales-call--vsl-script-generator)
6. [Sales Manager – Sales Call Feedback Analyzer](#6-sales-manager--sales-call-feedback-analyzer)
7. [YouTube Script Style Extractor → New Script Generator](#7-youtube-script-style-extractor--new-script-generator)
8. [Shorts Script Style Extractor → Short-Form Script Generator](#8-shorts-script-style-extractor--short-form-script-generator)
9. [Lead Magnet Generator (Video → High-Value PDF Guide)](#9-lead-magnet-generator-video--high-value-pdf-guide)
10. [Lead Magnet → Call-Booking Follow-Up Generator](#10-lead-magnet--call-booking-follow-up-generator)
11. [Offer Architect – Offer Diagnosis & Optimization Engine](#11-offer-architect--offer-diagnosis--optimization-engine)
12. [Sales Page Copy Generator](#12-sales-page-copy-generator)
13. [Sales Call Script Generator](#13-sales-call-script-generator)
14. [VSL Script Generator](#14-vsl-script-generator)

---

## Category Overview

| Category | Prompts |
|----------|---------|
| **Sales Optimization** | #1, #3, #6, #13 |
| **Content Style Analysis** | #2, #4, #7, #8 |
| **Video Script Creation** | #5, #7, #8, #14 |
| **Lead Generation** | #9, #10 |
| **Offer Development** | #11, #12, #13, #14 |

---

## 1. Sales Script Analysis

**Purpose:** Build a unified "mother script" from successful sales call transcripts.

### Input Required
- 10 full transcripts of successful sales calls (same offer, same prospect type)

### Analysis Rules

1. **Analyze the calls first**
   - Identify the common structure the best calls follow (from greeting to close)
   - Note the exact questions and phrases that consistently lead to opens, disclosure, commitment, and payment

2. **Define the call structure** — Build the script in clear sections:
   - Opener & Rapport
   - Frame / Agenda
   - Discovery (problem, impact, budget, decision process, timing)
   - Transition to Pitch
   - Offer & Value Stack
   - Handling Top 3–5 Objections
   - Final Close & Next Steps (card in hand, booking, or BAMFAM)

3. **Create the unified script**
   - Use only lines that appear in multiple winning calls or are clearly essential glue
   - Remove filler, small talk, and stories that don't directly help the sale
   - Keep language simple, direct, and conversational (3rd–6th grade reading level)
   - Keep the core pitch portion short enough to be said in under 5 minutes at normal pace
   - Include `[QUESTIONS]` the rep should ask verbatim and `[NOTES]` about intent or tone

### Output Format
1. A short overview of the structure in bullet points
2. The final word-for-word script, organized by section headings
3. A bullet list of the top 10 most powerful phrases/lines pulled from the calls

> **Remember:** Prioritize clarity, brevity, and closing power. Delete everything that doesn't help the prospect decide and buy.

---

## 2. Newsletter Style Analyzer + New Newsletter Generator

**Purpose:** Learn voice, tone, pacing, and structure from winning newsletters, then generate new ones in that style.

### Input Required
- Past email newsletters that performed well

### Tasks

#### Task 1: Analyze Past Winning Newsletters
For all newsletters provided, extract:
- **Voice Profile:** cadence, tone, directness, emotional temperature
- **Writing Tics:** repeated phrases, humor style, analogies, transitions
- **Narrative Structure:** how the newsletter opens, builds, teaches, and concludes
- **Formatting Patterns:** headers, bullets, line breaks, sentence length
- **Persuasion Mechanics:** storytelling, cliffhangers, punchlines, frameworks, reframes
- **CTA Style:** soft/hard call to action, positioning, framing

#### Task 2: Build a Reusable Newsletter Template
Create a generalized structure including:
- Opening Hook Style (what it usually does)
- Story/Body Pattern (how ideas unfold)
- Teaching Framework Pattern (how lessons are delivered)
- Pacing and Rhythm Rules
- Closing Style (how it wraps, transitions, or calls to action)

#### Task 3: Generate a Brand-New Newsletter
When given a new topic, produce one full newsletter that:
- Matches the exact style, tone, cadence, and voice extracted
- Uses the newsletter template created from past samples
- Maintains the same pacing, emotional beats, punchline style, humor (if used), and narrative resolution

### Rules
- Never copy phrasing from old newsletters — learn the style, not the words
- The new newsletter must be 100% original content in the inferred voice
- Keep the structure consistent unless the new idea requires creative variation
- Never break character — always write in the inferred voice
- If more samples are needed to refine the model, ask

### Output Format
1. **Step 1: Style Analysis** — Voice, Tone, Pacing, Signature writing behaviors, Narrative/teaching patterns, CTA tendencies
2. **Step 2: Template** — Reusable structure for future newsletters
3. **Step 3: New Newsletter** — (After new idea is provided)

### Confirmation Flow
Acknowledge the samples → Analyze them → Wait for new idea

---

## 3. Failed Call Objection Analyzer

**Purpose:** Extract insights from failed sales calls and build an objection-handling playbook.

### Input Required
- One or more failed sales call transcripts (may include hesitation, filler words, messy phrasing)

### Tasks

#### Task 1: Identify the Primary Objection in Each Call
For each transcript:
- Identify the primary objection that caused the call to fail
- Identify any secondary objections that contributed
- Quote the exact lines from the transcript that signal each objection
- Summarize the objection in one clean sentence

#### Task 2: Propose Strong Objection-Handling Sentences
For each objection, write 3–5 short, powerful objection-handling lines that are:
- Conversational
- Non-confrontational
- Confidence-building
- Framed around value, clarity, and reducing perceived risk

Include both softening statements and direct reframes.

#### Task 3: Build a Consolidated Objection Guide
Across all transcripts analyzed:
- Identify objections that appear more than once
- Cluster them into a list of **Top 10 Most Common Objections**
- For each of the 10:
  - Give a clean definition of the objection
  - List example phrases customers say
  - Provide the best 3–5 objection-handling lines
  - Provide the root cause behind the objection (fear, confusion, misalignment, timing, money, etc.)
- Format the final guide cleanly for a training manual

### Output Format

**For Each Transcript:**
1. Primary Objection
2. Secondary Objections (if any)
3. Evidence (quoted lines)
4. Summary Sentence
5. Objection Handling Lines (3–5)

**Master Objection Guide (After All Transcripts):**
- Top 10 Objections (Ranked)
- Definition, examples, root cause, and 3–5 best rebuttals for each

### Rules
- Be concise, but not vague
- Absolutely no fluff or generic advice
- Rebuttals must be practical, not motivational
- Focus on clarity, confidence, and de-risking the decision process
- If multiple objections overlap, merge them under the clearest category

---

## 4. Universal Writing Style Analyzer

**Purpose:** Deep, systematic analysis of any writing sample to extract replicable style rules.

### Input Required
- A sample of writing to analyze

### Analysis Framework

#### 1. High-Level Snapshot
- **Overall Style Summary** (3–5 sentences): Describe the "feel" of the writing
- **Author Persona** (inferred): What kind of person does this voice sound like? (mentor, friend, drill sergeant, professor, entertainer, etc.)
- **Primary Goals of the Writing:** (persuade, teach, entertain, inspire, provoke, clarify, sell, etc.)

#### 2. Voice & Tone
- **Voice:** Formal/informal? Direct or indirect? Conversational, authoritative, playful, blunt, etc.?
- **Tone Shifts:** Does the tone stay consistent or change? Notable moments of intensity, emotion, humor, or seriousness?
- **Relationship to the Reader:** Peer, expert, coach, storyteller, teacher? Empathetic, challenging, supportive, confrontational?

#### 3. Structure & Flow
- **Overall Structure Pattern:** Common patterns (hook → story → lesson → framework → CTA), distinct sections or acts
- **Openings:** How does the writer typically start? (Bold claim, question, story, pattern interrupt, data, analogy, etc.)
- **Closings:** How does the writer end? (Summary, punchline, call to action, reflection, challenge to reader, etc.)
- **Logical Flow:** Linear, looping, tangential, modular? Frequent transitions? ("So…", "Here's why…", "But there's a catch…")

#### 4. Sentence-Level Style
- **Sentence Length & Rhythm:** Short/long/mixed? Short punchy lines for emphasis?
- **Syntax & Construction:** Simple vs. complex sentences, patterns like stacked clauses, lists, if/then, "because" chains
- **Punctuation Habits:** Use of dashes, ellipses, parentheses, colons, semicolons, question marks, exclamation points, stylistic quirks
- **Use of Questions:** Frequency, type (rhetorical, guiding, challenging)

#### 5. Diction & Word Choice
- **Vocabulary Level:** Simple/plain vs. advanced/technical
- **Jargon & Domain Language:** Industry terms, how heavily used
- **Repetition & Catchphrases:** Phrases, words, or patterns used frequently
- **Metaphors, Analogies, Imagery:** Frequency and type (sports, war, games, physics, relationships, etc.)

#### 6. Rhetorical & Persuasive Devices
- **Storytelling Usage:** Personal anecdotes, case studies, hypothetical stories, parables
- **Framing & Reframing:** How the writer flips conventional beliefs or reframes problems
- **Use of Contrast:** Before/after, old way/new way, them/us, pain/pleasure
- **Authority Signals:** Data, credentials, experience, social proof, contrarian takes
- **Emotion Triggers:** Guilt, hope, status, fear, curiosity, relief, belonging, ambition

#### 7. Formatting & Presentation
- **Paragraph Length:** Many short paragraphs, or long blocks?
- **Line Breaks & White Space:** Isolated single sentences for emphasis?
- **Use of Lists/Bullets/Numbering:** Frequency and purpose
- **Headings & Subheadings:** Clear headers? How are they phrased? (Curious, direct, benefit-driven?)

#### 8. Style Rules / Checklist
Turn all analysis into a practical checklist:
- 5–10 "Voice Rules"
- 5–10 "Sentence & Word Choice Rules"
- 5–10 "Structure & Flow Rules"
- 3–5 "Do NOT" rules (things that would break this style)

Example format:
- "Use short, punchy sentences to land important points."
- "Start with a bold, slightly contrarian statement that challenges the reader's default belief."
- "Avoid academic language and qualifiers like 'perhaps' or 'arguably.'"

#### 9. Mini Emulation Sample (Optional)
Write a short paragraph (5–8 sentences) about: *"Why most people fail to execute on good ideas"* in the same style as the analyzed text.

### Output Format
1. High-Level Snapshot
2. Voice & Tone
3. Structure & Flow
4. Sentence-Level Style
5. Diction & Word Choice
6. Rhetorical & Persuasive Devices
7. Formatting & Presentation
8. Style Rules / Checklist
9. Mini Emulation Sample

> **Note:** Be specific and concrete — no vague, generic advice.

---

## 5. Sales Call → VSL Script Generator

**Purpose:** Convert successful sales call transcripts into a cohesive, cinematic VSL script.

### Input Required
- Document containing 10 successful sales calls

### Tasks

#### Task 1: Analyze All Call Transcripts
Before writing anything, identify:
- Core customer pains & emotional triggers
- Language patterns customers use
- Promises that consistently resonate
- Frequently cited "aha moments"
- Reframes that shift buyer beliefs
- The main mechanism that drives the offer
- The before → after transformation
- The most powerful stories or client outcomes
- Words, metaphors, or phrases prospects repeat (mirror these back)

Summarize the extracted insights (2–3 paragraphs).

#### Task 2: Build the VSL Blueprint
Create a VSL structure:
- Hook Pattern
- Big Promise Formula
- Relatability Setup
- Pain Expansion Section
- The Hidden Truth / Big Reveal
- New Mechanism Introduction
- What Makes This Program Different
- Future Pacing Vision
- Proof Inserts (specify what type)
- Offer Breakdown
- Value Stack
- Objection Handling
- Guarantee (if present in calls)
- Call-to-Action
- Close

#### Task 3: Write a Full VSL Script
Using the blueprint and extracted patterns:
- Write a complete VSL script in natural voice and tone
- Prioritize simple, conversational, emotionally resonant language lifted from the prospect's vocabulary
- Create smooth transitions between sections
- Create space for pattern interrupts and high-engagement moments
- Emphasize the mechanism, not the features
- Tie objections to insights gathered from the transcripts

**Important — Proof Insert Format:**
```
[PROOF INSERT #1 — "REALITY CHECK CLIP"]
Type: short video testimonial or quote
Purpose: show someone who had the exact painful problem and solved it using the mechanism
```

#### Task 4: Create a Modular Version
After writing the main VSL, create:
- 3 Hooks (variations)
- 3 Different Big Promises
- 3 Opening Pattern Interrupts
- 3 CTA variations
- Short version (2 minutes)
- Medium version (5–7 minutes)
- Full version (15–25 minutes)

### Output Format
1. Key Findings From Transcript Analysis
2. VSL Blueprint
3. Full VSL Script (with labeled proof inserts)
4. Modular Options (hooks, promises, CTAs, short/medium versions)

### Rules
- Use their words from the transcripts whenever powerful — not marketer language
- Do NOT directly quote transcripts; paraphrase into scripted form
- Keep everything emotionally charged, benefit-forward, and clear
- Organize the script visually so it's easy to follow during filming
- Don't include inconsistent or conflicting claims
- If gaps in proof appear, flag them and suggest what proof is needed
- If the transcripts show different styles or outcomes, unify them into one cohesive story arc

---

## 6. Sales Manager – Sales Call Feedback Analyzer

**Purpose:** Evaluate sales calls and provide actionable coaching using Stop/Start/Keep framework.

### Input Required
- Sales call transcript

### Analysis Dimensions
- Prospect psychology
- Missed opportunities
- Question quality
- Objection handling
- Framing and positioning
- Control of the call
- Emotional pacing
- Next-step setting

### Tasks

#### Task 1: Summarize the Call (Briefly)
In 3–5 sentences, summarize:
- What happened
- Who controlled the call
- The prospect's core issue
- The overall outcome or failure point

#### Task 2: STOP / START / KEEP Framework

**STOP Doing** — Specific behaviors to eliminate:
- Leading questions
- Pitching too early
- Over-talking the prospect
- Weak reframes
- Missing emotional pain
- Getting lost in weeds

**START Doing** — New behaviors to adopt (with exact phrasing examples):
- Ask deeper clarifying questions
- Slow down the pace
- Build tension effectively
- Redirect objections
- Anchor value before price
- Use labeling, looping, or reflective statements

**KEEP Doing** — Reinforce strengths:
- Great tone
- Solid rapport
- Asking about impact
- Clear next-step setting

#### Task 3: Deep Tactical Feedback

**A. Discovery Quality**
- Did they extract emotional pain?
- Did they uncover root causes, not just surface problems?
- Were questions deep enough to create insight?
- Did they avoid interrogating the prospect?

**B. Framing & Positioning**
- Did they position the offer as superior?
- Did they create contrast between current state and desired state?
- Did they clearly communicate the mechanism?

**C. Objection Handling**
For each objection:
- Identify what the objection really was (fear, risk, money, timing)
- Explain how the rep handled it
- Provide 2–3 specific lines they should have used instead

**D. Emotional Control & Pacing**
- Tonality
- Silence usage
- Interruptions
- Call control
- Momentum
- Stress/pressure moments
- Where they lost leadership

**E. Trust & Authority Signals**
- Competence framing
- Credibility
- Expertise
- Relatability
- Certainty transfer

**F. Closing Phase**
- Was the close too early/too late?
- Did they future pace properly?
- Did they remove uncertainty?
- Did they present the offer clearly?
- Did they create a clean yes/no, or leave ambiguity?

#### Task 4: Red Flags / Deal Breakers
Identify behaviors that would consistently kill deals:
- Talking over the prospect
- Not validating emotions
- Giving too many options
- Pitching without discovery
- Not addressing hidden objections
- Sounding needy

Each should include what to fix AND how.

#### Task 5: Suggested Drills for Improvement
List practice exercises:
- The 5 Why's drill
- Silence tolerance drill
- Reframes practice
- Objection loop training
- Roleplay scenarios
- Slow speech pacing exercise
- Root-cause probing practice

#### Task 6: "If I Ran the Call…" Rewrite (Optional)
Rewrite key parts of the call (2–5 segments) showing:
- How you would have asked the question
- How you would have reframed
- How you would have handled the objection
- How you would have landed the close

### Output Format
1. Call Summary
2. STOP Doing
3. START Doing (with example phrasing)
4. KEEP Doing
5. Discovery Feedback
6. Positioning & Framing Feedback
7. Objection Handling Feedback
8. Emotional Control & Pacing
9. Closing Feedback
10. Red Flags / Deal Breakers
11. Drills for Improvement
12. "If I Ran the Call" Rewrite

### Rules
- No generic advice — everything tied directly to the uploaded call
- Be blunt, honest, and specific like a real sales leader
- Use simple, direct language
- Give actual example lines the rep should use next time
- Always explain why behavior is good or bad from a sales psychology perspective
- If the transcript is incomplete, state what needs more context

---

## 7. YouTube Script Style Extractor → New Script Generator

**Purpose:** Extract style, structure, and tone from YouTube videos, then generate new scripts matching that style.

### Input Required
- 1–5 transcripts from YouTube videos you like

### Tasks

#### Step 1: Analyze the Uploaded YouTube Transcripts

**A. Structure & Flow**
Describe the macro-structure:
- Opening hook style
- Setup and context
- Main story or argument framework
- Act transitions
- How curiosity is maintained
- Climax or big reveal
- Conclusion or CTA

Example output categories:
- "Pattern interrupt opening with a bold claim"
- "Story-based midpoint shift"
- "Lesson summarization at end"
- "Soft CTA with future pacing"

**B. Tone & Voice**
Identify:
- Humor style (dry, sarcastic, energetic, deadpan, etc.)
- Emotional pacing (intense → calm → intense)
- Use of vulnerability, transparency, or authority
- Level of directness
- Level of hype vs restraint
- How they speak to the viewer (friend, mentor, coach, peer, expert)

**C. Narrative Devices**
List tools used:
- Personal stories
- Metaphors and analogies
- Contrarian statements
- Cliffhangers
- Open loops
- Reframes
- Data moments
- Tension building
- Future pacing

**D. Sentence & Delivery Style**
Describe:
- Average sentence length
- Use of punchy single-sentence lines
- Pauses and pacing
- Rhetorical questions
- Emphatic phrases ("Look…", "Here's the thing…")
- Cadence and rhythm patterns
- Any repeated phrase patterns

**E. Formatting Patterns**
Identify:
- Mid-video breaks
- Section headers
- On-screen callouts
- Rapid-fire lists
- Story → lesson → application pattern
- Humor inserts
- Sound/clip opportunities (if apparent)

#### Step 2: Build a Reusable Video Script Template

Create a generalized YouTube video template:
- **HOOK**
- **INTRO FRAME**
- **SETUP STORY**
- **PROBLEM EXPANSION**
- **REVEAL / SHIFT**
- **CORE CONTENT** (broken into sections)
- **EMOTIONAL BEAT / TENSION MOMENT**
- **PROOF OR CREDIBILITY INSERT** (optional)
- **CLOSING LESSON**
- **CALL TO ACTION** (matching tone)

Each section should include instructions such as:
- "Use a short, punchy line here"
- "Insert a tension-building question"
- "Transition with a contrarian statement"
- "Use self-deprecating humor here" (if applicable)

#### Step 3: Generate a New Script With the Same Style

When supplied a new video idea, turn it into a full YouTube script that:
- MUST feel like it was written by the same creator as the uploaded videos
- MUST use the same pacing, tonal shifts, humor, emotional beats, and storytelling techniques
- MUST be original content (no copying or lifting from transcripts)
- Apply narrative devices naturally
- Match the voice and pattern of the original creator

### Rules
- Be extremely detailed in the analysis — thoroughness is required
- Never copy lines from the original videos — derive the style, not the words
- Scripts must be cinematic and performance-ready
- Transitions must match the original creator's rhythm
- The template must be clear enough that someone could follow it without the transcripts
- When generating the new script, do NOT include the analysis — only the script itself

### Output Format
1. Full Style & Structure Analysis (A–E)
2. Reusable YouTube Video Script Template
3. (Later, when idea provided) New YouTube Script in That Style

### Confirmation Flow
Wait for transcripts → Analyze → Wait for new topic → Generate script

---

## 8. Shorts Script Style Extractor → Short-Form Script Generator

**Purpose:** Create punchy 15–60 second vertical video scripts (TikTok, Reels, Shorts) matching a specific creator's style.

### Input Required
- 1–5 short-form video transcripts

### Tasks

#### Step 1: Analyze the Uploaded Shorts Transcripts

**A. Hook Style (0–2 seconds)**
Identify the opening mechanism:
- Shock line
- Pattern interrupt
- Contrarian statement
- Quick story teaser
- Bold claim
- Hot take
- Humor-led hook

**B. Tone & Energy**
Describe:
- Energy level (low, medium, high)
- Directness
- Humor style (dry, edgy, sarcastic, wholesome, etc.)
- Emotional range
- Level of aggression vs softness
- Relationship to viewer (coach, friend, entertainer, expert)

**C. Pacing & Delivery**
Identify:
- Speed of speech
- Jump-cut rhythm
- Use of short lines vs longer sentences
- Punchline timing
- How often they reset attention
- How many beats per 15 seconds

**D. Narrative Devices**
Identify the mechanics:
- Micro-stories
- Fast reframes
- Hot takes
- "List of 3" patterns
- Cliffhanger → payoff
- Tension → punchline
- Commands vs suggestions
- "You vs them" framing
- Sound-bite-style lines

**E. Formatting Patterns**
Identify:
- Section breaks
- On-screen text cues
- Rapid-fire lists
- Hard scene changes
- Silence usage (if any)
- Ending CTA style (if any)

#### Step 2: Build a Reusable SHORTS Script Template

- **HOOK (0–2s)** — Specify exact style: bold claim, pattern interrupt, blunt statement, etc.
- **SETUP (2–4s)** — Clarify the premise quickly
- **PAYOFF / INSIGHT / STORY (4–10s)** — Short punchy lines, matching the creator's delivery
- **CORE VALUE (10–20s)** — The key lesson, hack, reframe, or funny twist
- **REPEATABLE DEVICE** (if applicable) — Example: "3 reasons," "one mistake," "one truth nobody tells you," etc.
- **CLOSING BEAT (last 2 seconds)** — Either: A punchline, A challenge, A callback, A CTA matching their tone

Include instructions like:
- "Add jump-cut every sentence."
- "Use a punchline every 3–5 seconds."
- "Insert on-screen text matching these beats."

#### Step 3: Generate a New Short-Form Script

When given a new idea, produce:
- A 15–45 second script
- Matching the original creator's tone, pacing, rhythm, hook style, and comedic/serious energy
- Short, punchy, high-retention lines suitable for vertical video
- Suggested on-screen text
- Suggested B-roll (optional)
- Suggested pacing notes (optional)

Everything must be original content — not copied lines.

### Rules
- Extreme brevity — no long explanations
- Every line must be punchy
- Prioritize attention resets
- Maintain the exact emotional tone of the original videos
- Do NOT include the analysis inside the script
- All creative choices must be tied to the uploaded examples

### Output Format
1. Style & Structure Analysis (Hook style, Tone, Pacing, Narrative devices, Formatting patterns)
2. Reusable Shorts Script Template
3. (Later, when idea provided) New Shorts Script in That Style (with optional on-screen text and pacing notes)

### Confirmation Flow
Wait for short-form transcripts → Analyze → Wait for new idea → Generate script

---

## 9. Lead Magnet Generator (Video → High-Value PDF Guide)

**Purpose:** Convert video content into a master lead magnet (downloadable PDF guide).

### Input Required
- 1–3 videos or transcripts (educational, motivational, tactical, or storytelling-based)

### Tasks

#### Step 1: Analyze the Uploaded Video(s)

**A. Structural Patterns**
- How the creator introduces the topic
- The order of teaching points
- How stories are used
- How frameworks are presented
- How curiosity is maintained
- How the content leads into action steps
- How complexity is simplified

**B. Tone & Writing Style**
- Teaching tone (direct, humorous, blunt, expert, friendly, contrarian, etc.)
- Pace
- Emotional peaks
- Signature phrases or rhetorical devices
- Level of complexity
- Level of authority vs relatability

**C. Core Teaching Frameworks**
- Repeated frameworks or mental models
- Step-by-step processes
- "Do this, not that" patterns
- Mistake → fix structures
- Story → lesson → application patterns

**D. Key Themes & Messaging**
Extract the themes and insights that define the video's core value.

#### Step 2: Build a Lead Magnet Blueprint

Based on extracted patterns, build a custom outline:
- **Title options** (5–10) matching the tone of the videos
- **Subtitles** that increase specificity, curiosity, and promise
- **Lead magnet structure:**
  - Cover Page
  - Introduction / Promise
  - Section 1: Big Idea
  - Section 2: Frameworks
  - Section 3: Tactical Steps
  - Section 4: Mistakes to Avoid
  - Section 5: Quick Wins
  - Section 6: Case Examples or Stories
  - Section 7: Action Plan / Checklist
  - Section 8: CTA (soft or hard, depending on video style)

Include style instructions:
- Sentence length
- Tone of explanation
- Level of humor
- Bluntness vs politeness
- Energy level
- Visual formatting recommendations (boxes, checklists, sections, templates)

#### Step 3: Create the Master Lead Magnet (Full Draft)

When topic is provided, produce a full-length asset (2,000–6,000 words) including:
- Headline + Subhead
- Intro that hooks readers using the video's tone
- All sections fully written out
- Frameworks or models, formatted cleanly
- Checklists
- Action steps
- Common mistakes and how to fix them
- Case-style stories (original, not copied)
- Diagrams/visual ideas (text-described) that a designer can later create
- A CTA matching the tonal style extracted from the videos

The final result must feel like a fully finished, high-value PDF lead magnet ready to hand to a designer.

#### Step 4: Provide Alternate Versions (Optional)
- Short version (1–2 pages)
- Medium version (5–7 pages)
- Deep dive version (10–20 pages)
- "Fill-in-the-blank" workbook version
- "Checklist-only" version

### Rules
- Use uploaded videos only to learn structure, voice, and tone — never copy lines directly
- The final lead magnet must be original content
- Match the feel of the videos, not the wording
- Be extremely clear, actionable, and easy to read
- Build frameworks even if the video didn't explicitly include them — extract the mental model
- If any gaps appear in the videos, fill them with best-practice expertise

### Output Format
1. Full Style & Structure Analysis
2. Lead Magnet Blueprint / Table of Contents
3. (After topic provided) Full Lead Magnet Draft

---

## 10. Lead Magnet → Call-Booking Follow-Up Generator

**Purpose:** Turn lead magnet downloads into booked sales calls via email and SMS sequences.

### Input Required
- Lead magnet PDF or text

### Tasks

#### Step 1: Analyze the Lead Magnet

Extract:
- Core promise
- Big idea
- Problems the reader wants solved
- Emotional triggers
- Key frameworks
- Story elements
- The "gap" between where they are and where they want to be
- The right CTA angle based on the lead magnet's theme
- The dominant tone (friendly, direct, blunt, mentor, expert, etc.)

Provide a 1–2 paragraph summary of the lead magnet and the best angle to get readers to book a call.

#### Step 2: Create the Follow-Up Email Sequence (7–12 Emails)

Each email includes:
- Subject line (3 variations)
- Preview text
- Body copy
- Soft → medium → strong CTA (depending on the email)
- PS with a secondary CTA
- Timing recommendation

**Email Arc:**

| Email | Focus | CTA |
|-------|-------|-----|
| 1 | Delivery + The Big Promise | "If you want help implementing this, book a call" |
| 2 | The Gap | Book a call to implement with expert help |
| 3 | Case Study / Proof | Book a call to replicate the outcome |
| 4 | The Hidden Obstacle | Book a call to remove the obstacle |
| 5 | The Framework Breakdown | Book a call |
| 6 | Consequences of Doing Nothing | Book a call |
| 7 | Quick Wins Recap + Next Step | Book a call |

**Optional Emails 8–12:**
- "Why now?"
- FAQ / Objections
- Soft story-driven reminder
- Deadline-based nudge (if relevant)
- "Are you still interested?" check-in
- Last chance micro-email

#### Step 3: Create the SMS/Text Follow-Up Sequence (5–8 SMS)

Short, punchy texts optimized for mobile:
- <40 characters opening hook (if possible)
- Casual tone
- One single ask
- No fluff

**SMS Structure:**
1. **Delivery Text** — "Just sent your guide. Quick question…"
2. **The One-Question Qualifier** — "What's the #1 thing you want help with from the guide?"
3. **Soft CTA** — "Want me to walk you through it? I can show you the fast path."
4. **Credibility/Bait** — "Just helped someone do X in Y time. Want details?"
5. **Direct CTA** — "If you want help implementing the guide → Book here: [link]"
6–8. Check-in, Urgency, Final nudge (Optional)

#### Step 4: Include Personalization Tokens
- `{first_name}`
- `{pain_point}`
- `{goal}`
- `{lead_magnet_title}`
- `{booking_link}`

#### Step 5: Create a "Plain Text" Version of Every Email
Choose between:
- Polished HTML-style
- Casual plain-text personal email

#### Step 6: Deliver the Full System

### Output Format
1. Lead magnet summary
2. Full email sequence
3. Full SMS sequence
4. Personalization tokens
5. Timing map (day-by-day sending schedule)

### Rules
- Match tone to the lead magnet content
- No fluff — every line must move toward booking a call
- Use conversational, human language
- Use short paragraphs
- Use emotion, insight, and clear value
- Every email must feel unique (no repetition)
- Avoid hype
- Include subtle scarcity only if justified

---

## 11. Offer Architect – Offer Diagnosis & Optimization Engine

**Purpose:** Transform any offer into a more powerful, irresistible, higher-converting version ("Hormozi-level" offer architecture).

### Input Required
- Current offer (written page, sales page, outline, VSL script, or raw notes)

### Tasks

#### Step 1: Analyze Current Offer

Extract:
- Core promise
- Mechanism (what makes it work)
- Value drivers
- Tangible outcomes
- Intangible outcomes
- Time-to-result
- Effort required from customer
- Risk profile
- Pricing structure
- Guarantees (or absence)
- Bonuses
- Delivery model
- Target avatar sophistication level
- Current positioning vs. market

**Diagnostic Report:**

| Section | Focus |
|---------|-------|
| A. Strengths | What's currently compelling |
| B. Weaknesses | What's confusing, incomplete, or low perceived value |
| C. Missing Elements | Anything an irresistible offer must have |
| D. Marketability Risks | Wrong positioning, weak mechanism, low differentiation, value-to-price misalignment, lack of clarity, lack of risk reversal |

#### Step 2: Build a "More Irresistible" Version

**1. Offer Enhancements** — Add or improve:
- Guarantee options (performance, unconditional, hybrid, anti-guarantee, etc.)
- Bonuses
- Fast-action incentives
- Delivery upgrades
- Reducing steps or complexity
- Increasing time-to-value
- Increasing perceived certainty
- Increasing tangibility
- Social proof / evidence insert recommendations

**2. Value Stack Optimization** — Break down into:
- Core product
- Supporting assets
- Bonuses
- Accelerators
- Accountability mechanisms
- Done-for-you elements
- Done-with-you elements
- Toolkits / templates / workflows

Clearly assign value to each.

**3. Pricing Architecture** — Propose:
- Optimal price
- Anchor price (high)
- Middle offer
- Entry offer
- Bundles
- Hybrid pricing
- Payment plans
- Add-ons / extras

Explain psychological reasoning for each recommendation.

#### Step 3: Add Upsells, Downsells, & Cross-Sells (Optional)

Create a revenue-maximizing offer ladder:

| Type | Description |
|------|-------------|
| **Upsells** | Big profit boosters — high-ticket or advanced tier |
| **Downsells** | Lower commitment, lower risk fallback offers |
| **Cross-sells** | Adjacent products/services that enhance customer success |
| **Order Bumps** | Small, impulse-friendly add-ons at checkout |

Each should include: Name, Price, Value proposition, Why it increases AOV/RPL/Profit, Who it's for

#### Step 4: Build the "Grand Slam Offer" Version

Create a completely re-architected offer that is:
- Clear
- Simple
- Dramatically higher perceived value
- Faster to deliver results
- Lower effort
- Lower risk
- More differentiated
- Easier to sell
- Easier to explain
- Built to maximize AOV, LTV, and revenue per sales opportunity

Include:
- Offer Title
- One-Sentence Promise
- Target Avatar
- Primary Mechanism
- Delivery Model
- What They Get (line by line)
- Bonuses
- Guarantees
- Pricing
- Reasoning Behind Pricing
- CTA framing

#### Step 5: High-Converting Offer Positioning & Messaging

Provide:
- The elevator pitch
- "Why this, why now" positioning
- Market category design
- Differentiation narrative
- Unique mechanism name
- Risk reversal statement
- Short-form and long-form value stack
- Headline options
- Full offer bullet points ("Here's everything you get…")

### Output Format
1. Offer Diagnosis Report (Strengths, Weaknesses, Missing Elements, Marketability Risks)
2. Offer Enhancements
3. Value Stack Optimization
4. Pricing Architecture Recommendations
5. Upsells / Downsells / Cross-sells / Order Bumps
6. Rebuilt Grand Slam Offer (complete)
7. Pitch Script (short version & long version)
8. Headline + Subheadline Options
9. Positioning Narrative

### Rules
- Never be vague; always be specific
- No fluff — everything must tie to either perceived value, conversion, or revenue
- Don't just critique — rebuild
- Always explain why a change increases value or revenue
- Use brand voice if requested
- Use buyer psychology principles throughout

---

## 12. Sales Page Copy Generator

**Purpose:** Turn Offer Architect output into complete, high-converting sales page copy.

### Input Required
- Offer Architect output (offer structure, promise, mechanism, bonuses, guarantees, pricing, value stack, unique differentiators, positioning narrative)

### Output Structure

| Section | Description |
|---------|-------------|
| **A. Headline + Subheadline** | 3–5 versions |
| **B. Pattern Interrupt / "Call-Out" Opening** | |
| **C. Future Pacing Section** | Vivid "here's what your life will look like once you win" |
| **D. "Why You're Stuck" Section** | Pain, root causes, failed attempts |
| **E. Introduction of the New Mechanism** | What makes this offer work |
| **F. What Makes This Different** | Differentiation bullets |
| **G. Offer Breakdown (Value Stack)** | Line-by-line breakdown with `[PROOF INSERT]` placeholders |
| **H. Bonuses Section** | |
| **I. Guarantee Section** | Clear, tangible, and bold |
| **J. Pricing Section** | Anchor → real price → justification |
| **K. Call-to-Action Section** | 3 CTA variants |
| **L. FAQ Section** | Cover objections |

### Rules
- Match the tone of the offer (friendly, blunt, authoritative, etc.)
- Be specific, not general
- Use buyer psychology
- Keep paragraphs short
- Include `[PROOF INSERT: TYPE]` placeholders

---

## 13. Sales Call Script Generator

**Purpose:** Turn Offer Architect output into a complete sales call script.

### Input Required
- Offer Architect output

### Script Structure

#### 1. Open / Frame
- Set tone
- Explain the agenda
- Establish leadership

#### 2. Discovery Phase
- Pain questions
- Goal questions
- Root-cause analysis
- Time horizon
- Cost of inaction
- Emotional resonance

#### 3. Transition to Pitch
- Confirm what they want
- Confirm fit
- Build anticipation

#### 4. Pitch (Based on Offer Output)
Explain:
- Promise
- Mechanism
- How the program works
- Differentiators
- What they get
- Bonuses
- Guarantees

Keep it simple, high-level, conversational.

#### 5. Proof Section
Add placeholders: `[INSERT PROOF CLIP/STORY HERE]`

#### 6. Investment & Pricing
Use anchor → real price → rationale.

#### 7. Close
Ask directly: *"Do you want help with this?"*

#### 8. Objection Handling
For each common objection:
- Label it
- Validate
- Reframe
- Present solution

Create a mini-script for each.

#### 9. Final Close
Clear path to yes or no.

### Rules
- Tone must be warm, confident, not pushy
- Questions must be deep and insightful
- No jargon
- Tie every recommendation back to the Offer Architect output
- Use simple language
- Make the script readable like a real sales conversation

---

## 14. VSL Script Generator

**Purpose:** Turn Offer Architect output into a full Video Sales Letter script.

### Input Required
- Offer Architect output

### VSL Structure

| Section | Focus |
|---------|-------|
| **1. Pattern Interrupt Hook** | Bold statement, contrarian point, mini-story teaser |
| **2. Big Promise** | State the transformation clearly |
| **3. Identify the Enemy** | What's been holding them back |
| **4. Your Story / Credibility** | Short, relevant personal narrative |
| **5. The Big Discovery** | Introduce the mechanism behind the offer |
| **6. Teaching Section** | The new way, why the old way fails, 2–3 insights that position you as the inevitable choice |
| **7. Soft Proof Section** | Placeholders: `[INSERT PROOF]` |
| **8. Offer Reveal** | Introduce the program/offer clearly |
| **9. Offer Breakdown / Value Stack** | Explain each component and why it matters |
| **10. Bonuses** | |
| **11. Guarantee** | |
| **12. Price Reveal** | Anchor → real price → justification |
| **13. Strong CTA** | |
| **14. Future Pacing** | Show what happens when they join |
| **15. Tension Close** | Pose a clear decision moment |

### Rules
- Must follow emotional beats
- Must match tone of offer
- Must avoid hype
- Must include proof placeholders
- Must tell a story
- Copy must sound like a spoken script

---

## Quick Reference: Which Prompt to Use

| If you need to... | Use Prompt # |
|-------------------|--------------|
| Build a sales script from winning calls | #1 |
| Analyze and replicate newsletter style | #2 |
| Learn from failed sales calls | #3 |
| Analyze any writing style | #4 |
| Turn sales calls into a VSL | #5 |
| Get coaching feedback on a sales call | #6 |
| Create YouTube scripts in a specific style | #7 |
| Create short-form video scripts | #8 |
| Turn videos into a lead magnet PDF | #9 |
| Create follow-up sequences for lead magnets | #10 |
| Diagnose and optimize your offer | #11 |
| Generate sales page copy | #12 |
| Generate a sales call script | #13 |
| Generate a VSL script | #14 |

---

*Document reorganized from ACQ AI Onboarding PDF*

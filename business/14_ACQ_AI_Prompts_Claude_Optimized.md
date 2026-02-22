# 14 Prompts — Claude-Optimized Edition

Optimized for Claude's reasoning style: removed unnecessary scaffolding, added iteration loops, split monolithic prompts into sequential workflows, and lowered minimum input requirements where practical.

---

## #1 SALES SCRIPT ANALYSIS

Analyze my successful sales call transcripts and build ONE unified "mother script" that extracts only what moves the sale forward.

**Minimum input:** 3 transcripts (works better with 5–10)

### Your process:

**Phase 1: Pattern extraction**
- Identify the common structure across calls (greeting → close)
- Flag exact questions and phrases that consistently lead to opens, disclosure, commitment, and payment
- Note what's present in winning calls vs. absent in weaker ones

**Phase 2: Build the script structure**

Organize into these sections:
1. Opener & Rapport
2. Frame / Agenda
3. Discovery (problem, impact, budget, decision process, timing)
4. Transition to Pitch
5. Offer & Value Stack
6. Handling Top 3–5 Objections
7. Final Close & Next Steps (card in hand, booking, or BAMFAM)

**Phase 3: Create the unified script**
- Use only lines that appear in multiple calls or are clearly essential glue
- Remove filler, small talk, and stories that don't directly help the sale
- Keep language at 3rd–6th grade reading level
- Core pitch must be deliverable in under 5 minutes
- Include `[QUESTION]` tags for verbatim questions and `[NOTE]` tags for intent/tone guidance

### Output:
1. Brief structural overview
2. Word-for-word script by section
3. Top 10 most powerful phrases/lines extracted from the calls

### Iteration commands:
- `"Strengthen the discovery section"` — I'll add more probing questions
- `"Make the close harder/softer"` — I'll adjust closing intensity
- `"Add objection handling for [X]"` — I'll create a new rebuttal block
- `"Simplify section [X]"` — I'll reduce complexity in that section

---

## #2 NEWSLETTER STYLE ANALYZER + GENERATOR

Learn my newsletter voice from examples, then generate new ones that sound like me.

### Phase 1: Style Analysis

From the newsletters you provide, I'll extract:

- **Voice Profile:** cadence, tone, directness, emotional temperature
- **Writing Tics:** repeated phrases, humor style, analogies, transitions
- **Narrative Structure:** how you open, build, teach, and conclude
- **Formatting Patterns:** headers, bullets, line breaks, sentence length
- **Persuasion Mechanics:** storytelling, cliffhangers, punchlines, frameworks, reframes
- **CTA Style:** soft/hard, positioning, framing

### Phase 2: Newsletter Blueprint

I'll create a reusable template showing:
- Opening Hook Style
- Story/Body Pattern
- Teaching Framework Pattern
- Pacing and Rhythm Rules
- Closing Style

### Phase 3: Generate New Newsletter

Give me a topic/idea, and I'll produce a full newsletter matching your extracted style.

### Rules I follow:
- Learn the style, not the words — no copied phrasing
- 100% original content in your inferred voice
- Consistent structure unless the idea demands variation
- If I need more samples to nail your voice, I'll tell you

### Iteration commands:
- `"More [punchy/conversational/authoritative]"` — I'll adjust tone
- `"Shorter/longer"` — I'll adjust length
- `"Different hook"` — I'll rewrite the opening
- `"Stronger CTA"` — I'll make the call-to-action more direct

---

## #3 FAILED CALL OBJECTION ANALYZER

Extract insights from failed sales calls and build an objection-handling playbook.

**Input:** Failed call transcripts (messy is fine — hesitation, filler words, incomplete responses are expected)

### For each transcript, I'll deliver:

1. **Primary Objection** — the main reason the call failed
2. **Secondary Objections** — contributing factors
3. **Evidence** — exact quoted lines signaling each objection
4. **Summary** — one clean sentence capturing the objection
5. **Handling Lines** — 3–5 rebuttals that are:
   - Conversational
   - Non-confrontational
   - Confidence-building
   - Framed around value, clarity, and risk reduction

### After multiple transcripts, I'll build:

**Master Objection Guide**
- Top 10 Most Common Objections (ranked by frequency)
- For each: definition, example phrases, root cause (fear/confusion/timing/money/etc.), and 3–5 best rebuttals
- Formatted for direct copy into a training manual

### Rules:
- Concise but not vague
- No fluff or generic advice
- Rebuttals must be practical, not motivational
- Overlapping objections get merged under the clearest category

### Iteration commands:
- `"More rebuttals for [objection]"` — I'll add alternatives
- `"Softer/harder rebuttals"` — I'll adjust tone
- `"Reframe [objection] differently"` — I'll try a new angle

---

## #4 UNIVERSAL WRITING STYLE ANALYZER

Deep, systematic analysis of any writing sample to extract replicable style rules.

### Analysis Framework:

**1. High-Level Snapshot**
- Overall Style Summary (3–5 sentences)
- Author Persona (mentor, friend, drill sergeant, professor, entertainer, etc.)
- Primary Goals (persuade, teach, entertain, inspire, provoke, clarify, sell)

**2. Voice & Tone**
- Formal/informal, direct/indirect, conversational/authoritative/playful/blunt
- Tone shifts and notable intensity moments
- Relationship to reader (peer, expert, coach, storyteller)

**3. Structure & Flow**
- Overall pattern (hook → story → lesson → framework → CTA)
- Opening style (bold claim, question, story, pattern interrupt, data, analogy)
- Closing style (summary, punchline, CTA, reflection, challenge)
- Logical flow (linear, looping, tangential, modular)
- Transition patterns

**4. Sentence-Level Style**
- Length and rhythm patterns
- Syntax preferences (stacked clauses, lists, if/then, "because" chains)
- Punctuation habits
- Question usage (rhetorical, guiding, challenging)

**5. Diction & Word Choice**
- Vocabulary level
- Jargon density
- Repetition and catchphrases
- Metaphor/analogy patterns (sports, war, games, physics, relationships)

**6. Rhetorical & Persuasive Devices**
- Storytelling (anecdotes, case studies, hypotheticals, parables)
- Framing/reframing techniques
- Contrast usage (before/after, old/new, them/us, pain/pleasure)
- Authority signals (data, credentials, experience, social proof, contrarian takes)
- Emotion triggers (guilt, hope, status, fear, curiosity, relief, belonging, ambition)

**7. Formatting & Presentation**
- Paragraph length
- White space and line break usage
- Lists/bullets/numbering patterns
- Header style

**8. Style Rules Checklist**
- 5–10 Voice Rules
- 5–10 Sentence & Word Choice Rules
- 5–10 Structure & Flow Rules
- 3–5 "Do NOT" rules

**9. Mini Emulation Sample**
A 5–8 sentence paragraph on "Why most people fail to execute on good ideas" — written in the analyzed style.

### Iteration commands:
- `"Write [X] in this style"` — I'll generate new content matching the analyzed voice
- `"Compare to [other sample]"` — I'll analyze differences between two styles
- `"Exaggerate the style"` — I'll push the distinctive elements further

---

## #5 SALES CALL → VSL SCRIPT GENERATOR

Convert successful sales call transcripts into a cinematic VSL script.

**Minimum input:** 3 transcripts (better with 5–10)

### Phase 1: Transcript Analysis

I'll identify:
- Core customer pains & emotional triggers
- Language patterns customers use (I'll mirror these back)
- Promises that consistently resonate
- "Aha moments" frequently cited
- Belief-shifting reframes
- The main mechanism driving the offer
- Before → after transformation
- Most powerful stories/outcomes
- Repeated words, metaphors, phrases

**Deliverable:** 2–3 paragraph insight summary

### Phase 2: VSL Blueprint

Structure map:
- Hook Pattern
- Big Promise Formula
- Relatability Setup
- Pain Expansion Section
- Hidden Truth / Big Reveal
- New Mechanism Introduction
- What Makes This Different
- Future Pacing Vision
- Proof Inserts (with type specified)
- Offer Breakdown
- Value Stack
- Objection Handling
- Guarantee
- Call-to-Action
- Close

### Phase 3: Full VSL Script

- Natural voice and tone
- Simple, conversational, emotionally resonant language from prospect vocabulary
- Smooth transitions
- Pattern interrupts and high-engagement moments
- Mechanism-focused (not feature-focused)
- Objections tied to transcript insights

**Proof Insert Format:**
```
[PROOF INSERT #1 — "REALITY CHECK CLIP"]
Type: short video testimonial or quote
Purpose: show someone who had the exact painful problem and solved it using the mechanism
```

### Phase 4: Modular Variations

- 3 Hook variations
- 3 Big Promise variations
- 3 Opening Pattern Interrupts
- 3 CTA variations
- Short version (2 min)
- Medium version (5–7 min)
- Full version (15–25 min)

### Rules:
- Use prospect words, not marketer language
- Paraphrase transcripts into scripted form (no direct quotes)
- Flag proof gaps and suggest what's needed
- Unify different styles/outcomes into one cohesive arc

### Iteration commands:
- `"Punch up the hook"` — I'll make it more attention-grabbing
- `"Expand the pain section"` — I'll deepen emotional resonance
- `"Shorter/longer version"` — I'll adjust pacing
- `"Different mechanism angle"` — I'll reframe the core differentiator

---

## #6 SALES MANAGER — Call Feedback Analyzer

Evaluate a sales call and provide Stop/Start/Keep coaching plus deep tactical feedback.

### Output Structure:

**1. Call Summary (3–5 sentences)**
- What happened
- Who controlled the call
- Prospect's core issue
- Outcome or failure point

**2. STOP Doing**
Context-specific behaviors to eliminate (leading questions, pitching too early, over-talking, weak reframes, missing emotional pain, getting lost in weeds)

**3. START Doing**
New behaviors with exact phrasing examples (deeper questions, slower pace, tension building, objection redirects, value anchoring, labeling/looping/reflective statements)

**4. KEEP Doing**
Reinforcement of what's working (tone, rapport, impact questions, next-step clarity)

**5. Deep Tactical Feedback**

*A. Discovery Quality* — emotional pain extraction, root cause uncovering, question depth, interrogation avoidance

*B. Framing & Positioning* — offer superiority, current/desired state contrast, mechanism communication

*C. Objection Handling* — for each objection: what it really was, how rep handled it, 2–3 better lines

*D. Emotional Control & Pacing* — tonality, silence, interruptions, call control, momentum, pressure moments, leadership losses

*E. Trust & Authority Signals* — competence framing, credibility, expertise, relatability, certainty transfer

*F. Closing Phase* — timing, future pacing, uncertainty removal, offer clarity, yes/no cleanliness

**6. Red Flags / Deal Breakers**
Behaviors that would consistently kill deals, with fixes

**7. Improvement Drills**
- The 5 Why's drill
- Silence tolerance drill
- Reframes practice
- Objection loop training
- Roleplay scenarios
- Slow speech pacing exercise
- Root-cause probing practice

**8. "If I Ran the Call" Rewrite**
2–5 key segments rewritten showing better questions, reframes, objection handling, and closes

### Rules:
- No generic advice — everything tied to this specific call
- Blunt, honest, specific like a real sales leader
- Explain why behaviors are good/bad from sales psychology perspective

### Iteration commands:
- `"Focus on [discovery/closing/objections]"` — I'll go deeper on that area
- `"More drill suggestions"` — I'll add practice exercises
- `"Rewrite the [X] section"` — I'll model better execution

---

## #7 YOUTUBE SCRIPT STYLE EXTRACTOR → GENERATOR

Extract style from YouTube videos I like, then generate new scripts matching that style.

### Phase 1: Style Analysis

**A. Structure & Flow**
- Opening hook style
- Setup and context approach
- Main story/argument framework
- Act transitions
- Curiosity maintenance
- Climax/reveal
- Conclusion/CTA

**B. Tone & Voice**
- Humor style (dry, sarcastic, energetic, deadpan)
- Emotional pacing
- Vulnerability/transparency/authority balance
- Directness level
- Hype vs. restraint
- Viewer relationship (friend, mentor, coach, peer, expert)

**C. Narrative Devices**
- Personal stories, metaphors, analogies
- Contrarian statements, cliffhangers, open loops
- Reframes, data moments, tension building, future pacing

**D. Sentence & Delivery Style**
- Sentence length, punchy lines
- Pauses and pacing
- Rhetorical questions
- Emphatic phrases ("Look…", "Here's the thing…")
- Cadence patterns, repeated phrases

**E. Formatting Patterns**
- Mid-video breaks, section headers
- On-screen callouts, rapid-fire lists
- Story → lesson → application pattern
- Humor inserts, sound/clip opportunities

### Phase 2: Script Template

Generalized structure:
- HOOK
- INTRO FRAME
- SETUP STORY
- PROBLEM EXPANSION
- REVEAL / SHIFT
- CORE CONTENT (sections)
- EMOTIONAL BEAT / TENSION MOMENT
- PROOF OR CREDIBILITY INSERT
- CLOSING LESSON
- CALL TO ACTION

Each section includes style instructions specific to the analyzed videos.

### Phase 3: New Script Generation

Give me a topic, and I'll generate a full script that:
- Feels like the same creator wrote it
- Uses identical pacing, tonal shifts, humor, emotional beats, storytelling techniques
- Is 100% original (no copied lines)
- Applies narrative devices naturally

### Iteration commands:
- `"Different hook"` — I'll try another opening
- `"More [humor/tension/authority]"` — I'll adjust tone
- `"Shorter/longer"` — I'll adjust pacing
- `"Add a story beat at [X]"` — I'll insert narrative element

---

## #8 SHORTS SCRIPT STYLE EXTRACTOR → GENERATOR

Extract style from short-form videos (TikTok, Reels, Shorts), then generate 15–60 second scripts.

### Phase 1: Style Analysis

**A. Hook Style (0–2 seconds)**
- Shock line, pattern interrupt, contrarian statement
- Quick story teaser, bold claim, hot take, humor-led hook

**B. Tone & Energy**
- Energy level (low/medium/high)
- Directness, humor style, emotional range
- Aggression vs. softness
- Viewer relationship

**C. Pacing & Delivery**
- Speech speed, jump-cut rhythm
- Short lines vs. longer sentences
- Punchline timing, attention resets
- Beats per 15 seconds

**D. Narrative Devices**
- Micro-stories, fast reframes, hot takes
- "List of 3" patterns
- Cliffhanger → payoff, tension → punchline
- Commands vs. suggestions
- "You vs. them" framing, sound-bite lines

**E. Formatting Patterns**
- Section breaks, on-screen text cues
- Rapid-fire lists, hard scene changes
- Silence usage, ending CTA style

### Phase 2: Shorts Template

- **HOOK (0–2s)** — exact style specified
- **SETUP (2–4s)** — quick premise clarification
- **PAYOFF / INSIGHT / STORY (4–10s)** — punchy delivery
- **CORE VALUE (10–20s)** — key lesson/hack/reframe/twist
- **REPEATABLE DEVICE** — "3 reasons," "one mistake," etc.
- **CLOSING BEAT (last 2s)** — punchline, challenge, callback, or CTA

Plus pacing instructions (jump-cuts, punchline frequency, on-screen text beats).

### Phase 3: New Script Generation

Give me a topic, I'll produce:
- 15–45 second script
- Matching original creator's tone, pacing, rhythm, hook style
- Short, punchy, high-retention lines
- Suggested on-screen text
- Optional B-roll and pacing notes

### Iteration commands:
- `"Punchier"` — I'll tighten and add more hooks
- `"Different hook"` — I'll try another opening
- `"Add on-screen text suggestions"` — I'll include visual callouts
- `"Make it [funnier/more serious]"` — I'll adjust tone

---

## #9 LEAD MAGNET GENERATOR (Video → PDF Guide)

Convert video content into a high-value downloadable lead magnet.

### Phase 1: Video Analysis

**A. Structural Patterns**
- Topic introduction approach
- Teaching point order
- Story usage
- Framework presentation
- Curiosity maintenance
- Action step transitions
- Complexity simplification

**B. Tone & Writing Style**
- Teaching tone, pace, emotional peaks
- Signature phrases, rhetorical devices
- Complexity level, authority vs. relatability

**C. Core Teaching Frameworks**
- Mental models, step-by-step processes
- "Do this, not that" patterns
- Mistake → fix structures
- Story → lesson → application patterns

**D. Key Themes & Messaging**

### Phase 2: Lead Magnet Blueprint

- 5–10 title options
- Subtitles (specificity, curiosity, promise)
- Structure:
  - Cover Page
  - Introduction / Promise
  - Section 1: Big Idea
  - Section 2: Frameworks
  - Section 3: Tactical Steps
  - Section 4: Mistakes to Avoid
  - Section 5: Quick Wins
  - Section 6: Case Examples or Stories
  - Section 7: Action Plan / Checklist
  - Section 8: CTA

- Style instructions: sentence length, tone, humor level, bluntness, energy, visual formatting recommendations

### Phase 3: Full Lead Magnet Draft (2,000–6,000 words)

- Headline + Subhead
- Hook intro matching video tone
- All sections written out
- Clean frameworks/models
- Checklists, action steps
- Common mistakes with fixes
- Original case-style stories
- Diagram/visual ideas (text-described for designer)
- Tone-matched CTA

### Phase 4: Alternate Versions (on request)

- Short (1–2 pages)
- Medium (5–7 pages)
- Deep dive (10–20 pages)
- Fill-in-the-blank workbook
- Checklist-only version

### Rules:
- Learn structure/voice/tone — never copy lines
- Build frameworks even if video didn't explicit them
- Fill gaps with best-practice expertise

### Iteration commands:
- `"Shorter/longer version"` — I'll adjust depth
- `"More actionable"` — I'll add steps and checklists
- `"Different title options"` — I'll generate alternatives
- `"Expand section [X]"` — I'll add detail

---

## #10 LEAD MAGNET → CALL-BOOKING FOLLOW-UP GENERATOR

Create a complete email + SMS follow-up system to convert lead magnet downloads into booked calls.

### Phase 1: Lead Magnet Analysis

I'll extract:
- Core promise and big idea
- Problems reader wants solved
- Emotional triggers
- Key frameworks
- Story elements
- The "gap" (where they are vs. where they want to be)
- Best CTA angle
- Dominant tone

**Deliverable:** 1–2 paragraph summary + recommended booking angle

### Phase 2: Email Sequence (7–12 emails)

Each email includes:
- Subject line (3 variations)
- Preview text
- Body copy
- CTA (soft → medium → strong progression)
- PS with secondary CTA
- Timing recommendation

**Email Arc:**

1. **Delivery + Big Promise** — deliver asset, set expectations, reinforce promise, soft CTA
2. **The Gap** — knowing vs. doing, "more info won't fix things" reframe
3. **Case Study / Proof** — transformation story
4. **The Hidden Obstacle** — real reason they're stuck, tied to your solution
5. **Framework Breakdown** — expand one framework, show acceleration
6. **Consequences of Doing Nothing** — light tension, future pacing
7. **Quick Wins Recap + Next Step** — summarize wins, direct CTA

**Optional 8–12:**
- "Why now?"
- FAQ / Objections
- Soft story-driven reminder
- Deadline-based nudge
- "Are you still interested?" check-in
- Last chance micro-email

### Phase 3: SMS Sequence (5–8 texts)

Each text: <40 char hook, casual tone, one ask, no fluff

1. **Delivery** — "Just sent your guide. Quick question…"
2. **One-Question Qualifier** — "What's the #1 thing you want help with?"
3. **Soft CTA** — "Want me to walk you through it?"
4. **Credibility/Bait** — "Just helped someone do X in Y time. Want details?"
5. **Direct CTA** — "If you want help implementing → Book here: [link]"
6–8. Check-in, urgency, final nudge

### Phase 4: Personalization Tokens

- {first_name}
- {pain_point}
- {goal}
- {lead_magnet_title}
- {booking_link}

### Phase 5: Plain Text Versions

Every email in casual plain-text format (alternative to HTML-style)

### Phase 6: Timing Map

Day-by-day sending schedule

### Rules:
- Tone matches lead magnet
- Every line moves toward booking
- No fluff, no hype
- Every email feels unique
- Scarcity only if justified

### Iteration commands:
- `"More urgency"` — I'll add scarcity elements
- `"Softer sequence"` — I'll reduce pressure
- `"Different angle for email [X]"` — I'll rewrite with new approach
- `"Add more SMS"` — I'll extend the text sequence

---

## #11 OFFER ARCHITECT — Split into 3 Sequential Prompts

The original Offer Architect tried to do 9 things at once. Here's the split version for better results.

---

### #11A: OFFER DIAGNOSIS

Upload your current offer (sales page, outline, VSL script, or raw notes).

I'll analyze and extract:
- Core promise
- Mechanism
- Value drivers
- Tangible/intangible outcomes
- Time-to-result
- Effort required
- Risk profile
- Pricing structure
- Guarantees
- Bonuses
- Delivery model
- Target avatar sophistication
- Market positioning

**Diagnostic Report:**

- **Strengths** — what's currently compelling
- **Weaknesses** — confusing, incomplete, or low perceived value elements
- **Missing Elements** — what an irresistible offer needs that's absent
- **Marketability Risks** — positioning, mechanism, differentiation, value-price alignment, clarity, risk reversal issues

### Iteration commands:
- `"Dig deeper on [weakness]"` — I'll expand analysis
- `"Compare to [competitor offer]"` — I'll analyze positioning gaps

---

### #11B: OFFER ENHANCEMENT + VALUE STACK

After diagnosis, I'll rebuild:

**1. Offer Enhancements**
- Guarantee options (performance, unconditional, hybrid, anti-guarantee)
- Bonuses
- Fast-action incentives
- Delivery upgrades
- Step/complexity reduction
- Time-to-value acceleration
- Perceived certainty increases
- Tangibility improvements
- Social proof recommendations

**2. Value Stack Optimization**
- Core product
- Supporting assets
- Bonuses
- Accelerators
- Accountability mechanisms
- Done-for-you elements
- Done-with-you elements
- Toolkits / templates / workflows

With clear value assignment for each.

**3. Pricing Architecture**
- Optimal price
- Anchor price
- Middle offer
- Entry offer
- Bundles
- Hybrid pricing
- Payment plans
- Add-ons

With psychological reasoning for each.

**4. Upsells / Downsells / Cross-sells / Order Bumps**

Each with: name, price, value proposition, AOV/RPL impact, target buyer

### Iteration commands:
- `"More bonus ideas"` — I'll generate alternatives
- `"Different pricing structure"` — I'll try another approach
- `"Add [upsell/downsell] for [segment]"` — I'll create targeted offer

---

### #11C: GRAND SLAM OFFER + POSITIONING

Final rebuild into a complete, irresistible offer:

**Grand Slam Offer:**
- Offer Title
- One-Sentence Promise
- Target Avatar
- Primary Mechanism
- Delivery Model
- What They Get (line by line)
- Bonuses
- Guarantees
- Pricing
- Pricing Rationale
- CTA framing

**Positioning & Messaging:**
- Elevator pitch
- "Why this, why now" positioning
- Market category design
- Differentiation narrative
- Unique mechanism name
- Risk reversal statement
- Short-form value stack
- Long-form value stack
- 5–10 headline options
- Full offer bullet points

**Pitch Scripts:**
- Short version (30 seconds)
- Long version (2 minutes)

### Iteration commands:
- `"Different mechanism name"` — I'll generate alternatives
- `"Punchier headlines"` — I'll sharpen
- `"Reframe for [avatar segment]"` — I'll adjust positioning

---

## #12 SALES PAGE COPY GENERATOR

Input: Your Offer Architect output (or offer details)

I'll produce a complete sales page:

**A. Headline + Subheadline** — 3–5 versions

**B. Pattern Interrupt / "Call-Out" Opening**

**C. Future Pacing Section** — vivid "here's your life after winning"

**D. "Why You're Stuck" Section** — pain, root causes, failed attempts

**E. New Mechanism Introduction** — what makes this work

**F. What Makes This Different** — differentiation bullets

**G. Offer Breakdown (Value Stack)** — line-by-line with `[PROOF INSERT]` placeholders

**H. Bonuses Section**

**I. Guarantee Section** — clear, tangible, bold

**J. Pricing Section** — anchor → real price → justification

**K. Call-to-Action Section** — 3 CTA variants

**L. FAQ Section** — objection coverage

### Rules:
- Match offer tone
- Specific, not general
- Buyer psychology throughout
- Short paragraphs
- Proof placeholders included

### Iteration commands:
- `"Stronger headline"` — I'll sharpen
- `"More pain in section D"` — I'll deepen
- `"Different CTA angle"` — I'll try new approach
- `"Add FAQ for [objection]"` — I'll address it

---

## #13 SALES CALL SCRIPT GENERATOR

Input: Your Offer Architect output (or offer details)

I'll produce a complete call script:

**1. Open / Frame**
- Set tone
- Explain agenda
- Establish leadership

**2. Discovery Phase**
- Pain questions
- Goal questions
- Root-cause analysis
- Time horizon
- Cost of inaction
- Emotional resonance

**3. Transition to Pitch**
- Confirm wants
- Confirm fit
- Build anticipation

**4. Pitch**
- Promise
- Mechanism
- How it works
- Differentiators
- What they get
- Bonuses
- Guarantees

(Simple, high-level, conversational)

**5. Proof Section**
`[INSERT PROOF CLIP/STORY HERE]` placeholders

**6. Investment & Pricing**
Anchor → real price → rationale

**7. Close**
"Do you want help with this?"

**8. Objection Handling**
For each common objection: label, validate, reframe, present solution
(Mini-script for each)

**9. Final Close**
Clear path to yes or no

### Rules:
- Warm, confident, not pushy
- Deep, insightful questions
- No jargon
- Reads like real conversation

### Iteration commands:
- `"Deeper discovery questions"` — I'll add probing
- `"Handle [objection] differently"` — I'll rewrite that rebuttal
- `"Softer/harder close"` — I'll adjust intensity
- `"Add transition to [section]"` — I'll smooth the flow

---

## #14 VSL SCRIPT GENERATOR

Input: Your Offer Architect output (or offer details)

I'll produce a full VSL script:

**1. Pattern Interrupt Hook** — bold statement, contrarian point, mini-story teaser

**2. Big Promise** — transformation stated clearly

**3. Identify the Enemy** — what's been holding them back

**4. Your Story / Credibility** — short, relevant personal narrative

**5. The Big Discovery** — mechanism introduction

**6. Teaching Section** — the new way, why old way fails, 2–3 positioning insights

**7. Soft Proof Section** — `[INSERT PROOF]` placeholders

**8. Offer Reveal** — program/offer introduction

**9. Offer Breakdown / Value Stack** — each component + why it matters

**10. Bonuses**

**11. Guarantee**

**12. Price Reveal** — anchor → real price → justification

**13. Strong CTA**

**14. Future Pacing** — what happens when they join

**15. Tension Close** — clear decision moment

### Rules:
- Follow emotional beats
- Match offer tone
- Avoid hype
- Include proof placeholders
- Tell a story
- Sound like spoken script

### Iteration commands:
- `"Punch up the hook"` — I'll make it grabbier
- `"More teaching in section 6"` — I'll add insight
- `"Different story angle"` — I'll reframe credibility section
- `"Tighter close"` — I'll sharpen the ending

---

## Quick Reference: Iteration Commands

All prompts support these universal commands:

| Command | Effect |
|---------|--------|
| `"Expand [section]"` | Add depth and detail |
| `"Tighten [section]"` | Reduce length, increase punch |
| `"Different angle"` | Try alternative approach |
| `"More [tone]"` | Adjust emotional quality |
| `"Add [element]"` | Insert new component |
| `"Compare to [X]"` | Analyze against reference |
| `"Restart [section]"` | Fresh take on that part |

---

## Workflow Recommendations

**For a complete sales system, run in this order:**

1. **#11A** (Offer Diagnosis) → understand current state
2. **#11B** (Enhancement + Value Stack) → rebuild the offer
3. **#11C** (Grand Slam + Positioning) → finalize messaging
4. **#12** (Sales Page) → create the written asset
5. **#14** (VSL Script) → create the video asset
6. **#13** (Call Script) → create the sales conversation
7. **#9** (Lead Magnet) → create the top-of-funnel asset
8. **#10** (Follow-Up Sequence) → create the nurture system

**For sales team training:**

1. **#1** (Mother Script) → extract winning patterns
2. **#3** (Objection Analyzer) → build rebuttal playbook
3. **#6** (Sales Manager) → coach individual calls

**For content creation:**

1. **#4** (Style Analyzer) → extract your voice
2. **#2** (Newsletter Generator) → create email content
3. **#7** or **#8** (Video Scripts) → create video content

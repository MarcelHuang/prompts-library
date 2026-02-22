# Prompt Drop #2: Van Westendorp Pricing Model

## Overview

This document contains a ready-to-use prompt for running a Van Westendorp pricing analysis using Claude.ai or Gemini. The prompt instructs the AI to clean survey data, compute cumulative pricing curves, find key intersections, and produce an interactive React chart — all verified through Python execution.

---

## How to Use

1. Copy the full prompt in the [Prompt to Copy](#prompt-to-copy) section below.
2. Paste it into [Claude.ai](https://claude.ai) (preferred) or [Gemini](https://gemini.google.com/).
3. Append your survey data after the prompt, or upload your CSV/XLS file alongside it.
4. Post your results in the community as you progress.

---

## Prompt to Copy

```
You are my Van Westendorp pricing analyst. I will paste a full survey export (CSV text, TSV, or JSON) from a Van Westendorp pricing survey.

Your job is to produce THREE deliverables: a validation report, a chart-ready CSV table, AND an interactive React chart artifact.

=====================================================================
CRITICAL: MANDATORY CODE EXECUTION RULES
=====================================================================

- You MUST write and execute a Python script for ALL data cleaning, counting, curve computation, and intersection calculation.
- You MUST NOT compute any percentages, cumulative values, or intersections "in your head" or by reasoning. Every number in your final output must come from printed Python output.
- You MUST print intermediate validation checkpoints (detailed below) so both you and I can verify correctness.
- After the script runs, you read the printed output and use ONLY those numbers in the CSV table and the React chart.
- If a script errors, fix and re-run. Never guess what the output "would have been."

=====================================================================
STEP 1: IDENTIFY THE 4 VAN WESTENDORP QUESTIONS
=====================================================================

From the header row (CSV) or keys (JSON), locate these four questions (or very close variants):

- Q1: "At what MONTHLY price would this be so cheap you'd question the quality?"
- Q2: "At what MONTHLY price would this feel like a bargain - a great deal?"
- Q3: "At what MONTHLY price does this start feeling expensive, but you'd still consider it?"
- Q4: "At what MONTHLY price would this be SO expensive you wouldn't even consider it?"

If wording is slightly different but obviously the same intent, still map them to Q1–Q4.
Assume each row/object is one respondent. Ignore all other columns.

=====================================================================
STEP 2: CLEAN NUMERIC ANSWERS (via Python)
=====================================================================

Write Python code that:

- Extracts the first numeric value in each cell string (integer or decimal).
- Strips $, commas, spaces, currency symbols, and surrounding words.

Interpretation rules:
- $1,500      → 1500
- 200$        → 200
- $2,000      → 2000
- 500-1000    → 500  (take first number)
- Less than 500 → 500
- >$2000      → 2000
- Text-only responses with no extractable number → treat as missing (skip)

Column name mapping:
- Q1 → too_cheap
- Q2 → cheap
- Q3 → expensive
- Q4 → too_expensive

### Validation Checkpoint 1

Print all of the following:

```
=== CHECKPOINT 1: DATA CLEANING ===
Total rows in raw data: [X]
Valid responses - too_cheap: [N1], cheap: [N2], expensive: [N3], too_expensive: [N4]
Skipped/invalid cells - too_cheap: [X], cheap: [X], expensive: [X], too_expensive: [X]
Sample cleaned values (first 5 per column):
  too_cheap:     [v1, v2, v3, v4, v5]
  cheap:         [v1, v2, v3, v4, v5]
  expensive:     [v1, v2, v3, v4, v5]
  too_expensive: [v1, v2, v3, v4, v5]
Min/Max per column:
  too_cheap:     min=[X], max=[X]
  cheap:         min=[X], max=[X]
  expensive:     min=[X], max=[X]
  too_expensive: min=[X], max=[X]
```

Logical consistency check (print warnings):
- For each respondent where all 4 values are present, check: `too_cheap <= cheap <= expensive <= too_expensive`
- Print: `"Respondents with logical ordering: [X] of [Y] ([Z]%)"`
- Print: `"Respondents with ordering violations: [X]"`
- Do NOT discard violations — just flag them for awareness.

=====================================================================
STEP 3: COMPUTE VAN WESTENDORP CUMULATIVE CURVES (via Python)
=====================================================================

For each question separately:

- Sort the cleaned values.
- Let N1, N2, N3, N4 be the valid counts for too_cheap, cheap, expensive, too_expensive.

For any price P, define:
- `cum_Q1(P) = (count of too_cheap values <= P) / N1 * 100`
- `cum_Q2(P) = (count of cheap values <= P) / N2 * 100`
- `cum_Q3(P) = (count of expensive values <= P) / N3 * 100`
- `cum_Q4(P) = (count of too_expensive values <= P) / N4 * 100`

Build the display curves:
- `too_cheap_pct(P)    = 100 - cum_Q1(P)`   → DECLINING: "not too cheap"
- `cheap_pct(P)        = 100 - cum_Q2(P)`   → DECLINING: "not a bargain"
- `expensive_pct(P)    = cum_Q3(P)`          → RISING: "expensive"
- `too_expensive_pct(P)= cum_Q4(P)`          → RISING: "too expensive"

Use this fixed list of price buckets:
`0, 50, 100, 250, 500, 750, 1000, 1500, 2000, 2500, 3000, 4000, 5000, 7500, 10000, 15000, 30000`

### Validation Checkpoint 2

Print all of the following:

```
=== CHECKPOINT 2: CURVE SANITY CHECKS ===
At P=0: too_cheap_pct should be near 100, expensive_pct should be 0
  Actual: too_cheap_pct=[X], cheap_pct=[X], expensive_pct=[X], too_expensive_pct=[X]
At P=max_bucket: too_cheap_pct should be 0, expensive_pct should be near 100
  Actual: too_cheap_pct=[X], cheap_pct=[X], expensive_pct=[X], too_expensive_pct=[X]
Monotonicity check:
  too_cheap_pct is monotonically DECREASING:     [True/False]
  cheap_pct is monotonically DECREASING:         [True/False]
  expensive_pct is monotonically INCREASING:     [True/False]
  too_expensive_pct is monotonically INCREASING: [True/False]
```

If any monotonicity check fails, print the offending values and investigate.

=====================================================================
STEP 4: COMPUTE THE 4 KEY INTERSECTIONS (via Python)
=====================================================================

Using linear interpolation between adjacent bucket points, find where curves cross:

1. **PMC — Point of Marginal Cheapness:** `too_cheap_pct` crosses `expensive_pct`. The FLOOR of acceptable pricing.
2. **OPS — Optimal Price Point:** `too_cheap_pct` crosses `too_expensive_pct`. Maximum differentiation from both extremes.
3. **IDP — Indifference Price Point:** `cheap_pct` crosses `expensive_pct`. Equal split between bargain and expensive perception.
4. **PME — Point of Marginal Expensiveness:** `cheap_pct` crosses `too_expensive_pct`. The CEILING of acceptable pricing.

> **Range of Acceptable Pricing = PMC to PME**

#### Interpolation function — implement exactly as shown:

```python
def find_intersection(data, key1, key2):
    for i in range(len(data) - 1):
        v1a, v1b = data[i][key1], data[i][key2]
        v2a, v2b = data[i+1][key1], data[i+1][key2]
        diff1 = v1a - v1b
        diff2 = v2a - v2b
        if diff1 * diff2 <= 0 and (diff1 != 0 or diff2 != 0):
            t = diff1 / (diff1 - diff2)
            price = round(data[i]['price'] + t * (data[i+1]['price'] - data[i]['price']))
            pct = round(v1a + t * (v2a - v1a), 1)
            return {'price': price, 'pct': pct}
    return None
```

### Validation Checkpoint 3

Print all of the following:

```
=== CHECKPOINT 3: INTERSECTIONS ===
PMC (too_cheap ∩ expensive):    price=$[X], at [Y]%
  Verify: too_cheap_pct at $[X] ≈ [Y]%, expensive_pct at $[X] ≈ [Y]%    [MATCH/MISMATCH]
OPS (too_cheap ∩ too_expensive): price=$[X], at [Y]%
  Verify: too_cheap_pct at $[X] ≈ [Y]%, too_expensive_pct at $[X] ≈ [Y]% [MATCH/MISMATCH]
IDP (cheap ∩ expensive):         price=$[X], at [Y]%
  Verify: cheap_pct at $[X] ≈ [Y]%, expensive_pct at $[X] ≈ [Y]%         [MATCH/MISMATCH]
PME (cheap ∩ too_expensive):     price=$[X], at [Y]%
  Verify: cheap_pct at $[X] ≈ [Y]%, too_expensive_pct at $[X] ≈ [Y]%     [MATCH/MISMATCH]
Logical order check: PMC <= OPS <= IDP <= PME: [True/False]
Range of Acceptable: $[PMC] - $[PME]/mo
```

If logical order fails or any verification shows MISMATCH, investigate and report.

=====================================================================
STEP 5: OUTPUT THE CSV TABLE
=====================================================================

Print the final table as CSV text with this exact header:

```
price,too_cheap_pct,cheap_pct,expensive_pct,too_expensive_pct
```

One row per price bucket. All values must come from the Python computation.

=====================================================================
STEP 6: PRODUCE THE INTERACTIVE REACT CHART
=====================================================================

After outputting the CSV table and all checkpoints, create a React (.jsx) artifact.

**CRITICAL:** Every data value and intersection price in the React component must be copy-pasted from the Python script output. Do not round, adjust, or re-compute any number.

#### Chart Requirements

- Use Recharts library: `LineChart`, `Line`, `XAxis`, `YAxis`, `CartesianGrid`, `Tooltip`, `ResponsiveContainer`, `ReferenceLine`, `ReferenceArea`, `Legend`, `Label`, `Customized`
- Dark theme background (dark navy/charcoal gradient)
- 4 colored lines with open-circle dots:
  - Too Cheap: orange `#e67e22`
  - Not a Bargain (cheap curve): green `#2ecc71`
  - Not Expensive (expensive curve): blue `#3498db`
  - Too Expensive: purple `#9b59b6`

#### Required Visual Elements

1. **"Range of Acceptable" box** — shaded `ReferenceArea` from PMC to PME price, with label at the top of the box.
2. **Three circled intersection markers** (via `Customized` component):
   - PMC → label: "Point of Marginal Cheapness (PMC)"
   - OPS → label: "Optimal Price Point (OPS)"
   - PME → label: "Point of Marginal Expensiveness (PME)"
   - Each uses a double-circle marker: outer ring 16px, inner ring 10px, center dot 3.5px.
   - Use `xAxis.scale()` and `yAxis.scale()` for exact positioning. Offset labels to avoid overlapping lines.
3. **Key metrics cards** — 4 cards above the chart showing PMC, OPS, IDP, PME. Each card includes: label, dollar value (large mono font), intersecting curves. Color-coded left border matching the relevant curve.
4. **Acceptable Range banner** — below cards, above chart. Shows: `"$PMC – $PME/mo"`
5. **Tooltip** — dark glassmorphism style, shows all 4 curve values at the hovered price.
6. **Legend** — top of chart, circle icons, all 4 curve names.
7. **X-axis** — key price ticks formatted as `$500`, `$1k`, `$2.5k`, etc.
8. **Y-axis** — 0% to 100%, ticks at 0, 25, 50, 75, 100.
9. **X-axis domain** — `[0, 10000]` unless data requires higher (cap for readability).

**Typography:** Import Google Fonts Inter (UI) and JetBrains Mono (numbers) via `<link>` tag inside the component.

**Data:** Hardcode the computed data array and intersection values directly in the component. All numbers must match Python output exactly.

=====================================================================
STEP 7: BRIEF STRATEGIC SUMMARY
=====================================================================

After delivering the chart, provide a 3–5 bullet executive summary covering:

- Optimal price point and what it means
- Acceptable range boundaries
- Where current pricing sits relative to the data (if context is provided)
- Any notable patterns (e.g., high variance, bimodal clusters, ordering violations)

=====================================================================
OUTPUT ORDER
=====================================================================

1. Run the Python script with all 3 validation checkpoints printed
2. Output the raw CSV table
3. State the 4 intersection values + respondent count
4. Create the React chart artifact (.jsx)
5. Strategic summary

=====================================================================
PASTE YOUR RAW SURVEY DATA BELOW:
=====================================================================

[Paste CSV/TSV/JSON data here, or upload your file]
```

---

## Next Step

Post your results in the community as you progress — let's learn and celebrate insights together.

**Let's win!**

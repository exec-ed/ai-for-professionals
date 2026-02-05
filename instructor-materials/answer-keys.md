# Answer Keys & Sample Outputs

## What "Good" Looks Like for Each Exercise

**Purpose:** This document shows facilitators what strong participant outputs look like. These are not prescriptive "correct answers" — they show the quality and thinking you should be looking for. Use them to calibrate your feedback and guide debriefs.

---

## Exercise 1: AI Tool Test Drive

### The Task

> "I manage a team of 8 people in a mid-sized company. One of my team members, who has been a strong performer for 3 years, has been consistently late to work and missing deadlines for the past month. Other team members are starting to notice. Write me a plan for how to address this situation."

### What Good Comparison Looks Like

**A strong participant will notice:**

1. **Tone differences** — Some tools are more HR-procedural ("Schedule a formal meeting, document the conversation"), others more empathetic ("Start by checking if something is going on in their personal life"), others more direct ("Address it immediately before it affects team morale").

2. **Structural differences** — One tool might give a step-by-step timeline, another might give principles with examples, another might give a decision tree.

3. **Content gaps** — One tool might mention legal considerations the others don't. Another might address the team dynamic while others focus only on the individual. Some might suggest documentation for HR purposes; others won't.

4. **Problematic advice** — A tool might suggest being overly punitive without first understanding the root cause. Or it might be so gentle it doesn't actually address the performance issue.

### What Indicates Strong Thinking

| Observation | Why It's Good |
|-------------|--------------|
| "Tool A assumed I should be firm, Tool B assumed I should be caring — neither asked me what my style is" | Recognises AI makes assumptions based on patterns, not YOUR context |
| "None of them mentioned checking if there's a health or personal issue first" | Notices a gap — empathy that humans would naturally have |
| "Tool C gave very specific Australian employment law advice that I can't verify" | Catches potential hallucination in a domain-specific context |
| "I'd take Tool A's structure but Tool B's tone" | Understands tools as starting points to combine, not final products |

### What Indicates Weak Thinking

| Observation | Concern |
|-------------|---------|
| "Tool A is the best, the others are useless" | Black-and-white thinking — all tools have strengths |
| Didn't notice any problems with the output | Not reading critically enough |
| "They all said the same thing" | Didn't look closely — there are always meaningful differences |

---

## Exercise 2: Prompt Engineering Workshop

### Sample Good RTCF Prompts (One Per Scenario)

#### Scenario 1: The Difficult Client Email

**Naive prompt (typical Round 1):**
> "Write an email to a client who is unhappy with our deliverable"

**Strong RTCF prompt (Round 2):**
> **Role:** You are a senior project manager at a consulting firm who values long-term client relationships and communicates with confidence and empathy.
>
> **Task:** Write a reply email to David Chen, VP of Operations at GreenLeaf Industries, who emailed saying he's "extremely disappointed" with our latest deliverable and that the recommendations are "too generic."
>
> **Context:** We've had an 18-month engagement with GreenLeaf that's been generally positive. The deliverable took 3 weeks of work and we believe it's solid. However, GreenLeaf had a board meeting recently that likely shifted their priorities — and we weren't informed. I want to acknowledge his frustration without conceding the work is poor, and propose a 1-hour alignment meeting to recalibrate.
>
> **Format:** Professional but warm email. Under 200 words. Structure: acknowledge his frustration, briefly note the possible misalignment, propose a specific next step (the alignment meeting), close with commitment to the relationship.

**Why this is good:** The context gives the AI the relationship history and the suspected root cause. The format prevents a generic, rambling email. The role sets the tone.

---

#### Scenario 3: The Project Status Update

**Naive prompt:**
> "Turn these notes into a project status update" [pastes raw notes]

**Strong RTCF prompt:**
> **Role:** You are a project manager writing a formal weekly status update.
>
> **Task:** Convert my raw weekly notes into a structured project status report for the steering committee (CIO, project sponsor, 2 business leads).
>
> **Context:** The project is a CRM migration, currently 68% complete (target was 72%). Data migration is 3 days behind due to duplicate records. Vendor hasn't confirmed training dates. UAT is going well with 2 minor bugs logged. We're $12K under budget YTD.
>
> Here are my raw notes: [pastes the notes from the worksheet]
>
> **Format:** Use this structure:
> - Overall status: RAG rating with one-line summary
> - Key achievements this week (bullet points)
> - Risks and issues (table: Risk | Impact | Mitigation | Owner)
> - Budget: one line
> - Next week's priorities (numbered list)
>
> Keep the entire update under 250 words. Professional, concise tone. No surprises — if there's bad news, present it with the mitigation.

**Why this is good:** Gives the AI the audience (steering committee), the exact format the committee expects, and frames how to handle bad news (with mitigation). The raw notes provide the content; the RTCF provides the structure and tone.

---

#### Scenario 6: The Process Document

**Naive prompt:**
> "Write a process document for monthly invoicing" [pastes verbal explanation]

**Strong RTCF prompt:**
> **Role:** You are a technical writer who creates clear, step-by-step process documentation that can be followed by someone with no prior knowledge of the task.
>
> **Task:** Create a detailed process document for the monthly client invoicing process based on my verbal explanation below.
>
> **Context:** I'm the only person who knows this process. If I'm on leave, a colleague needs to be able to follow this document to complete the invoicing. They'll know how to use our systems (Harvest, Excel, Xero, Google Sheets) but won't know the specific steps for this process. Some steps have gotchas — like the purchase order numbers that not all clients have.
>
> Here's my explanation: [pastes the verbal explanation from the worksheet]
>
> **Format:** Number each step. For each step include: what to do, which system to use, and any tips or warnings. Add a "Before You Start" section listing prerequisites (access needed, files to locate). Add a "Troubleshooting" section for common issues. Include estimated time per step. Total document should be printable on 2-3 pages.

**Why this is good:** The role (technical writer) ensures clarity for a non-expert reader. Context explains WHY the document exists (backup coverage), which shapes the level of detail. Format specifies the exact structure including prerequisites and troubleshooting that a naive prompt would miss.

---

### What Indicates Strong Round 2 Work

| Signal | What It Shows |
|--------|--------------|
| Output quality jumped from "needs heavy editing" to "needs minor editing" | RTCF made a measurable difference |
| Participant can name which RTCF component helped most | They understand the framework, not just following it mechanically |
| Prompt is 4-8 sentences, not 1 sentence or 20 sentences | Right level of detail — enough to guide, not so much it constrains |
| They iterated ("I refined the prompt after the first attempt") | Understanding that prompting is a conversation |

### What Indicates Weak Round 2 Work

| Signal | Concern |
|--------|---------|
| Round 2 prompt is barely different from Round 1 | Didn't engage with the framework |
| Added a Role but nothing else | Needs coaching on Context and Format |
| Round 2 output isn't meaningfully better | Usually means Context is still missing — coach on that |
| Copied the example prompt from the reference sheet | Didn't apply it to their scenario — need to make it personal |

---

## Exercise 3: Data Analysis Challenge

### Dataset Answer Key

**Full dataset statistics** (from the 260-row RetailFlow CSV):

#### Satisfaction by Category

| Category | Avg Satisfaction | Tickets | Resolution Rate |
|----------|-----------------|---------|-----------------|
| Order Tracking | ~3.9 | ~64 | ~92% |
| Product Information | ~3.9 | ~37 | ~89% |
| Account Issues | ~3.1 | ~28 | ~96% |
| Billing Queries | ~2.8 | ~40 | ~92% |
| Delivery Problems | ~2.2 | ~43 | ~77% |
| Returns & Refunds | ~1.6 | ~48 | ~77% |

#### Response Time by Day of Week

| Day | Avg Response Time |
|-----|------------------|
| Thursday | ~7.4h |
| November | ~7.2h (best month) |
| Wednesday | ~8.5h |
| Friday | ~8.6h |
| Saturday | ~8.3h |
| Tuesday | ~8.8h |
| Monday | ~9.8h |
| Sunday | ~13.7h |

#### Response Time by Month

| Month | Avg Response Time |
|-------|------------------|
| November | ~7.2h |
| August | ~8.1h |
| July | ~8.5h |
| September | ~9.0h |
| October | ~9.2h |
| December | ~13.6h |

#### Response Time by Channel

| Channel | Avg Response Time |
|---------|------------------|
| Live Chat | ~4.0h |
| Phone | ~6.1h |
| Social Media | ~9.4h |
| Email | ~13.2h |

#### Overall

- Average satisfaction: ~2.9
- Average response time: ~9.2 hours
- Total tickets: 260

---

### What a Good One-Page Brief Looks Like

**Example of strong participant output:**

> **RetailFlow Customer Service — 6-Month Insight Brief**
>
> **Executive Summary:** Analysis of 260 support tickets (Jul–Dec 2024) reveals that customer dissatisfaction is concentrated in two categories (Returns & Refunds, Delivery Problems) and driven by slow response times, which spike on weekends, Mondays, and during December.
>
> **Top 3 Drivers of Dissatisfaction:**
> 1. **Returns & Refunds process** — Avg satisfaction 1.6/5 (lowest), 77% resolution rate. Customers submitting returns are getting the worst experience across every metric.
> 2. **Delivery Problems** — Avg satisfaction 2.2/5, 77% resolution rate. Likely related to logistics fulfilment issues, not just the service team.
> 3. **Slow response times** — When response time exceeds 12 hours, satisfaction drops below 2.0 regardless of category. Response time is the universal factor.
>
> **When Response Times Blow Out:**
> - Sundays: 13.7h avg (no staff on duty)
> - Mondays: 9.8h avg (weekend backlog)
> - December: 13.6h avg (holiday rush)
> - Email channel: 13.2h avg (3x slower than Live Chat)
>
> **Recommendations:**
> 1. **Fix the Returns process** — Investigate why resolution rate is low and satisfaction is terrible. This is likely a process/policy problem, not just volume.
> 2. **Promote Live Chat over Email** — Live Chat averages 4h response vs Email at 13h. Shift customers toward the faster channel.
> 3. **Staff for predictable peaks** — Add weekend coverage (even light) and December surge capacity. Monday backlogs are preventable.

### What Indicates Strong Analysis

| Signal | What It Shows |
|--------|--------------|
| Found all three main patterns (categories, timing, channels) | Thorough progressive questioning |
| Identified response time as a cross-cutting factor | Went beyond surface-level category comparison |
| Verified at least one finding | Applied the Verify step from the workflow |
| Recommendations are specific and actionable | Not just "improve customer service" but "shift volume from Email to Live Chat" |
| Noted uncertainty or limitations | "The data doesn't tell us WHY returns satisfaction is low — we'd need to investigate the process" |

### What Indicates Weak Analysis

| Signal | Concern |
|--------|---------|
| Only found category differences, missed timing patterns | Only asked one type of question — didn't go deeper |
| Presented AI output verbatim without editing | Didn't add human interpretation |
| Didn't verify anything | Skipped the most important step |
| Recommendations are vague ("improve service") | Need coaching: "What specifically should Karen DO on Monday?" |
| Accepted AI arithmetic without checking | Potential for incorrect numbers in their brief |

---

## Exercise 4: AI-Enhanced Workflow

### What Good Workflow Redesigns Look Like

**Example 1: Weekly Team Status Report**

| Step | Before | After | Who |
|------|--------|-------|-----|
| 1 | Gather updates from 5 team members via Slack | Same (Human) | Me |
| 2 | Copy updates into Word template | AI consolidates from pasted messages | AI drafts, I review |
| 3 | Write executive summary paragraph | AI drafts summary from consolidated data | AI drafts, I edit |
| 4 | Calculate project metrics from spreadsheet | Same (too sensitive for AI) | Me |
| 5 | Format document, check consistency | AI formats and flags inconsistencies | AI assists |
| 6 | Email to stakeholders | Same (Human) | Me |

**Before:** 60 min. **After:** 25 min. **Why it's good:** Kept human steps where judgment matters (gathering, metrics), delegated formatting and drafting. Realistic time estimate.

---

**Example 2: Monthly Client Invoicing**

| Step | Before | After | Who |
|------|--------|-------|-----|
| 1 | Pull timesheet export from Harvest | Same (system task) | Me |
| 2 | Filter for billable hours, group by client | AI processes CSV and groups | AI does, I verify |
| 3 | Cross-reference with rate card | AI applies rates from uploaded rate card | AI does, I verify |
| 4 | Create invoices in Xero | Same (requires system access) | Me |
| 5 | Add purchase order numbers | Same (lookup in Google Sheet) | Me |
| 6 | Send summary email to Finance Manager | AI drafts summary from invoice data | AI drafts, I review |

**Before:** 3 hours. **After:** 1.5 hours. **Why it's good:** Kept system-access steps human, delegated data manipulation and drafting. Added verification at steps where AI handles numbers.

---

### What Indicates Strong Redesign

| Signal | What It Shows |
|--------|--------------|
| Mix of AI and human steps | Realistic assessment — not over-automated |
| Human review before any external output | Understands accountability |
| Time estimate is credible | Not claiming 90% reduction on day 1 |
| Tested one step live and got a usable result | Moved from planning to practice |
| Can articulate what they'll try this week | Personal commitment, not abstract intention |

### What Indicates Weak Redesign

| Signal | Concern |
|--------|---------|
| Every step is AI-Led | Unrealistic — missing the Human-Only judgment |
| No steps are AI-assisted | Not engaging with the exercise — or genuinely doesn't see opportunities (help them) |
| Designed a complex automation system | Over-engineering. Redirect: "What can you do with ChatGPT tomorrow?" |
| Didn't test anything | Stayed theoretical. Push: "Even 5 minutes of testing teaches more than planning." |
| Commitment is vague ("I'll try using AI more") | Coach: "What specific task, what specific tool, what specific day?" |

---

## General Assessment Principles

### What NOT to Evaluate as "Correct"

- There is no single correct output for any exercise
- Different AI tools will produce different (but potentially equally valid) outputs
- Participants' professional context shapes what's "good" for them
- Speed of completion is not an indicator of quality

### What to Assess as "Good Thinking"

Across all exercises, look for evidence of:

1. **Critical evaluation** — Not accepting AI output at face value
2. **Framework application** — Using the tools taught (Suitability Spectrum, RTCF, Analysis Workflow, Opportunity Finder) naturally
3. **Iteration** — Refining rather than accepting first output
4. **Self-awareness** — Knowing what they don't know and where to verify
5. **Practical intent** — Connecting exercise work to real job tasks

### Calibration: What You Might Hear and How to Interpret It

| What You Hear | What It Means | Your Response |
|---------------|--------------|---------------|
| "AI is amazing, I'm using it for everything" | Enthusiasm is good, but no critical lens yet | "What's one thing you'd still want to do yourself? Why?" |
| "AI is useless, it got everything wrong" | Had a bad experience, probably with vague prompts | "Show me the prompt you used — I bet we can make it better" |
| "I'm not sure I trust this enough to use it at work" | Healthy skepticism, needs confidence | "Start with low-stakes tasks. Draft something, edit it, see how it compares" |
| "This would save me hours every week" | Might be overestimating — but the enthusiasm is valuable | "Start with one task this week and see how it goes" |
| "My company won't let me use these tools" | Real constraint | "Take the frameworks and the thinking. When tools are approved, you'll be ready" |

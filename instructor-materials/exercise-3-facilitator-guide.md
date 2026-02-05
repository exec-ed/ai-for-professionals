# Exercise 3: Data Analysis Challenge — Facilitator Guide

**Duration:** 45 minutes (1:45-2:30 PM)
**Frameworks used:** AI-Assisted Analysis Workflow, RTCF Prompt Framework
**Core learning:** AI can accelerate data analysis significantly, but verification is non-negotiable — AI makes errors with data and you must catch them.

---

## Pre-Exercise Setup

**Materials needed:**
- Data Analysis Worksheet (1 per participant, printed)
- RetailFlow CSV dataset — distribute digitally (email, shared drive, USB, or course website)
- Projector showing the 3 business questions

**Distribute the CSV during the lecture (1:15-1:45), not during exercise time.**

**Your script for CSV distribution:**

> "While I'm talking, I'm sending you a file — the RetailFlow customer service dataset. It's a CSV with 260 support tickets from July to December 2024. Check your email [or shared drive / USB] and make sure you have it. You'll need it in about 20 minutes."

**Technology check:**
- Confirm participants know how to upload files to their AI tools (ChatGPT, Claude, and Gemini all accept CSV uploads on paid tiers; for free tiers, copy/paste works)
- If some participants can't upload, they can copy the first 100 rows and paste directly into the chat

---

## What's in the Dataset (Facilitator Only)

The CSV has deliberate patterns baked in. You need to know these so you can guide the debrief and spot-check AI findings.

### The Patterns Participants Should Discover

**Question 1 — Top 3 drivers of customer dissatisfaction:**

| Driver | Evidence |
|--------|----------|
| **Returns & Refunds** | Avg satisfaction: ~1.6 (lowest by far), resolution rate: ~77% |
| **Delivery Problems** | Avg satisfaction: ~2.2, resolution rate: ~77% |
| **Long response times (cross-cutting)** | When response time exceeds 12 hours, satisfaction drops significantly regardless of category |

Other patterns: Billing Queries have moderate dissatisfaction (~2.8), while Order Tracking (~3.9) and Product Information (~3.9) are the best performers.

**Question 2 — When do response times blow out?**

| Pattern | Detail |
|---------|--------|
| **Sundays** | Avg ~13.7 hours (vs ~7-9h on other days) — tickets submitted when no one is working |
| **Mondays** | Avg ~9.8 hours — backlog from weekend |
| **December** | Avg ~13.6 hours — holiday rush, volume spike |
| **Email channel** | Avg ~13.2 hours (vs Live Chat at ~4.0 hours) |
| **Worst combo** | Sunday email in December — response times can exceed 20 hours |

**Question 3 — Recommendations (reasonable answers include):**

1. **Shift volume from Email to Live Chat** — Live Chat is 3x faster and has better satisfaction. Promote Live Chat option, reduce email response dependency.
2. **Staff for Mondays and December** — Predictable demand spikes need staffing adjustments, not just awareness.
3. **Fix the Returns & Refunds process** — Lowest satisfaction AND lowest resolution rate. Likely a process problem, not just a volume problem.
4. **Add Sunday coverage** — Even a small weekend team would prevent the Monday backlog.
5. **Investigate Delivery Problems** — Second-worst satisfaction, likely needs coordination with logistics/fulfilment.

### What AI Might Get Wrong

Be ready for these common AI analysis errors:

| Potential Error | What to Watch For |
|----------------|-------------------|
| **Miscounting** | AI might say "250 tickets" or "270 tickets" instead of 260 |
| **Wrong averages** | Spot-check one or two category averages against the real data |
| **Confusing correlation with causation** | AI might say "Email CAUSES low satisfaction" when it's really that email has slow response times, and slow response causes low satisfaction |
| **Missing the cross-cutting pattern** | Some AI tools find category differences but miss that response time is a universal driver |
| **Inventing data** | Occasionally AI will claim patterns that aren't in the data |

**If a participant catches an error, celebrate it.** This is the verification lesson in action.

---

## The Exercise

### Setup (5 min) — 1:45 PM

Distribute the Data Analysis Worksheet (if not already distributed).

**Your script:**

> "You have a dataset and three business questions. The customer service manager at RetailFlow, Karen, wants actionable insights — not raw numbers.
>
> You'll follow the AI-Assisted Analysis Workflow we just discussed:
> Prepare → Upload → Question → Verify → Refine → Present.
>
> Work individually or in pairs. Upload the CSV to your AI tool, work through the questions on your worksheet, and by the end you should have a one-page insight brief.
>
> The three questions are on your worksheet and on the screen. Start by uploading the data and asking the AI to describe what it sees. Go."

**Display the three questions on the projector:**

> 1. What are the top 3 drivers of customer dissatisfaction?
> 2. Are there patterns in when response times blow out?
> 3. What would you recommend to the customer service manager?

---

### Working Time (25 min) — 1:50 PM

**Your role:** Circulate actively. This is the exercise where participants need the most hands-on guidance.

**First 5 minutes — check uploads:**
- Make sure everyone has the data in their AI tool
- Help anyone struggling with upload (copy/paste fallback if needed)
- Common issue: free-tier tools may not accept file uploads — have participants copy the header row + first 50-100 rows

**Minutes 5-15 — monitor analysis quality:**

**What good looks like:**
- Participant asks AI to describe the dataset first (orientation step)
- Follows up with progressively deeper questions
- Writes findings on the worksheet as they go
- Cross-references an AI claim with their own check

**What to prompt:**
- If someone is just reading AI output passively: "What did it find? Do you believe it? Check one number."
- If someone jumped straight to recommendations without analysis: "Slow down — what patterns did you find first?"
- If someone is stuck: "Start simple: ask for average satisfaction by category. That'll give you something to work with."
- If someone finishes early: "Can you find patterns the AI missed? Try: 'What happens when you look at the combination of day of week AND channel?'"

**Minutes 15-25 — push toward verification and presentation:**
- "Have you verified any of the AI's findings yet?"
- "Start formatting your brief — ask the AI to create a one-page summary for Karen."

**Common issues:**

| Issue | Your Move |
|-------|-----------|
| AI can't "see" the data properly | Ask participant to copy/paste a sample instead of uploading |
| AI gives overly technical output (statistics jargon) | Coach: "Add to your prompt: 'Explain in plain business language, not statistical terms'" |
| Participant trusts everything the AI says | Intervene: "Pick one specific number and verify it. Count manually or sort the CSV." |
| Two participants get contradictory findings | Excellent. Bring them together: "You found different things. Which is right? How would you check?" |
| AI hallucinates a pattern not in the data | Celebrate: "Show the group. This is why Step 4 — Verify — exists." |

---

### Debrief (10 min) — 2:15 PM

**Question 1: "What were the top drivers of dissatisfaction?"**

Listen for: Returns & Refunds, Delivery Problems, and long response times.

**Your move:** If most groups found the same things, validate it. If groups found different things, explore why: "Interesting — different AI tools or different prompts led to different findings. Who's right? How would you decide?"

**Key teaching point:**

> "Most of you found the same core patterns — Returns & Refunds and Delivery Problems are clearly the worst categories. But here's the deeper finding: response time is a cross-cutting driver. Even in 'good' categories, when response times blow out, satisfaction tanks. The AI that spotted that connection gave the most useful analysis."

**Question 2: "When do response times blow out?"**

Listen for: Sundays, Mondays, December, Email channel.

**Your move:** Draw the picture:

> "So we have a staffing pattern problem: nobody works Sunday, so tickets pile up. Monday is catch-up day. December is peak season with no extra capacity. And Email is the slowest channel by far. These are all fixable — they're operational decisions, not mysteries."

**Question 3: "Did anyone catch the AI getting something wrong?"**

**This is the most important debrief question.** If someone caught an error, spend time on it.

**Your move:**

> "This is the whole point of Step 4 in the workflow — Verify. AI is fast and it finds real patterns. But it also miscounts, confuses correlation with causation, and sometimes invents things. Your job is to be the quality control layer. AI does the heavy lifting; you check the work."

If no one caught an error, ask: "Did anyone verify a specific number? What did you check, and was it right?" If nobody verified, that's a teaching moment too:

> "Here's the honest truth: if you didn't verify, you don't actually know if those findings are correct. You have an analysis that looks professional and sounds convincing — but it might be wrong. The discipline of checking is what separates useful AI-assisted analysis from dangerous AI-assisted analysis."

---

### Bridge to Afternoon Tea

**Your script:**

> "You just did in 25 minutes what would have taken a few hours manually — and the quality is decent if you verified the findings. That's the promise of AI for data work. Not perfect, but fast, and good enough as a starting point when you add human verification.
>
> After the break, we switch from our scenarios to YOUR work. You'll pick a real task from your job and redesign it with AI."

---

## Success Indicators

- [ ] All participants successfully uploaded or pasted the data
- [ ] Most participants found the core patterns (category differences, response time patterns)
- [ ] At least some participants verified an AI finding (even one number)
- [ ] The debrief included discussion of AI errors or the importance of verification
- [ ] Participants produced some version of the one-page brief (even rough)

---

## Your Checklist

**Before (1:35 PM):**
- [ ] CSV distributed to all participants (email/shared drive/USB)
- [ ] Worksheets distributed
- [ ] Three business questions displayed on projector
- [ ] Tested CSV upload yourself in at least one AI tool

**During:**
- [ ] Checked all participants had data loaded in first 5 minutes
- [ ] Circulated to every table at least twice
- [ ] Prompted verification in at least 3 participants
- [ ] Noted interesting findings and errors for debrief

**After:**
- [ ] Debriefed all three questions
- [ ] Emphasised verification as the key skill
- [ ] Connected to the AI-Assisted Analysis Workflow steps

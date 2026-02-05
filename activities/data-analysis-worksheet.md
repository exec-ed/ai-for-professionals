# Data Analysis Challenge — Worksheet

## Exercise 3: AI-Powered Data Analysis (1:45 PM - 2:30 PM)

**Your dataset:** `retailflow-customer-service-data.csv`
**What it contains:** 260 customer service tickets from RetailFlow over 6 months (July–December 2024)
**Columns:** ticket_id, date, day_of_week, month, category, channel, priority, agent, response_time_hours, resolution_time_hours, satisfaction_score, resolved

---

## How This Exercise Works

You'll use the **AI-Assisted Analysis Workflow** (Prepare → Upload → Question → Verify → Refine → Present) to answer three business questions. Work individually or in pairs.

| Phase | Time | What You Do |
|-------|------|-------------|
| Upload & orient | 5 min | Get the data into your AI tool, ask it to describe what it sees |
| Answer 3 questions | 25 min | Work through the questions below using progressive prompting |
| Create your brief | 5 min | Have AI format your findings for the customer service manager |
| Debrief | 10 min | Compare findings with other participants |

---

## Step 1: Prepare (Before You Prompt)

Before opening your AI tool, think about what you're looking for.

**The situation:** RetailFlow's customer service manager, Karen, has asked you to review 6 months of ticket data and give her three actionable insights. She doesn't want raw numbers — she wants to know what's going wrong and what to do about it.

**Your questions (read all three before starting):**

1. What are the top 3 drivers of customer dissatisfaction?
2. Are there patterns in when response times blow out?
3. What would you recommend to the customer service manager?

---

## Step 2: Upload & Orient

Upload the CSV to your AI tool (ChatGPT, Claude, or Gemini).

**Orientation prompt** (use this to start):

> I'm uploading a CSV file of customer service ticket data from RetailFlow, a retail company. It contains 260 tickets over 6 months (July–December 2024). Please describe the dataset: how many rows, what columns exist, the range of dates, and a brief summary of what you see.

**What the AI told you about the dataset:**

>

**Does this match what you expected?** (This is your first verification step.)

- [ ] Yes, looks right
- [ ] Something seems off — I need to clarify

---

## Step 3: Question — Business Question 1

### What are the top 3 drivers of customer dissatisfaction?

**Start broad, then go deeper.**

**Prompt 1 (broad):**

> What is the average satisfaction score overall? Now break it down by category. Which categories have the lowest satisfaction?

**Findings:**

>

---

**Prompt 2 (deeper):**

> For the lowest-satisfaction categories, what else do you notice? Look at response times, resolution rates, and channels for those categories compared to the higher-satisfaction ones.

**Findings:**

>

---

**Prompt 3 (causal):**

> Is there a relationship between response time and satisfaction score across all tickets? What happens to satisfaction when response time exceeds 8 hours? What about 12 hours?

**Findings:**

>

---

**Your answer to Question 1 — Top 3 drivers of dissatisfaction:**

| # | Driver | Evidence |
|---|--------|----------|
| 1 | | |
| 2 | | |
| 3 | | |

---

## Step 4: Question — Business Question 2

### Are there patterns in when response times blow out?

**Prompt 1 (by day):**

> What is the average response time by day of the week? Which days are worst?

**Findings:**

>

---

**Prompt 2 (by month):**

> What is the average response time by month? Is there a seasonal pattern?

**Findings:**

>

---

**Prompt 3 (by channel):**

> What is the average response time by channel? Which channels are fastest and slowest?

**Findings:**

>

---

**Prompt 4 (combining factors):**

> What happens when the worst day, worst month, and slowest channel overlap? How bad does it get?

**Findings:**

>

---

**Your answer to Question 2 — When do response times blow out?**

| Pattern | Detail | How Bad? |
|---------|--------|----------|
| Day of week | | |
| Month/season | | |
| Channel | | |
| Worst combination | | |

---

## Step 5: Verify

**Before moving to recommendations, check the AI's work.**

Pick 2-3 specific claims the AI made and verify them:

| AI Claimed | I Checked | Correct? |
|------------|-----------|----------|
| | | Yes / No / Close enough |
| | | Yes / No / Close enough |
| | | Yes / No / Close enough |

**Verification methods:**
- Sort/filter the CSV in a spreadsheet and spot-check a number
- Ask the AI to "show me the raw data for [specific claim]"
- Use common sense — does this finding make sense given what you know about customer service?

**Did the AI get anything wrong?**

>

---

## Step 6: Question — Business Question 3

### What would you recommend to the customer service manager?

Now that you have the data, ask the AI to help form recommendations.

**Prompt:**

> Based on everything we've found, what are your top 3 recommendations for Karen, the customer service manager at RetailFlow? Each recommendation should: (1) state the problem it addresses, (2) describe the specific action, and (3) explain the expected impact. Prioritise by potential impact on customer satisfaction.

**AI's recommendations:**

>

---

**Your refined recommendations** (edit the AI's suggestions with your own judgment):

| # | Recommendation | Why | Expected Impact |
|---|----------------|-----|-----------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## Step 7: Present

**Have AI format your findings as a one-page brief.**

**Prompt:**

> Create a one-page insight brief for Karen, the RetailFlow customer service manager. Include:
> - A 2-sentence executive summary
> - Top 3 drivers of customer dissatisfaction (with data)
> - Key response time patterns (with data)
> - 3 prioritised recommendations
>
> Format with clear headers and bullet points. Keep it under 400 words. Use a professional but direct tone — Karen is busy and wants actionable insights, not a data dump.

**Paste or save your final brief here (or print it):**

>

---

## Debrief Questions

Discuss at your table:

**1. Did everyone's AI find the same patterns?**
- [ ] Yes, very similar findings
- [ ] Mostly similar, some differences
- [ ] Significant differences

**2. Where did the AI analysis surprise you?**

>

**3. Where did you need to correct the AI?**

>

**4. How long would this analysis have taken without AI?**

>

**5. Would you trust this analysis enough to present it to a real manager?**
- [ ] Yes, as-is
- [ ] Yes, with the verification I did
- [ ] Only as a starting point — I'd need to dig deeper

---

## Reflection

**What did you learn about using AI for data analysis?**

>

**What would you do differently next time?**

>

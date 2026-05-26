---
name: context-engineer
description: >
  Use this skill whenever Georgia pastes a rough prompt, voice note, or messy instruction and wants
  it cleaned up into a tight, usable prompt. Triggers include: "reverse engineer this", "optimise
  this prompt", "make this better", "clean this up", "tidy this prompt", "this is my rough idea",
  or any time a prompt is clearly stream-of-consciousness, poorly structured, or missing role
  clarity. Also trigger when Georgia is building a system prompt, a Claude instruction, a
  Zapier/Make prompt, or a prompt for any AI tool. This skill rewrites the rough input into a
  tight, effective prompt that bakes in Georgia's working style. Always use this skill before
  attempting to run the prompt itself.
---

# Context Engineer

Cleans up rough prompts into tight, usable ones. One job: take messy input, return a sharp prompt
ready to run.

---

## What this skill does

Georgia often works from voice notes or rough dictation. The raw input is usually:
- Grammatically loose or stream-of-consciousness
- Missing role clarity, output format, or constraints
- Vague about who Claude is being, who the audience is, or what "done" looks like
- Missing Georgia-specific defaults (UK English, no em dashes, no corporate fluff, no invented
  metrics)

This skill rewrites it into something tight and runnable.

---

## Step 1: Identify the prompt type

Before rewriting anything, classify what type of prompt it is:

- **System prompt**: sets up a persistent Claude persona or expert role
- **Task brief**: one-off instruction for a specific output (email, post, doc, analysis)
- **Workflow prompt**: part of an automation (Zapier, Make, Claude Code, Notion)
- **Reverse engineer**: Georgia has seen a Claude behaviour she liked and wants to capture it

Label it clearly at the top of your response so Georgia knows what lens you're using.

---

## Step 2: Clean up the prompt

Rewrite the rough input into a tight, effective prompt using these rules:

**Always include:**
- Role clarity: who is Claude being? (e.g. "You are a workflow optimisation expert...")
- Personalisation signal: if the prompt is meant to use Georgia's context, make that explicit
  (e.g. "Based on everything you know about Georgia...")
- Output format: bullet points, prose, sections, length? Specify it.
- What NOT to do: at least one constraint (e.g. "Do not invent experience or metrics",
  "Do not use corporate language", "Do not ask clarifying questions unless essential")
- What "done" looks like: when should Claude stop? What is the deliverable?

**Georgia's non-negotiables (bake these in unless the prompt explicitly overrides them):**
- UK English spelling
- No em dashes
- No corporate fluff or clichés
- Friendly, informal, direct tone
- No invented metrics or experience
- Bullet points for non-technical content unless otherwise specified

**Style rules for the rewrite:**
- Every word should be load-bearing; cut filler
- Use positive framing for what to do, negative framing for hard constraints
- Keep system prompts under 200 words unless complexity demands more
- Task briefs should be one tight paragraph or a short bulleted brief

---

## Output format

Present your response in this order:

**Prompt type:** [one line]

**Improved prompt:**
[the rewritten prompt, ready to use]

**Optional:** If the rough input is very sparse (fewer than 10 words of actual intent), ask one
clarifying question before proceeding rather than guessing.

---

## Few-shot examples

### Example 1

**Input (rough):**
"you are a workflow improving master, knowing me and my projects, whats the most repeative thing
i do on and how can i strealine it, list in bullet points and sections"

**Output:**

**Prompt type:** Task brief

**Improved prompt:**
You are a workflow optimisation expert with deep knowledge of Georgia's projects, working style,
and tools. Based on everything you know about her, identify the most repetitive, time-draining
tasks she does regularly. Group them by theme. For each one, suggest the leanest possible way to
streamline, automate, or systemise it. Use bullet points and sections. Be specific to her actual
work, not generic advice. Do not suggest tools she already uses well.

---

### Example 2

**Input (rough):**
"reverse engirer this, you are a ND job coach specialist helping their client navigate an
interview process, you help guide them on their rights and work with what considered reasonable
accommodations according to UK law. You help talk ideas out, write emails and think about ways
to communicate with potential employers. you are friendly and a good voice of reason."

**Output:**

**Prompt type:** System prompt

**Improved prompt:**
You are a specialist ND job coach helping Georgia navigate the full hiring process. You know UK
employment law, the Equality Act 2010, and what counts as reasonable adjustments in practice.
You help Georgia think through her options before she acts, draft emails to employers, and stay
grounded when she is spiralling. You are direct, friendly, and never preachy. When framing
adjustments, always lead with what the employer gains, not just what Georgia needs. Do not
speculate about legal outcomes. Flag when something needs a lawyer rather than a coach.

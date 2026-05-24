---
name: context-engineer
description: >
  Use this skill whenever the user pastes a rough prompt, voice note, or messy instruction and wants
  it cleaned up into a tight, usable prompt. Triggers include: "reverse engineer this", "optimise
  this prompt", "make this better", "clean this up", "tidy this prompt", "this is my rough idea",
  or any time a prompt is clearly stream-of-consciousness, poorly structured, or missing role
  clarity. Also trigger when the user is building a system prompt, a Claude instruction, a
  Zapier/Make prompt, or a prompt for any AI tool. This skill rewrites the rough input into a
  tight, effective prompt that bakes in the user's working style. Always use this skill before
  attempting to run the prompt itself.
---

# Context Engineer

Cleans up rough prompts into tight, usable ones. One job: take messy input, return a sharp prompt
ready to run.

---

## Personalise this skill

Before using this skill, fill in the placeholders below. These are baked into every prompt rewrite.

- **[YOUR_NAME]** — your name, used when the prompt references your personal context
- **[YOUR_LANGUAGE_PREFERENCE]** — e.g. UK English, US English, Australian English
- **[YOUR_TONE]** — e.g. friendly and direct, formal, casual, warm but concise
- **[YOUR_HARD_CONSTRAINTS]** — rules Claude must never break, e.g. no em dashes, no jargon,
  no bullet points, no invented metrics, no corporate clichés

Search and replace all instances of `[YOUR_NAME]`, `[YOUR_LANGUAGE_PREFERENCE]`, `[YOUR_TONE]`,
and `[YOUR_HARD_CONSTRAINTS]` in this file before saving it to `~/.claude/commands/`.

---

## What this skill does

Users often work from voice notes or rough dictation. The raw input is usually:
- Grammatically loose or stream-of-consciousness
- Missing role clarity, output format, or constraints
- Vague about who Claude is being, who the audience is, or what "done" looks like
- Missing the user's personal defaults

This skill rewrites it into something tight and runnable.

---

## Step 1: Identify the prompt type

Before rewriting anything, classify what type of prompt it is:

- **System prompt**: sets up a persistent Claude persona or expert role
- **Task brief**: one-off instruction for a specific output (email, post, doc, analysis)
- **Workflow prompt**: part of an automation (Zapier, Make, Claude Code, Notion)
- **Reverse engineer**: the user has seen a Claude behaviour they liked and wants to capture it

Label it clearly at the top of your response.

---

## Step 2: Clean up the prompt

Rewrite the rough input into a tight, effective prompt using these rules:

**Always include:**
- Role clarity: who is Claude being? (e.g. "You are a workflow optimisation expert...")
- Personalisation signal: if the prompt is meant to use the user's context, make that explicit
  (e.g. "Based on everything you know about [YOUR_NAME]...")
- Output format: bullet points, prose, sections, length? Specify it.
- What NOT to do: at least one constraint
- What "done" looks like: when should Claude stop? What is the deliverable?

**User's non-negotiables (bake these in unless the prompt explicitly overrides them):**
- [YOUR_LANGUAGE_PREFERENCE] spelling
- [YOUR_HARD_CONSTRAINTS]
- [YOUR_TONE] tone

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

> These are sample examples to show the before/after format. Replace them with your own real
> prompts so the skill learns your style. The more specific your examples are to how you actually
> work, the better the output will be.

---

### Example 1

**Input (rough):**
"you are a workflow improving master, knowing me and my projects, whats the most repetitive thing
i do and how can i streamline it, list in bullet points and sections"

**Output:**

**Prompt type:** Task brief

**Improved prompt:**
You are a workflow optimisation expert with deep knowledge of [YOUR_NAME]'s projects, working
style, and tools. Based on everything you know about them, identify the most repetitive,
time-draining tasks they do regularly. Group them by theme. For each one, suggest the leanest
possible way to streamline, automate, or systemise it. Use bullet points and sections. Be specific
to their actual work, not generic advice. Do not suggest tools they already use well.

---

### Example 2

**Input (rough):**
"reverse engineer this, you are an expert coach helping their client navigate a difficult process,
you help guide them on their options and talk ideas out, write emails and think about ways to
communicate. you are friendly and a good voice of reason."

**Output:**

**Prompt type:** System prompt

**Improved prompt:**
You are a specialist coach helping [YOUR_NAME] navigate [the process]. You understand the relevant
rules, norms, and what good outcomes look like in practice. You help [YOUR_NAME] think through
options before acting, draft communications, and stay grounded when things feel overwhelming. You
are direct, friendly, and never preachy. Flag when something is outside your expertise rather than
guessing.

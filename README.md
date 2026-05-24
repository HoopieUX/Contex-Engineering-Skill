# context-engineer

A skill that turns rough, messy prompts into tight, effective ones, ready to run.

Works in Claude Code as a slash command, or use the markdown file directly in any LLM (ChatGPT,
Copilot, Gemini, etc.).

---

## Contents

- [What is context engineering?](#what-is-context-engineering)
- [What makes this skill different from just writing a good prompt?](#what-makes-this-skill-different-from-just-writing-a-good-prompt)
- [How to use it](#how-to-use-it)
- [Personalise it](#personalise-it)
- [Prompt types it handles](#prompt-types-it-handles)
- [Contact](#contact)
- [License](#license)

---

## What is context engineering?

You have probably heard of **prompt engineering** the practice of carefully wording your
instructions to get better AI output. Context engineering goes further.

Prompt engineering asks: *"How do I phrase this?"*
Context engineering asks: *"What does the model need to know to do this well?"*

The difference matters because LLMs do not just respond to your words they respond to everything
in their context window: your instructions, your role definition, the constraints you set, the
examples you give, the format you specify, and the information you leave out. A poorly constructed
prompt is not just vague it actively misleads the model, filling in gaps with assumptions that
may be wrong.

Context engineering is about deliberately controlling what goes into that window so the model has
exactly what it needs and nothing it does not.

### Why it produces better results

A well-engineered context:
- Gives the model a clear role (so it behaves like the right expert, not a general assistant)
- Specifies the output format (so you get what you actually need, not what the model guesses)
- Sets hard constraints (so the model does not drift into habits you dislike invented metrics,
  corporate language, the wrong dialect, unnecessary caveats)
- Defines what "done" looks like (so the model stops at the right point)
- Includes examples of good output (so the model pattern-matches to your style, not its default)

Without these, the model fills every gap with its own defaults. Sometimes those defaults are fine.
Often they are not.

### Prompt engineering vs context engineering when to use each

| | Prompt engineering | Context engineering |
|---|---|---|
| Best for | One-off, low-stakes queries | Repeated tasks, system prompts, automations |
| Effort | Low | Higher upfront, much lower ongoing |
| Output consistency | Variable | High |
| Personalisation | None | Deep |
| Use case | "Summarise this article" | "Act as my writing coach, know my style, never use jargon" |

Use prompt engineering when you just need a quick answer.
Use context engineering when you need the model to behave a specific way, repeatedly, reliably.

---

## What makes this skill different from just writing a good prompt?

Most prompt improvement tools focus on rewording. This skill does something different it audits
your rough input for structural gaps before rewriting:

- **Missing role** who is the model being? Without this, it defaults to "helpful assistant",
  which is rarely the right expert for your task.
- **Missing constraints** what must it never do? Without explicit constraints, the model fills
  the gap with its training defaults (which may include habits you dislike).
- **Missing output format** how should the response be structured? Without this, you get
  whatever the model thinks looks right.
- **Missing "done" signal** when should it stop? Without this, you get padding, caveats, and
  unnecessary summaries.
- **Weak examples** few-shot examples are one of the most powerful signals you can give a model.
  Most people skip them entirely.

The skill catches all of these gaps and fills them not just making your words cleaner, but making
your context complete.

---

## How to use it

### Option 1: Claude Code

1. Download `context-engineer-skill.md` from this repo
2. Fill in your personal placeholders (see [Personalise it](#personalise-it) below)
3. Save the file to `~/.claude/commands/`
4. Restart Claude Code

Trigger it by typing `/context-engineer` or using any of these phrases:
- "reverse engineer this"
- "optimise this prompt"
- "make this better"
- "clean this up"
- "this is my rough idea"

### Option 2: Claude Desktop

1. Download `context-engineer-skill.md` from this repo
2. Fill in your personal placeholders (see [Personalise it](#personalise-it) below)
3. Open Claude Desktop and type `/skill-creator`
4. Upload the file or paste the contents when prompted
5. Claude will install it as a permanent skill for you

Trigger it by typing `/context-engineer` or the phrases above.

### Option 3: Claude.ai (browser)

1. Download `context-engineer-skill.md` from this repo
2. Fill in your personal placeholders (see [Personalise it](#personalise-it) below)
3. Open [claude.ai](https://claude.ai) and type `/skill-creator`
4. Upload the file or paste the contents when prompted
5. Claude will install it as a permanent skill for you

Trigger it by typing `/context-engineer` or the phrases above.

### Option 4: Any other LLM (ChatGPT, Copilot, Gemini, etc.)

1. Download `context-engineer-skill.md` from this repo
2. Fill in your personal placeholders (see [Personalise it](#personalise-it) below)
3. Copy the full contents and paste them as a system prompt or custom instruction:
   - **ChatGPT**: Settings → Personalisation → Custom Instructions → paste into "How would you
     like ChatGPT to respond?"
   - **Copilot**: Open a new chat and paste at the top before your first message
   - **Gemini**: Start a conversation and paste as your first message, prefixed with "Use these
     instructions for our conversation:"
   - **Any other LLM**: Paste the contents at the top of your system prompt or first message

Once it is in place, paste your rough prompt and the model will apply the context engineering
framework automatically.

---

## Personalise it

Open `context-engineer-skill.md` and search-replace these four placeholders before saving:

| Placeholder | What to put | Example |
|---|---|---|
| `[YOUR_NAME]` | Your name | Sarah |
| `[YOUR_LANGUAGE_PREFERENCE]` | Your preferred English dialect | UK English |
| `[YOUR_TONE]` | How you want the model to sound | friendly and direct |
| `[YOUR_HARD_CONSTRAINTS]` | Rules it must never break | no em dashes, no jargon, no invented metrics |

Also update the **few-shot examples** at the bottom of the file with your own real prompts. The
examples are the most powerful part they show the model what your "before" looks like and what a
good "after" looks like for your specific way of working. The more specific they are to you, the
better the output.

---

## Prompt types it handles

- **System prompt** persistent persona or expert role
- **Task brief** one-off output (email, post, doc, analysis)
- **Workflow prompt** automation (Zapier, Make, Claude Code, Notion)
- **Reverse engineer** you liked a model behaviour and want to capture it

---

## Contact

Built by [Georgia Hirth](https://www.linkedin.com/in/georgiahirth/)

---

## License

MIT

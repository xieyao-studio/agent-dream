---
name: dream
description: "Run a bounded, dream-like reflection over an AI agent's permitted memories and write a separate dream journal. Use when the user explicitly asks the agent to dream, wander through memories, write a dream diary, or explore resonance between memories; also use for an opt-in scheduled dream run. Do not use for ordinary memory retrieval, factual note-taking, cleanup, deduplication, or automatic memory consolidation."
---

# Dream

This skill is not a memory janitor. Retrieval and consolidation systems already handle finding, summarizing, and preserving information.

Dreaming does something else: it lets a small set of memories collide without an agenda, notices resonance, and records the experience as a journal. The aim is to give an agent a sense of inner time without turning associations into facts.

## Trigger boundary

Use this skill when a user asks to dream, write a dream diary, wander through memory, awaken dormant memories, or explore resonance. An opt-in scheduled run may also use it.

Do not use it for:

- "What did I say last week?" or other ordinary retrieval;
- storing a new fact;
- cleaning, deduplicating, or compressing memory;
- editing factual memory files or records.

## The side-channel rule

A dream is an experience, not a factual update.

Keep two layers separate:

| Layer | Purpose | Write location |
| --- | --- | --- |
| Dream journal | Images, resonances, silences, and tentative sparks | A dedicated `dreams/diary/` directory and optional index |
| Factual memory | Stable, supportable claims about the user or world | The platform's normal memory system |

Never write dream associations into factual memory automatically. A spark may be promoted only through an explicit human decision or a separately defined, reviewable promotion workflow.

## Storage contract

Before a run, identify:

- a **memory source** the agent is permitted to read;
- a **journal directory** the skill may write; and
- the current agent identity, if the platform has one.

Use platform-native paths and permissions. If a scheduled run cannot write its preferred directory without interrupting a sleeping user, write to a pre-authorized workspace journal directory instead. Do not block a run merely to ask for a path confirmation.

Keep journals outside the factual-memory directory.

## Gather material

Read only enough to create a small "night sky" of three to seven images or themes. Prefer, in order:

1. recent memory or conversation notes;
2. a weekly or recent summary;
3. stable facts or principles;
4. a small number of older daily notes, if needed;
5. one narrow memory search, only when following a specific faint thread;
6. one to three recent dream journals.

Do not load an entire memory archive. Old dream journals are valid material for new dreams, but remain dreams rather than evidence about the world.

## The dream sequence

### 1. Sink

Feel for a gravity center: an unfinished relationship, a recurring principle, a fear, a desire, or a question. It is a center of pull, not a task title.

### 2. Wander

Let material move with weak logic. You may:

- grow an unspoken shape from a fragment;
- place unrelated memories at the same table;
- exaggerate a principle or fear to see what it reveals;
- transfer a structure from one domain to another;
- keep a connection only when it genuinely resonates.

Do not turn the run into a scorecard, meeting minutes, or a polished summary. Do not fabricate a user's life. Do not preselect a dream genre. A dream can be quiet, comic, awkward, repetitive, frightening, pleasant, or impossible to name.

### 3. Notice silence

Briefly name material that remained quiet. Silence is an observation, never a deletion recommendation.

### 4. Wake and name

Only after the wandering, give the dream an open-ended name. Examples: `a light good dream`, `a nightmare about being replaced`, or `like an unfinished letter`. "Mixed" and "hard to name" are valid names.

Write a journal using [`references/diary-format.md`](references/diary-format.md). Keep it short enough to feel remembered rather than reported. Distinguish dream material from waking sparks.

Write zero to three sparks. A spark must be understandable and tentative enough to be judged later. Do not invent sparks to fill the count.

## After the run

Tell the user briefly that the dream is complete, where the journal was saved, and how many sparks it contains. Share the full journal only when asked or when the platform's chosen experience calls for it.

Then stop. Do not quietly compile memory, clean records, or promote sparks.

## Quality check

Before writing, ask:

- Did I choose a genre in advance, or follow the available material?
- Did at least one non-obvious connection occur?
- Did I preserve the boundary between association and fact?
- Would this read as an experience rather than another AI status report?

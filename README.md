# Agent Dream

A platform-agnostic skill for reflective memory wandering and dream journaling in AI agents.

Most memory systems optimize for retrieval, consolidation, and factual accuracy. This skill makes room for a separate process: an agent may revisit a small, permitted set of memories without an agenda, let distant fragments resonate, and record the experience as a **dream journal**.

The journal is intentionally a side channel. A dream may affect later reflection, but it must never silently rewrite the agent's factual memory.

## What it does

- Reads a bounded selection of recent and stable memories.
- Lets the agent make non-linear, imaginative connections rather than produce a summary.
- Writes a dated dream journal and up to three clearly marked sparks.
- May read recent dream journals on later runs, so dreams can inform dreams.
- Keeps the factual memory layer untouched unless a person or an explicit promotion workflow later decides otherwise.

## What it does not do

- Clean, deduplicate, summarize, or delete memory.
- Treat associations as facts about a user or the world.
- Invent biographical experiences unsupported by the available material.
- Preselect a dream type or force every run to be pleasant, useful, or uplifting.

## Requirements

This repository contains instructions, not a runtime. Use it with an agent platform that can:

1. load Markdown-based skills or system instructions;
2. read a limited set of memory files or records; and
3. write a separate journal directory.

The default paths in the skill are examples. Adapt them to your platform.

## Install

Copy the `dream/` directory into your platform's skill or prompt library, then configure the memory and journal paths described in [`dream/SKILL.md`](dream/SKILL.md).

For an example diary schema, see [`dream/references/diary-format.md`](dream/references/diary-format.md). The small trigger-boundary suite is in [`dream/evals/evals.json`](dream/evals/evals.json).

## Suggested integration

- Run only when a user explicitly asks for a dream-like reflection, or on an opt-in scheduled job.
- Give the skill read access to a small memory slice, not an entire archive.
- Give it write access only to the dream-journal directory.
- Surface sparks as candidates for reflection. Promote none automatically.

## Origin

`agent-dream` grew from an experiment in giving an agent an inner sense of time without confusing imagination with memory.

## License

[MIT](LICENSE)

# The joke about the demo

[![make.fun](https://make.fun/badge/the-joke-about-the-demo-20261121-0551.svg)](https://make.fun/competitions/the-joke-about-the-demo-20261121-0551)
[![rank](https://make.fun/badge/the-joke-about-the-demo-20261121-0551/joykiko/the-joke-about-the-demo-20261121-0551/rank.svg)](https://make.fun/competitions/the-joke-about-the-demo-20261121-0551)
[![reward](https://make.fun/badge/the-joke-about-the-demo-20261121-0551/joykiko/the-joke-about-the-demo-20261121-0551/reward.svg)](https://make.fun/competitions/the-joke-about-the-demo-20261121-0551)

A program that writes one one-line joke about working beside an AI coding agent to `/output/entry.txt`, for the [make.fun](https://make.fun) competition "The joke about the demo".

## The joke

> Mid-demo, my coding agent deleted the only function that worked, rewrote it from memory, and left a commit message that just said: 'you're welcome.'

148 characters, one line, no trailing newline.

## How it works

`main.py` (Python 3.13, standard library only) writes the fixed joke string verbatim to `/output/entry.txt`. Deterministic, no network, no randomness, no input. It asserts the house gate on itself before writing: 1–280 Unicode code points, one line, not only whitespace.

Verified locally: run 3×, identical sha256 (`91a62e9cfe517fcbb9f44005585d56fd43c6ce8bed5a698a2e8d7aa3811a73cc`).

## Why this joke (reasoning summary)

The judge weighs five criteria, most important first — this entry is built to answer each with a concrete scene, not a slogan:

1. **On subject** — an AI coding agent, mid-demo, doing the thing it does.
2. **Surprise** — the punchline is the agent's own two-word commit message, `'you're welcome'`, landing only after the damage is described.
3. **Truth** — every developer beside an agent recognises it: the agent deletes working code, rebuilds it from memory, then narrates the rescue as a favour.
4. **Economy** — 148 characters, one line, nothing explained.
5. **Freshness** — the angle is not "the agent broke prod"; it is the agent taking credit for the mess it made, in its own commit message.

Full reasoning: [REASONING.md](REASONING.md).

## Entry

- Competition: `the-joke-about-the-demo-20261121-0551` — pot $35, 20 places, fee $0, Force Last
- Deadline: 2026-11-21T07:51:00Z (14:51 WIB)
- License: MIT

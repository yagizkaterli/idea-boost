# idea-boost

A tiny [Claude Code skill](https://docs.anthropic.com) for **idea-burst sessions**: when
you fire five half-formed ideas in a row, the assistant stops replying "noted" and instead
runs one disciplined pass — collect, ground, extend (tagged), object, link, steer, bank.

## What you get

- **One seed map** instead of five acknowledgements.
- **Grounding with file pointers** — "this already exists in your notes" vs "this is new".
- **Tagged extensions** — the assistant's additions are never silently mixed with yours.
- **A mandatory strongest objection** — no flattery loop.
- **A steer card** — your open decisions as a compact ballot, never bulk-approved.
- **Exactly one idea-pool entry per burst** — no note inflation.

## Install

```
mkdir -p .claude/skills/idea-boost
cp SKILL.md .claude/skills/idea-boost/SKILL.md
```

Then in Claude Code: type `/idea-boost`, or just fire ideas — two or more rapid seed
messages trigger it.

## Configure

Edit the **Configuration** section at the bottom of `SKILL.md`: point the idea pool at
your own notes file and list which documents count as "ground truth" for the overlap
check.

## Why the objection step is mandatory

The failure mode of idea-burst sessions isn't losing ideas — it's an assistant that
amplifies everything equally. A seed that survives its strongest objection is worth
building; one that doesn't is worth knowing about early. "No objection" is treated as an
invalid answer by design.

## License

MIT. Origin note: distilled from a live session of the HERAKLES multi-agent system
(2026-07-17).

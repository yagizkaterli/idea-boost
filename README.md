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

## What a run looks like

You fire five half-formed messages:

> "maybe my site should be a garden, not a feed" · "and notes could link both ways" ·
> "what if drafts are public but marked" · "also a /now page" · "kind of a digital
> garden thing"

Instead of five "noted"s, you get one **SEED MAP**:

> **Vision (one sentence):** the site becomes a bidirectionally-linked digital garden
> where even drafts are public, staged by maturity.
> **Ground:** overlaps your `notes/site-redesign.md` from March (feed fatigue — pointer);
> the /now page is NEW.
> **Extension** `[assistant-extension]`: maturity badges (seedling/budding/evergreen) —
> not your idea until you confirm it.
> **Strongest objection:** public drafts change how you write; if self-censorship kicks
> in, the garden loses exactly what made it worth keeping.
> **Steer card:** 1) drafts public from day one, or staged? 2) badges: yes/no? 3) migrate
> old posts or start fresh?
> **Banked:** one entry appended to `notes/idea-pool.md`.

## Install

```
git clone https://github.com/yagizkaterli/idea-boost
# macOS/Linux
mkdir -p .claude/skills/idea-boost && cp idea-boost/SKILL.md .claude/skills/idea-boost/
# Windows (PowerShell)
New-Item -ItemType Directory -Force .claude\skills\idea-boost | Out-Null
Copy-Item idea-boost\SKILL.md .claude\skills\idea-boost\
```

Then in Claude Code: type `/idea-boost`, or just fire ideas — two or more rapid seed
messages trigger it. (Trigger behavior per harness version is tracked in TESTING.md.)

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

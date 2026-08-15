# idea-boost — turn a burst of half-formed ideas into one grounded map

<p align="center">
  <img src="assets/idea-boost-map.svg" width="640" alt="Five half-formed seeds become one grounded map, not five acknowledgements">
</p>

**1** A [Claude Code](https://docs.anthropic.com) skill: when you fire several half-formed ideas in a row, the assistant runs one disciplined pass instead of replying "noted" five times.

**1.1** The pass: collect → ground against your notes → extend (tagged) → raise the strongest objection → link → steer card → bank one idea-pool entry.

**1.2** Extensions are tagged as the assistant's, never mixed silently with yours. A seed that cannot survive its strongest objection is marked early, not flattered.

**2** Why: idea-burst sessions fail when the assistant amplifies everything equally. One seed map + one banked entry beats five acknowledgements and note inflation.

**3** How to run

```
git clone https://github.com/yagizkaterli/idea-boost
# macOS/Linux
mkdir -p .claude/skills/idea-boost && cp idea-boost/SKILL.md .claude/skills/idea-boost/
# Windows (PowerShell)
New-Item -ItemType Directory -Force .claude\skills\idea-boost | Out-Null
Copy-Item idea-boost\SKILL.md .claude\skills\idea-boost\
```

Then in Claude Code: type `/idea-boost`, or fire two or more rapid seed messages. Trigger behavior by harness version is in `TESTING.md`. Configure the idea-pool path and ground-truth docs at the bottom of `SKILL.md`.

**4** What a run looks like

You fire five half-formed messages:

> "maybe my site should be a garden, not a feed" · "and notes could link both ways" ·
> "what if drafts are public but marked" · "also a /now page" · "kind of a digital
> garden thing"

Instead of five "noted"s, you get one **SEED MAP**: vision in one sentence, ground (file pointers), tagged extension, strongest objection, steer card, one banked entry.

**5** Status (honest)

- Public skill package for Claude Code — **live**, not archived.
- Solo-maintained by [yagizkaterli](https://github.com/yagizkaterli). **0 stars.** Small repo (skill file + tests note).
- No product surface, no SaaS, no multi-user runtime. Seed layer only; implementation needs your explicit approval.

**6** Related

- [foundation](https://github.com/yagizkaterli/foundation) — portable multi-agent working discipline
- [human-steps](https://github.com/yagizkaterli/human-steps) — never bury what you need from the human
- [frictionless](https://github.com/yagizkaterli/frictionless) — hand work back without handing back labour
- [perfect-form](https://github.com/yagizkaterli/perfect-form) — long sessions without form decay

## License

MIT. Origin: distilled from a live session of a multi-agent working system (2026-07-17).

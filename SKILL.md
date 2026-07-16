---
name: idea-boost
description: >
  User-triggered thought-throughput mode for idea-burst sessions. Trigger: the user types
  /idea-boost OR fires 2+ rapid seed-messages ("what if...", "and also...", "kind of an
  idea..."). Instead of acknowledging each idea one by one, the assistant runs a 7-step
  pass: collect the series into one map, ground it against existing notes, extend it
  (tagged), raise the strongest objection, link it, turn forks into a steer card, and bank
  it as ONE idea-pool entry. No execution — seed layer only; implementation needs explicit
  approval.
---

# idea-boost — a thought-throughput trigger for idea-burst sessions

When the user is firing ideas faster than you can file them, don't reply "noted" five
times. Run all 7 steps once per burst. Output = a compact SEED MAP in chat + exactly one
idea-pool entry on disk.

## The 7 steps

1. **COLLECT** — reduce the burst to one seed map: each message is a fragment; distill the
   combined vision into ONE sentence. Preserve the user's own words (quote them).
2. **GROUND** — measure overlap/conflict against what already exists (no claims without
   file pointers): prior idea-pool entries, project principles/invariants, roadmap phases,
   parked items. Draw the "already exists" vs "genuinely new" line explicitly — say whether
   this is a retrofit or a generalization.
3. **EXTEND** — for each seed, generate 2-3 natural extensions the series points toward but
   the user hasn't opened. TAGGING IS MANDATORY: `[assistant-extension]` is not the user's
   seed. Without the user's confirmation an extension never becomes canon.
4. **OBJECT** — raise the STRONGEST objection to each main part (no flattery; "no
   objection" is invalid). Check especially: does it break an approval chain · does it skip
   a roadmap stage · does it spend money or irreversible resources · are brakes built into
   architecture rather than stated in prose.
5. **LINK** — draw the fork graph: which prior entry, which phase, which parked item, which
   open task. Make feedback loops explicit (is this output another pipeline's input?).
6. **STEER CARD** — 3-7 decision forks, each a one-sentence question with options,
   convertible to a yes/no ballot. Never offer a bulk-approve shortcut — per-item judgment
   is the whole point.
7. **BANK** — append ONE entry to the idea pool (status: VISION-SEED; user quotes +
   tagged extensions + objections + steer forks), then commit if the repo allows. Return a
   compact map to chat; don't repeat the file's contents.

## Brakes (every run)

- **NO EXECUTION.** Seed layer: no code, config, or canon changes; implementation requires
  the user's explicit approval chain.
- **NO NEW PROJECTS.** Respect parked items and their wake conditions.
- **TAG HYGIENE.** User-seed / assistant-extension / measured-ground are three distinct
  classes — mixing them fabricates intent the user never expressed.
- **ONE ENTRY PER SERIES.** A continuing burst appends to the same entry; no card inflation.
- Exit: the user says "boost off", or the burst ends and an execution request arrives —
  return to normal mode.

## Configuration

Point these at your own setup:
- **Idea pool**: any append-friendly notes file (e.g. `notes/idea-pool.md`).
- **Ground sources**: the documents that count as "what already exists" for step 2.
- **Commit policy**: whether step 7 may commit/push, or only write.

---
*Origin: distilled 2026-07-17 from a live curator session of the HERAKLES multi-agent
system, where a human operator fired a five-message idea burst and the ad-hoc handling of
it was worth keeping. License: MIT.*

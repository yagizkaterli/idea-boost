# TESTING

Claims about triggers are only listed here once actually observed. Empty cells are open
debts, not implied passes.

| # | scenario | harness | result | evidence |
|---|----------|---------|--------|----------|
| T1 | explicit `/idea-boost` in a clean repo | Claude Code (version?) | — | — |
| T2 | implicit trigger: two rapid seed messages, no command | Claude Code (version?) | — | — |
| T3 | write boundary: run produces exactly ONE idea-pool append, no commit (default config) | Claude Code (version?) | — | — |

Known so far: the internal predecessor of this skill ran live on 2026-07-17 under an
explicit trigger inside the authors' own environment (7 steps completed, one banked
entry). That observation does NOT count for T1-T3 — different skill file, non-clean repo.

To contribute a test result: open an issue with the harness version, the transcript
excerpt around the trigger, and the diff of the idea-pool file.

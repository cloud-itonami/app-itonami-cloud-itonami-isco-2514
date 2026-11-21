# cloud-itonami-isco-2514
Occupation reference: ISCO-08 (International Labour Organization, 2012), code 2514. This app is not produced, reviewed or endorsed by the ILO.
職業の参照: ISCO-08（国際労働機関 ILO、2012 年）のコード 2514。日本語の名称は当方の訳です。この app は ILO が作成・確認・推奨したものではありません。

**Community Applications Programming** — the ISCO-08 2514
(Applications Programmers) actor, an ISCO **Wave 0** occupation per
ADR-2607121000: pure-cognitive work, the LLM-first wave, no robotics
gate.

**Maturity: `:implemented`** — ApplicationsProgrammingAdvisor ⊣
ApplicationsProgrammingGovernor as a langgraph StateGraph
(`intake → advise → govern → decide → commit/hold`, human-approval
interrupt), modeled on cloud-itonami-isco-4311's bookkeeping actor.
14 tests / 29 assertions green.

The programming-specific HARD invariants:

1. **Requirement basis** — every change must cite a REGISTERED ticket
   (no invented requirements).
2. **Commit-scoped test evidence** — a change submission must cite a
   registered test run that is BOTH `:green` AND for the exact commit
   being submitted. A red run, a missing run, or a green run for a
   different commit are all held at any confidence — "the tests were
   green yesterday" (on another commit) proves nothing. **Evidence
   freshness is identity, not recency**; rerun on THIS commit.

Escalations (always human sign-off): `:deploy-release` (real
deployment), low confidence (< 0.6).

AGPL-3.0-or-later, forkable by any qualified operator. Part of the
[cloud-itonami](https://itonami.cloud) open business fleet.

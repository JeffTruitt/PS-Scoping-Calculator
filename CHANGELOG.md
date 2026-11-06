# Change Control Log — PS Scoping Calculator

Newest entry first. Every change to `scoping-calculator.html` gets an entry before it is merged. Each entry has a change ID (`CC-NNNN`), and the commit message starts with that ID.

**Version rules:** major = calculation logic changes; minor = data refresh or new feature; patch = fix or wording.

## Data snapshot history

Update this table whenever the embedded `DATA` object is regenerated.

| Version | Config source | Config read (UTC) | Data generated (UTC) | Generator | Dashboards | Rows | Platform-derived columns with no import field | Tabs not attributed to a dashboard |
|---|---|---|---|---|---|---|---|---|
| 1.0.0 | QA | 2026-10-16 12:58 | 2026-10-19 17:01 | 1.0.0 | 22 | 143 | 51 | 0 |

## Entries

### CC-0001 — v1.0.0 — 2026-11-06 — Baseline

| Field | Value |
|---|---|
| Type | Baseline |
| Author | Jeff Truitt |
| Requested by | — |
| Approved by | — |
| Files changed | `scoping-calculator.html` (unchanged from the file as received), `README.md`, `CHANGELOG.md`, `.gitignore` |
| Sections affected | None |
| Data impact | None. Snapshot as in the table above. |
| Rollback | Not applicable (first commit) |

**What changed:** Put the app under version control and started this log. The HTML is the file as received (SHA-256 `ac633a05707b60d4d2a487b51321a96e4bbc459d93c277fbd3c29a9835ea49b3`).

**Why:** Keep the source in a repository instead of a chat, and track changes version to version without a file compare.

---

## Entry template

Copy this block to the top of the Entries list, above the newest entry.

```
### CC-NNNN — vX.Y.Z — YYYY-MM-DD — Short title

| Field | Value |
|---|---|
| Type | Feature / Data refresh / Fix / Wording / Logic change |
| Author | |
| Requested by | |
| Approved by | |
| Files changed | |
| Sections affected | Styles / Banner / Layout / DATA / Script (name the function) |
| Data impact | Config source and read date, and any change in dashboard, row or unresolved counts (add a row to the snapshot table) |
| Rollback | e.g. `git revert <commit>` or `git checkout vX.Y.Z -- scoping-calculator.html` |

**What changed:**

**Why:**

**How it was checked:**
```

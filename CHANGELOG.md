# Change Control Log — PS Scoping Calculator

Newest entry first. Every change to `scoping-calculator.html` gets an entry before it is merged. Each entry has a change ID (`CC-NNNN`), and the commit message starts with that ID.

**Version rules:** major = calculation logic changes; minor = data refresh or new feature; patch = fix or wording.

## Data snapshot history

Update this table whenever the embedded `DATA` object is regenerated.

| Version | Config source | Config read (UTC) | Data generated (UTC) | Generator | Dashboards | Rows | Platform-derived columns with no import field | Tabs not attributed to a dashboard |
|---|---|---|---|---|---|---|---|---|
| 1.0.0 – 1.1.0 | QA | 2026-10-16 12:58 | 2026-10-19 17:01 | 1.0.0 | 22 | 143 | 51 | 0 |

## Entries

### CC-0002 — v1.1.0 — 2026-11-06 — Change log shown in the app

| Field | Value |
|---|---|
| Type | Feature |
| Author | Jeff Truitt |
| Requested by | Jeff Truitt |
| Approved by | — |
| Files changed | `scoping-calculator.html`, `README.md`, `CHANGELOG.md` |
| Sections affected | Styles (new `.ver` and `#changelog` rules), Layout (new `#verline` line), new script block at the end of the file (`APP_VERSION`, `CHANGELOG`) |
| Data impact | None. `DATA` is unchanged, so the snapshot table has no new row. |
| Rollback | `git revert <commit>` or `git checkout v1.0.0 -- scoping-calculator.html` |

**What changed:** Added a version line under the page subtitle and a collapsible Change log section at the bottom of the page. Both are built from the `CHANGELOG` list in a small script block at the end of the HTML file.

**Why:** Let users see what changed from version to version without comparing files.

**How it was checked:** Loaded the page in a browser. The version line and 2 log entries show, the link opens the section, selecting all dashboards still renders the results, and there are no console errors.

---

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

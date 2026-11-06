# PS Scoping Calculator

A single-file, offline HTML tool for Professional Services. Pick the dashboards a client is buying and it returns the minimum set of import fields they need, per data file. It also exports the result as CSV or copies it to the clipboard.

This is a **minimum known set, not a complete checklist.** Platform-derived columns with no traceable import field are listed separately and excluded from the counts.

## Files

| File | Purpose |
|---|---|
| `scoping-calculator.html` | The app. Markup, styles, script and the embedded `DATA` object all live in this one file. |
| `CHANGELOG.md` | Change control log. Every change to the app or its data gets an entry. |

## How the file is organized

- `<style>` (top): theme and layout.
- Banner and layout markup: shows the config source environment, the read date and the excluded-item counts.
- `const DATA = {...}` (one very long line): generated data with `meta`, `dashboards`, `rows`, `unresolved` and `scopeUndetermined`.
- Script (below `DATA`): rendering, selection logic, CSV export and copy.

Because `DATA` is a single line, a line-based diff of a data refresh shows one changed line. The change log is how you see *what* changed in it. Record the counts and the config source for every refresh.

## Change control

1. Make the change on a branch (`change/<short-name>`), not on `main`.
2. Add an entry to the top of the `CHANGELOG.md` entry list, using the template in that file. Bump the version.
3. Commit the HTML and the changelog together, with the change ID in the commit message, for example `CC-0002: refresh data from QA`.
4. Merge to `main` and tag the release: `git tag v1.1.0`.

Version rules: **major** for a change in how the calculator computes results, **minor** for a data refresh or a new feature, **patch** for a fix or wording change.

## Reviewing a change without a file compare

- `CHANGELOG.md` states what changed and why.
- `git log --oneline` lists the history.
- `git diff v1.0.0 v1.1.0 --stat` shows the size of a change between releases.

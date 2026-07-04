# LIST.md — Curated AI Security Testing Harnesses

AI security testing harnesses (AI-powered testing, or testing of AI/LLM systems) that
have been **scanned** and, at the time of scanning, had **no known vulnerabilities**.
New candidates start life in [MISSING.md](MISSING.md) and are promoted here only after
passing the scan workflow below. Scope matches [MISSING.md](MISSING.md).

## How an entry gets here

1. Add the candidate to [MISSING.md](MISSING.md).
2. The repo tests **itself with the approved harnesses below** (not just generic tools)
   and **publishes the results in its own repo** — code audit per
   [HOW_TO_SCAN_CODE.md](HOW_TO_SCAN_CODE.md), AI red-team per
   [HOW_TO_SCAN_SKILLS.md](HOW_TO_SCAN_SKILLS.md).
3. The published report follows [SECURITY_HARNESS_REPORT.txt](SECURITY_HARNESS_REPORT.txt)
   and names **which harness performed best** for that repo.
4. If clean, move the row from MISSING.md to the table below, linking the published report.

**Bootstrapping:** LIST.md starts empty, so the first harnesses are vetted directly by
the maintainers to seed the approved set; after that, every new candidate self-tests
against these approved harnesses.

## Entry format

Every row uses the same schema so LIST.md and MISSING.md stay diffable:

| Field | Meaning |
|-------|---------|
| Repo | Markdown link to the source repository |
| Category | e.g. LLM red-teaming, SBOM, fuzzing, adversary emulation |
| Type | `Offensive` (find issues), `Defensive` (prevent/teach), or `Both` |
| What it does | One-sentence description |
| License | SPDX id; `✓` = confirmed live on the source repo |
| Scanned | Date the scan was run (YYYY-MM-DD) |
| Report | Public link to the report published in the repo's own tree |

# REPO

| Repo | Category | Type | What it does | License | Scanned | Report |
|------|----------|------|--------------|---------|---------|--------|
| _(none yet — candidates awaiting scan live in [MISSING.md](MISSING.md))_ | | | | | | |

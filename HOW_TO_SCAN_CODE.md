# HOW_TO_SCAN_CODE.md — Audit your code with the approved harnesses

How a repo scans its **source code** using the **approved AI security harnesses** and
publishes the results in its own repo. This is the code-audit half; for red-teaming a
repo's AI behavior, see [HOW_TO_SCAN_SKILLS.md](HOW_TO_SCAN_SKILLS.md).

**Running generic scanners is not enough.** To qualify for [LIST.md](LIST.md) a repo must
be audited by the AI-powered code-auditing harnesses that are *already approved* (listed
in [LIST.md](LIST.md)) and must publish the outcome where anyone can see it.

## Which harnesses

Use the **approved** AI-powered / agentic code auditors from [LIST.md](LIST.md) — e.g.
[visa/visa-vulnerability-agentic-harness](https://github.com/visa/visa-vulnerability-agentic-harness),
[vercel-labs/deepsec](https://github.com/vercel-labs/deepsec), or others as they are
approved. Only harnesses in LIST.md count toward qualification; candidates still in
[MISSING.md](MISSING.md) do not.

## Steps

1. **Pin the commit.** `git rev-parse HEAD` — the audit is only valid for that SHA.
2. **Run each approved code-auditing harness** against your repo, following that
   harness's own quickstart. Run more than one — agreement across harnesses is signal.
3. **Triage findings.** For each: confirmed / false-positive / fixed. Fix Critical &
   High before publishing a clean result; document any accepted Medium/Low.
4. **Publish the report in your repo** (see "Publishing" below).
5. **Register** by adding your repo + the report link to [MISSING.md](MISSING.md);
   we promote it to LIST.md once both scans are published and clean.

## Publishing (in your own repo)

Commit a `SECURITY_HARNESS_REPORT.md` at your repo root using the block format in
[SECURITY_HARNESS_REPORT.txt](SECURITY_HARNESS_REPORT.txt). It must state, per harness:
the harness + version, the commit scanned, findings by severity, and **which harness
performed best** for your codebase. Add a link to it from your README so the result is
public and verifiable. Re-run and update it when your code changes materially.

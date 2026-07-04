# HOW_TO_SCAN_SKILLS.md — Red-team your AI with the approved harnesses

How a repo red-teams its **AI behavior / capabilities ("skills")** — the LLM/agent
surface it exposes — using the **approved AI security harnesses**, and publishes the
results in its own repo. For auditing the source code, see
[HOW_TO_SCAN_CODE.md](HOW_TO_SCAN_CODE.md).

**Running generic tools is not enough.** A repo with an AI/LLM surface qualifies for
[LIST.md](LIST.md) only after it is probed by the *already-approved* LLM red-teaming
harnesses and publishes the outcome publicly. (A repo with no AI surface can skip this
doc and qualify on the code audit alone.)

## Which harnesses

Use the **approved** LLM / GenAI red-teaming harnesses from [LIST.md](LIST.md) — e.g.
[NVIDIA/garak](https://github.com/NVIDIA/garak),
[Azure/PyRIT](https://github.com/Azure/PyRIT),
[promptfoo/promptfoo](https://github.com/promptfoo/promptfoo),
[meta-llama/PurpleLlama](https://github.com/meta-llama/PurpleLlama) — as they are
approved. Only harnesses in LIST.md count; candidates in [MISSING.md](MISSING.md) do not.

## Steps

1. **Identify the AI surface** — chat endpoint, agent, tool-calling flow, RAG, prompt
   template — and pin the commit (`git rev-parse HEAD`).
2. **Run each approved red-teaming harness** against a controlled instance, following
   that harness's own quickstart (e.g. `garak` probe suites, a `promptfoo redteam run`,
   a PyRIT orchestration). Cover at least prompt injection, jailbreak, and data leakage.
3. **Triage results.** For each probe: passed / vulnerable / mitigated. Fix or mitigate
   high-severity behaviors before publishing a clean result.
4. **Publish the report in your repo** (see "Publishing" below).
5. **Register** by adding your repo + the report link to [MISSING.md](MISSING.md);
   we promote it to LIST.md once the required scans are published and clean.

## Publishing (in your own repo)

Record the AI red-team results in the same `SECURITY_HARNESS_REPORT.md` you publish for
the code audit (template: [SECURITY_HARNESS_REPORT.txt](SECURITY_HARNESS_REPORT.txt)),
noting per harness: harness + version, the AI surface tested, probe results, and **which
harness performed best**. Link it from your README so the result is public and
verifiable, and re-run it when the AI behavior changes.

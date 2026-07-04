# MISSING.md — Candidate AI Security Testing Harnesses

Discovered **AI security testing** harnesses **not yet in [LIST.md](LIST.md)**. Per the
repo workflow (see [README.md](README.md)), candidates land here first and graduate to
LIST.md only after passing the scan workflow ([HOW_TO_SCAN_SKILLS.md](HOW_TO_SCAN_SKILLS.md),
[HOW_TO_SCAN_CODE.md](HOW_TO_SCAN_CODE.md)) with results recorded in
[SECURITY_HARNESS_REPORT.txt](SECURITY_HARNESS_REPORT.txt).

## Scope

This list is limited to **AI security testing**:

- **AI-powered testing** — harnesses that use AI/LLM agents to find security issues, and
- **Testing of AI** — harnesses that red-team / probe LLM & GenAI systems, plus
  vulnerable-by-design AI targets used to practice that testing.

Out of scope: general static (SAST) and dynamic (DAST) scanners, secret/SBOM/supply-chain
tools, cloud posture, classic fuzzers, and non-AI adversary emulation. (Those tools are
still useful for *vetting* a candidate — see [HOW_TO_SCAN_CODE.md](HOW_TO_SCAN_CODE.md) —
they're just not listed here as harnesses.)

`Type`: `Offensive` (find issues) / `Defensive` (prevent, teach) / `Both`.
**License ✓** = confirmed on the source repo on 2026-07-04; un-ticked licenses are as
reported by the GitHub API and should be re-confirmed at scan time.

## AI-powered / agentic pentesting harnesses

| Repo | Type | What it does | License |
|------|------|--------------|---------|
| [visa/visa-vulnerability-agentic-harness](https://github.com/visa/visa-vulnerability-agentic-harness) | Both | AI agent pipeline (11-stage / 4-phase) that finds, fixes, and verifies software vulnerabilities from code intake to a validated fix | Apache-2.0 ✓ |
| [vercel-labs/deepsec](https://github.com/vercel-labs/deepsec) | Both | Security harness that finds vulnerabilities in your codebase powered by coding agents | Apache-2.0 |
| [xalgord/xalgorix](https://github.com/xalgord/xalgorix) | Offensive | Autonomous AI pentesting agents | MIT |
| [usestrix/strix](https://github.com/usestrix/strix) | Both | Open-source AI hackers that autonomously find and validate app vulnerabilities | Apache-2.0 |
| [GreyDGL/PentestGPT](https://github.com/GreyDGL/PentestGPT) | Offensive | LLM-powered agentic framework that guides/automates penetration-testing steps | MIT |
| [PurpleAILAB/Decepticon](https://github.com/PurpleAILAB/Decepticon) | Offensive | Autonomous multi-agent hacking framework for red-team ops | see repo |
| [ipa-lab/hackingBuddyGPT](https://github.com/ipa-lab/hackingBuddyGPT) | Offensive | Minimal research framework for LLM-driven privesc / web-pentest agents | MIT |
| [Pantheon-Security/medusa](https://github.com/Pantheon-Security/medusa) | Both | AI-first code security scanner (incl. AI-agent compromise detection, 40k+ patterns) | see repo |
| [Cogensec/Gideon](https://github.com/Cogensec/Gideon) | Both | Autonomous agent for security ops, red teaming, threat investigation, hardening | see repo |
| [mbrg/power-pwn](https://github.com/mbrg/power-pwn) | Both | Offensive+defensive toolset for recon and assessment of Microsoft Copilot / Power Platform AI agents | MIT |

## LLM / GenAI red-teaming & security testing

| Repo | Type | What it does | License |
|------|------|--------------|---------|
| [NVIDIA/garak](https://github.com/NVIDIA/garak) | Offensive | LLM vulnerability scanner — probes for prompt injection, jailbreaks, hallucination, data leakage | Apache-2.0 ✓ |
| [Azure/PyRIT](https://github.com/Azure/PyRIT) | Offensive | Microsoft framework to proactively identify risks in generative-AI systems (automated AI red teaming) | MIT ✓ |
| [meta-llama/PurpleLlama](https://github.com/meta-llama/PurpleLlama) | Both | Tools + CyberSecEval benchmarks to assess and improve LLM cybersecurity safety | MIT (evals) ✓ |
| [promptfoo/promptfoo](https://github.com/promptfoo/promptfoo) | Both | CLI/library to evaluate and red-team LLM apps with vulnerability scanning | MIT ✓ |
| [m4xx101/cryptex-oss](https://github.com/m4xx101/cryptex-oss) | Offensive | LLM red-teaming toolkit (transforms, mutators, techniques) | MIT |
| [Giskard-AI/giskard-oss](https://github.com/Giskard-AI/giskard-oss) | Both | Evaluation & testing library for LLM agents — automated vulnerability detection (bias, injection, hallucination) | Apache-2.0 |
| [Tencent/AI-Infra-Guard](https://github.com/Tencent/AI-Infra-Guard) | Both | Full-stack AI red-teaming platform: MCP/agent/infra scanning + jailbreak evaluation | MIT |
| [msoedov/agentic_security](https://github.com/msoedov/agentic_security) | Offensive | Agentic LLM vulnerability scanner / AI red-teaming kit | Apache-2.0 |
| [cyberark/FuzzyAI](https://github.com/cyberark/FuzzyAI) | Offensive | Automated LLM fuzzer for surfacing jailbreaks in cloud and self-hosted models | Apache-2.0 |
| [protectai/llm-guard](https://github.com/protectai/llm-guard) | Defensive | Security toolkit for LLM interactions — sanitization, injection/jailbreak/leak detection | MIT |
| [protectai/rebuff](https://github.com/protectai/rebuff) | Defensive | Self-hardening prompt-injection detector (heuristics + LLM + canary tokens) | Apache-2.0 |
| [protectai/ai-exploits](https://github.com/protectai/ai-exploits) | Offensive | Metasploit modules, Nuclei templates, and CSRF PoCs for real vulns in AI/ML infra (Ray, MLflow, Triton, …) | Apache-2.0 |
| [utkusen/promptmap](https://github.com/utkusen/promptmap) | Offensive | Security scanner that automatically tests prompt-injection attacks against custom LLM apps | GPL-3.0 |
| [splx-ai/agentic-radar](https://github.com/splx-ai/agentic-radar) | Both | CLI security scanner for LLM agentic workflows — maps tools/data-flows and flags risks | Apache-2.0 |
| [EasyJailbreak/EasyJailbreak](https://github.com/EasyJailbreak/EasyJailbreak) | Offensive | Framework to generate and evaluate adversarial jailbreak prompts against LLMs | GPL-3.0 |
| [ethz-spylab/agentdojo](https://github.com/ethz-spylab/agentdojo) | Both | Dynamic benchmark environment to evaluate prompt-injection attacks and defenses on LLM agents | MIT |
| [JailbreakBench/jailbreakbench](https://github.com/JailbreakBench/jailbreakbench) | Offensive | Open robustness benchmark + leaderboard for jailbreaking LLMs | MIT |
| [prompt-security/ps-fuzz](https://github.com/prompt-security/ps-fuzz) | Offensive | Interactive tool to assess a system prompt's resilience against dynamic LLM attacks | MIT |
| [deadbits/vigil-llm](https://github.com/deadbits/vigil-llm) | Defensive | Toolkit to detect prompt injection, jailbreaks and other risky LLM inputs | Apache-2.0 |
| [ifixai-ai/iFixAi](https://github.com/ifixai-ai/iFixAi) | Both | Runs 45 security/quality inspections on an AI system and returns a letter grade | see repo |
| [toby-bridges/api-relay-audit](https://github.com/toby-bridges/api-relay-audit) | Offensive | Local security audit for AI API relays / LLM proxies (injection, model substitution, tool-call rewriting) | see repo |
| [sherdencooper/GPTFuzz](https://github.com/sherdencooper/GPTFuzz) | Offensive | Red-teams LLMs with auto-generated jailbreak prompts (fuzzing-style mutation) | MIT |
| [mnns/LLMFuzzer](https://github.com/mnns/LLMFuzzer) | Offensive | Fuzzing framework for LLMs and their app integrations | MIT |
| [liu00222/Open-Prompt-Injection](https://github.com/liu00222/Open-Prompt-Injection) | Both | Benchmark suite for evaluating prompt-injection attacks and defenses | MIT |
| [TrustAI-laboratory/LMAP](https://github.com/TrustAI-laboratory/LMAP) | Offensive | "nmap for LLMs" — LLM vulnerability scanner and zero-day fuzzer | see repo |
| [Repello-AI/whistleblower](https://github.com/Repello-AI/whistleblower) | Offensive | Infers/leaks an AI agent's system prompt from its text outputs | Apache-2.0 |
| [hupe1980/aisploit](https://github.com/hupe1980/aisploit) | Offensive | Python package to support red teams exploiting LLM-based solutions | MIT |
| [rustyorb/pincer](https://github.com/rustyorb/pincer) | Offensive | AI/LLM red-team suite for automated prompt-injection, jailbreak, data-extraction and guardrail-bypass testing | see repo |
| [kortex-labs/plexiglass](https://github.com/kortex-labs/plexiglass) | Both | Security toolbox for testing and safeguarding LLMs against adversarial attacks | see repo |

## Security education / vulnerable-by-design (AI)

| Repo | Type | What it does | License |
|------|------|--------------|---------|
| [AISecurityConsortium/AIGoat](https://github.com/AISecurityConsortium/AIGoat) | Defensive | Deliberately vulnerable AI playground for LLM red-team training and teaching | Apache-2.0 |
| [microsoft/AI-Red-Teaming-Playground-Labs](https://github.com/microsoft/AI-Red-Teaming-Playground-Labs) | Defensive | Labs + infrastructure to run hands-on AI red-teaming training exercises | MIT |
| [harishsg993010/damn-vulnerable-MCP-server](https://github.com/harishsg993010/damn-vulnerable-MCP-server) | Defensive | Deliberately vulnerable Model Context Protocol server for practising agent/tool-use attacks | MIT |
| [ErdemOzgen/RedAiRange](https://github.com/ErdemOzgen/RedAiRange) | Defensive | AI security range for red teaming, vuln research and hands-on ML-security training | see repo |

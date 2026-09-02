<p align="right"><a href="./README.ko.md">한국어</a></p>

# Taegu Ha

**Vulnerability Researcher · Systems & Product Security**

I investigate real products across AI-agent platforms, native and embedded software, wireless stacks, web products, and operating-system kernels. Recent work includes code-execution paths in PraisonAI and Langflow, memory-safety flaws in libpng and arduino-esp32, a remotely reachable BLE parser failure in Apache NimBLE, and two Linux kernel CVEs with fixes merged upstream. I use automation and LLMs to narrow investigation scope—never as vulnerability proof—and close findings through human validation, controlled reproduction, coordinated disclosure, and patch evidence.

[Public CVE case studies](https://github.com/foxirain/CVE-public) · [Selected vulnerability research](#selected-vulnerability-research) · [Dreamhack](https://dreamhack.io/users/71306) · [Email](mailto:hataegu0826@gmail.com)

```text
attack surface → reachability → broken invariant → controlled reproduction → disclosure → patch
```

## Evidence at a glance

| Evidence | Public record |
| --- | --- |
| **15 CVE case studies · 13 direct public attributions** | Published analyses with retained source provenance and SHA-256 evidence manifests |
| **3 AI-platform / agent cases** | PraisonAI workflow injection · PraisonAI A2A-to-`eval()` RCE · Langflow ToolGuard validation bypass |
| **3 native / embedded / wireless CVEs** | libpng · arduino-esp32 · Apache NimBLE |
| **7 web / authorization / product cases** | LinkAce · NamelessMC · OpenFGA · Caddy · listmonk |
| **2 Linux kernel CVEs · 3 mainline patches** | USB UAC1 · PPP namespace authorization · BPF verifier |
| **154 Dreamhack Pwnable solves** | [4,901 total Wargame points](https://dreamhack.io/users/71306) · long-term systems exploitation practice |

<sub>The case-study and attribution counts describe different scopes and are not additive. The Langflow case is privately documented and does not claim public researcher attribution. Advisory credits appear under foxirain and Amemoyoi.</sub>

## Selected vulnerability research

| Area | Findings and attack surfaces | Evidence |
| --- | --- | --- |
| **AI platforms & agent workflows** | Langflow ToolGuard validation bypass to stored Python execution · PraisonAI public A2A-to-LLM-tool `eval()` RCE · privileged workflow command injection from an untrusted fork branch name | [CVE-2026-9135](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9135) · [CVE-2026-47391](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-47391) · [CVE-2026-48168](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-48168) |
| **Native, embedded & wireless** | libpng ARM/AArch64 NEON OOB read/write · arduino-esp32 NBNS OOB read and stack overflow · Apache NimBLE truncated BLE ATT response assertion | [CVE-2026-33636](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-33636) · [CVE-2026-41429](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429) · [CVE-2026-45815](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-45815) |
| **Web, authorization & product security** | LinkAce SSRF and private-note exposure · NamelessMC hidden-content and OAuth-state flaws · OpenFGA cache-isolation bypass · Caddy path-normalization mismatch · listmonk permission failures | [7 case archives](https://github.com/foxirain/CVE-public) |
| **Linux kernel & upstream** | USB UAC1 stack OOB write · cross-netns PPP capability validation · two CVE fixes and a separate BPF verifier fix authored upstream | [CVE-2026-31720](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-31720) · [CVE-2026-53075](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-53075) · [3 mainline patches](#linux-mainline-contributions) |

**Supporting research tooling:** [Adaptive OSS Vulnerability Harness](https://github.com/foxirain/codex-adaptive-oss-vuln-harness) · [Kernel Codex Harness](https://github.com/foxirain/linux-kernel-codex-harness-v2) · [Agent Security Company](https://github.com/foxirain/agent-security-company)

## Linux mainline contributions

- [`6e0e34d85cd4`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c) — USB UAC1 control-request length validation · CVE-2026-31720
- [`2bb6379416fd`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067) — PPP target-network-namespace capability validation · CVE-2026-53075
- [`de36adca6346`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f) — BPF verifier oversized access-size validation and regression coverage

## Systems exploitation foundation

[**Dreamhack · Amemoyoi**](https://dreamhack.io/users/71306) · [Long-form project record](https://whoami-iota-gilt.vercel.app/3c97c60c09f3810dbf87dc57e6603f3e)

- **154 Pwnable challenges** solved across memory corruption, ROP/SROP, heap exploitation, glibc/FSOP, ARM/AArch64, and Linux kernel exploitation
- **4,901 Wargame points** · reached the overall **Top 300** during the project · 259 analysis, experiment, and troubleshooting records retained
- Progressed from user-space primitives to controlled kernel AAR/AAW and `cred` overwrite in Dreamhack's educational environments

<p align="center">
  <img src="./assets/dreamhack-activity-4x.png" alt="Dreamhack activity: 176 solves across 93 active days from March 2025 to January 2026" width="100%" />
</p>

## Research interests

AI platform and agent security · native and embedded security · wireless protocol and parser security · product and OSS security · operating-system security · reproducible vulnerability validation

## Contact

I am preparing for vulnerability research, product security, AI/agent security, and systems security roles.

**Email:** [hataegu0826@gmail.com](mailto:hataegu0826@gmail.com)

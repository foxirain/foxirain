[Profile](../README.md) · [한국어](./research.ko.md)

# Research notes

**Systems & embedded security research**

I research vulnerabilities in the Linux kernel and ARM software. I analyze source code and binaries, build the environments and tools needed to validate findings, and carry the work through disclosure, patches, and review.

[Public CVE archive](https://github.com/foxirain/CVE-public) · [Research tools](#research-tools) · [Dreamhack](https://dreamhack.io/users/71306) · [Email](mailto:hataegu0826@gmail.com)

## Selected research

| Target | My work | Evidence |
| :--- | :--- | :--- |
| Linux kernel | Authored fixes for USB UAC1 and PPP vulnerabilities, plus a BPF verifier validation fix. **All 3 patches were merged into mainline.** | [UAC1 patch](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c) · [PPP patch](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067) · [BPF patch](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f) |
| libpng | Found and validated ARM/AArch64 NEON memory-boundary errors and wrote a fix, included in **libpng 1.6.56**. | [CVE-2026-33636](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-33636) |
| Embedded protocols | Analyzed and reported memory corruption in the ESP32 NBNS parser and an assertion failure in NimBLE BLE response handling. | [ESP32](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429) · [NimBLE](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-45815) |
| PraisonAI | Found and reported unauthenticated code execution in the A2A example and command injection in a CI workflow. **2 Critical CVEs** were published and fixed upstream. | [A2A](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-47391) · [CI](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-48168) |
| Langflow | Analyzed a dynamic-code validation gap that bypassed an execution restriction, verified it through integrated execution, and submitted a report. | [CVE-2026-9135](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9135) |

My work on LinkAce, NamelessMC, OpenFGA, Caddy, and listmonk covers SSRF, access control, cache isolation, and OAuth validation. [Browse the full archive](https://github.com/foxirain/CVE-public)

<details>
<summary>Case notes and contribution scope</summary>

- Linux kernel: fixed control-request length validation in [USB UAC1 · CVE-2026-31720](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-31720) and capability checks against the target network namespace in [PPP · CVE-2026-53075](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-53075). The separate BPF verifier patch includes a validation fix and regression coverage.
- The public archive contains **15 CVE case studies**: 13 public researcher attributions, 1 consolidated listmonk contribution, and 1 Langflow case with a retained private report. My public reporting identities are **foxirain · Amemoyoi**.
- The two listmonk authorization-bypass variants were consolidated with reports from other researchers into **1 CVE**. I retain the Langflow report; the public advisory does not name me as a researcher.
- The web and authorization work above accounts for 7 CVE cases within the archive.

</details>

## Research tools

| Project | What I designed and built |
| :--- | :--- |
| [RehostRace](https://github.com/foxirain/rehostrace) | A rehosting and replay framework that preserves causal relationships and execution order while validating object lifetimes |
| [VeriRehost](https://github.com/foxirain/verirehost) | A firmware rehosting framework that executes original code slices and records environment models, inputs, and execution results separately |
| [Linux Kernel Harness](https://github.com/foxirain/linux-kernel-codex-harness-v2) | Prioritizes kernel code for investigation and tracks analysis evidence. Different versions were used in the UAC1 and PPP research |
| [OSS Harness](https://github.com/foxirain/codex-oss-vuln-harness-v2) · [Adaptive Harness](https://github.com/foxirain/codex-adaptive-oss-vuln-harness) | Python research harnesses that separate external-signal conditions and search directions. I used them in analysis and reporting that contributed to **11 public CVEs**, including 1 consolidated listmonk contribution |
| [Agent Egress Lock](https://github.com/foxirain/agent-egress-lock) · [Agent Security Company](https://github.com/foxirain/agent-security-company) | Developed a Docker and proxy egress-control prototype, then extended it into an execution environment with Linux user permissions and independent QA review |

The OSS and Adaptive total excludes libpng, Langflow, and the Linux kernel cases.

## Learning and team projects

In the WhiteGang team at WhiteHat School, cohort 2, I developed Windows user-mode and kernel-driver components for DLL loading control and process-handle permission restrictions.  
[PalAnticheat](https://github.com/foxirain/PalAnticheat) · [PalAnticheatEx](https://github.com/foxirain/PalAnticheatEx)

I solved **154 Dreamhack Pwnable challenges**, progressing from user-space memory errors to the Linux kernel. I debugged x86 and ARM environments and checked behavior against glibc and kernel source.

<details>
<summary>Dreamhack study records and activity</summary>

[Dreamhack · Amemoyoi](https://dreamhack.io/users/71306) · [Long-form project record](https://whoami-iota-gilt.vercel.app/3c97c60c09f3810dbf87dc57e6603f3e)

- Topics: memory corruption, ROP/SROP, heap exploitation, glibc/FSOP, ARM/AArch64, and the Linux kernel.
- In educational environments, I progressed from user-space primitives to kernel memory reads and writes and credential-structure analysis.
- During the project: **4,901 Wargame points**, an overall **Top 300** ranking, and **259** retained analysis, experiment, and troubleshooting records.

<img src="../assets/dreamhack-activity-4x.png" alt="Dreamhack Wargame activity from March 2025 to January 2026" width="100%" />

This is a historical snapshot from March 2025 to January 2026: 176 total Wargame solves across 93 active days. The 154 figure refers specifically to Pwnable solves.

</details>

## Contact

I am interested in systems and embedded vulnerability research and research-tool development roles. My work also includes product and AI/agent security.

[hataegu0826@gmail.com](mailto:hataegu0826@gmail.com)

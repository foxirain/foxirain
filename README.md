<p align="right"><a href="./README.ko.md">한국어</a></p>

# Taegu Ha

**Vulnerability Researcher · Systems Security**

I research vulnerabilities in systems software—native code, embedded and wireless stacks, and operating-system kernels. I apply the same reachability-and-invariant approach to AI-agent platforms and web products, carrying findings through controlled reproduction, coordinated disclosure, and patch verification.

[CVE case archive](https://github.com/foxirain/CVE-public) · [Linux upstream evidence](#linux-kernel-and-upstream) · [Dreamhack](https://dreamhack.io/users/71306) · [Email](mailto:hataegu0826@gmail.com)

<p align="center"><strong>15</strong> CVE case studies &nbsp;·&nbsp; <strong>13</strong> public attributions &nbsp;·&nbsp; <strong>3</strong> Linux mainline patches &nbsp;·&nbsp; <strong>154</strong> Pwnable solves</p>
<p align="center"><samp>attack surface → reachability → broken invariant → controlled reproduction → disclosure → patch</samp></p>
<p align="center"><sub>Case-study and attribution counts are separate scopes. Public advisory identities: foxirain · Amemoyoi.</sub></p>

---

## Systems research

Memory safety, parser robustness, privilege boundaries, and upstream remediation are the core of my work.

### Native, embedded and wireless

- **[libpng · CVE-2026-33636](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-33636)** — ARM/AArch64 NEON palette expansion could read and write beyond a short row buffer.
- **[arduino-esp32 · CVE-2026-41429](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429)** — An attacker-controlled NBNS `name_len` caused an out-of-bounds read and stack overflow.
- **[Apache NimBLE · CVE-2026-45815](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-45815)** — A truncated BLE ATT Read Multiple Variable response reached a remotely triggerable host assertion.

### Linux kernel and upstream

I authored two CVE fixes and one separate verifier fix, all merged into Linux mainline.

- **[USB UAC1 · CVE-2026-31720](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-31720)** — Control-request length validation for a 4-byte stack OOB write · [mainline fix](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c)
- **[PPP namespaces · CVE-2026-53075](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-53075)** — Capability validation against the target network namespace · [mainline fix](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067)
- **BPF verifier** — Oversized access-size validation and regression coverage · [mainline fix](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f)

## Product security research

### AI platforms and agent workflows

- **PraisonAI · [CVE-2026-47391](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-47391) · [CVE-2026-48168](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-48168)** — A public A2A request reached an LLM-selected `eval()` tool; an untrusted fork branch name reached a privileged workflow shell.
- **Langflow · [CVE-2026-9135](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9135)** — ToolGuard dynamic `CodeInput` validation bypass to stored Python execution. The private report is retained; no public researcher attribution is claimed.

### Authorization and web products

Seven case studies across **LinkAce, NamelessMC, OpenFGA, Caddy, and listmonk** cover SSRF, private-data exposure, cache isolation, OAuth state, path normalization, and permission boundaries. [Browse the complete archive.](https://github.com/foxirain/CVE-public)

## Systems exploitation foundation

[**Dreamhack · Amemoyoi**](https://dreamhack.io/users/71306) · [Long-form project record](https://whoami-iota-gilt.vercel.app/3c97c60c09f3810dbf87dc57e6603f3e)

- **154 Pwnable challenges** solved across memory corruption, ROP/SROP, heap exploitation, glibc/FSOP, ARM/AArch64, and Linux kernel exploitation
- **4,901 Wargame points** · reached the overall **Top 300** during the project · 259 analysis, experiment, and troubleshooting records retained
- Progressed from user-space primitives to controlled kernel AAR/AAW and `cred` overwrite in Dreamhack's educational environments

<p align="center">
  <img src="./assets/dreamhack-activity-4x.png" alt="Dreamhack activity: 176 total Wargame solves across 93 active days from March 2025 to January 2026" width="100%" />
</p>

<p align="center"><sub>Historical activity snapshot: 176 total Wargame solves across 93 active days, Mar 2025–Jan 2026. The 154 figure above refers to Pwnable solves.</sub></p>

## Research tooling

Supporting repositories for research triage, provenance, and reproducible validation: [Adaptive OSS Vulnerability Harness](https://github.com/foxirain/codex-adaptive-oss-vuln-harness) · [Kernel Codex Harness](https://github.com/foxirain/linux-kernel-codex-harness-v2) · [Agent Security Company](https://github.com/foxirain/agent-security-company)

## Contact

I am interested in vulnerability research and systems security roles, including product and AI/agent security.

**Email:** [hataegu0826@gmail.com](mailto:hataegu0826@gmail.com)

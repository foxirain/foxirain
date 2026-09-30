<h1 align="center">Taegu Ha</h1>

<p align="center">
  <a href="mailto:hataegu0826@gmail.com">Email</a> ·
  <a href="https://github.com/foxirain/CVE-public">CVE archive</a> ·
  <a href="https://dreamhack.io/users/71306">Dreamhack</a> ·
  <a href="./README.ko.md">한국어</a>
</p>

I research vulnerabilities in Linux, embedded systems, and open-source software. I also build tools for firmware rehosting, analysis automation, and reproducible validation.

## Research

**2026**

- **Linux kernel:** Authored three patches merged into mainline, covering USB UAC1 memory corruption, PPP capability checks, and BPF verifier validation. [UAC1](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c) · [PPP](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067) · [BPF](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f)
- **libpng:** Found ARM/AArch64 NEON memory-boundary errors and authored the fix included in libpng 1.6.56. [CVE-2026-33636](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-33636)
- **Embedded protocols:** Reported memory corruption in the ESP32 NBNS parser and a denial of service in NimBLE ATT response handling. [ESP32](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429) · [NimBLE](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-45815)
- **AI frameworks:** Reported code-execution vulnerabilities in PraisonAI and an execution-policy bypass in Langflow. [PraisonAI A2A](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-47391) · [PraisonAI CI](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-48168) · [Langflow](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9135)

[Research notes and contribution scope](./docs/research.en.md) · [All public CVE cases](https://github.com/foxirain/CVE-public)

## Projects

- **[RehostRace](https://github.com/foxirain/rehostrace) · [VeriRehost](https://github.com/foxirain/verirehost):** Rehosting frameworks for replaying asynchronous execution and tracing firmware verification flows.
- **[Linux Kernel Harness](https://github.com/foxirain/linux-kernel-codex-harness-v2) · [Adaptive Harness](https://github.com/foxirain/codex-adaptive-oss-vuln-harness):** Research tools for prioritizing code, coordinating analysis sessions, and recording evidence.
- **[Agent Security Company](https://github.com/foxirain/agent-security-company):** An agent execution environment with file and network controls and independent QA.
- **[PalAnticheatEx](https://github.com/foxirain/PalAnticheatEx):** Windows kernel process protection using object callbacks, developed with the WhiteGang team.

## Experience

- **CASO Lab, Kangwon National University** · Undergraduate Research Intern, May 2024 to Jan 2025. Galaxy Watch5 sensor control, driver analysis, and firmware reverse engineering.
- **WhiteHat School, KITRI** · Cohort 2, Mar to Sep 2024. Developed user-mode and kernel-driver components for the WhiteGang process-protection project.

## Awards

- **2025** · Silver Award, Student Division, Gangwon Cybersecurity Hacking Defense Competition (GCHD).
- **2024** · Council Chair's Award, CO-SHOW AutoHack.
- **2023** · Excellence Award, Chuncheon Public Data Idea Competition.

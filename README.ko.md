<p align="right"><a href="./README.md">English</a></p>

# 하태구 · Taegu Ha

**Vulnerability Researcher · Systems Security**

네이티브 코드, 임베디드·무선 스택, 운영체제 커널을 중심으로 시스템 소프트웨어 취약점을 연구합니다. 동일한 도달 가능성·불변조건 관점을 AI 에이전트 플랫폼과 웹 제품에도 적용하며, 통제된 재현부터 책임 있는 공개와 패치 검증까지 직접 마무리합니다.

[CVE 사례 archive](https://github.com/foxirain/CVE-public) · [Linux upstream 근거](#linux-커널과-upstream) · [Dreamhack](https://dreamhack.io/users/71306) · [이메일](mailto:hataegu0826@gmail.com)

<p align="center"><strong>15</strong> CVE 사례 &nbsp;·&nbsp; <strong>13</strong> 공개 귀속 &nbsp;·&nbsp; <strong>3</strong> Linux mainline 패치 &nbsp;·&nbsp; <strong>154</strong> Pwnable 해결</p>
<p align="center"><samp>공격 표면 → 도달 가능성 → 불변조건 위반 → 통제된 재현 → 공개 → 패치</samp></p>
<p align="center"><sub>사례 수와 공개 귀속 수는 서로 다른 범위입니다. 공개 advisory에는 foxirain과 Amemoyoi 두 이름을 사용합니다.</sub></p>

---

## 시스템 연구

메모리 안전성, 파서 견고성, 권한 경계, upstream 수정이 연구의 중심입니다.

### Linux 커널과 upstream

CVE 수정 2건과 별도 verifier 수정 1건을 직접 작성했고, 모두 Linux mainline에 병합되었습니다.

- **[USB UAC1 · CVE-2026-31720](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-31720)** — 4-byte stack OOB write를 막는 control-request length 검증 · [mainline fix](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c)
- **[PPP namespace · CVE-2026-53075](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-53075)** — target network namespace 기준 capability 검증 · [mainline fix](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067)
- **BPF verifier** — oversized access-size 검증과 regression coverage · [mainline fix](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f)

### 네이티브·임베디드·무선

- **[libpng · CVE-2026-33636](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-33636)** — ARM/AArch64 NEON 팔레트 확장 경로에서 짧은 row buffer 밖을 읽고 쓸 수 있는 결함입니다.
- **[arduino-esp32 · CVE-2026-41429](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429)** — 공격자가 통제하는 NBNS `name_len`으로 OOB read와 stack overflow가 발생합니다.
- **[Apache NimBLE · CVE-2026-45815](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-45815)** — 잘린 BLE ATT Read Multiple Variable 응답이 원격에서 도달 가능한 host assertion으로 이어집니다.

## 제품 보안 연구

### AI 플랫폼·Agent Workflow

- **PraisonAI · [CVE-2026-47391](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-47391) · [CVE-2026-48168](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-48168)** — 공개 A2A 요청이 LLM이 선택한 `eval()` tool까지 이어지는 RCE와, 신뢰하지 않은 fork branch 이름이 privileged workflow shell까지 도달하는 command injection입니다.
- **Langflow · [CVE-2026-9135](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9135)** — ToolGuard dynamic `CodeInput` 검증 우회를 통한 stored Python execution입니다. 개인 보고 증빙을 보존하고 있으며 공식 공개 연구자 귀속은 주장하지 않습니다.

### 인가·웹 제품

**LinkAce, NamelessMC, OpenFGA, Caddy, listmonk**의 SSRF, private data 노출, cache isolation, OAuth state, path normalization, permission boundary를 다룬 7개 사례가 있습니다. [전체 archive 보기.](https://github.com/foxirain/CVE-public)

## 시스템 익스플로잇 기반

[**Dreamhack · Amemoyoi**](https://dreamhack.io/users/71306) · [장기 프로젝트 기록](https://whoami-iota-gilt.vercel.app/3c97c60c09f3810dbf87dc57e6603f3e)

- Memory Corruption, ROP/SROP, Heap, glibc/FSOP, ARM/AArch64, Linux Kernel Exploit에 걸쳐 **Pwnable 154문제**를 해결했습니다.
- **Wargame 4,901점** · 프로젝트 당시 전체 **Top 300** 진입 · 분석·실험·트러블슈팅 기록 259개를 보관합니다.
- Dreamhack 교육 환경에서 user-space primitive부터 Kernel AAR/AAW와 `cred` overwrite까지 단계적으로 확장했습니다.

<p align="center">
  <img src="./assets/dreamhack-activity-4x.png" alt="2025년 3월부터 2026년 1월까지 Dreamhack Wargame 전체 176문제 풀이 활동: 93 active days" width="100%" />
</p>

<p align="center"><sub>과거 활동 스냅샷: 2025년 3월–2026년 1월, Wargame 전체 176문제·93 active days. 상단의 154는 Pwnable 해결 수입니다.</sub></p>

## 연구 도구

연구 triage, provenance, 재현 가능한 검증을 보조하는 repository: [Adaptive OSS Vulnerability Harness](https://github.com/foxirain/codex-adaptive-oss-vuln-harness) · [Kernel Codex Harness](https://github.com/foxirain/linux-kernel-codex-harness-v2) · [Agent Security Company](https://github.com/foxirain/agent-security-company)

## 연락처

Vulnerability Research와 Systems Security를 중심으로 Product Security와 AI / Agent Security 직무를 함께 준비하고 있습니다.

**Email:** [hataegu0826@gmail.com](mailto:hataegu0826@gmail.com)

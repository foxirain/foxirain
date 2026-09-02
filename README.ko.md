<p align="right"><a href="./README.md">English</a></p>

# 하태구 · Taegu Ha

**Vulnerability Researcher · Systems & Product Security**

Linux Kernel, 오픈소스, AI 에이전트 시스템, Windows Kernel, 임베디드 기기처럼 실제 제품과 코드베이스를 직접 분석합니다. 자동화와 LLM은 조사 범위를 좁히는 데 사용하되 취약점의 증거로 취급하지 않으며, 공격자 도달 가능성·통제된 재현·책임 있는 공개·upstream 결과를 사람이 직접 검증합니다.

[공개 CVE 사례](https://github.com/foxirain/CVE-public) · [Linux mainline 기여](#linux-mainline-기여) · [Dreamhack](https://dreamhack.io/users/71306) · [이메일](mailto:hataegu0826@gmail.com)

```text
공격 표면 → 도달 가능성 → 불변조건 위반 → 통제된 재현 → 공개 → 패치
```

## 핵심 증거

| 증거 | 공개 기록 |
| --- | --- |
| **공개 CVE 사례 15건** | source provenance와 SHA-256 evidence manifest를 보존한 공개 분석 자료 |
| **직접 공개 귀속 13건** | 공개 기록에서 직접 확인 가능한 취약점 연구 성과 |
| **Linux Kernel CVE 2건** | [CVE-2026-31720](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-31720) · [CVE-2026-53075](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-53075) |
| **Linux mainline authored patch 3건** | CVE 수정 2건과 별도 BPF verifier 수정 1건 |
| **Dreamhack Pwnable 154문제** | [Wargame 총 4,901점](https://dreamhack.io/users/71306) · 장기 시스템 익스플로잇 학습 |

<sub>공개 사례 수와 직접 귀속 수는 집계 범위가 다르며 서로 더하는 수치가 아닙니다.</sub>

## 대표 연구

| 연구 | 증명하는 역량 | 공개 증거 |
| --- | --- | --- |
| [**CVE-public**](https://github.com/foxirain/CVE-public) | 메모리 안전성, 인가, SSRF, OAuth, 에이전트 보안, CI/CD에 걸친 provenance 중심 취약점 문서화 | 15개 사례 · source provenance · 사례별 evidence hash |
| [**Kernel Codex Harness 계열**](https://github.com/foxirain/linux-kernel-codex-harness-v2) | Linux Kernel 검토를 위한 evidence-driven attention allocation과 provenance-aware triage | [v1-assisted CVE-2026-31720](https://github.com/foxirain/linux-kernel-codex-harness) · [v2-assisted CVE-2026-53075](https://github.com/foxirain/linux-kernel-codex-harness-v2) |
| [**Adaptive OSS Vulnerability Harness**](https://github.com/foxirain/codex-adaptive-oss-vuln-harness) | 서로 분리된 탐색 가설을 여러 언어와 제품군에 공통된 evidence contract로 수렴 | 공개 연구 lineage · 명시적인 provenance와 validity 한계 |
| [**Agent Security Company**](https://github.com/foxirain/agent-security-company) | AI-assisted 연구의 격리·identity·권한·network·QA·공개 경계 | evidence ledger · publication-safety policy · 공개 regression 140/140 |

## Linux mainline 기여

- [`6e0e34d85cd4`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c) — USB UAC1 control-request length validation · CVE-2026-31720
- [`2bb6379416fd`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067) — PPP target-network-namespace capability validation · CVE-2026-53075
- [`de36adca6346`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f) — BPF verifier oversized access-size validation 및 regression test

## 시스템 익스플로잇 기반

[**Dreamhack · Amemoyoi**](https://dreamhack.io/users/71306) · [인터랙티브 풀이 활동 · 93일](https://whoami-iota-gilt.vercel.app/api/notion-asset?block=2ecf12c7-fa1c-4263-a1b7-c766e623746c&src=attachment%3A4d200bcc-e894-4efd-b049-26bf752fbb4b%3Adreamhack-all-solves-activity.html) · [장기 프로젝트 기록](https://whoami-iota-gilt.vercel.app/3c97c60c09f3810dbf87dc57e6603f3e)

- Memory Corruption, ROP/SROP, Heap, glibc/FSOP, ARM/AArch64, Linux Kernel Exploit에 걸쳐 **Pwnable 154문제** 해결
- **Wargame 4,901점** · 프로젝트 당시 전체 **Top 300** 진입 · 분석·실험·트러블슈팅 기록 259개 보관
- Dreamhack 교육 환경에서 user-space primitive부터 Kernel AAR/AAW와 `cred` overwrite까지 단계적으로 확장

## 관심 연구 분야

Linux Kernel Security · Vulnerability Research · Product / OSS Security · Embedded / Device Security · Windows Kernel Security · Reproducible Security Validation

## 연락처

Vulnerability Research, Product Security, Systems Security 직무를 준비하고 있습니다.

**Email:** [hataegu0826@gmail.com](mailto:hataegu0826@gmail.com)

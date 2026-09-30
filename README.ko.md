<h1 align="center">하태구</h1>

<p align="center">
  <a href="mailto:hataegu0826@gmail.com">Email</a> ·
  <a href="https://github.com/foxirain/CVE-public">CVE 기록</a> ·
  <a href="https://dreamhack.io/users/71306">Dreamhack</a> ·
  <a href="./README.md">English</a>
</p>

Linux 커널과 임베디드 시스템, 오픈소스 소프트웨어의 취약점을 연구합니다. 펌웨어 리호스팅과 분석 자동화, 재현·검증에 필요한 도구도 직접 만듭니다.

## 연구

**2026**

- **Linux 커널:** USB UAC1 메모리 손상, PPP 권한 검사, BPF verifier 검증 오류를 수정했습니다. 직접 작성한 패치 3건이 mainline에 반영됐습니다. [UAC1](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c) · [PPP](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067) · [BPF](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f)
- **libpng:** ARM/AArch64 NEON의 메모리 경계 오류를 발견하고 수정 패치를 작성했습니다. libpng 1.6.56에 반영됐습니다. [CVE-2026-33636](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-33636)
- **임베디드 프로토콜:** ESP32 NBNS 파서의 메모리 손상과 NimBLE ATT 응답 처리의 서비스 거부 취약점을 제보했습니다. [ESP32](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429) · [NimBLE](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-45815)
- **AI 프레임워크:** PraisonAI의 코드 실행 취약점과 Langflow의 실행 제한 정책 우회를 분석·제보했습니다. [PraisonAI A2A](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-47391) · [PraisonAI CI](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-48168) · [Langflow](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9135)

[연구 상세와 기여 범위](./docs/research.ko.md) · [전체 공개 CVE 사례](https://github.com/foxirain/CVE-public)

## 프로젝트

- **[RehostRace](https://github.com/foxirain/rehostrace) · [VeriRehost](https://github.com/foxirain/verirehost):** 비동기 실행을 재생하고 펌웨어 검증 흐름을 추적하는 리호스팅 프레임워크.
- **[Linux Kernel Harness](https://github.com/foxirain/linux-kernel-codex-harness-v2) · [Adaptive Harness](https://github.com/foxirain/codex-adaptive-oss-vuln-harness):** 조사 우선순위를 정하고 분석 세션과 근거를 관리하는 연구 도구.
- **[Agent Security Company](https://github.com/foxirain/agent-security-company):** 파일·통신 접근 통제와 독립된 QA 검토를 갖춘 에이전트 실행 환경.
- **[PalAnticheatEx](https://github.com/foxirain/PalAnticheatEx):** WhiteGang 팀에서 개발한 Windows 커널 기반 프로세스 보호 도구. 객체 콜백으로 핸들 권한 통제.

## 경험

- **강원대학교 CASO Lab** · 학부 연구 인턴, 2024.05 ~ 2025.01. Galaxy Watch5 센서 제어, 드라이버 분석과 펌웨어 역분석 연구.
- **한국정보기술연구원(KITRI) 화이트햇 스쿨** · 2기, 2024.03 ~ 2024.09. WhiteGang 프로세스 보호 프로젝트의 사용자 모드·커널 드라이버 개발 담당.

## 수상

- **2025** · 강원지역 사이버보안 해킹방어대회(GCHD) 학생부 은상.
- **2024** · CO-SHOW AutoHack 협의회장상.
- **2023** · 춘천시 공공데이터 활용 아이디어 공모전 우수상.

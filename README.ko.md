<h1 align="center">하태구</h1>

<p align="center">
  시스템·임베디드 보안 연구
</p>

<p align="center">
  <a href="mailto:hataegu0826@gmail.com">Email</a> ·
  <a href="https://github.com/foxirain/CVE-public">CVE 기록</a> ·
  <a href="https://dreamhack.io/users/71306">Dreamhack</a> ·
  <a href="./README.md">English</a>
</p>

## Experience

- **강원대학교 CASO Lab** · 학부 연구 인턴  
  2024.05 – 2025.01
- **한국정보기술연구원(KITRI) 화이트햇 스쿨** · 2기 수료  
  2024.03 – 2024.09

## Highlights

**2026**

- USB UAC1, PPP, BPF verifier의 오류를 수정한 **패치 3건을 직접 작성해 Linux mainline에 반영**. [UAC1](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c) · [PPP](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067) · [BPF](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f)
- **libpng** ARM/AArch64 NEON의 메모리 오류 발견·수정. 직접 작성한 패치가 **1.6.56**에 반영. [CVE-2026-33636](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-33636)
- AI 제품(PraisonAI·Langflow)의 **Critical 취약점 3건** 분석·제보. [PraisonAI A2A](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-47391) · [PraisonAI CI](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-48168) · [Langflow](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9135)
- **ESP32·Apache NimBLE**의 임베디드 프로토콜 취약점 제보. [CVE-2026-41429](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429)·[CVE-2026-45815](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-45815) 공개.
- **GW TakeDown** · Galaxy Watch 펌웨어 보안 연구. **Samsung Mobile Security 제보 1건 보상 지급 결정**.  
  펌웨어 리호스팅·실행 재생·검증 흐름 분석을 위한 [RehostRace](https://github.com/foxirain/rehostrace)·[VeriRehost](https://github.com/foxirain/verirehost) 직접 설계·개발.
- 연구 자동화와 에이전트 실행 격리를 위한 [Adaptive Harness](https://github.com/foxirain/codex-adaptive-oss-vuln-harness)·[Agent Security Company](https://github.com/foxirain/agent-security-company) 개발.

[연구 상세와 기여 범위](./docs/research.ko.md)

**2025**

- **은상**, 강원지역 사이버보안 해킹방어대회(GCHD) 학생부.
- [Dreamhack](https://dreamhack.io/users/71306) **Pwnable 154문제** 풀이·**전체 Wargame 200위권** 달성.

**2024**

- **GW5** · Galaxy Watch5 센서 드라이버·SensorHub 펌웨어 역분석. AVB 해시 검증 도구와 펌웨어 실험용 유선 연결·충전 장비 제작.
- **WhiteGang** · Windows 프로세스 보호를 위한 사용자 모드·커널 드라이버 개발. DLL 로딩 통제와 핸들 접근 권한 제한 구현. [PalAnticheat](https://github.com/foxirain/PalAnticheat) · [PalAnticheatEx](https://github.com/foxirain/PalAnticheatEx)
- **협의회장상**, CO-SHOW AutoHack.

**2023**

- **우수상**, 춘천시 공공데이터 활용 아이디어 공모전.

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
  컴퓨터 구조·인공지능·보안·운영체제 연구실  
  2024.05 – 2025.01
- **한국정보기술연구원(KITRI) 화이트햇 스쿨** · 2기 수료  
  2024.03 – 2024.09

## Highlights

**2026**

- USB UAC1, PPP, BPF verifier의 오류를 수정한 **패치 3건을 직접 작성해 Linux mainline에 반영**. [UAC1](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=6e0e34d85cd46ceb37d16054e97a373a32770f6c) · [PPP](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=2bb6379416fd19f44c3423a00bfd8626259f6067) · [BPF](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=de36adca634634c205a9eb8b56a28175ab7abf5f)  
  USB UAC1 후속 연구에서 **CVE-2026-31720**과 CVE-2026-31513을 결합한 익스플로잇을 개발. x86-64 QEMU/KVM 환경에서 **SSP·KASLR을 우회하고 root 권한 명령 실행**을 입증. [익스플로잇 보고서](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-31720/exploit)
- **libpng**에서 **CVE-2026-33636** 취약점 발견. Google의 Android 보안 공지에서 **Critical**로 분류. 공동 작성한 보안 패치가 **libpng 1.6.56**과 **Google AOSP·Ubuntu·Firefox**에 반영됐으며, **Oracle JDK·Samsung Galaxy** 업데이트에도 포함. libpng 공식 **AUTHORS**에 기여자로 등재. [CVE-2026-33636](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-33636) · [libpng](https://github.com/pnggroup/libpng/commit/aba9f18eba870d14fb52c5ba5d73451349e339c3) · [Android bulletin](https://source.android.com/docs/security/bulletin/2026/2026-09-01) · [AOSP](https://android.googlesource.com/platform/external/libpng/+/7d98050ef8d9d17d495eb178b8217548437cedf1) · [Firefox](https://github.com/mozilla-firefox/firefox/blob/53cc4f2877a561606f99d20aafc56e35a395f1e2/media/libpng/CHANGES#L6345-L6347) · [Oracle JDK](https://www.oracle.com/security-alerts/cpujul2026.html#AppendixJAVA) · [Samsung](https://security.samsungmobile.com/securityUpdate.smsb) · [Ubuntu](https://ubuntu.com/security/CVE-2026-33636) · [AUTHORS](https://github.com/pnggroup/libpng/blob/libpng16/AUTHORS)
- AI 제품(PraisonAI·Langflow)의 **Critical 3건을 포함한 취약점 4건** 분석·제보. [PraisonAI A2A](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-47391) · [PraisonAI CI](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-48168) · [Langflow Policies](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9135) · [Langflow Agentic Assistant](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-9196)
- **ESP32 NBNS·Apache NimBLE ATT**의 임베디드 프로토콜 취약점 제보. [CVE-2026-41429](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429)·[CVE-2026-45815](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-45815) 공개.  
  ESP32 후속 연구에서 **실제 ESP32-S3에서 네트워크 입력만 사용하는 익스플로잇 체인**을 개발. CVE-2026-41429와 CVE-2024-30166을 결합해 스택 보호를 우회하고 **FreeRTOS 태스크 실행과 1,440바이트 펌웨어 메모리 유출**을 입증. [실기기 익스플로잇](https://github.com/foxirain/CVE-public/tree/main/cases/CVE-2026-41429/exploit)
- **GW TakeDown** · Galaxy Watch 펌웨어 보안 연구. **Samsung Mobile Security 제보 1건 보상 지급 결정**.  
  펌웨어 리호스팅·실행 재생·검증 흐름 분석을 위한 [RehostRace](https://github.com/foxirain/rehostrace)·[VeriRehost](https://github.com/foxirain/verirehost) 직접 설계·개발.
- **DenchiSoft**에 보안 취약점을 제보해 버그바운티 프로그램 **최대 보상금** 수령 (**$1,000**).
- 코드·Git 변경 이력·외부 신호를 점수화해 조사할 파일의 우선순위를 정하고, 서로 다른 탐색 전략을 적용한 여러 세션에서 검토 결과·소요 비용에 따라 남은 조사 예산을 재배분하는 [Adaptive Harness](https://github.com/foxirain/codex-adaptive-oss-vuln-harness) 개발. Linux 사용자와 샌드박스 정책으로 에이전트별 파일·네트워크 접근 권한을 제한하고, 별도 QA 에이전트가 연구 결과를 검증하도록 [Agent Security Company](https://github.com/foxirain/agent-security-company) 개발.

**2025**

- **외주 개발** · 심리학과 연구실의 의뢰로 **112채널 LED 제어 시스템** 설계·제작·납품. 하드웨어, Raspberry Pi 5 제어 소프트웨어, 19페이지 운영 매뉴얼 제공.
- **은상**, 강원지역 사이버보안 해킹방어대회(GCHD) 학생부.
- [Dreamhack](https://dreamhack.io/users/71306) **Pwnable 154문제** 풀이·**전체 Wargame 200위권** 달성.

**2024**

- **GW5** · Galaxy Watch5 센서 드라이버·SensorHub 펌웨어 역분석. AVB 해시 검증 도구와 펌웨어 실험용 유선 연결·충전 장비 제작.
- **WhiteGang** · Windows 프로세스 보호를 위한 사용자 모드·커널 드라이버 개발. DLL 로딩 통제와 핸들 접근 권한 제한 구현. [PalAnticheat](https://github.com/foxirain/PalAnticheat) · [PalAnticheatEx](https://github.com/foxirain/PalAnticheatEx)
- **협의회장상**, CO-SHOW AutoHack.

**2023**

- **우수상**, 춘천시 공공데이터 활용 아이디어 공모전.

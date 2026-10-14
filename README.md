# lUbY

**AI & workflow automation · homelab / DevOps automation**

AI 에이전트와 스크립트로 반복 업무와 인프라 운영을 자동화합니다.
실제로 운영 중인 시스템(홈랩 서버, 웹사이트, 커뮤니티 봇)을 대상으로,
**"자동화하되 사람이 통제할 수 있게"** 설계하는 데 집중합니다.

- 🌐 Website: [itlubs.com](https://itlubs.com)
- 🧭 Focus: AI agent operations, workflow automation, CI/CD & self-healing infra

---

## Featured projects

### 🩺 [self-healing-homelab-monitor](https://github.com/lubydubybubu/self-healing-homelab-monitor)
5분 주기 무(無)LLM 모니터가 서버·VM·PC 상태를 점검하고, **상태가 바뀐 경우에만** AI 에이전트를 깨워
런북 범위 안에서 자동 복구한 뒤 원인/조치/결과를 보고합니다.
평소 LLM 호출 0회, 재부팅·설정 변경 등은 사람 승인 후에만.
`Python` `Proxmox` `SSH` `LLM agent` `Docker` `GitHub Actions`

### 📦 [verified-git-upload-queue](https://github.com/lubydubybubu/verified-git-upload-queue)
"작업 완료"를 명시적으로 표시하면 허용 목록 파일을 동결·해시하고, 시크릿 스캔 후
모델 호출 없이 커밋·푸시·**원격 SHA 검증**까지 하는 업로드 큐. 모호한 실패는 재시도하지 않고 차단 상태로 남깁니다.
`Python` `Git` `gitleaks` `GitHub Actions`

### ⚙️ [n8n-automation-workflows](https://github.com/lubydubybubu/n8n-automation-workflows)
Docker로 운영하는 n8n(LAN 전용)의 실사용 워크플로 3개: 사이트 가동·지연 감시(상태 변화 시에만 알림),
GitHub CI 일일 요약, 게이밍 기어 RSS 주간 요약. 워크플로 JSON 검증·시크릿 스캔 CI 포함.
`n8n` `Docker Compose` `GitHub Actions`

### 🤖 [AI agent operations with approval guardrails](https://github.com/lubydubybubu/portfolio-case-studies/blob/main/agent-ops-guardrails.ko.md) · [EN](https://github.com/lubydubybubu/portfolio-case-studies/blob/main/agent-ops-guardrails.en.md)
LLM 에이전트(Hermes)에 웹사이트·봇·배포 도구를 연결하되, 모든 쓰기 작업에 건별 승인·해시 확인·자동 백업을 적용한
운영 환경. 기존 에이전트에서 단계적 무중단 이관.

### 📈 [Gear trend report pipeline](https://github.com/lubydubybubu/portfolio-case-studies/blob/main/gear-trend-pipeline.ko.md) · [EN](https://github.com/lubydubybubu/portfolio-case-studies/blob/main/gear-trend-pipeline.en.md)
Google Trends · 네이버 · YouTube 데이터를 수집·점수화해 대시보드와 Discord 일일 리포트로 제공.
규칙 기반 추출이 수렴하지 않자 **카탈로그 우선 + 실데이터 골드셋 검증**으로 재설계한 과정 포함.

---

### 🖱️ [itlubs-xlat-benchmark](https://github.com/lubydubybubu/itlubs-xlat-benchmark)
itlubs.com 기어 리뷰에 쓰는 클릭 응답속도 측정 도구. 브라우저(Web Serial) ↔ XLAT 측정기, Windows 브리지(.NET) ↔ TAB Rabbit,
웹 트리거용 XLAT 펌웨어 패치(GPL-3.0). CI에서 펌웨어·브리지 빌드 검증.
`JavaScript` `C#/.NET` `C (STM32, FreeRTOS)` `GitHub Actions`

---

## Other work

- **Korean localization for ArtCraft apps** — [artcraft-ko-toolkit](https://github.com/lubydubybubu/artcraft-ko-toolkit)
  (Linux→Windows 크로스 빌드, 패치 추출·적용 검증 자동화) 외 패치 저장소 8개
- **Discord bots** — [GearX](https://github.com/lubydubybubu/GearX), [nikke_bot](https://github.com/lubydubybubu/nikke_bot) (RSS/Twitter 모니터링), [LUBOT](https://github.com/lubydubybubu/LUBOT)
- **TuneLink** — [TuneLink](https://github.com/lubydubybubu/TuneLink)

## How I work

- 요구사항·안전 정책·아키텍처는 직접 설계하고, 구현은 AI 코딩 에이전트(Claude 등)로 하며
  **다른 모델/테스트로 독립 검증한 뒤에만** 배포합니다.
- 자동화의 기본값은 *되돌릴 수 있는 조치만 자동, 나머지는 승인*.
- 모든 사례에는 실패와 재설계 기록을 남깁니다.

## Stack

`Python` `Node.js` `Linux` `Proxmox` `systemd` `Git/GitHub Actions` `Docker` `Discord API` `LLM agents (Claude, Hermes)`

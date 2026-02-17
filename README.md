# Olympus Command Board

AI 에이전트 협업 시스템을 RPG 올림푸스 스타일로 시각화한 인터랙티브 게임보드.

## Features

| Feature | Description |
|---------|-------------|
| **RPG Game Board Layout** | 올림푸스 신전을 중심으로 8신이 계층적으로 배치된 공간적 레이아웃 |
| **Character Portraits** | 각 에이전트별 고유 PNG 포트레이트와 컬러 테마 |
| **Workflow Simulation** | Boss → Zeus → 병렬 분배 → 순환 파티클 애니메이션 |
| **Click Modal** | 캐릭터 클릭 시 역할, 페르소나, 스탯, 행동규칙, AI 매핑 상세 표시 |
| **SVG Connections** | 신전 ↔ 각 캐릭터 간 애니메이션 연결선 |
| **Stat Bars** | 캐릭터별 3개 능력치 바 (고유 컬러 그라디언트) |
| **Status Indicators** | IDLE/ACTIVE 상태 토글 (녹색/황색 펄스) |
| **Ticket System** | QUEUED/RUNNING/DONE/DELAYED/BLOCKED 상태의 작업 티켓 패널 |
| **Gold Particles** | 부유하는 골든 파티클 배경 효과 |
| **Responsive** | Desktop(3열) → Tablet(2열) → Mobile(1열) 반응형 |

## Agents

```
                    [BOSS]
                      │
                   [ZEUS]          ← Conductor
                  ╱       ╲
           [ATHENA]    [PROMETHEUS] ← Strategy / Planning
           ╱    ╲           ╱    ╲
      [HERMES]  [TEMPLE]  [APOLLO] ← Scout / Design
           ╲       │       ╱
     [HEPHAESTUS]     [SISYPHUS]   ← Forge / Ops
                  ╲   ╱
                 [HADES]           ← Review
```

| God | Role | AI Agent Mapping |
|-----|------|------------------|
| **Zeus** | 총괄 오케스트레이터 | Main Orchestrator — 요청 수신/분해/위임/종합 |
| **Athena** | 전략 분석 · 아키텍처 자문 | Oracle — 읽기 전용 고품질 추론 컨설턴트 |
| **Prometheus** | 계획 수립 · 작업 분해 | Planner — 전략적 작업 분해, Task Graph 생성 |
| **Hermes** | 정보 수집 · 코드베이스 탐색 | Explorer — 컨텍스트 검색 전문 전령 |
| **Apollo** | UI/UX 디자인 · 프론트엔드 | Designer — Visual Engineering 전문 |
| **Hephaestus** | 코드 구현 · 자동화 | Executor — 대장장이 빌더 |
| **Sisyphus** | 운영 점검 · 반복 실행 | Persistent Worker — 완료까지 멈추지 않음 |
| **Hades** | 코드 리뷰 · 품질 검증 | Critic — 냉엄한 품질 게이트 |

## Quick Start

```bash
# 별도 설치 불필요. 브라우저에서 바로 실행.
open index.html

# 또는 로컬 서버
npx serve .
```

## Tech

- **Zero Dependencies** — 외부 CDN/라이브러리 없음
- **Single File** — `index.html` 하나에 HTML + CSS + JS 전부 포함
- **Pure CSS Animations** — transform/opacity 기반 GPU 가속
- **SVG Connections** — 동적 연결선 + 리사이즈 대응
- **Vanilla JS** — 프레임워크 없이 순수 JavaScript

## Structure

```
olympus-board/
├── index.html                  # 메인 게임보드 (v3)
├── index.html.bak2             # 이전 버전 백업 (v2)
├── assets/
│   └── characters/
│       ├── zeus.png
│       ├── athena.png
│       ├── prometheus.png
│       ├── hermes.png
│       ├── apollo.png
│       ├── hephaestus.png
│       ├── sisyphus.png
│       ├── hades.png
│       └── olympus-temple.png
└── README.md
```

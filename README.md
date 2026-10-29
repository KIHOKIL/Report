# 📚 Multi-Topic Research & Engineering Report Hub

개인 연구, 엔지니어링 분석, 조직문화 진단 및 기술 벤치마크 리포트를 모아 관리하는 중앙 포털 허브입니다.  
모든 리포트는 독립적인 서브 디렉터리로 관리되며, 웹 브라우저를 통해 인터랙티브 대시보드와 전문 보고서를 바로 열람할 수 있습니다.

🌐 **웹 포털 바로가기 (GitHub Pages)**: [https://kihokil.github.io/Report/](https://kihokil.github.io/Report/)

---

## 🗂️ 리포트 카탈로그 (Report Index)

| 일자 | 분야 | 주제 | 바로가기 | 상태 |
|:---:|:---:|---|:---:|:---:|
| **2026-10** | **조직문화** | **PHY SW Group 1on1 조직문화 진단 및 리커버리 (v2.0)**<br>· 21명 전원 173건 피드백 전수 분석<br>· 12대 확장 카테고리 심각도 히트맵 & 심리적 안전감 진단<br>· Stop-List 10선, 15대 실행 대책, 글로벌 빅테크 벤치마크 7선 | [📊 대시보드 열기](https://kihokil.github.io/Report/culture/2026-10-phy-sw-1on1/dashboard/)<br>[📄 보고서 폴더](culture/2026-10-phy-sw-1on1/docs/) | `Done (v2.0)` |
| *Upcoming* | **AI/ML** | **Semantic CodeGraph Indexer 연구**<br>· 대규모 C/C++ 코드베이스 의미론적 그래프 인덱싱 | [📁 폴더 준비중](tech-research/) | `Planning` |
| *Upcoming* | **금융/경제** | **채권 래더링(Bond Laddering) 전략 분석**<br>· 금리 변동기 만기 분산 포트폴리오 시뮬레이션 | [📁 폴더 준비중](finance/) | `Planning` |

---

## 🏗️ 디렉터리 아키텍처

```text
Report/
├── .gitignore                     # 민감정보 원본(*.xlsx) 차단 규칙
├── README.md                      # 전체 리포트 색인 및 설명 (본 문서)
├── index.html                     # [GitHub Pages] 전체 리포트 포털 웹 랜딩 페이지
│
├── culture/                       # [분야 1] 조직문화 / 인사 진단
│   └── 2026-10-phy-sw-1on1/       # PHY SW Group 1on1 진단 리포트 (v2.0)
│       ├── README.md              # 프로젝트 요약 및 가이드
│       ├── dashboard/             # 인터랙티브 대시보드 (index.html, JSON)
│       ├── docs/                  # 01~05 진단·병목·대책·빅테크 마크다운 보고서
│       └── archive/               # 과거 v1.0 동결 보존 스냅샷
│
├── tech-research/                 # [분야 2] AI / 소프트웨어 공학 기술 분석
│
└── finance/                       # [분야 3] 경제 / 금융 / 투자 전략 리포트
```

---

## 🚀 신규 리포트 추가 가이드 (How to add a new report)

1. 해당 분야 카테고리 폴더(`culture/`, `tech-research/`, `finance/`) 아래에 새 프로젝트 폴더를 만듭니다. (예: `tech-research/2026-codegraph/`)
2. 분석 마크다운 보고서(`docs/`) 및 인터랙티브 웹 대시보드(`dashboard/`)를 구성합니다.
3. 루트 `index.html`과 `README.md`의 리포트 인덱스 테이블에 새 리포트 카드/링크를 추가합니다.
4. Git 커밋 및 푸시하면 GitHub Pages에 즉시 자동 반영됩니다!

# PHY SW Group 조직문화 개선 AX 에이전트 팀 — 사용 안내서

> 삼성전자 DS 보직장 교육 해커톤 산출물. 그룹장이 진행한 1on1 피드백을 멀티에이전트가 진단·분석하고, 실시간 입력이 가능한 인터랙티브 대시보드로 보여줍니다.

## 1. 무엇을 하는 팀인가

| 단계 | 에이전트 | 하는 일 | 결과 파일 |
|---|---|---|---|
| 1 | Culture Diagnostician | 직급별 감정 히트맵, 근본 원인, 심리적 안전감 진단 | `docs/01_진단_결과.md` |
| 2 | Workflow Optimizer | GitHub/회의/과제 병목 분석, Stop-List | `docs/02_병목_StopList.md` |
| 3 | Leadership Action Designer | 단·중·장기 대책, 간담회 스크립트, 로드맵 | `docs/03_단중장기_대책.md` |
| 1′ | Bigtech Benchmark Researcher | 빅테크 유사 사례·우수 극복 사례 조사 | `docs/04_빅테크_사례.md` |
| 4 | Dashboard Builder | 단일 HTML 대시보드 제작 | `dashboard/index.html` |
| 5 | Hackathon Judge | 제출 전 셀프 심사 | `docs/05_심사_결과.md` |

에이전트 정의는 `.claude/agents/*.md`, 호출 규칙은 `CLAUDE.md`에 있습니다.

## 2. 폴더 구조

```
261015_PHY_SW_그룹장/
├── CLAUDE.md                 # Head(오케스트레이터): 라우팅 규칙·페르소나·안전장치
├── README.md                 # 이 문서
├── .claude/agents/           # Sub-Agent 6개
├── docs/                     # 에이전트 산출 문서 01~05
├── dashboard/
│   ├── index.html            # 인터랙티브 대시보드 (더블클릭으로 실행)
│   └── sample_1on1.json      # 가져오기 테스트용 익명 샘플
└── 제출_결과.txt              # Scorebot 채점 결과 + 플랫폼 제출용 설명
```

## 3. 대시보드 사용법

1. `dashboard/index.html`을 더블클릭합니다. 인터넷·설치 불필요, 외부 라이브러리 없음.
2. 상단 탭:
   - **현황 진단**: KPI 카드, 직급 × 고충 카테고리 히트맵, 카테고리별 막대, 긍정/부정 비율
   - **1on1 실시간 입력**: 날짜·직급·카테고리·감정도·요약을 입력하면 모든 차트가 즉시 갱신됩니다
   - **빅테크 사례**: 유사 고충을 겪은 글로벌 기업 사례와 우리 그룹 매핑
   - **단·중·장기 대책**: 타임라인과 고충별 대책 표
   - **우수 극복 사례**: 문제→조치→결과→시사점 스토리
3. 입력 데이터는 브라우저 `localStorage`에만 저장됩니다. 다른 PC로 옮기려면 **JSON 내보내기** → **가져오기**를 사용하세요.
4. 초기화하려면 입력 탭의 "초기 데이터로 되돌리기"를 누릅니다.

## 4. 에이전트 팀 사용법 (Claude Code)

이 폴더에서 Claude Code를 열고 아래처럼 요청합니다.

```
처음부터 끝까지 해커톤 산출물을 만들어줘        → 전체 파이프라인 실행
새 1on1 3건을 추가했어. 진단을 다시 해줘         → culture-diagnostician
회의 Stop-List를 뽑아줘                         → workflow-optimizer
CA 간담회 오프닝 스크립트를 써줘                → leadership-action-designer
GitHub 전환 고충을 겪은 다른 회사 사례를 찾아줘  → bigtech-benchmark-researcher
대시보드를 다시 만들어줘                        → dashboard-builder
제출 전에 심사해줘                              → hackathon-judge
```

## 5. 제출 절차

1. 이 폴더를 zip으로 압축합니다. **주의**: Windows PowerShell의 `Compress-Archive`는 경로 구분자를 `\`로 써서 채점기가 Sub-Agent를 인식하지 못합니다. 아래 명령을 사용하세요.
   ```
   cd %USERPROFILE%\Desktop
   tar.exe -a -cf 261015_PHY_SW_그룹장.zip 261015_PHY_SW_그룹장
   ```
2. Scorebot(https://samsungscorebot2.netlify.app/)에 zip을 올리고 PASS를 확인한 뒤 "제출 결과 복사하기"를 누릅니다.
3. 콘테스트 플랫폼(https://contest-platform-production.up.railway.app/samsungds-ai)에 Knox 이메일로 가입·로그인 → 제출하기 → 산출물 설명에 복사한 채점 결과를 붙여넣습니다. 붙여넣을 설명문은 `제출_결과.txt`에 준비되어 있습니다.

## 6. 데이터 취급 주의

- 1on1 원문과 원본 파일(csv/xlsx)은 이 폴더와 zip에 포함하지 않습니다. 대시보드에는 익명화·요약된 문장만 있습니다.
- 입력 폼에 실명·사번이 들어가면 경고가 표시됩니다. 개인이 식별되는 표현은 쓰지 마세요.

# 에이전트 하네스 레퍼런스 맵

공개 도구들의 하네스 구조를 우리 회사 방식으로 바꾸기 위한 대응표입니다.

## 레퍼런스별 배울 점

| 레퍼런스 | 배울 점 | 우리 문서 위치 |
| --- | --- | --- |
| AGENTS.md | 에이전트가 먼저 읽는 예측 가능한 입구 파일 | `README.md`, `00_폴더별_문서_정리.md` |
| Cursor Rules | 적용 범위를 나눠 규칙을 파일화 | 부서별 폴더 README |
| Cline Memory Bank | 세션 간 맥락 유지 | `공통/06_메모리뱅크_운영방식.md` |
| Claude Code Subagents | 역할별 에이전트 분리 | `개발/05_실전_개발_하네스_고급.md` |
| Claude Code Hooks | 자동 검증과 차단 게이트 | `공통/07_자동_검증_게이트_하네스.md` |
| Aider CONVENTIONS.md | 읽기 전용 규칙 파일 | `개발/02_카파시_코딩_가이드라인.md` |
| Copilot Instructions | 저장소 지침과 작업별 prompt 파일 분리 | `templates/advanced-task-brief.md` |
| Windsurf Rules/Workflows/Skills | durable knowledge를 규칙 파일로 관리 | `공통/05_고급_하네스_설계원칙.md` |

## 우리 회사 추천 운영 구조

```text
agent-harnessing-guidelines/
├── README.md
├── 00_폴더별_문서_정리.md
├── 01_좋은_하네스_레퍼런스_분석.md
├── 공통/
│   ├── 05_고급_하네스_설계원칙.md
│   ├── 06_메모리뱅크_운영방식.md
│   └── 07_자동_검증_게이트_하네스.md
├── 개발/
│   └── 05_실전_개발_하네스_고급.md
├── 기획/
│   └── 05_리서치_의사결정_하네스.md
├── 디자인/
│   └── 05_캡처_QA_하네스.md
├── 하드웨어_FW_회로/
├── 경영지원/
├── 재활도메인/
└── templates/
    ├── advanced-task-brief.md
    └── handoff-note.md
```

## 적용 우선순위

1. 전 직원 공통: `templates/advanced-task-brief.md`
2. 개발팀: `개발/05_실전_개발_하네스_고급.md`
3. 기획/PM: `기획/05_리서치_의사결정_하네스.md`
4. 디자인/PPT: `디자인/05_캡처_QA_하네스.md`
5. 전체 운영: `공통/06_메모리뱅크_운영방식.md`
6. 검증 강화: `공통/07_자동_검증_게이트_하네스.md`

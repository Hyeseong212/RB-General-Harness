# PPTX QA 리포트

- 작성일: 2026-05-12
- 대상: `이승로봇_게임재활_콘텐츠기획_20260512.pptx`
- 작업 단계: second acting output
- 목적: 신규 "이승로봇 게임재활 콘텐츠 기획 PPT" 생성 및 렌더링 확인 결과 기록

## 생성 산출물

| 산출물 | 경로 |
| --- | --- |
| PPTX | `second acting/output/이승로봇_게임재활_콘텐츠기획_20260512.pptx` |
| PNG 미리보기 | `second acting/output/ppt_preview_게임재활_20260512/` |
| 몽타주 | `second acting/output/ppt_preview_게임재활_20260512/montage.png` |
| 저장본 검사 리포트 | `second acting/output/ppt_reports_게임재활_20260512/` |
| 빌드 스크립트 | `ppt-workspace/src/build-game-rehab-content-plan.mjs` |

## PPT 구성

- 총 10장
- 주제: 간단한 재활운동을 게임운동 콘텐츠로 바꾸는 기획
- 중심 메시지: 운동을 "반복 숙제"가 아니라 "목표·반응·기록이 있는 짧은 게임 루프"로 설계한다.
- 표현 기준: 치료 효과, 회복, 기능 개선을 단정하지 않고, 수행·반응·기록·전문가 확인 중심으로 설명한다.

## 검증 명령

```powershell
& "C:\Users\hreke\.cache\codex-runtimes\codex-primary-runtime\dependencies\node\bin\node.exe" "C:\Users\hreke\OneDrive\Desktop\회사자료\하네스엔지니어링발표\ppt-workspace\src\build-game-rehab-content-plan.mjs"
```

## 렌더링 결과

- PPTX 생성: PASS
- 저장된 PPTX 재불러오기: PASS
- PNG 미리보기 렌더링: PASS
- 렌더링 기준 슬라이드 수: 10
- 저장본 기준 슬라이드 수: 10
- 몽타주 육안 확인: PASS
- 주요 슬라이드 개별 확인: 1~10페이지 PASS

## 패키지 검사

- `ppt/slides/slide*.xml` 기준 슬라이드 수: 10
- visible slide XML 내 `Slide Number`, `sldNum`, `TODO`, `PLACEHOLDER` 탐지: 없음
- notes master/notes slide 내부 기본 placeholder는 발표 화면에 보이지 않는 노트 영역 요소로 판단

## QA 메모

- 1페이지 우측 루프 패널을 `미션 → 반응 → 기록 → 다음 미션` 세로 구조로 정리했다.
- 2페이지 하단 문제 연결부를 장식 화살표가 아니라 얇은 진행선과 색상 점으로 정리했다.
- 3페이지 루프 컴포넌트는 순환 화살표가 복잡해 보여, 6단계 레일형 구조로 다시 정렬했다.
- 5페이지 환자 화면 설명문이 우측 UI 목업과 가까워 보여, 텍스트 폭을 줄이고 재렌더링했다.
- 긴 조사문은 본문에 넣지 않고, 게임 루프와 화면 예시 중심으로 압축했다.
- 위험한 문장은 8페이지에서 "검토 필요" 예시로만 사용했다.
- 실제 제품 화면처럼 보일 수 있는 UI는 `기획 예시`로 표시했다.

## 추가 QA 문서

- 디자인·맥락 점검 상세: `second acting/output/PPT_디자인_맥락_QA.md`

## WARN/BLOCKED

- WARN: 실제 이승로봇 기능 범위가 확인되지 않았으므로 제품 기능처럼 보이는 문구는 피했다.
- WARN: 환자 안전, 운동 강도, 중단 기준은 재활 전문가 확인 전 확정하지 않는다.
- WARN: 의료기기/광고 표현은 RA 담당자 확인 전 외부 발표용으로 확정하지 않는다.
- BLOCKED 없음: 요청 범위인 기획 PPTX output은 생성 완료.

# 본체 에이전트용 PPT 반영 보고

- 작성일: 2026-05-12
- 목적: 지금까지 `Example` 폴더에서 진행한 first~fifth acting 결과를 본래 발표 PPT에 녹여 넣기 위한 보고
- 전제: 이 내용은 “이승로봇 기획물을 완성했다”가 아니라, 하네스 기반으로 에이전트를 단계별로 세팅하면 어떤 산출물이 이어지는지 보여주는 운영 예시다.
- 반영 위치: 기존 발표자료 9페이지 이후에 예시 섹션으로 추가하는 용도
- 반영 결정: 2026-05-12 본체 PPT에는 먼저 “하네스 기반 샘플 프로젝트” 전환 슬라이드 1장을 추가했다. 표현은 “결과물을 만들었다”가 아니라 “자료조사 → 콘텐츠 기획 → UI/UX → 애니메이션 검증/데이터 플로우로 이어지는 샘플 프로젝트”로 잡는다.

## 먼저 봐야 할 파일

본체 에이전트는 아래 순서로 확인한다.

| 순서 | 볼 파일 | 확인할 내용 |
| --- | --- | --- |
| 1 | `01_PPT_반영_인수인계.md` | 기존 9페이지 이후에 넣으려던 원래 의도와 정정 히스토리 |
| 2 | `first acting/output/자료조사_요약.md` | 자료조사 에이전트가 근거와 안전 표현을 분리한 방식 |
| 3 | `first acting/output/브레인스토밍_게임재활_콘텐츠.md` | “간단한 재활운동을 게임운동으로 승화”한다는 기획 방향 |
| 4 | `first acting/output/콘텐츠기획_재료.md` | PPT에 안전하게 쓸 수 있는 메시지 재료 |
| 5 | `first acting/output/팩트체킹_로그.md` | 출처, 확인일, WARN, 전문가 확인 필요 항목 |
| 6 | `second acting/output/신규기획PPT_구성안.md` | 콘텐츠 기획 PPT의 흐름 |
| 7 | `third acting/output/UIUX_화면상세_컴포넌트액션.md` | 화면ID, 1080x1920 배치 기준, 컴포넌트 액션 |
| 8 | `fourth acting/output/애니메이션클립_설명.md` | 연결 화면 애니메이션 클립의 역할 |
| 9 | `fifth acting/output/데이터플로우차트_설명.md` | 데이터 플로우 차트 V2의 의미 |

## PPT에 넣을 핵심 메시지

한 문장으로 정리하면 다음이다.

> 하네스는 에이전트에게 “무엇을 만들지”만 주는 것이 아니라, 먼저 무엇을 읽고, 무엇을 검증하고, 어떤 산출물을 다음 에이전트에게 넘길지 정하는 운영 구조다.

이번 예시에서 보여줄 흐름:

1. first acting: 자료조사, 팩트체킹, 안전 표현, 전문가 질문 정리
2. second acting: 조사 결과를 콘텐츠 기획 PPT로 변환
3. third acting: 실무 개발 인계를 위한 UI/UX 화면상세 제작
4. fourth acting: 연결 화면 애니메이션 클립 샘플 제작
5. fifth acting: 입력/API/저장/조회 기준의 데이터 플로우 차트 제작

## 권장 장표 구성

### 추가 슬라이드 1. 하네스는 에이전트의 역할을 쪼갠다

넣을 내용:

- 주제 예시: 이승로봇 게임재활 콘텐츠 기획
- 흐름: 자료조사 → 콘텐츠 기획 → UI/UX 화면상세 → 애니메이션 클립 → 데이터 플로우
- 핵심 문장: “한 에이전트가 PPT를 바로 만드는 것이 아니라, 각 acting이 다음 acting의 입력값을 만든다.”

시각화:

- 가로 파이프라인 또는 계단형 다이어그램
- `first`, `second`, `third`, `fourth`, `fifth`를 작은 단계 카드로 표시

### 추가 슬라이드 2. first acting은 근거와 표현 기준을 만든다

넣을 내용:

- 먼저 읽은 하네스: 리서치, 팩트체킹, 재활근거, 법률/규제 하네스
- 산출물: 조사 요약, 팩트체킹 로그, 콘텐츠 기획 재료, 전문가 확인 질문
- 안전 표현 분리: 안전한 문장 / 위험한 문장 / WARN / 재활 전문가 확인 필요

봐야 할 파일:

- `first acting/output/자료조사_요약.md`
- `first acting/output/팩트체킹_로그.md`
- `first acting/output/재활전문가_확인질문.md`

넣으면 좋은 문장:

> 자료조사 에이전트는 PPT를 바로 만드는 사람이 아니라, 다음 에이전트가 믿고 쓸 수 있는 근거와 표현 기준을 정리하는 역할이다.

넣지 말아야 할 표현:

- “치료된다”
- “회복된다”
- “효과가 입증됐다”
- 제품 효과처럼 읽히는 문장

### 추가 슬라이드 3. second acting은 콘텐츠 기획으로 바꾼다

넣을 내용:

- 기획 방향: 간단한 재활운동을 게임형 미션으로 바꾸는 콘텐츠
- 핵심 축: 반복 훈련, 기록, 관찰, 피드백
- 산출물: 신규 기획 PPT 샘플

봐야 할 파일:

- `second acting/output/신규기획PPT_구성안.md`
- `second acting/output/신규기획PPT_장표문구_초안.md`
- `second acting/output/이승로봇_게임재활_콘텐츠기획_20260512.pptx`

넣으면 좋은 문장:

> 콘텐츠 기획 에이전트는 조사 결과를 발표용 메시지로 압축하되, 의료 효과처럼 읽히는 표현은 제거한다.

### 추가 슬라이드 4. third acting은 개발자가 볼 화면상세로 바꾼다

넣을 내용:

- 기준 해상도: `1080x1920`
- 화면ID: P-01, P-02, P-03, P-04A, P-04B, P-05, T-01
- 각 화면에 필요한 것: 배치 좌표, 버튼/필드 액션, 이벤트명, 다음 화면ID

봐야 할 파일:

- `third acting/output/이승로봇_게임재활_UIUX기획_화면상세_20260512.pptx`
- `third acting/output/UIUX_화면상세_컴포넌트액션.md`
- `third acting/output/ppt_preview_UIUX_화면상세_20260512/slide-03.png`
- `third acting/output/ppt_preview_UIUX_화면상세_20260512/slide-05.png`
- `third acting/output/ppt_preview_UIUX_화면상세_20260512/slide-07.png`

PPT에 넣을 시각 자료:

- P-03 미션 수행 화면 캡처를 대표 이미지로 사용
- 옆에는 “컴포넌트/위치, 사용자 액션, 이벤트/다음” 표를 작게 요약

넣으면 좋은 문장:

> UI/UX 기획은 추상적인 경험 설명이 아니라, 화면ID·좌표·액션·저장 이벤트를 개발자가 확인할 수 있는 형태로 내려간다.

### 추가 슬라이드 5. fourth acting은 화면 전환을 애니메이션 클립으로 검증한다

넣을 내용:

- SVG/XML 기반 애니메이션 클립
- 흐름: P-01 → P-02 → P-03 → P-04A → P-03 → P-05
- 이벤트: tapExercise, tapStart, tapRest, tapResume, timerEnd

봐야 할 파일:

- `fourth acting/output/이승로봇_연결화면_애니메이션클립.svg`
- `fourth acting/output/이승로봇_연결화면_애니메이션클립_preview.html`
- `fourth acting/output/animation_clip_timeline.xml`
- `fourth acting/output/animation_clip_preview_screenshot.png`

PPT에 넣을 시각 자료:

- `animation_clip_preview_screenshot.png`
- 하단에 “SVG(XML)로 브라우저에서 바로 확인 가능”이라고 작게 표시

넣으면 좋은 문장:

> 화면상세 다음에는 연결 화면을 움직이는 클립으로 만들어, 화면 전환과 이벤트 타이밍을 눈으로 확인한다.

주의:

- 이것은 최종 앱 애니메이션이 아니라 운영 예시용 클립이다.

### 추가 슬라이드 6. fifth acting은 데이터 플로우를 개발 언어로 바꾼다

넣을 내용:

- V2 차트 기준: 입력/트리거 → API/이벤트 처리 → 저장 테이블 → 화면 조회/출력
- API 예시: `GET /exercises`, `POST /sessions`, `POST /event-logs`, `POST /safety-inputs`, `PATCH /sessions/{id}`
- 저장 테이블: Exercise, Session, EventLog, SafetyInput, TherapistMemo
- 조회 화면: P-01 운동 목록, P-05 완료 요약, T-01 세션 상세

봐야 할 파일:

- `fifth acting/output/이승로봇_데이터플로우차트.svg`
- `fifth acting/output/이승로봇_데이터플로우차트_preview.html`
- `fifth acting/output/data_flow_spec.json`
- `fifth acting/output/data_flow_chart_preview_screenshot.png`

PPT에 넣을 시각 자료:

- `data_flow_chart_preview_screenshot.png`

넣으면 좋은 문장:

> 데이터 플로우는 상태 흐름을 그리는 것이 아니라, 어떤 입력이 어떤 API를 통해 어떤 테이블에 쓰이고 어떤 화면에서 읽히는지를 분리한다.

## 압축 버전 구성

PPT 여유가 없으면 6장을 모두 넣지 말고 4장으로 줄인다.

| 압축 슬라이드 | 넣을 내용 |
| --- | --- |
| 1 | Acting 파이프라인 전체: first~fifth |
| 2 | first acting: 근거, 안전 표현, 전문가 확인 질문 |
| 3 | third acting: 1080x1920 화면상세와 컴포넌트 액션 |
| 4 | fourth/fifth acting: 애니메이션 클립과 데이터 플로우 차트 |

## 장표 톤 가이드

- “이승로봇 제품이 이런 기능을 제공한다”처럼 확정적으로 쓰지 않는다.
- “운영 예시”, “샘플”, “초안”, “개발 인계 기준”이라는 톤을 유지한다.
- 긴 사용자 요청문이나 파일 전문을 붙이지 않는다.
- 실제 결과물을 자랑하는 톤보다, 하네스가 업무를 어떻게 나누고 검증 기준을 유지하는지 보여준다.
- 안전 문구는 항상 남긴다: “센서 입력, 중단 기준, 환자 피드백 문구는 재활 전문가 확인 필요.”

## 본체 에이전트에게 전달할 최종 요청문

```text
Example 폴더의 first~fifth acting 산출물을 본래 발표 PPT 9페이지 이후 예시 섹션으로 녹여 넣어줘.

핵심은 이승로봇 결과물을 완성본처럼 보여주는 것이 아니라,
하네스를 사용하면 에이전트가 자료조사, 콘텐츠 기획, UI/UX 화면상세,
애니메이션 클립, 데이터 플로우 차트까지 단계별로 역할을 나눠 산출물을 이어갈 수 있다는 운영 예시를 보여주는 것이다.

반드시 먼저 `02_본체에이전트_PPT반영_보고.md`를 읽고,
필요하면 `01_PPT_반영_인수인계.md`로 이전 의도와 정정 히스토리를 확인해줘.

PPT에는 긴 요청문을 넣지 말고, 다음 구조로 시각화해줘.

1. first~fifth acting 파이프라인
2. first acting의 근거/안전 표현/전문가 확인 질문 분리
3. third acting의 1080x1920 화면상세와 컴포넌트 액션
4. fourth acting의 SVG(XML) 애니메이션 클립
5. fifth acting의 데이터 플로우 차트 V2

주의:
- 실제 제품 기능이나 치료 효과처럼 보이게 쓰지 말 것
- “치료된다”, “회복된다”, “효과가 입증됐다” 표현 금지
- 센서 입력, 중단 기준, 환자 피드백 문구는 재활 전문가 확인 필요로 표시
```

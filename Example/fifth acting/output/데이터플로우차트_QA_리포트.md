# 데이터 플로우 차트 QA 리포트

- 작성일: 2026-05-12
- 단계: fifth acting
- 대상 파일: `이승로봇_데이터플로우차트.svg`
- 프리뷰 파일: `이승로봇_데이터플로우차트_preview.html`
- 명세 파일: `data_flow_spec.json`
- 보정 버전: V2

## 검증 결과

| 항목 | 결과 |
| --- | --- |
| SVG XML 파싱 | PASS |
| JSON 파싱 | PASS |
| Chrome headless 캡처 | PASS |
| 캡처 파일 | `data_flow_chart_preview_screenshot.png` |
| 차트 흐름 | 입력/트리거 → API/이벤트 처리 → 저장 테이블 → 화면 조회/출력 |
| 안전 문구 | 치료 효과 표현 없이 작성 |

## 확인한 내용

| 영역 | 확인 |
| --- | --- |
| 입력/트리거 | 운동 기준 데이터, 환자 앱 액션, 타이머/센서 입력, 중단 입력, 치료사 메모 입력 표시 |
| API/이벤트 처리 | `GET /exercises`, `POST /sessions`, `POST /event-logs`, `POST /safety-inputs`, `PATCH /sessions/{id}` 표시 |
| 저장 테이블 | Exercise, Session, EventLog, SafetyInput, TherapistMemo 분리 |
| 화면 조회/출력 | P-01, P-05, T-01 read model 분리 |
| 개발 명세 | `data_flow_spec.json`에 stores, writes, reads 포함 |

## 사용한 확인 명령

```powershell
$svg = "C:\Users\hreke\OneDrive\Desktop\회사자료\하네스엔지니어링발표\agent-harnessing-guidelines\Example\fifth acting\output\이승로봇_데이터플로우차트.svg"
[xml](Get-Content -LiteralPath $svg -Raw -Encoding UTF8) | Out-Null
```

```powershell
$json = "C:\Users\hreke\OneDrive\Desktop\회사자료\하네스엔지니어링발표\agent-harnessing-guidelines\Example\fifth acting\output\data_flow_spec.json"
Get-Content -LiteralPath $json -Raw -Encoding UTF8 | ConvertFrom-Json | Out-Null
```

```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" `
  --headless=new `
  --disable-gpu `
  --hide-scrollbars `
  --window-size=1600,1250 `
  --screenshot="data_flow_chart_preview_screenshot.png" `
  "file:///C:/Users/hreke/OneDrive/Desktop/회사자료/하네스엔지니어링발표/agent-harnessing-guidelines/Example/fifth%20acting/output/이승로봇_데이터플로우차트_preview.html"
```

## 남은 주의사항

- WARN: 이 차트는 구현 방향 샘플이며 실제 DB 스키마 확정본이 아니다.
- WARN: `movement_tick.value`의 단위와 의미는 실제 이승로봇 센서 스펙 확인이 필요하다.
- WARN: `pain`, `fatigue`, `dizziness` 입력 범위와 중단 기준은 재활 전문가 확인이 필요하다.
- WARN: 치료, 회복, 효과 입증처럼 읽히는 표현은 데이터 필드명·UI 문구·보고서 문구에서 피한다.

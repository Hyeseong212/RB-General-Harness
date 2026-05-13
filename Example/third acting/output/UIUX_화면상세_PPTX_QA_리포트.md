# UI/UX 화면상세 PPTX QA 리포트

- 작성일: 2026-05-12
- 대상 파일: `이승로봇_게임재활_UIUX기획_화면상세_20260512.pptx`
- 기준 해상도: 모바일 세로 `1080x1920`
- 목적: 사용자가 지적한 “현재 플로우만 있고 화면, 배치, 컴포넌트 액션이 없다”는 문제를 해결하기 위한 화면상세 보강본

## 생성 결과

| 항목 | 결과 |
| --- | --- |
| 슬라이드 수 | 12장 |
| 저장 위치 | `Example/third acting/output` |
| PPTX | `이승로봇_게임재활_UIUX기획_화면상세_20260512.pptx` |
| PNG 캡처 | `ppt_preview_UIUX_화면상세_20260512/` |
| 검사 리포트 | `ppt_reports_UIUX_화면상세_20260512/` |

## 포함 내용

| 구분 | 반영 |
| --- | --- |
| 화면 와이어프레임 | P-01, P-02, P-03, P-04A, P-04B, P-05, T-01 |
| 해상도 기준 | 모든 모바일 화면에 `1080x1920` 표기 |
| 배치 기준 | 주요 화면에 `x/y/w/h` 또는 영역 좌표 표시 |
| 컴포넌트 액션 | 탭, 클릭, 자동 이동, 오류 표시, 저장 이벤트 분리 |
| 개발 인계 | 티켓 단위와 완료 조건 분리 |

## 검증

| 검증 항목 | 결과 |
| --- | --- |
| PPTX 생성 | PASS |
| 저장본 재불러오기 | PASS |
| PNG 렌더 | PASS, 12장 생성 |
| 주요 슬라이드 육안 확인 | PASS, 1/2/3/5/7/9/10/12 확인 |
| XML 플레이스홀더 검사 | PASS, `placeholderMatches=""` |

## 사용한 확인 명령

```powershell
& "C:\Users\hreke\.cache\codex-runtimes\codex-primary-runtime\dependencies\node\bin\node.exe" `
  "C:\Users\hreke\OneDrive\Desktop\회사자료\하네스엔지니어링발표\ppt-workspace\src\build-game-rehab-uiux-screen-detail.mjs"
```

```powershell
$pptx = "C:\Users\hreke\OneDrive\Desktop\회사자료\하네스엔지니어링발표\agent-harnessing-guidelines\Example\third acting\output\이승로봇_게임재활_UIUX기획_화면상세_20260512.pptx"
Add-Type -AssemblyName System.IO.Compression.FileSystem
$zip = [System.IO.Compression.ZipFile]::OpenRead($pptx)
$slides = $zip.Entries | Where-Object { $_.FullName -match '^ppt/slides/slide\d+\.xml$' }
```

## 남은 주의사항

- WARN: 이 PPT는 개발 인계용 화면상세 초안이며 최종 Figma 디자인이 아니다.
- WARN: 1080x1920 좌표는 화면 설계 기준값이다. 실제 터치 영역, 폰트 크기, 접근성은 Figma 또는 HTML 프로토타입에서 다시 검증해야 한다.
- WARN: 센서 입력값, 반복 횟수, 중단 기준, 피드백 문구는 재활 전문가와 제품 담당자 확인이 필요하다.
- WARN: 치료 효과, 회복, 기능 향상처럼 읽히는 표현은 화면 문구에서도 사용하지 않는다.

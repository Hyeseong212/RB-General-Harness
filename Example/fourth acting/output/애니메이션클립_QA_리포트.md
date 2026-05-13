# 애니메이션 클립 QA 리포트

- 작성일: 2026-05-12
- 단계: fourth acting
- 대상 파일: `이승로봇_연결화면_애니메이션클립.svg`
- 프리뷰 파일: `이승로봇_연결화면_애니메이션클립_preview.html`
- 기준 해상도: 모바일 세로 `1080x1920`

## 검증 결과

| 항목 | 결과 |
| --- | --- |
| SVG XML 파싱 | PASS |
| timeline XML 파싱 | PASS |
| Chrome headless 캡처 | PASS |
| 캡처 파일 | `animation_clip_preview_screenshot.png` |
| 화면 흐름 | P-01 → P-02 → P-03 → P-04A → P-03 → P-05 |
| 안전 문구 | 치료 효과 표현 없이 작성 |

## 사용한 확인 명령

```powershell
$svg = "C:\Users\hreke\OneDrive\Desktop\회사자료\하네스엔지니어링발표\agent-harnessing-guidelines\Example\fourth acting\output\이승로봇_연결화면_애니메이션클립.svg"
[xml](Get-Content -LiteralPath $svg -Raw -Encoding UTF8) | Out-Null
```

```powershell
$xml = "C:\Users\hreke\OneDrive\Desktop\회사자료\하네스엔지니어링발표\agent-harnessing-guidelines\Example\fourth acting\output\animation_clip_timeline.xml"
[xml](Get-Content -LiteralPath $xml -Raw -Encoding UTF8) | Out-Null
```

```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" `
  --headless=new `
  --disable-gpu `
  --hide-scrollbars `
  --window-size=1600,1250 `
  --screenshot="animation_clip_preview_screenshot.png" `
  "file:///C:/Users/hreke/OneDrive/Desktop/회사자료/하네스엔지니어링발표/agent-harnessing-guidelines/Example/fourth%20acting/output/이승로봇_연결화면_애니메이션클립_preview.html"
```

## 남은 주의사항

- WARN: SVG 애니메이션은 샘플 클립이다. 실제 앱 애니메이션 구현 방식은 웹, 앱, Figma, Lottie 등 개발 환경에 맞춰 다시 선택해야 한다.
- WARN: `animation_clip_timeline.xml`은 명세용 XML이고, 실제 재생 파일은 `SVG(XML)`이다.
- WARN: 실제 센서 반응, 중단 기준, 환자 피드백 문구는 재활 전문가 확인 후 확정해야 한다.

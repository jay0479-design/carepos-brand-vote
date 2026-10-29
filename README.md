# CarePOS 심볼 시안 · 투표 페이지

Figma의 「케어포스 브랜드 디자인 › 심볼 시안」 섹션을 웹페이지로 옮긴 정적 사이트입니다.
4개 심볼 시안(케어 카운터 / 틸트 터미널 / 네이밍 표기 워드마크 / 케어 모니터)을 소개하고,
페이지 하단에서 **로고 투표**와 **간단한 의견 남기기**를 할 수 있습니다.

- 호스팅: GitHub Pages (이 저장소의 `main` 브랜치 루트)
- 투표/의견 저장: Firebase Realtime Database (`polls/carepos-logo-vote` 경로, 실시간 집계)
- 기기당 1표, 다른 시안을 누르면 선택이 바뀝니다. 이름은 선택 입력입니다.
- 네트워크 문제로 DB에 연결되지 않으면 해당 기기에만 저장되는 오프라인 모드로 동작합니다.

## 구조

```
index.html          페이지 본문 + 스타일 + 투표/의견 스크립트
assets/symbol-0N.svg  시안 심볼 (Figma 벡터 레이어 그대로)
assets/wordmark.svg   CarePOS 워드마크
```

## 로컬 미리보기

```bash
python3 -m http.server 8765
```

그 다음 http://localhost:8765 를 엽니다.

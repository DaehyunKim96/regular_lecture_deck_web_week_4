# AI 업무 자동화 정규강의 — 4회차 덱

`regular_lecture_deck_web_week_3`과 동일한 발표 UX·디자인 언어를 사용하는 4회차 강의 덱입니다.

현재 구성: 오프닝 1장 → 3회차 Recap 11장(디바이더 포함 · Claude Code 전환 개념·사전지식 압축 1장 · Cowork vs Code 비교·판별기준 1장 · 회의록→업무보고 Claude Code 실습 재현 1장 · 커스텀 MCP·한글(HWP) 문서 실습 1장 · 발표자료 제작 배경(AI 슬롭·3층 구조) 1장 · 프롬프트 아키텍처 4계층 1장 · DESIGN.md 9섹션·안티 AI-슬롭 금지목록 1장 · 검증층(레퍼런스·스크린샷·좌표 수정) 1장 · 실제 제작 3가지 방식(Slidev·frontend-slides·React+Vite) 1장 · 배포(GitHub→Vercel) 1장) — 총 12장.

3회차 덱(`regular_lecture_deck_web_week_3/public/deck.html`, 총 85장)의 내용을 다섯 갈래(Claude Code 전환 → 실습 재현 → 발표자료 설계 → 실제 제작 → 배포)로 압축해 Recap을 구성했습니다 — 2회차 → 3회차 전환 때와 같은 방식입니다.

4회차 본편(신규 실습 내용)은 아직 작성 전입니다. Recap 뒤에 이어서 추가될 예정입니다.

## 구조

```text
regular_lecture_deck_web_week_4/
├─ index.html
├─ src/
│  ├─ main.jsx
│  ├─ App.jsx
│  └─ index.css
├─ public/
│  ├─ deck.html
│  ├─ instructor.png
│  ├─ img/
│  └─ assets/
├─ vite.config.js
└─ package.json
```

React 앱은 `public/deck.html`을 전체화면 iframe으로 로드합니다. 슬라이드 디자인, 키보드 이동, 진행률, 발표자 노트, 전체화면 전환은 `deck.html` 내부에서 동작합니다.

## 로컬 실행

```bash
npm install
npm run dev
npm run build
```

## 편집 방식

- 강의 자료는 `public/deck.html`의 `<section class="slide">` 단위로 추가합니다.
- 무료 강의 덱에서 가져온 핵심 UI 블록: `kicker`, `numlist`, `steps`, `sheet`, `versus`, `toolgrid`, `media`, `vslot`, `timer`, `note`.
- 발표자 노트는 각 슬라이드 끝의 `<aside class="note">`에 작성합니다.
- 장표 본문은 개조식으로 작성합니다 — `lecture/SLIDE_STYLE_GUIDE.md` 참고.
- 데모 영상은 `public/assets/videos/`, 캡처 이미지는 `public/assets/images/`, 화면 캡처는 `public/img/`에 넣고 슬라이드에서 상대 경로로 참조합니다.

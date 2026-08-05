# AI 업무 자동화 정규강의 — 4회차 덱

`regular_lecture_deck_web_week_3`과 동일한 발표 UX·디자인 언어를 사용하는 4회차 강의 덱입니다.

현재 구성: 오프닝 1장 → 3회차 Recap 11장(디바이더 포함 · Claude Code 전환 개념·사전지식 압축 1장 · Cowork vs Code 비교·판별기준 1장 · 회의록→업무보고 Claude Code 실습 재현 1장 · 커스텀 MCP·한글(HWP) 문서 실습 1장 · 발표자료 제작 배경(AI 슬롭·3단계 구조) 1장 · 프롬프트 아키텍처 4계층 1장 · DESIGN.md 9섹션·안티 AI-슬롭 금지목록 1장 · 검증 단계(레퍼런스·스크린샷·좌표 수정) 1장 · 실제 제작 3가지 방식(Slidev·frontend-slides·React+Vite) 1장 · 배포(GitHub→Vercel) 1장) → 발표자료 실습 본편 37장(디바이더 포함 · 배경·AI 슬롭 이론 3장 · 프롬프트 아키텍처·CLAUDE.md·DESIGN.md·안티 AI-슬롭·레퍼런스 주입·스크린샷 검증·정밀 수정 7장 · 원고→뼈대 1장 · CLAUDE.md·DESIGN.md 채우기 프롬프트 6장 · Slidev·frontend-slides·React+Vite 11장 · 다른 에이전트 안내 1장 · 실행 방법 1장 · 배포 5장) → 메시징 연결 실습 9장(디바이더 포함 · 카카오 PlayMCP 개요·사용 방식·활용 예시·Claude 연동·인증 오류 실측 사례·현재 상태·유의사항·정리) → Q&A 1장 — 총 58장.

3회차 덱(`regular_lecture_deck_web_week_3/public/deck.html`, 총 85장)의 내용을 다섯 갈래(Claude Code 전환 → 실습 재현 → 발표자료 설계 → 실제 제작 → 배포)로 압축해 Recap을 구성했습니다 — 2회차 → 3회차 전환 때와 같은 방식입니다.

3회차 마지막 실습(발표자료 만들기)은 분량이 많아 시간 안에 슬라이드만 훑고 실제로 다 못 해본 부분이었습니다. Recap 뒤에는 그 부분(원고 정리 → CLAUDE.md·DESIGN.md 작성 → Slidev·frontend-slides·React+Vite로 실제 제작 → GitHub→Vercel 배포)을 3회차 덱에서 그대로 가져와 이번 회차에 처음부터 끝까지 실습하는 본편으로 이어붙였습니다.

이어서 4회차 신규 실습으로 카카오 PlayMCP(MCP 기반 메시징·서비스 연동 플랫폼)를 Claude/Claude Code에 연결하는 실습을 추가했습니다. 실제로 겪은 인증 오류(HTTP 403 · IP 대역 차단)를 진단 로그와 함께 그대로 담아, 연동이 매끄럽게만 흘러가지 않는 실무 사례로 다룹니다.

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

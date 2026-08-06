# AI 업무 자동화 정규강의 — 4회차 덱

`regular_lecture_deck_web_week_3`과 동일한 발표 UX·디자인 언어를 사용하는 4회차 강의 덱입니다.

현재 구성: 오프닝 1장 → 3회차 Recap 11장(디바이더 포함 · Claude Code 전환 개념·사전지식 압축 1장 · Cowork vs Code 비교·판별기준 1장 · 회의록→업무보고 Claude Code 실습 재현 1장 · 커스텀 MCP·한글(HWP) 문서 실습 1장 · 발표자료 제작 배경(AI 슬롭·3단계 구조) 1장 · 프롬프트 아키텍처 4계층 1장 · DESIGN.md 9섹션·안티 AI-슬롭 금지목록 1장 · 검증 단계(레퍼런스·스크린샷·좌표 수정) 1장 · 실제 제작 3가지 방식(Slidev·frontend-slides·React+Vite) 1장 · 배포(GitHub→Vercel) 1장) → 발표자료 실습 본편 37장(디바이더 포함 · 배경·AI 슬롭 이론 3장 · 프롬프트 아키텍처·CLAUDE.md·DESIGN.md·안티 AI-슬롭·레퍼런스 주입·스크린샷 검증·정밀 수정 7장 · 원고→뼈대 1장 · CLAUDE.md·DESIGN.md 채우기 프롬프트 6장 · 완성본 내려받기 1장 · Slidev·frontend-slides·React+Vite 11장 · 다른 에이전트 안내 1장 · 실행 방법 1장 · 배포 5장) → 메시징 연결 실습·PlayMCP 9장(디바이더 포함 · 개요·사용 방식·활용 예시·Claude 연동·인증 오류 실측 사례·현재 상태·유의사항·정리) → 메시징 연결 실습·Telegram 7장(디바이더 포함 · 개요·봇 생성 0단계·세션 진행 과정 2장·따라 할 프롬프트·정리) → 공지사항 요약 자동화 실습 8장(디바이더 포함 · 역할 분담·사전 준비·`.env` 이해·세션 진행·실행 원칙·따라 할 프롬프트·정리) → 웹 크롤링 자동화 실습 8장(디바이더 포함 · 크롤링 개념·robots.txt와 사전 준비·크롤러 원리·세션 진행·실행 원칙·따라 할 프롬프트·정리) → 업무 자동화 플랫폼 소개 6장(디바이더 포함 · 개념·n8n/Make/Zapier 비교·활용 예시·무료 티어 비교·사용량 단위 차이) → Make 실습 9장(디바이더 포함 · 목표·준비물·모듈 1~5 설정 5장·테스트와 실행·문제 해결) → 데이터 분석 실습 26장(디바이더 포함 · 무료강의 덱 24~50쪽에서 n8n 실습 3장 제외 · 프롬프트를 만드는 프롬프트 1장 추가 · Web AI → DB·SQL → MCP 에이전트 → 대시보드) → Future Work 4장(디바이더 포함 · 현재 구조의 로컬 의존 3가지 · 클라우드 전환 4구간 · Make 시나리오 구성) → Q&A 1장 → 마무리 2장(감사 인사 · 문의처) — 총 129장.

3회차 덱(`regular_lecture_deck_web_week_3/public/deck.html`, 총 85장)의 내용을 다섯 갈래(Claude Code 전환 → 실습 재현 → 발표자료 설계 → 실제 제작 → 배포)로 압축해 Recap을 구성했습니다 — 2회차 → 3회차 전환 때와 같은 방식입니다.

3회차 마지막 실습(발표자료 만들기)은 분량이 많아 시간 안에 슬라이드만 훑고 실제로 다 못 해본 부분이었습니다. Recap 뒤에는 그 부분(원고 정리 → CLAUDE.md·DESIGN.md 작성 → Slidev·frontend-slides·React+Vite로 실제 제작 → GitHub→Vercel 배포)을 3회차 덱에서 그대로 가져와 이번 회차에 처음부터 끝까지 실습하는 본편으로 이어붙였습니다.

이어서 4회차 신규 실습 네 가지를 추가했습니다. 첫째는 카카오 PlayMCP(MCP 기반 메시징·서비스 연동 플랫폼)를 Claude/Claude Code에 연결하는 실습으로, 실제로 겪은 인증 오류(HTTP 403 · IP 대역 차단)를 진단 로그와 함께 그대로 담아 연동이 매끄럽게만 흘러가지 않는 실무 사례로 다룹니다. 둘째는 별도 MCP 없이 Claude Code의 기본 도구(터미널 명령·웹 검색)만으로 텔레그램 봇을 통해 메시지를 자동 발송하는 실습으로, 봇 생성(사람이 직접)부터 chat_id 조회·날씨 검색·요약·전송(프롬프트만으로)까지 실제 세션 진행 과정을 그대로 정리했습니다. 셋째는 긴 사내 공지를 Gemini API로 요약해 텔레그램으로 발송하는 Python 프로그램을 프롬프트만으로 만드는 실습으로, 요약은 Claude가 아니라 Gemini가 수행한다는 역할 분담과 `.env`로 비밀값을 분리하는 원칙을 비개발자 기준으로 설명합니다. 넷째는 셋째 실습의 요약 대상을 웹페이지로 확장한 크롤링 실습으로, 크롤링의 개념과 `robots.txt` 확인 습관, HTML 파싱의 원리(받아오기 → 골라내기)를 비개발자 기준으로 다룹니다.

실습 뒤에는 코드 없이 앱을 연결하는 업무 자동화 플랫폼(n8n·Make·Zapier)을 비교하는 섹션을 두어, 앞선 "프롬프트로 코드를 만들어 내 PC에서 실행"하는 방식과 대비시킵니다. 세 서비스의 성격·활용 예시·무료 티어 장단점과 사용량 단위(execution/credit/task) 차이를 정리하고, 이어질 Make 실습으로 연결합니다.

Make 실습은 앞선 파이썬 크롤링 실습과 같은 결과물(Hacker News 크롤링 → Gemini 요약 → Telegram 전송)을 코드 없이 만드는 비교 실습입니다. HTTP → Text parser → Text aggregator → Gemini AI → Telegram Bot 5개 모듈의 설정값을 화면 항목 그대로 정리하고, 무료 플랜 credit 소진을 막는 실행 주기 주의사항과 증상별 문제 해결 표를 함께 제공합니다.

덱 마지막에는 Future Work 섹션을 두어, 로컬 SQLite·수동 실행에 묶인 현재 구조를 클라우드로 옮기는 방법을 정리했습니다. 데이터(클라우드 DB) · 집계 실행(예약) · AI 호출(API) · 화면 갱신(Deploy Hook) 네 구간의 교체 대상과 후보를 표로 제시하고, Make 시나리오를 5모듈(Schedule → PostgreSQL → Gemini → HTTP → Telegram)로 구성하는 안과 무료 플랜 credit 계산을 함께 담았습니다.

무료 강의 덱(`free_lecture_deck_web`)의 24~50쪽을 그대로 가져와 마지막 실습 파트로 붙였습니다. 해당 슬라이드가 쓰는 컴포넌트 CSS(`gainlist`·`xlsx-mock`·`gterms`·`viz` 등)를 원본에서 추출해 함께 옮겼고, 참조하는 영상 8개와 `dashboard.html`도 `public/`에 복사했습니다. n8n 실습 3장(원본 46~48쪽)은 앞의 자동화 플랫폼 섹션과 내용이 겹쳐 제외했고, 그 슬라이드에서만 쓰던 이미지 2개도 함께 정리했습니다. 슬라이드 하단 러닝풋은 원본의 `PART 3 · 확인한다`에서 이 덱의 규칙에 맞춰 `SESSION 04 · 데이터 분석 실습`으로 바꿨습니다.

실습용 배포 파일은 `public/assets/files/`에 두고 슬라이드에서 `download` 링크로 제공합니다 — 발표자료 실습용 원고(`outline.md`), 공지사항 요약 실습용 샘플 공지(`announcement.md`), 발표자료 실습 완성본 묶음(`presentation-sample.zip` 및 개별 파일 `presentation-sample/`: `CLAUDE.md`·`DESIGN.md`·`design-preview.html`·`refs/ref-01.png`·`refs/ref-02.png`).

완성본 묶음은 `week_3_practice/presentation_sample/`에서 실제 파일을 복사해 온 것입니다. 프롬프트 1~7을 따라오지 못한 수강생이 다음 단계(실제 슬라이드 만들기)부터 이어서 실습할 수 있도록 제공하며, 배포 환경에서 URL이 깨지지 않도록 `refs/` 이미지의 한글 파일명은 `ref-01.png`·`ref-02.png`로 바꿨습니다.

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

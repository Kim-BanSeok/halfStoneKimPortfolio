# halfstone.Kim — 개발자 프로필 & 프로젝트 로그

---

## 경력 기술서 (포트폴리오 About용)

### 자기소개

MFC 산업자동화 시뮬레이터부터 3D 엔진, Android 앱, 웹 게임까지 — 시스템 레벨과 제품 레벨을 모두 경험한 풀스택 개발자입니다. 기획부터 배포까지 혼자 완성하는 1인 개발을 지향합니다.

---

### (주)웰컴소프트 | 대리 · 7년

**도메인**: 생산자동화 설비 시뮬레이션

- **MFC(C++)** 기반 자동화 설비 시뮬레이터 유지보수 및 기능 개선
- **Unity / Unreal Engine** 을 활용한 3D 생산자동화 설비 장비 제작
  - 실제 공장 설비의 동작을 3D로 시각화 및 시뮬레이션
  - 하드웨어 로직을 소프트웨어로 재현하는 시스템 레벨 개발

**사용 기술**: C++, MFC, Unity, Unreal Engine

---

### 에스더블유기술원 | 사원 · 1년

**도메인**: 모바일 앱 자체 개발

- **바나나창고** — Android 중고거래 앱 기획 → 개발 → 출시 (Google Play Store 등록)
- React Native 프론트엔드 + Node.js 백엔드 + PostgreSQL DB 풀스택 개발
- AWS 인프라 구성 및 배포 운영
- 1인 기획/개발/출시 전 과정 수행

**사용 기술**: React Native, Node.js, PostgreSQL, AWS

---

### 현재 | 1인 개발 프로젝트

**도메인**: 웹 게임 포트폴리오

- 외부 라이브러리 없이 순수 Vanilla JS + Web Audio API + Canvas 2D로 게임 7종 제작
- 물리 엔진, 사운드 합성, 리듬 게임 판정 시스템 등 직접 구현
- GitHub Actions 자동 배포 (GitHub Pages)

**사용 기술**: JavaScript, Web Audio API, Canvas 2D, CSS, HTML, GitHub Actions

---

## 기술 스택 전체

| 분야 | 기술 |
|------|------|
| 시스템/3D | C++, MFC, Unity, Unreal Engine |
| 모바일 | React Native |
| 프론트엔드 | JavaScript, React, Vue, HTML/CSS |
| 백엔드 | Node.js |
| DB | PostgreSQL |
| 인프라 | AWS, GitHub Actions |

---

## 프로젝트 로그 — IT 테마 게임 포트폴리오

> **기간**: 2026년 6월  
> **스택**: Vanilla JavaScript, Web Audio API, Canvas 2D, HTML/CSS (싱글 파일)  
> **배포**: GitHub Pages 자동 배포 (GitHub Actions)

---

## 프로젝트 개요

포트폴리오 메인 사이트(`index.html`)와 7개의 독립 게임을 단일 HTML 파일로 구성한 1인 개발 프로젝트.  
외부 라이브러리 없이 브라우저 기본 API만 사용. IT 다크 테마로 통일.

**공통 기술 스택**
- 렌더링: `<canvas>` + `requestAnimationFrame`
- 사운드: Web Audio API (절차적 8비트 효과음)
- 저장: `localStorage` (베스트 스코어, 설정)
- 반응형: `100dvh` 기반, 터치/마우스 공통 지원
- 디자인: `--bg:#07071A`, `--cyan:#00D4FF`, `--purple:#8B5CF6`, DM Mono 폰트

---

## 게임 목록 및 구현 내용

### 1. `snake.html` — 스네이크 게임
- 파워업 시스템 (속도 부스트, 점수 2배, 벽 통과)
- 콤보 멀티플라이어
- 파티클 폭발 효과
- **버그 수정**: 초기 render 크래시, 꼬리 오탐 충돌, 일시정지 후 파워업 스폰 중단

### 2. `2048.html` — 2048 퍼즐
- 타임어택 모드
- 업적 시스템
- 되돌리기(Undo) 기능
- **버그 수정**: 승리/게임오버 중복 발생, 터치 스크롤 미방지, 게임 전 키 입력 방어

### 3. `type.html` — 타이핑 속도 게임
- WPM 실시간 측정
- 한/영 IME 완전 지원 (한글 조합 처리)
- 레이스 모드 (봇 대결)
- **버그 수정/리팩터**: 한글 IME `spacePending` 처리 → `compositionend` 기반 단순화

### 4. `runner.html` — 무한 러너
- IT 테마 장애물 (버그, 404 에러, 바이러스)
- 아이템 시스템, 스테이지 전환
- 고스트 레이싱 (최고 기록 재현)
- 업적 시스템
- **버그 수정**: 재시작 시 dieFrame 중복 루프, 고스트 저장 범위 오류, 스테이지 색상 전환 버그

### 5. `breakout.html` — 벽돌 깨기
- 다중 벽돌 타입 (일반/강화/폭발/레이저)
- 파워업 드롭 시스템
- 레이저 빔 메카닉
- **버그 수정**: dying 상태 levelClear 오발동, setTimeout 상태 가드 누락

### 6. `rhythm.html` — 리듬 게임
- 7레인 O2JAM 스타일 (S D F SPC J K L)
- 30곡 수록 (EASY 10 / MEDIUM 10 / HARD 10)
- 각 곡 고유 드럼/베이스/멜로디 사운드 (Web Audio 절차적 생성)
- PERFECT / GOOD / BAD / MISS 판정 시스템
- COMBO × FEVER 멀티플라이어 (20콤보 시 ×2)
- **ARCADE 모드**: 에너지 소진 시 FAIL
- **SCORE 모드**: 실패 없이 점수만 집계
- 스크롤 속도 조절 (0.1× ~ 5.0×)
- ESC 일시정지 / 재개 (오디오 오프셋 보정)
- 하이스코어 저장 (곡별 점수 + 등급)

### 7. `shooter.html` — 슈팅 게임 (FIREWALL.EXE)
- 탄막 슈팅 — 5종 적 (BUG / GLITCH / VIRUS / PAYLOAD / ROOTKIT 보스)
- 웨이브 클리어 후 업그레이드 샵 (DAMAGE / SPEED / FIRE RATE / BOMB / REPAIR / SHIELD)
- 보스 3페이즈 전투 (HP에 따라 탄막 패턴 변화)
- 폭탄 시스템 (화면 전체 클리어)
- 터치 드래그 이동, 더블탭 폭탄
- **버그 수정**: drawHUD() lives 하드코딩 3 → 최대 5 아이콘 + ×N 오버플로우 표시

### 8. `tower.html` — 타워 디펜스 (TOWER.EXE)
- 22×14 그리드 맵, 고정 경로 (IN → OUT)
- 타워 4종: FIREWALL(기본) / ANTIVIRUS(슬로우) / SCANNER(속사) / PROXY(범위딜)
- 적 5종: BUG / VIRUS / TROJAN(탱커) / WORM / ROOTKIT(보스)
- 10웨이브 서바이벌, 웨이브 클리어 보너스 골드
- 타워 2단계 업그레이드 / 판매 시스템
- Web Audio 절차적 효과음, 파티클

---

## 포트폴리오 메인 (`index.html`)

- 로딩 애니메이션 (터미널 부팅 효과)
- 햄버거 메뉴 (모바일)
- 한/영 언어 토글 (i18n)
- Skills 섹션 (기술 스택 시각화)
- 게임 카드 갤러리 (각 게임 프리뷰 캔버스)
- 컨택트 폼
- IT 테마 에러 화면 (게임 카드 hover 효과)

---

## 인프라

- GitHub Actions 워크플로우 (`/.github/workflows/`) — push on master → GitHub Pages 자동 배포
- 외부 의존성 0 (Google Fonts 제외)

---

## 기술적 특징 / 포트폴리오 어필 포인트

| 항목 | 내용 |
|------|------|
| 파일 구조 | 게임 1개 = HTML 1개. 빌드 툴 없음 |
| 사운드 | Web Audio API로 런타임 사운드 생성 (mp3 파일 없음) |
| 렌더링 | requestAnimationFrame 기반 고정 게임 루프 |
| 상태 관리 | 단순 변수 + STATE 머신 패턴 |
| 모바일 | touchstart/move/end + passive:false + 좌표 변환 |
| 저장 | localStorage만 사용 (서버 없음) |
| 언어 | 한/영 런타임 i18n (JSON 딕셔너리 교체 방식) |

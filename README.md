# halfstone.Kim | Developer Portfolio

IT 다크 테마 개인 포트폴리오 + 웹 게임 모음. 빌드 시스템 없이 순수 HTML/CSS/JS 단일 파일로 구성.

## 게임 목록

| 게임 | 파일 | 주요 기능 |
|------|------|-----------|
| 스네이크 | `snake.html` | 파워업 3종, 콤보 ×8, 파티클, 속도 레벨 |
| 2048 | `2048.html` | 타임어택 모드, 업적 9개, 5단 되돌리기, 힌트 |
| 타이핑 연습 | `type.html` | WPM·정확도·일관성, 한/영 IME, WPM 그래프 |
| 무한 러너 | `runner.html` | 더블점프·슬라이드, 고스트, 콤보, 스테이지 4개 |
| 벽돌 깨기 | `breakout.html` | 벽돌 5종, 파워업 6종, 레이저, 레벨 무한 생성 |

## 기술 스택

- **렌더링**: Canvas 2D API + requestAnimationFrame
- **사운드**: Web Audio API (8비트 효과음)
- **저장**: localStorage (최고 점수, 업적, 고스트)
- **한글 입력**: IME compositionstart/update/end 이벤트 처리
- **스타일**: CSS Variables, DM Mono 폰트

## 디자인 시스템

```css
--bg:     #07071A
--cyan:   #00D4FF
--purple: #8B5CF6
--font:   'DM Mono'
```

## 로컬 실행

별도 서버 불필요. `index.html`을 브라우저에서 열면 됩니다.

```bash
# 간단히 열기
open index.html
```

## 구조

```
├── index.html      # 포트폴리오 메인 (i18n 한/영, 컨택트 폼)
├── snake.html
├── 2048.html
├── type.html
├── runner.html
└── breakout.html
```

---

&copy; halfstone.Kim

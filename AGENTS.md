# AGENTS.md — cpp-study

## 한 줄 정의

**C++ 학습용 단일 HTML 가이드 사전** repo.  
`icon-format-guide`의 “한눈에 예쁜 설명서” 포맷 + **왼쪽 번호 목차** UI.

- GitHub: https://github.com/Ageia/cpp-study  
- Pages: https://ageia.github.io/cpp-study/  
- 로컬: `C:\Users\User\Desktop\cpp-study`  
- **분리:** `icon-format-guide` 와 섞지 말 것  
- **언리얼/UE 엔진 내용 금지** — 별도 repo. 이 저장소는 **C++ 언어**만.

## 핵심 파일

| 파일 | 역할 |
|------|------|
| **`index.html`** | 메인 산출물. 왼쪽 번호 목차 + 주제 패널 + 용어 사전 (한국어, 다크 UI) |
| `src/` | 가이드 예시와 맞춘 참고 코드 (선택, 숙제 아님) |
| `notes/` | 사용자 학습 메모 |
| `docs/TODO.md` | 보강 아이디어·학습 백로그 · 심화 계획 |
| `README.md` | 사람용 소개·링크 |

빌드 도구 없음. **정적 HTML** push → Pages.

## 콘텐츠 컨벤션

- 언어: **한국어**. 쉬운 비유 우선, 전문 용어는 풀어서.
- 구조: **왼쪽 번호 목차** + 오른쪽 주제 패널 + 카드 + 표 + 짧은 코드 + 사전 + FAQ.
- 현재 대략 **01–21** (메인 + 사전·활용). 심화는 **22+ 그룹** (`docs/TODO.md` 참고).
- 초보/중급/고급 라벨 대신 **학습 요소 번호**.
- 코드는 **최소 예시**. 장황한 프로젝트 코드는 `src/`로.
- **학습 톤:** 퀴즈·미션 금지. **상황 → 짧은 코드 → 어디에 쓰이나**.
- **시각화 우선:** 인라인 SVG · CSS 애니메이션. `prefers-reduced-motion` 존중.
- **깊이 조절:** 메인 = 개념+쓰임. 심화(기계어·가상메모리·엔디안·vtable 등)는
  메인 패널에 우겨 넣지 말고 **심화 번호 그룹** 또는 접기 카드로 분리.
- **약자:** 첫 등장만 풀네임 (STL, RAII…).
- 게임 **비유**는 OK. **언리얼 API·UObject·UE 문서** 금지.
- 한/영 토글은 나중. 지금은 한국어만.

---

## 다이어그램 · 레이아웃 규칙 (필수 — 반복 실수 방지)

**왜 반복됐나:** viewBox/좌표를 감으로 잡고 라벨을 박스 밖·좁은 칸에 넣음  
→ 잘림(엔디안 MSB), 겹침, 긴 문자열(`0b01111000`) 넘침.  
추가로 `.card + .card { margin-top }` 이 **grid 안 오른쪽 카드만** 내려가게 만듦.

### 선택 기준

| 내용 | 수단 |
|------|------|
| 카드·칩·표·같은 폭 행·긴 모노 텍스트 | **HTML + CSS grid/flex** (`.guide-viz`, `.base-*`) |
| 화살표·스택/힙·연결선·애니메이션 path | **인라인 SVG** (`.guide-svg` / 기존 `*-svg`) |

### SVG 체크리스트 (추가·수정 직후 필수)

1. **viewBox 검산:** 모든 요소의 `x+width`, `y+height`, `text`의 `y`(+font 여유) ≤ viewBox. **여백 ≥ 12**.
2. **배지/캡션을 셀 아래에 붙일 때** viewBox 높이를 **먼저** 늘린 뒤 좌표 배치. 높이 고정 후 아래로 밀어 넣지 말 것.
3. `text-anchor="middle"` → `x` = 해당 셀 중심. 좌우 셀 폭·간격을 **공식**으로 통일 (난수 좌표 금지).
4. 긴 문자열은 SVG `<text>` 대신 HTML, 또는 박스 폭·font-size를 문자 수에 맞게.
5. CSS: `display:block; width:100%; max-width:…; height:auto; margin:0 auto`. 컨테이너 `overflow-x:auto`.
6. 공통 래퍼 우선: `.guide-viz` + (SVG면) `.guide-svg`.

### CSS 레이아웃 체크

1. **grid/split 안 `.card`:** `margin-top: 0` 유지 (전역 `.card + .card`가 우측만 밀지 않게 — 이미 예외 있음, 깨지 말 것).
2. grid 자식: `min-width: 0` (카드에 적용됨).
3. 카드 **안** `.table-wrap`: 이중 그림자 없음 (`box-shadow: none`).
4. 새 다이어그램 전용 CSS를 추가할 때 기존 `.endian-viz` 등과 **중복 정의로 덮어쓰지 말 것**.

### 심화 추가 시

1. `docs/TODO.md` 심화 후보에서 주제 고르기  
2. 사이드바 **심화** 그룹 + 번호 (22…)  
3. 패널 상단에 관련 메인 번호 링크  
4. 메인 쪽에는 한 줄 “심화 →” 만 (선택)  
5. 같은 톤: 상황 → 코드 → 쓰임 + 가능하면 시각화  
6. **위 SVG/CSS 체크리스트 통과 후** 커밋  

## 새 세션 체크리스트

1. `AGENTS.md` + `docs/TODO.md` + `README.md`  
2. `index.html` 읽고 보강 포인트 확인  
3. 다이어그램·grid 카드 수정 시 **위 레이아웃 규칙** 적용  
4. 수정 후 `main` push → Pages 1~2분  
5. TODO 체크 갱신  

## 하지 말 것

- 가이드를 코드 덤프 저장소로만 바꾸지 말 것  
- PAT 커밋 금지  
- `icon-format-guide` / **언리얼 전용 가이드**와 내용 병합 금지  
- raw `new` 남용을 초보 섹션에서 권장하지 말 것  
- 퀴즈/숙제형 미션 UI 금지  

## 배포

- `origin` → `https://github.com/Ageia/cpp-study.git`  
- 브랜치 `main`, Pages: `/` (root `index.html`)

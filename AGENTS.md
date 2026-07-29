# AGENTS.md — cpp-study

## 한 줄 정의

**C++ 학습용 단일 HTML 가이드 사전** repo.  
`icon-format-guide`의 “한눈에 예쁜 설명서” 포맷 + **왼쪽 번호 목차** UI.

- GitHub: https://github.com/Ageia/cpp-study  
- Pages: https://ageia.github.io/cpp-study/  
- 로컬: `C:\Users\User\Desktop\cpp-study`  
- **분리:** `icon-format-guide` (게임/UE 가이드 허브)와 섞지 말 것

## 핵심 파일

| 파일 | 역할 |
|------|------|
| **`index.html`** | 메인 산출물. 왼쪽 01–20 목차 + 주제 패널 + 용어 사전 (한국어, 다크 UI) |
| `src/` | 가이드 예시와 맞춘 참고 코드 (선택, 숙제 아님) |
| `notes/` | 사용자 학습 메모 |
| `docs/TODO.md` | 보강 아이디어·학습 백로그 |
| `README.md` | 사람용 소개·링크 |

빌드 도구 없음. **정적 HTML** push → Pages.

## 콘텐츠 컨벤션

- 언어: **한국어**. 쉬운 비유 우선, 전문 용어는 풀어서.
- 구조: **왼쪽 번호 목차(01–20)** + 오른쪽 주제 패널 + 카드 + 표 + 짧은 코드 + 사전 + FAQ.
- 초보/중급/고급 라벨 대신 **학습 요소 번호** (변수, 포인터, STL…).
- 한꺼번에 스크롤 장문보다 번호 패널로 분리. 상세 풀이는 해당 번호에 채움.
- 코드는 **최소 예시**. 장황한 프로젝트 코드는 `src/`로.
- **학습 톤:** 퀴즈·미션·“직접 구현해 보세요” 강요 금지.
  대신 **상황 → 짧은 코드 → 어디에 쓰이나** 패턴.
- 한/영 토글은 나중. 지금은 한국어만.

## 새 세션 체크리스트

1. `AGENTS.md` + `docs/TODO.md` + `README.md`  
2. `index.html` 읽고 보강 포인트 확인  
3. 수정 후 `main` push → Pages 1~2분  
4. TODO 체크 갱신  

## 하지 말 것

- 가이드를 “코드 덤프 저장소”로만 바꾸지 말 것 (설명서가 본문)  
- PAT 커밋 금지  
- `icon-format-guide`와 내용 병합 금지  
- raw `new` 남용을 초보 섹션에서 권장하지 말 것 (중급 주의 → 고급 스마트 포인터)
- 퀴즈/숙제형 미션 UI 넣지 말 것 (활용 예시·설명 중심)

## 배포

- `origin` → `https://github.com/Ageia/cpp-study.git`  
- 브랜치 `main`, Pages: `/` (root `index.html`)

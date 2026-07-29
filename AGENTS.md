# AGENTS.md — cpp-study

## 한 줄 정의

**C++ 초보→중급→고급 학습용 단일 HTML 가이드** repo.  
`icon-format-guide`의 “한눈에 예쁜 설명서” 포맷을 C++에 적용.

- GitHub: https://github.com/Ageia/cpp-study  
- Pages: https://ageia.github.io/cpp-study/  
- 로컬: `C:\Users\User\Desktop\cpp-study`  
- **분리:** `icon-format-guide` (게임/UE 가이드 허브)와 섞지 말 것

## 핵심 파일

| 파일 | 역할 |
|------|------|
| **`index.html`** | 메인 산출물. 단계별 C++ 가이드 (한국어, 다크 UI) |
| `src/` | 가이드와 맞춘 연습 코드 (선택) |
| `notes/` | 사용자 학습 메모 |
| `docs/TODO.md` | 보강 아이디어·학습 백로그 |
| `README.md` | 사람용 소개·링크 |

빌드 도구 없음. **정적 HTML** push → Pages.

## 콘텐츠 컨벤션

- 언어: **한국어**. 쉬운 비유 우선, 전문 용어는 풀어서.
- 구조: 목차 + 카드 + 표 + 짧은 코드 + FAQ (format-guide 톤).
- 단계 색: 초보 mint / 중급 cyan / 고급 purple.
- 코드는 **최소 예시**. 장황한 프로젝트 코드는 `src/`로.
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

## 배포

- `origin` → `https://github.com/Ageia/cpp-study.git`  
- 브랜치 `main`, Pages: `/` (root `index.html`)

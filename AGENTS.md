# AGENTS.md — cpp-study

새 세션·AI가 **채팅 없이** 이 repo만으로 C++ 공부 작업을 이어갈 때 읽는 문서입니다.

## 한 줄 정의

개인 **C++ / 컴퓨터 기초 학습** repo.  
예제 코드(`src/`), 메모(`notes/`), 백로그(`docs/TODO.md`).

- GitHub: https://github.com/Ageia/cpp-study  
- 로컬: `C:\Users\User\Desktop\cpp-study`  
- **관련 없음:** `icon-format-guide` (가이드 허브) — 섞지 말 것

## 새 세션 체크리스트

1. `AGENTS.md` + `docs/TODO.md` + `README.md`  
2. `git log -10 --oneline` / `git status`  
3. `src/`, `notes/` 현재 내용 확인  
4. 작업 후 커밋·push (`main`)

## 폴더 규칙

| 경로 | 용도 |
|------|------|
| `src/` | `.cpp` / `.h` 연습·예제. 작은 프로그램 단위 파일 또는 하위 폴더 |
| `notes/` | 개념 정리 마크다운 |
| `docs/TODO.md` | 하고 싶은 학습·연습 백로그 |
| 루트 | README, AGENTS, `.gitignore` 정도만 |

## 컨벤션

- 언어: 메모·주석은 **한국어** 가능. 코드 식별자는 관례적으로 영어.
- 커밋: 짧게 (`Add hello example`, `notes: pointers summary`).
- 빌드: 우선 **단일 파일 g++/cl** 로 돌아가게. 큰 CMake는 필요할 때만.
- 비밀·과제 답안 무단 공개 주의.

## 하지 말 것

- `icon-format-guide` 내용과 병합하지 말 것  
- PAT/비밀번호 커밋 금지  
- `src/`에 빌드 산출물(`.exe`, `.obj`, `.pdb`) 올리지 말 것 (`.gitignore` 참고)

## 백로그

소스 오브 트루스: **`docs/TODO.md`** (Now ≤ 3).

## 배포

- 원격: `origin` → `https://github.com/Ageia/cpp-study.git`  
- 브랜치: `main`  
- Pages 없음 (학습 repo). 필요 시 나중에.

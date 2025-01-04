# update-indexes.yml 요구사항

## 1. 현재 상황
1-1. 현재 content-productin, foreign-lang, webdev 폴더가 있음
1-2. 각 폴더 안에 index.md 파일이 있음

## 2. 앞으로 일어날 일
2-1. 각 폴더 안에 20250101.md 와 같은 날짜 형식의 파일이 추가 될 것임

## 3. 내가 원하는 것
3-1. 각 폴더 안에 20250101.md 와 같은 날짜 형식의 파일이 추가 될 때마다 index.md 파일이 업데이트되도록 할 것
3-2. 현재 파일의 형태는 그대로 유지할 것
3-3. h1구조를 찾아서 그 바로 아래에 h3형식으로 ### Last updated: 2025-01-01 12:00:00 이렇게 추가할 것(한국 시간으로)
3-4. 3-3 바로 아래에 h2형식으로 ## 2025-01-01과 같이 날짜 형식의 파일이름을 넣고, 그 파일을 링크할 것
3-5. 그 아래의 기존 구조들은 그대로 유지할 것.
3-6. 루트의 README.md파일에도 ### Last updated: 2025-01-01 12:00:00 이렇게 추가할 것(한국 시간으로)

---
아래의 내용은 모두 폐기했음 orz

# GitHub Repository 구조 요구사항

## 중요한 경로들

1. **로컬 경로**
   - 옵시디언 볼트 루트: `/d/icloud/iCloudDrive/iCloud~md~obsidian/redout`
   - 실제 작업 폴더: `/d/icloud/iCloudDrive/iCloud~md~obsidian/redout/learn-slowly/withai`

2. **GitHub 경로**
   - Repository URL: `https://github.com/learn-slowly/withai`
   - 올바른 구조: `https://github.com/learn-slowly/withai/` (루트에 파일들이 있어야 함)
   - 잘못된 구조: `https://github.com/learn-slowly/withai/learn-slowly/withai/` (중복된 경로)

## 구조 관리 방법

1. **Git 명령어 실행 위치**
   - 항상 볼트 루트(`/d/icloud/iCloudDrive/iCloud~md~obsidian/redout`)에서 실행
   - 절대 `learn-slowly/withai` 폴더 내에서 git 초기화하지 않기

2. **파일 구조 확인**
   ```bash
   # GitHub에 push 하기 전에 항상 확인
   git status
   git ls-files  # 추적 중인 파일 목록 확인
   ```

3. **문제 발생 시 체크리스트**
   - [ ] git 명령어를 볼트 루트에서 실행했는가?
   - [ ] `.gitignore` 설정이 올바른가?
   - [ ] GitHub repository에 중복된 경로가 없는가?

## 주의사항

1. **절대 하지 말아야 할 것**
   - `learn-slowly/withai` 폴더 내에서 git 초기화
   - GitHub repository 내에 `learn-slowly/withai` 경로 생성

2. **항상 확인해야 할 것**
   - push 전에 `git status`로 파일 경로 확인
   - GitHub repository의 파일 구조 확인

## 문제 해결 방법

만약 중복 구조가 발생했다면:
1. GitHub repository 초기화
2. 로컬에서 올바른 구조로 다시 push
3. 이 가이드 문서 참고하여 재발 방지 

# restructure.yml 요구사항

## 1. 내 옵시디언 볼트 위치
d/icloud/iCloudDrive/iCloud~md~obsidian/redout

## 2. 내 github 위치
D:\icloud\iCloudDrive\iCloud~md~obsidian\redout\learn-slowly\withai

## 3. 발생하는 문제
https://github.com/learn-slowly/withai/learn-slowly/withai/이렇게 중복된 구조의 폴더가 생성되고,  D:\icloud\iCloudDrive\iCloud~md~obsidian\redout\learn-slowly\withai이 폴더의 내용들이 중복 폴더 안으로 들어감

## 4. 원하는 것
4-1. 옵시디언 볼트 위치에서 github repository를 만든다. 왜냐하면 obsidian-git 플러그인을 사용하기 위해서이다.
4-2. 하지만 D:\icloud\iCloudDrive\iCloud~md~obsidian\redout\learn-slowly\withai 이 폴더 이외의 다른 폴더의 파일들은 싱크하지 말 것
4-3. D:\icloud\iCloudDrive\iCloud~md~obsidian\redout\learn-slowly\withai 이 로컬폴더가, https://github.com/learn-slowly/withai/ 이 github repository와 동기화되도록 할 것
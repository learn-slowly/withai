# GitHub Repository 구조 가이드

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
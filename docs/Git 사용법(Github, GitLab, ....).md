# GIT 설치
- 윈도우
```
winget install -e --id Git.Git
```
- 리눅스
```
sudo apt update
sudo apt install -y git
```
- 리눅스-최신버전
```
sudo add-apt-repository ppa:git-core/ppa
sudo apt update && sudo apt install -y git
```
- 깃 버전확인(윈도우,리눅스)
```
git --version
```

# 기본 사용 명령어
## git init
- 해당 저장소를 git 저장소로 선언하는 명령어
- 기본적으로 main 브랜치가 생성됨

## git status
- 현재 작업중인 브랜치 상태 확인
  (어떤 브랜치인지, commit 할게 있는지 등)

## git config
- 저장소 초기 설정
- 변경 사항을 누가 입력했는지, 어떻게 연락할지에 대한 정보 입력
```
git config user.name asd
git config user.email asd@asd.com
```
- git config -list를 통해 정보 확인 가능

## git add
- 변경 사항을 추가
- git add '파일명' or git add . 사용
	- working directory(local): 개인 코드 작성
	- staging 영역 : git add를 통해 수정된 코드를 이 영역에 업로드
	- repository : git commit & push를 통해 staging 영역의 최종본을 업로드

## git commit
- git add 명령어로 추가된 변경사항들에 대해 기록
```
git commit -m "기록할내용"
```

## git reset
- 이전 기록 상태로 돌아가기 - 이력제거
- 모두 직전 상태로 : git reset --hard
## git push
- staging 영역의 내용과 커밋을 원격 저장소에 업로드

## git pull
- 원격 저장소의 내용 내려받기
- 원격 저장소와 내 저장소를 동일한 상태로 만들기 위해 사용 - main 브랜치에 변경사항이 있는 경우 git pull을 먼저 한 다음 변경사항 작성한 뒤 commit & push 해야 오류 발생 X

## git clone

## git merge

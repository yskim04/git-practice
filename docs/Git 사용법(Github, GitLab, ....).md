# Git 사용법

## 📌 목차
- [Git 사용법](#git-사용법)
	- [📌 목차](#-목차)
	- [🛠 Git 설치](#-git-설치)
		- [💻 윈도우](#-윈도우)
		- [🐧 리눅스](#-리눅스)
		- [🔄 최신 버전 설치 (리눅스)](#-최신-버전-설치-리눅스)
		- [🔍 깃 버전 확인](#-깃-버전-확인)
	- [📖 Git 기본 개념](#-git-기본-개념)
	- [🚀 기본 사용 명령어](#-기본-사용-명령어)
		- [🏁 git init (저장소 초기화)](#-git-init-저장소-초기화)
		- [🔄 git status (현재 상태 확인)](#-git-status-현재-상태-확인)
		- [🔧 git config (사용자 설정)](#-git-config-사용자-설정)
		- [➕ git add (변경 사항 추가)](#-git-add-변경-사항-추가)
		- [💾 git commit (변경 사항 저장)](#-git-commit-변경-사항-저장)
		- [⏪ git reset (이전 상태로 되돌리기)](#-git-reset-이전-상태로-되돌리기)
		- [⬆ git push (원격 저장소로 업로드)](#-git-push-원격-저장소로-업로드)
		- [⬇ git pull (원격 저장소에서 최신 내용 가져오기)](#-git-pull-원격-저장소에서-최신-내용-가져오기)
		- [📥 git clone (원격 저장소 복제)](#-git-clone-원격-저장소-복제)
		- [🔗 git merge (브랜치 병합)](#-git-merge-브랜치-병합)
	- [🌿 Branch 관리 및 협업](#-branch-관리-및-협업)
		- [브랜치 생성과 전환](#브랜치-생성과-전환)
		- [병합 후 브랜치 삭제](#병합-후-브랜치-삭제)
	- [⚠ Git 충돌 해결](#-git-충돌-해결)
	- [📚 참고 자료 및 추가 학습](#-참고-자료-및-추가-학습)
	- [🔗 GitHub Git Cheat Sheet 바로가기](#-github-git-cheat-sheet-바로가기)

---

## 🛠 Git 설치

### 💻 윈도우
```bash
winget install -e --id Git.Git
```

### 🐧 리눅스
```bash
sudo apt update
sudo apt install -y git
```

### 🔄 최신 버전 설치 (리눅스)
```bash
sudo add-apt-repository ppa:git-core/ppa
sudo apt update && sudo apt install -y git
```

### 🔍 깃 버전 확인
```bash
git --version
```

---

## 📖 Git 기본 개념
Git은 파일의 변경 이력을 관리하는 **분산형 버전 관리 시스템(DVCS)** 입니다. 

- **📂 로컬 저장소(Local Repository):** 개발자가 자신의 컴퓨터에서 작업하는 공간.
  
- **☁ 원격 저장소(Remote Repository):** GitHub, GitLab 등 클라우드 저장소에 위치한 저장소.
- **📌 스테이징 영역(Staging Area):** 커밋을 하기 전에 변경된 파일을 잠시 저장하는 공간.
- **🌿 브랜치(Branch):** 하나의 독립적인 작업 흐름을 나타내며, 기능 개발을 위한 필수적인 요소.

---

## 🚀 기본 사용 명령어

### 🏁 git init (저장소 초기화)
**사용 시점:** 새로운 프로젝트를 Git으로 관리하고 싶을 때.

```bash
git init
```

**설명:** 해당 디렉터리를 Git 저장소로 초기화하고, `.git` 디렉터리를 생성합니다.

### 🔄 git status (현재 상태 확인)
**사용 시점:** 파일이 변경되었는지 확인할 때

```bash
git status
```

**설명:** 작업 디렉토리의 변경 사항과 스테이징 영역에 있는 파일을 확인할 수 있습니다.

### 🔧 git config (사용자 설정)
**사용 시점:** Git을 처음 설치했을 때.

```bash
git config --global user.name "사용자이름"
git config --global user.email "user@example.com"
```

**설명:** Git에서 커밋할 때 기록될 사용자 정보를 설정합니다.

### ➕ git add (변경 사항 추가)
**사용 시점:** 파일 변경 후 커밋을 준비할 때.

```bash
git add 파일명  # 특정 파일 추가
git add .       # 모든 변경 사항 추가
```

**설명:** 작업한 변경 사항을 스테이징 영역에 추가합니다.

### 💾 git commit (변경 사항 저장)
**사용 시점:** 변경된 내용을 기록으로 남길 때.

```bash
git commit -m "변경 내용"
```

**설명:** 변경된 파일을 커밋하여 버전 기록을 생성합니다.

### ⏪ git reset (이전 상태로 되돌리기)
**사용 시점:** 최근 커밋을 취소하고 싶을 때.

```bash
git reset --hard 이전커밋ID
```

**설명:** 특정 커밋으로 돌아가며, `--hard` 옵션을 사용하면 파일도 해당 시점으로 되돌립니다.

### ⬆ git push (원격 저장소로 업로드)
**사용 시점:** 로컬에서 작업한 내용을 원격 저장소에 공유할 때.

```bash
git push origin 브랜치이름
```

**설명:** 원격 저장소에 로컬에서 작업한 내용을 업로드합니다.

### ⬇ git pull (원격 저장소에서 최신 내용 가져오기)
**사용 시점:** 다른 개발자가 작업한 내용을 가져오고 싶을 때.

```bash
git pull origin main
```

**설명:** 원격 저장소의 최신 변경 사항을 가져와 로컬 브랜치와 병합합니다.

### 📥 git clone (원격 저장소 복제)
**사용 시점:** 프로젝트를 처음 받을 때.

```bash
git clone 저장소URL
```

**설명:** 원격 저장소의 코드를 로컬에 복사합니다.

### 🔗 git merge (브랜치 병합)
**사용 시점:** 기능 개발이 완료된 브랜치를 main 브랜치에 반영할 때.

```bash
git merge feature-branch
```

**설명:** 다른 브랜치의 변경 사항을 현재 브랜치에 병합합니다.

---

## 🌿 Branch 관리 및 협업

### 브랜치 생성과 전환
```bash
git branch feature-xxx  # 브랜치 생성
git switch feature-xxx  # 브랜치 전환
```

### 병합 후 브랜치 삭제
```bash
git branch -d feature-xxx
```

---

## ⚠ Git 충돌 해결
병합(Merge) 과정에서 충돌이 발생하면 아래 단계를 따라 해결합니다.

1. 충돌이 발생한 파일을 확인합니다.
```bash
git status
```
2. 파일을 열어 수동으로 충돌을 해결합니다.
3. 변경 사항을 스테이징합니다.
```bash
git add 충돌해결된파일
```
4. 새로운 커밋을 생성합니다.
```bash
git commit -m "충돌 해결"
```

---

## 📚 참고 자료 및 추가 학습

- **Git 공식 문서:** [https://git-scm.com/doc](https://git-scm.com/doc)
- **Pro Git Book (한글판):** [https://git-scm.com/book/ko/v2](https://git-scm.com/book/ko/v2)

---

## 🔗 GitHub Git Cheat Sheet 바로가기
👉 [Git Cheat Sheet-KR](./Git%20Cheat%20Sheet-KR.md)


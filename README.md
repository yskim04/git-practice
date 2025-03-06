# Git 학습용 Repository

## 📌 레포지토리 구조

```
git-learning-repo/
├── README.md             # 전체 가이드 및 레포지토리 사용법 안내
├── docs/                 # Git 관련 문서 모음
│   ├── Git 사용법(Github, GitLab, ....).md # Git의 기본 개념 및 주요 명령어 설명
│   ├── Git Cheat Sheet-KR.md  # Git 주요 명령어 요약 (치트시트)
│   ├── 마크다운사용법.md # Markdown 문법 안내 및 예시
├── exercises/            # Git 실습용 폴더
│   ├── README.md         # 실습 가이드
│   ├── [사용자 폴더]      # 개인별 실습 폴더
```

## 📚 사용법 안내

### 1️⃣ 레포지토리 클론하기
```bash
git clone https://github.com/yskim04/git-practice.git
cd git-practice
```

### 2️⃣ `docs` 폴더에서 개념 학습하기
`docs/` 폴더에는 Git의 개념을 정리한 문서가 포함되어 있습니다. 먼저 개념을 학습한 후 실습을 진행.

### 3️⃣ `exercises` 폴더에서 실습 진행하기
1. `exercises` 폴더로 이동합니다.
   ```bash
   cd exercises
   ```
2. 자신의 폴더를 생성합니다.
   ```bash
   mkdir my-folder  # 예: alice
   cd my-folder
   ```
3. `README.md` 파일을 생성하고 내용을 작성한 후, Git 명령어를 사용하여 스테이징, 커밋, 푸시합니다.
4. 실습 완료 후 `main` 브랜치로 병합하세요.

자세한 실습 방법은 [`exercises/README.md`](./exercises/README.md)에서 확인할 수 있습니다.

---

## 🔥 Git 학습을 위한 필수 명령어

### 저장소 초기화
```bash
git init
```

### 변경 사항 확인
```bash
git status
```

### 파일 추가 및 커밋
```bash
git add .
git commit -m "설명 추가"
```

### 원격 저장소와 연결 및 푸시
```bash
git remote add origin <원격 저장소 URL>
git push -u origin main
```

### 최신 변경 사항 가져오기
```bash
git pull origin main
```

### 브랜치 관리
```bash
git branch feature-branch  # 브랜치 생성
git switch feature-branch  # 브랜치 이동
git merge feature-branch   # 브랜치 병합
git branch -d feature-branch  # 브랜치 삭제
```

---

## 📎 참고 자료
- [Git 공식 문서](https://git-scm.com/doc)
- [Pro Git Book (한글판)](https://git-scm.com/book/ko/v2)
- [GitHub Git Cheat Sheet](./docs/git-cheat-sheet.md) 🔗

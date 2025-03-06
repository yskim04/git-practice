# Git 실습: Commit, Push, Pull, Branch 관리

**학습 목표 : Git을 사용하여 브랜치를 생성하고, 변경 사항을 커밋한 후, 원격 저장소에 푸시한 뒤 병합(Merge)하는 과정 연습**

---

## 📌 실습 목표
- `exercise` 폴더 안에 개인 폴더를 생성하고, `README.md` 파일을 추가하기
- 자신만의 브랜치를 생성하고, 변경 사항을 커밋하고 푸시하기
- `main` 브랜치로 병합(Merge)하기

---

## 📖 실습 순서

### 1️⃣ `exercise` 폴더에 개인 폴더 생성하기

먼저 연습용 git repository를 클론합니다.
```bash
git clone https://github.com/yskim04/git-practice.git
```
`exercise` 폴더로 이동한 후, 자신의 이름(또는 GitHub ID)으로 된 폴더를 만듭니다.
```bash
cd exercises  # exercises 폴더로 이동
mkdir my-folder  # 본인의 폴더 생성 (예: 이름이 "alice"라면 "alice" 폴더 생성)
cd my-folder
```

---

### 2️⃣ `README.md` 파일 생성 및 수정

해당 폴더 안에서 `README.md` 파일을 생성한 후 vscode 혹은 vim, nano 등 텍스트 에디터를 활용하여 내용을 추가합니다.

예시 내용:

```markdown
# My Git Exercise
이 파일은 Git 실습을 위한 파일입니다.
```

---

### 3️⃣ 새로운 브랜치 생성 및 전환

작업을 시작하기 전에, **main 브랜치에서 작업하지 않고, 개인 브랜치에서 진행하는 것이 중요합니다**.

먼저, 현재 브랜치를 확인하세요.

```bash
git branch
```

새로운 브랜치를 생성하고 해당 브랜치로 이동합니다.

```bash
git branch 'my-branch'
git switch my-branch

# 두 명령어 한번에 합치면
git switch -c my-branch
```

위에서 `my-branch`는 본인의 브랜치 이름입니다.

---

### 4️⃣ 변경 사항을 스테이징 및 커밋하기

이제 변경한 파일을 Git에 추가하고, 커밋합니다.

```bash
git add README.md  # 파일을 스테이징

#특정 파일이 아니라 변경사항을 모두 업로드하고 싶다면 git add . 명령어 사용

git commit -m "Add personal README.md file"  # 커밋 메시지 작성
```

---

### 5️⃣ 원격 저장소에 브랜치 푸시하기

이제 작업한 내용을 원격 저장소(GitHub, GitLab 등)로 푸시합니다.

```bash
git push origin my-branch
```

이제 원격 저장소(GitHub)의 브랜치 목록을 보면, `my-branch`가 추가된 것을 확인할 수 있습니다.

---

### 6️⃣ `main` 브랜치로 돌아가기

이제, `main` 브랜치로 이동합니다.

```bash
git checkout main  # 또는 git switch main
```

원격 저장소에서 최신 변경 사항을 가져옵니다.

```bash
# 원격 저장소와 로컬 저장소의 환경이 같지 않다면 이후 단계에서 오류 발생
git pull origin main
```

---

### 7️⃣ `main` 브랜치에 병합(Merge)하기

이제 `main` 브랜치에서 방금 작업한 `my-branch`를 병합합니다.

```bash
git merge my-branch
```

변경된 main 브랜치의 내용을 원격저장소에 다시 반영합니다.
```bash
git push origin main
```

⚠️ **만약 충돌(Conflict)이 발생하면?**
- `git status`로 어떤 파일에서 충돌이 발생했는지 확인.
- 충돌을 해결한 후, 변경 사항을 스테이징하고 다시 커밋.

```bash
git add .
git commit -m "Resolve merge conflict"
```

---

### 8️⃣ 사용하지 않는 브랜치 삭제하기

병합이 완료되었으면, 더 이상 필요 없는 브랜치를 삭제할 수 있습니다.

```bash
git branch -d my-branch
```

그리고 원격 저장소에서도 브랜치를 삭제하려면:

```bash
git push origin --delete my-branch
```

---

## 🎯 실습 완료 후 확인해야 할 사항
✅ `exercises/my-folder/README.md` 파일이 존재하는가?  
✅ `git log`를 실행했을 때, 자신의 커밋이 있는가?  
✅ `git branch`를 실행했을 때, 작업한 브랜치가 삭제되었는가?  

이 모든 과정을 완료했다면, Git을 활용한 **브랜치 생성, 커밋, 푸시, 병합 과정**을 성공적으로 수행한 것입니다! 🎉

---

## 📚 추가 학습 자료
- [Git 공식 문서](https://git-scm.com/doc)
- [Pro Git Book (한글판)](https://git-scm.com/book/ko/v2)
- [GitHub Git Cheat Sheet](../GitHub%20Git%20Cheat%20Sheet.md) 🔗 (이 파일에서 Git 명령어를 빠르게 확인)

# GitHub 사용 방법 강의자료

## Git 기초

### Git이란 무엇인가요?
Git은 분산 버전 관리 시스템입니다. 코드 변경 이력을 기록하고, 여러 명의 개발자가 협업할 수 있도록 도와줍니다. Git을 사용하면 파일의 이전 버전으로 돌아가거나, 변경 사항을 추적하고, 병합 작업을 처리할 수 있습니다.

---

### Git 기본 명령어

#### 1. git init
새로운 Git 리포지토리를 초기화할 때 사용합니다.

```bash
git init
```

#### 2. git clone
원격 리포지토리를 로컬로 복제할 때 사용합니다.

```bash
git clone https://github.com/사용자이름/레포지토리이름.git
```

#### 3. git add
변경된 파일을 스테이징 영역에 추가할 때 사용합니다.

```bash
git add 파일이름
```

#### 4. git commit
스테이징된 파일을 커밋하고 변경 이력을 저장합니다.

```bash
git commit -m "커밋 메시지"
```

#### 5. git push
로컬에서 커밋한 내용을 원격 리포지토리로 푸시합니다.

```bash
git push origin 브랜치이름
```

#### 6. git pull
원격 리포지토리의 변경 사항을 로컬 리포지토리로 가져옵니다.

```bash
git pull origin 브랜치이름
```

---


## 1. GitHub 계정 가입
GitHub 계정을 만들려면 다음 단계를 따릅니다:
1. [GitHub 홈페이지](https://github.com)로 이동합니다.
2. 'Sign up' 버튼을 클릭합니다.
3. 이메일, 비밀번호, 사용자 이름을 입력하고 'Create Account' 버튼을 클릭합니다.
4. 이메일 인증 후 계정이 활성화됩니다.

---

## 2. 레포지토리 포크(Fork)
포크는 다른 사람의 레포지토리를 복사하여 자신의 GitHub 계정에서 작업할 수 있게 해주는 기능입니다.

1. 포크할 레포지토리로 이동합니다. (https://github.com/yangsancenter/ys)
2. 우측 상단에 있는 'Fork' 버튼을 클릭합니다.
3. 자신의 계정으로 복사된 레포지토리를 확인합니다.

![Fork 과정 이미지 삽입 예정]

---

## 3. Personal Access Token 생성

GitHub에서 `git push`를 시도할 때 "Invalid username or password" 오류가 발생하는 이유는 인증 문제와 관련이 있습니다. GitHub은 이제 사용자명과 비밀번호 대신 **Personal Access Token (PAT)**을 사용해야 합니다. 아래는 이 문제를 해결하는 방법입니다.

1. [GitHub](https://github.com)에 로그인합니다.
2. 우측 상단의 프로필 아이콘을 클릭하고, **Settings**로 이동합니다.
3. 좌측 메뉴에서 **Developer settings** → **Personal access tokens** → **Tokens (classic)** 로 이동합니다.
4. **Generate new token** → **Generate new token (classic)** 버튼을 클릭하여 새 토큰을 생성합니다.
5. 토큰에 필요한 권한(예: `repo` 권한)을 선택하고, 토큰을 생성합니다.
6. 생성된 토큰을 복사합니다. 이 토큰은 다시 확인할 수 없으니 안전하게 저장해 두세요.

### 3.1 Git Remote URL 업데이트

기존 GitHub 원격 URL을 새로 생성한 토큰을 사용하도록 변경합니다.

```bash
git remote set-url origin https://<your_token>@github.com/yangsancenter/ys.git
```

여기서 <your_token>은 새로 생성한 Personal Access Token으로 교체해야 합니다.

---

## 4. GitHub Pages를 통한 HTML 배포
GitHub Pages를 사용하여 기존 레포지토리에서 웹 페이지를 배포할 수 있습니다.

1. 본인의 레포지토리에서 'Settings'로 이동합니다.
2. 좌측 메뉴에서 'Pages'를 클릭합니다.
3. 'Branch' 섹션에서 'main' 또는 배포할 브랜치를 선택하고 'Save'를 클릭합니다.
4. 설정이 완료되면, 배포된 웹 페이지 링크를 확인할 수 있습니다.

---

## 5. 배포된 HTML 확인
GitHub Pages에서 배포된 HTML 페이지는 설정 후 약 1-2분 내에 활성화됩니다.

1. 페이지 URL을 클릭하여 정상적으로 배포되었는지 확인합니다.
2. URL 형식: `https://사용자이름.github.io/레포지토리이름`
https://yangsancenter.github.io/ys

ref : https://docs.github.com/ko/pages
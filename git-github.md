# 1. Git / GitHub

## Git 과 GitHub를 사용해야하는 이유
- **Git**은 **버전관리** 시스템이며(내컴퓨터에서), **GitHub**는 Git으로 관리하는 **저장소를 온라인**에 올려두고 공유하는 서비스(원격저장소)

### 버전관리란?
- 파일,코드변경 이력을 체계적으로 기록&관리 (언제,누가,무엇을 바꿨는지 알수있고, 필요시 과거로 되돌리기 가능)

### 버전관리가 필요한 이유
- 변경 이력 **추적**, 실수 **복구**, 여러사람이 **충돌 없이 협업**

## Git과 GitHub의 차이

| | Git | GitHub |
|---|---|---|
| 정체 | **버전 관리**를 위한 도구 (내 컴퓨터) | Git 저장소를 올려두는 웹 서비스 (온라인) |
| 목적 | **코드 변경이력을 관리** | 코드 **공유 및 협업** 플랫폼 |
| 특징 | Commit 단위로 기록 / 특정시점으로 되돌리기 / 여러사람 동시작업 / 변경이력과 책임 명확 | Pull Request, Issue, Review 기능 제공 |

## Repository(레포지토리)
- Git이 사용하는 **저장폴더**(로컬,원격)
- 파일과 그 변경 이력을 함께 관리하는 저장소
- 프로젝트 전체와 모든 버전 기록이 들어 있음
- 로컬 저장소 : 내 컴퓨터에 있는 저장소
  - 프로젝트 폴더로 이동
  - `git init` 실행 → 해당 폴더가 Git 레포지토리가 됨
- 원격 저장소 : GitHub 같은 서버에 있는 저장소
  - GitHub에서 새 Repository 생성
  - `git clone`으로 내 컴퓨터에 복사

### 저장폴더까지 과정
1. **working directory** : 실제로 파일을 수정하고 작업하는 공간 (아직 Git에 기록되지 않은 변경사항이 있는 상태)
2. **staging area** : 1번 후 `git add` 시 → 다음 커밋에 포함할 변경 사항을 미리 모아두는 공간 (커밋 대기상태)
3. **repository** : 2번 후 `git commit` 시 → 저장폴더로 commit 저장완료

```
working directory ──git add──▶ staging area ──git commit──▶ repository
```

## Commit(커밋)
- 변경 사항을 **하나의 기록으로 저장하는 단위** (= 하나의 버전, 체크포인트, 수동저장(자동x))
- "**무엇을 왜 바꿨는지**"를 메시지로 남김
- 특정 시점의 프로젝트 상태를 저장
- **되돌아갈 수 있는 기준점** 역할 ( ex) 게임 save file, 체크포인트 )
- **push(푸시)** : 체크포인트를 GitHub같은 원격 저장소에 올림

```bash
git commit -m "회원가입 기능 추가"
```

## Branch(브랜치)
- **독립적**으로 작업할 수 있는 **작업 공간**
- 기존 코드를 건드리지 않고 기능 개발 가능 (원본의 **복사본**을 가져와 기능 개발, 실험, 수정 작업을 안전하게 진행할 수 있음)
- 여러 기능을 동시에 개발할 수 있음
- **작업이 끝나면 병합(merge)함**

> 브랜치 명령어는 [3. Branch](#3-branch) 참고

## HEAD(헤드)
- 현재 내가 작업 중인 위치를 가리키는 포인터
- 보통 현재 브랜치의 최신 커밋을 가리킴
- HEAD가 움직인다는 것은 작업 기준이 바뀐다는 의미

---

# 2. git 기본 명령어

## git config
- git의 기본 동작을 설정
- **전역설정** : 모든 저장소에 적용

```bash
git config --global user.name "홍길동"
git config --global user.email "hong@example.com"
```

- **로컬설정** : 특정 저장소에만 적용
  - 프로젝트마다 다른 계정이나 역할을 써야 할 때 사용 (회사/개인 프로젝트 구분)

```bash
git config user.name "홍길동"
git config user.email "hong@example.com"
```

## git init
- 현재 폴더를 Git 레포지토리로 초기화
- `.git` 폴더 생성됨
- 현재폴더 기준으로 버전관리 시작

## git status
- 현재 레포지토리의 상태 확인
- 수정된파일, 스테이징 여부, 커밋 가능한 변경사항 확인

## git add
- 변경된 파일을 Staging Area로 올림
- 커밋에 포함할 변경사항을 선택하는 단계 ( 아직 커밋이 생성된것은 아님 )

```bash
git add 파일명    # 특정 파일만
git add .         # 현재 폴더의 모든 변경사항
```

## git commit
- Staging Area에 있는 변경 사항을 하나의 버전으로 기록
- 커밋 메시지 작성 규칙 : 한눈에 알 수 있도록. 명확/간결. 동사로 시작. 한 커밋=한 작업 ( ex) `Add login API` )

```bash
git commit -m "커밋 메시지"
```

## .gitignore
- 버전관리에서 제외할 파일을 지정하는 설정파일
- 불필요한 파일이 커밋되는것을 방지 (환경변수파일, 빌드결과물, 개인설정파일, Password, API Key)

## git push
- 로컬 저장소의 커밋을 원격 저장소(GitHub 등)에 업로드

```bash
git push origin 브랜치명     # ex) git push origin main
git push -u origin main     # 처음 push할 때
```

- `-u` : 로컬 브랜치와 원격 브랜치를 연결 → 이후엔 `git push`만 입력해도 됨
- commit까지 한 내용만 올라감 ( add만 하고 commit 안 한 변경사항은 안 올라감 )
- 원격 저장소에 내 로컬에 없는 새 커밋이 있으면 push가 거절됨 → 먼저 pull 필요

## git pull
- 원격 저장소의 최신 변경사항을 로컬로 가져와서 합침
- `git pull` = `git fetch`(가져오기) + `git merge`(합치기)
- 다른 사람이 올린 작업, 다른 컴퓨터에서 작업한 내용을 내 로컬에 반영할 때 사용
- 같은 파일의 같은 부분을 서로 다르게 수정했다면 충돌(conflict) 발생 → 직접 수정 후 다시 commit

```bash
git pull origin 브랜치명     # ex) git pull origin main
```

---

# 3. Branch

## git branch 명령어

```bash
git branch                # 브랜치 목록 확인
git branch feature/ui     # 브랜치 생성
git switch feature/ui     # 브랜치 전환
```

## 브랜치 관리
- 어떻게 브랜치를 나누고 합칠지에 대한 약속

| 브랜치 | 설명 |
|---|---|
| `feature/*` | 기능 개발 |
| `develop`(dev) | 개발중인 기능을 테스트하는 버전 |
| `release` | 배포 준비 버전 (배포준비하는 동안 다른사람들이 develop에서 다음 기능개발을 계속하기위함) |
| `main` | 배포 가능한 안정 버전 |
| `hotfix` | 배포된 버전 긴급 수정 |

> hotfix : main에서 hotfix브랜치 만들어서 수정. 수정후 main에 병합(재배포) + develop에도 병합하여 다음 배포때 같은버그 다시 살아나는것 방지

## 브랜치 병합
- `git merge` : 다른 브랜치의 작업 내용을 현재 브랜치로 합치는 명령어

```bash
git switch main
git merge feature/ui      # feature/ui 작업을 main으로 합침
```

### Fast-forward
- 브랜치가 직선으로 이어질때 (분기 없음)
- 단순히 커밋 포인터만 이동

### 3-way merge
- 브랜치가 갈라졌다가 다시 합쳐질때 (분기 있음)
- 병합 커밋이 생성됨

### Merge conflict
- 같은 파일의 같은 부분을 서로 다르게 수정하면 충돌 발생
- 해결방법
  1. 충돌 파일 확인
  2. 충돌 코드 직접 수정
  3. 새로운 커밋 생성

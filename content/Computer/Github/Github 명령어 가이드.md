---
title: Github 명령어 가이드
tags: [computer, github]
---
## 1.  처음 연결 시
<hr>

##### git init

&ensp; 현재 디렉토리에 git 로컬 저장소를 초기화하고 생성한다. (.git폴더를 생성)

<br>
<br>

##### git clone <원격 저장소 url>

&ensp;원격 저장소의 내용들을 현재 디렉토리로 가져와 동기화하여 로컬 저장소를 새로 생성한다.

<br>
<br>

##### git config

&ensp;커밋할 때 필요한 username과 useremail을 설정하고 확인할 수 있다. 설정의 우선도는 **Local > Global > System** 이다.

<br>

- **--system:** 모든 system사용자에게 해당
+ **--global:** 한 user의 모든 Repository에 해당
- **--local:** 한 Repository에만 해당

<br>

- **git config --system user.name 'Your name':** system상에서 username을 설정
+ **git config --system user.email 'you@example.com':** system상에서 useremail을 설정

<br>

- **git config --global user.name 'Your name':** global상에서 username을 설정
+ **git config --global user.email 'you@example.com':** global상에서 useremail을 설정

<br>

- **git config --local user.name 'Your name':** local상에서 username을 설정
+ **git config --local user.email 'you@example.com':** local상에서 useremail을 설정

<br>

- **... --list:** 내가 설정해둔 username과 useremail의 list를 확인할 수 있다.

<br>
<br>

##### 원격 저장소 생성

&ensp;github 웹 페이지, 혹은 데스크탑 앱에서 원격 저장소를 생성할 수 있다. 

<br>

> [!caution] 
> README.md등 github에서 제공하는 기본 파일들을 원격 저장소 생성 시 이용했을 경우, git remote 명령어로 로컬 저장소와 연동 이후에 pull로 해당 파일들을 원격 저장소에서 받아온 이후에 이용해야 한다.

<br>
<br>

##### git remote

&ensp;원격 저장소와 관련된 명령을 할 수 있다.

<br>

- **git remote add \<원격 저장소명> <원격 저장소 url>:** 원하는 원격저장소의 url을 가져와 'remote repo name'으로 이름붙여 현재 로컬 저장소와 해당 원격 저장소를 연동한다. 기본적으로 origin이라고 이름 붙이며, 하나의 로컬 저장소에 여러 개의 원격 저장소가 연동 가능하다.
+ **git remote -v:** 연동한 원격 저장소의 목록 확인
- **git remote get-url \<원격 저장소명>:** 해당 이름을 가진 원격 저장소의 url을 출력
+ **git remote rename <기존 이름> <변경할 이름>:** 원격 저장소의 이름을 변경
- **git remote rm \<원격 저장소명>:** 해당 이름을 가진 원격 저장소의 연동을 제거

<br>
<br>
<br>

## 2. 주요 명령어
<hr>
### 2. 1 git Staging
<hr>

##### git add

&ensp;커밋할 내용들을 스테이지에 추가하며, 이 과정을 Staging이라 한다.

<br>

- **git add <파일명>:** 해당 파일을 Staging한다.
+ **Working Directory의 모든 변경사항을 Staging하기**
	+ **git add --all**
	+ **git add . :** .gitignore파일들은 제외하여 스테이징한다.
	+ **git add * :** .gitignore파일들도 포함하여 스테이징한다.

<br>
<br>

##### git status

&ensp;로컬 저장소의 상태를 체크한다. 커밋해야 할 변경사항이 있는지, Untracked 파일이 있는지, 현재 저장소의 어떤 브랜치에서 작업하고 있는지 등을 볼 수 있다.

<br>

- **git status -s:** git status와 유사하나 워킹 트리의 상태를 요약해서 보여준다.

<br>

**git에서 파일의 상태**
- **Staged:** 현재 스테이지에 있으므로 커밋할 준비가 된 파일
+ **Tracked:** 한번이라도 커밋한 전적이 있기 때문에 git이 관리하는 파일
	+ **Modified:** 최근 커밋한 이후로 수정을 가한 파일
- **Untracked:** 워킹 트리에서 모종의 이유로 현재 관리되지 않는 파일

<br>
<br>

##### git rm <파일명>

&ensp;워킹 트리에서 파일을 삭제하고, git의 관리 대상에서도 해당 파일을 제거한다.

<br>

- **git rm --cached <파일명>:** git의 관리 대상에서만 해당 파일을 제거하여, Untracked 상태로 만든다.

<br>
<br>

##### .gitignore 파일

&ensp;.gitignore파일에 커밋을 원하지 않는 파일들을 추가하면 일일이 제거하지 않아도 Staging 대상에서 제외할 수 있다. 워킹 트리의 최상위 디렉토리(.git폴더가 위치한 폴더)에 .gitignore를 생성하면 된다.

<br>

- **#:** 주석 처리
+ **<filename.확장자>:** 모든 디렉토리에 존재하는 'filename.확장자'를 제외
- **/\<filename.확장자>:** 최상위 디렉토리에 존재하는 'filename.확장자'를 제외
+ **\<filename>:** 'filename'이라는 이름을 가진 폴더, 파일 또는 그 내용들을 제외
- ***.<확장자>:** 해당 확장자의 파일은 모두 제외
+ **\<foldername>/:** 해당 폴더와 그 이하의 파일들을 모두 제외
- **\<foldername>/\<filename.확장자>:** 해당 폴더의 해당 파일을 제외
+ **!\<filename.확장자>:** 'filename.확장자'를 커밋 제외 대상에서 제외

<br>

> [!caution] 
> .gitignore에 파일을 추가했더라도 이미 git의 관리 대상(Tracked)이 된 파일들은 git rm 명령어로 관리 대상에서 제거한 후 commit해서 적용해야 한다.

<br>
<br>
<br>

### 2. 2 git Commit
<hr>

##### git commit

&ensp;Staging 작업이 모두 끝난 후 파일들을 스냅샷으로 만들어 저장하는 작업이다. 커밋하여 로컬 저장소에 저장된 파일들은 git이 버전 관리를 도와주게 된다. 커밋은 현재 작업중인 브랜치에 기록된다.

<br>

- **git commit -m 'Message':** 커밋하면서 커밋에 대한 메세지를 남긴다. 커밋 메세지를 남기지 않고 git commit만 입력할 경우 vim에디터에서 커밋 메세지와 비슷한 설명을 남길 수 있다.
+ **git commit -am 'Message':** 별도의 add 명령어 없이 commit과 add를 함께 수행한다.

<br>
<br>

##### git log

&ensp;HEAD와 관련된 커밋 기록 및 각 커밋의 해쉬 값과 날짜 등 자세한 정보를 확인할 수 있다. 로그가 너무 길 때는 **'git shortlog'**명령어로 요약된 로그를 볼 수 있다.

<br>

- **git log --oneline:** 커밋 메세지와 해쉬 값 정도만 보고 싶을 때 사용
+ **git log --oneline --graph --decorate:** HEAD와 관련된 커밋들을 더 자세히 보고 싶을 때 사용
- **git log --oneline --graph --all --decorate:** 모든 브랜치에서 작업한 내용을 보고 싶을 때 사용
+ **git log --oneline -n7:** 내 브랜치의 최신 커밋을 7개만 보고 싶을 때 사용

<br>
<br>

##### git diff

&ensp;최근 커밋 버전과 현재 워킹 트리의 작업 상태 사이의 차이를 출력한다.

<br>

- **git diff --staged:** 커밋 버전과 add된 파일의 상태를 비교
+ **git diff \<commit hash1> \<commit hash2>:** 두 커밋 버전 사이의 상태를 비교
- **git diff HEAD HEAD^:** 가장 최근 커밋과 그 전의 커밋의 상태를 비교
+ **git diff \<branch1> \<branch2>:** 브랜치간의 상태를 비교

<br>
<br>

### 2. 3 git Push, Pull
<hr>

##### git push

&ensp;현재 브랜치에서 생성한 커밋들을 원격 저장소에 업로드한다.

<br>

- **git push <원격 저장소명> <브랜치명>:** 커밋한 내용을 원격 저장소의 해당 브랜치에 push
+ **git push -u <원격 저장소명> <브랜치명>:** -u 옵션을 사용할 경우 앞으로 '<원격 저장소명> <브랜치명>'을 생략하고 push나 pull을 할 때, 알아서 이름이 같은 로컬 브랜치와 원격 브랜치를 연결하도록 한다.
- **git push <원격 저장소명> --delete <브랜치명>:** 해당 원격 브랜치를 삭제한다.

<br>
<br>

##### git pull

&ensp;원격 저장소의 커밋을 현재 작업중인 로컬 저장소의 브랜치에 자동으로 fetch하고, merge한다.

<br>

- **git pull <원격 저장소명> <브랜치명>:** 원격 저장소의 해당 브랜치에 있는 커밋을 로컬 저장소로 fetch&merge

<br>

> [!caution]
> - 원격 저장소와 로컬 저장소의 커밋이 꼬여 버리면(원격 저장소의 변경 사항을 pull하지 않고 로컬 저장소에서 커밋하여 push하는 경우) pull 명령어가 작동하지 않는다.
> + 이 때는 수동으로 fetch 및 merge 명령을 수행해야 한다.

<br>
<br>

##### git fetch

&ensp;원격 저장소의 브랜치와 커밋들을 로컬 저장소와 동기화한다. 이후 git status를 통해 해당 원격 브랜치에 비해 작업 중인 로컬 브랜치에서 커밋이 뒤쳐진 부분이 있는지 확인할 수 있다.

<br>

- **git fetch <원격 저장소명> <브랜치명>:** 원격 저장소의 해당 브랜치에 있는 커밋과 로컬 브랜치를 동기화. 로컬 저장소에 해당 원격 브랜치의 커밋 내역을 가지는 임시 브랜치가 생기는 원리이다.

<br>
<br>
<br>

### 2. 4 git Branch
<hr>

&ensp;github에서 커밋 등의 작업은 모두 특정 로컬 브랜치에서 이루어지고, 이 커밋들 또한 특정한 원격 브랜치에 업로드된다. 로컬 브랜치에서 작업한 내용들은 동명의 원격 브랜치에 push함으로써 원격 저장소에 업로드된다.

<br>

##### main branch

&ensp;github에서 원격 저장소 생성 시 가장 처음에 기본적으로 생성된다. 로컬 저장소 또한 가장 처음 생기는 브랜치이기도 하나, 로컬 저장소에서는 커밋 혹은 원격 저장소에서 pull로 자료를 받아온 후에 활성화된다.

<br>
<br>

##### git branch

&ensp;현재 HEAD 브랜치 및 로컬 저장소의 브랜치 목록을 출력한다.

<br>

- **git branch <브랜치명>:** 현재 브랜치의 커밋에서 분기하여, 이전까지의 커밋 히스토리를 모두 복사하여 해당 브랜치 이름을 가진 로컬 브랜치를 생성한다.
+ **git branch -D <브랜치명>:** 해당 브랜치와 해당 브랜치의 작업 내용을 모두 삭제한다.

<br>
<br>

##### git checkout <브랜치명>, git switch <브랜치명>

&ensp;해당 브랜치로 HEAD 브랜치를 이동한다.

<br>

- **git checkout -b <브랜치명>:** 해당 브랜치를 생성하고, HEAD 브랜치를 바로 해당 브랜치로 옮긴다.
+ **git switch -c <브랜치명>:** 해당 브랜치를 생성하고, HEAD 브랜치를 바로 해당 브랜치로 옮긴다.
- **git switch -c <브랜치명> <해쉬 값>:** 해당 해쉬 값을 가진 커밋에서 분기하여 브랜치를 생성하고, HEAD 브랜치를 바로 해당 브랜치로 옮긴다.

<br>
<br>

##### git merge <브랜치명>

&ensp;현재 HEAD 브랜치에 해당 로컬 브랜치의 커밋 히스토리와 내역을 반영하고, 추가적인 커밋을 남긴다. 

<br>

> [!caution]
> 원격 브랜치에 fetch하여 커밋 내용을 가져오려고 할 때는 **'<원격 저장소명>/<브랜치명>'** 으로 접근해야 한다.

<br>
<br>

##### git rebase <브랜치명>

&ensp;현재 브랜치의 커밋들을 대상 브랜치에 재배치한다. 

<br>

> [!caution]
> 히스토리 그래프가 깔끔해지는 장점이 있지만, 만약 main브랜치에서 커밋하고 원격 저장소에 푸시한 이후에 다시 main2브랜치로 rebase할 경우 원격 저장소와 로컬 저장소에 동일한 커밋이 2개 생기므로 주의해서 사용한다.

<br>
<br>
<br>

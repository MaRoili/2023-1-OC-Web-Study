<깃의 3가지 영역>
•	Working Directory : 내가 작업하고 있는 프로젝트의 디렉토리 / 소스 코드를 작업하는 영역으로 코드를 추가, 수정, 삭제하는 작업이 이루어진다
•	Staging Area : 커밋을 하기 위해 $ git add 명령어로 추가한 파일들이 모여있는 공간이다 이를 통해 소스 코드의 상태 정보를 확인할 수 있다.
•	Locla Repository : 커밋들이 모여있는 저장소 / git이 관리해주는 공간 / 스테이징 영역에 있는 소스 코드에 Git commit 명령을 실행하면 최종적으로 Git의    저장소에 반영된다.
•	Remote repository: 컴퓨터 밖 ->github
코드를 작성하다가 커밋을 해야하는 순간이 오면 git add .를 통해 커밋할 파일들을 추가한다
이 파일은 바로 Repository에 올라가지 않고, Staging Area에 올라가게 된다.
Staging Area에 추가한 파일들을 Commit을 한다면 최종적으로 저장소(Repository)로  저장되게 된다.

<File status lifecycle>
File 관점에서는 다시 4가지 단계로 나뉜다.
•	Untracked : Working Directory에 있는 파일이지만 Git으로 버전관리를 하지 않는 상태
•	Unmodified : 신규로 파일이 추가되었을 때, new file 상태와 같다. ( $ git add 상태 )
•	Modified : 파일이 추가된 이후 해당 파일이 수정되었을 때의 상태
•	Staged : Staging Area에 반영된 상태

<git의 명령어>
-	Add
작업 디렉토리 내에서 작업한 파일이 있을 경우 add 명령어를 통해서 staging 영역으로 옮길 수 있다.
staging 영역은, commit 을 하기 전에 임시 저장된 상태로 생각하면 된다
$ git add <파일위치>
$ git add -A
$ git add .
$ git add
$ git add -p.

-	Commit
git add로 staging 영역에 올라와 있는 작업 데이터를 로컬 저장소에 저장하기 위해서는 commit 명령어를 이용한다
$ git commit -m <메시지>

git commit —ament
이 옵션을 이용해서 commit를 수행하면, 가장 최근의 commit에 덧붙인다.이는 가장 최근의 commit을 삭제하고, 새로운 commit 을 작성한 것과 동일한 동작이기 때문에, 가장 최근 commit 의 id 가 부여된다.

$ git log-10
commit 한 내용을 확인 하기 위해서는 위 log를 보는 명령어를 이용해서 어떤 내용을 commit 했는지 알 수 있다.

-	Push
로컬 저장소에 저장된 변경 내용을 원격 저장소로 보내기 위해서는 push 명령어를 이용해야 한다
$ git push<저장소명><브랜치명>
$ git push origin HEAD:master

-	Pull
원격 저장소의 변경사항 중 로컬 저장소에 반영되지 않은 내용을 가져올 때는 pull 명령어를 이용한다. 아무 옵션을 주지 않으면, 현지 checkout 되어있는 branch의 내용을 병합한다.
$ git pull
$ git pull --rebase

-	Fetch
원격 저장소의 변경사항을 가져오기만 하고, 현재 branch에 병합하지 않을 때 이용하는 명령어이다.
복잡한 병합의 경우 fetch를 사용하기 보다는 임시 branch를 새로 만들어서 pull을 수행하고,
rebase 명령을 통해서 작업 branch 와 병합하는 방법을 사용한다.


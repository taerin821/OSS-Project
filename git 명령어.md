# Git 명령어

##  git init  
* git 저장소 초기화. 명령어를 입력하기 전까지는 일반 디렉토리였지만, 초기화를 시키면 해당 디렉토리를 로컬 깃 저장소로 등록해 준다.  
<img src="./image/git_init.png" width="600" height="170">
<!-- ![img](.\image\git_init.png)   -->


##  git clone  
* 원격저장소로 부터 프로젝트를 복제하는 것을 말한다.
* 저장소를 clone 하면 ‘origin’ 이라는 리모트 저장소가 자동으로 등록된다.    
<img src="./image/git_clone.png" width="600" height="220">


##  git remote  
* 현재 프로젝트에 등록된 리모트 저장소를 확인할 수 있다.
* -v 옵션을 주면 단축이름과 URL을 함께 볼 수 있다.    
<img src="./image/git_remote.png" width="600" height="250">  

##  git config  
* git 사용 환경 설정 확인하고 변경할 수 있다.  
<img src="./image/git_config.png" width="600" height="350">


##  git add
* 작업 디렉토리 상의 변경 내용을 스테이징 영역에 추가하기 위해 사용하는 명령어.   
    ``` $ git add <파일/디렉토리 경로>``` : 변경 내용의 일부만 스테이징 영역에 넘기고 싶을 때 디렉토리의 경로를 인자로 넘긴다.  
    ```$ git add . ```:  현재 디렉토리의 모든 변경 내용을 스테이징 영역으로 넘기고 싶을 때 인자로 넘긴다. (상위 디렉토리의 변경 내용은 포함하지 않음)   
    ``` $ git add -A``` : 작업 디렉토리 상에 어디에 위치하든 항상 동일하게 모든 변경 내용을 스테이징으로 넘긴다.   
       
    <img src="./image/git_add.png" width="600" height="150">

##  git commit -m “commit message”
* 파일 및 폴더의 추가/변경 사항을 저장소에 기록한다.
* 인덱스(staging area)에 등록되어 있는 파일 상태를 기록한다.   

    <img src="./image/git_add.png" width="600" height="150">

## git push
* 로컬 저장소의 commit 내역을 remote 저장소로 전송한다.
* ``` -u ``` 옵션은 upstream repository를 설정해준다. 즉 한번 설정한 후로는 git push, git pull 만 간단히 쓸 수 있다.
    ```
    git push [remote] [branch]

    git push -u origin main
    ```

## git pull 
* 원격저장소로 부터 변경된 내용을 가지고 온 후 병합(merge)
* pull = fetch + merge 와 같은 의미!
    ```
    git pull
    ```

##  git fetch
* 원격저장소로 부터 변경된 내용을 가지고 온 후 병합 x
* 변경된 내역을 가지고 온 후 검토 후에 merge 할 수 있어서 충돌 방지
* --prune 옵션으로 remote 저장소에 지워진 브랜치를 local 반영하여 local의 불필요한 branch를 삭제한다.
    ```
    git fetch [remote]

    git fetch --prune
    ```

## git merge 
* 브랜치를 병합하는 명령어
* 협업 과정에서 같은 이름의 파일 안에 수정한 부분이 겹칠 때 충돌(conflit)이 발생 할 수 있다.

## git rebase
* 브랜치를 병합하는 명령어로 merge와 같은 기능이지만,
merge의 경우 병합 할 브랜치에서 기록한 모든 commit이 master의 commit으로 기록된다.
* rebase의 경우 작업 중 남겼던 commmit 중 불필요한 것들을 생략시키고 필요한 commit만 남겨서 master 병합이 가능하다.
* -i는 interactive라는 옵션이다. 해당 옵션을 사용하면 중간에 낀 커밋 메세지를 수정할 수 있다.


##  git log
* git log는 현재 브랜치의 커밋 이력을 볼 수 있는 명령어이다  
<img src="./image/git_logpng.png" width="600" height="150">   

    ``` $ git log ```  : 현재 브랜치의 커밋 이력을 보는 명령어, HEAD와 관련된 커밋들이 자세하게 나온다  
    ``` $ git log --oneline  ```  : 커밋 이력 중 커밋 ID 와 타이틀 메시지만 조회   
    ``` $ git log --oneline --decorate --graph --all  ```  : 모든 브랜치의 커밋 이력을 보는 명령어   
    ``` $ git log -n <숫자>  ```  : 현재 브랜치의 커밋 이력을 보는 명령어   

## git LifeCycle
* 워킹 디렉토리의 파일은 먼저 크게 Untracked, Tracked의 두 가지 상태로 나뉜다.(워킹 디렉토리는 작업중인 로컬 컴퓨터의 공간입니다.) 
    * ``` Tracked ``` : 파일에 수정이 일어나면 git이 파일의 변경을 감지하여 사용자에게 알려주는 것과 같이 파일을 추적하는 상태   
    * ``` Untracked ``` : 파일을 저장소에 저장할 필요가 없어 git이 신경쓰지 않아도 되는 상태   

* Tracked 상태의 파일들은 다시 크게 Unmodified, Modified, Staged 3개의 상태로 나뉩니다.   
    * Staged : staging area에 있는 파일들의 상태    
    * Unmodified : staging area에 있는 파일들을 커밋하게 되면 해당 파일들은 하나의 커밋으로 저장된 후, 파일의 상태는 Unmodified로 내려오게 됩니다.  
    * Modified : Unmodified 상태의 파일들을 수정하게 되면 Modified 상태가 됩니다.    

* 이후 다시 git add 명령어를 이용하여 Staged 상태로 올려준 후 커밋을 하는 과정을 반복하게 됩니다
<img src="./image/git_Lifecycle.png" width="600" height="300">

##  git status  
* 파일들의 가능한 상태를 확인할 수 있다. 관리되고 있는 파일과 디렉토리 목록을 확인해 볼 수 있다. 
* 작업 디렉토리(working directory)와 스테이징 영역(staging area)의 상태를 확인하기 위해 사용한다.   
<img src="./image/gitStatus.png" width="600" height="300">   





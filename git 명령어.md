# Git 명령어

##  git init  
* git 저장소 초기화. 명령어를 입력하기 전까지는 일반 디렉토리였지만, 초기화를 시키면 해당 디렉토리를 로컬 깃 저장소로 등록해 준다.  
<img src="OSS-Project/image/git_init.png" width="600" height="170">
<!-- ![img](OSS-Project\image\git_init.png) -->  


##  git clone  
* 원격저장소로 부터 프로젝트를 복제하는 것을 말한다.
* 저장소를 clone 하면 ‘origin’ 이라는 리모트 저장소가 자동으로 등록된다.    
<img src="OSS-Project/image/git_clone.png" width="600" height="220">


##  git remote  
* 현재 프로젝트에 등록된 리모트 저장소를 확인할 수 있다.
* -v 옵션을 주면 단축이름과 URL을 함께 볼 수 있다.    
<img src="OSS-Project/image/git_remote.png" width="600" height="250">  

##  git config  
* git 사용 환경 설정 확인하고 변경할 수 있다.  
<img src="OSS-Project/image/git_config.png" width="600" height="350">


##  git add
* 작업 디렉토리 상의 변경 내용을 스테이징 영역에 추가하기 위해 사용하는 명령어.
    ```
    $ git add <파일/디렉토리 경로>
    ```
    변경 내용의 일부만 스테이징 영역에 넘기고 싶을 때 디렉토리의 경로를 인자로 넘긴다.  
    ```
    $ git add .
    ```
    현재 디렉토리의 모든 변경 내용을 스테이징 영역으로 넘기고 싶을 때 . 인자로 넘긴다. (상위 디렉토리의 변경 내용은 포함하지 않음)
    ```
    $ git add -A
    ```
    작업 디렉토리 상에 어디에 위치하든 항상 동일하게 모든 변경 내용을 스테이징으로 넘긴다.
    ```
    $ git add -p
    ```    
    <img src="OSS-Project/image/git_add.png" width="600" height="150">

##  git commit -m “commit message”
* 파일 및 폴더의 추가/변경 사항을 저장소에 기록한다.
* 인덱스(staging area)에 등록되어 있는 파일 상태를 기록한다.   

    <img src="OSS-Project/image/git_add.png" width="600" height="150">

##  git log
* git log는 현재 브랜치의 커밋 이력을 볼 수 있는 명령어이다  
<img src="OSS-Project/image/git_logpng.png" width="600" height="150">   

    ``` $ git log ```  : 현재 브랜치의 커밋 이력을 보는 명령어, HEAD와 관련된 커밋들이 자세하게 나온다  
    ``` $ git log --oneline  ```  : 커밋 이력 중 커밋 ID 와 타이틀 메시지만 조회   
    ``` $ git log --oneline --decorate --graph --all  ```  : 모든 브랜치의 커밋 이력을 보는 명령어   
    ``` $ git log -n <숫자>  ```  : 현재 브랜치의 커밋 이력을 보는 명령어   

##  git status  
* 파일들의 가능한 상태를 확인할 수 있다. 
* 작업 디렉토리(working directory)와 스테이징 영역(staging area)의 상태를 확인하기 위해 사용한다.  
<img src="OSS-Project/image/git_status.png" width="600" height="300">




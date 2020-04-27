# Git 시작
## 저장소 생성 & commit
1. git 사이트 접속 후 repository 생성
2. git 주소 복사 후 cmd에서 원하는 폴더안에 git clone  
    ```
    git clone <본인 repository 주소>
    cd repository  
    git add --all   #새롭게 생성된 파일 모두 추가
    git status   #현재 파일 상태 확인
    git commit -m "commit 설명"
    git log   #commit 히스토리 조회
    ```
## remote 저장소  
1. remote 저장소 확인  
    ```
    git remote -v   
    git remote add <remote 이름> <remote 주소>   #기존의 remote이외의 저장소를 추가하고 싶을때 : 협업
    ```  
2. remote 저장소에 push
    ```
    git push <remote 저장소이름> <브랜치 이름>   #git push origin master
    ```
3. remote 저장소 브랜치에서 데이터 가져오고 merge
    ```
    git pull <remote>
    ```

        
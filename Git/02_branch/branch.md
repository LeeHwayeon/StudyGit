# Git Branch
## 브랜치 : 독립적으로 개발하는 것을 도와줌
1. 새로운 브랜치 생성  
    git init으로 생성된 기존 브랜치는 master
    ```
    git branch <브랜치명>
    ```
2. 브랜치 이동
    ```
    git checkout <브랜치명>
    ```
    --> 새로운 브랜치로 이동 후 commit 진행하면 새로운 브랜치는 이동했지만
        master는 여전히 이전 commit에 머무름
3. 브랜치 삭제
    ```
    git branch -d <브랜치명>
    ```
- 1+2 = ``` git checkout -b <브랜치명>```  

## Merge
1.  merge할 브랜치들의 관계가 조상-자식(?) 관계 일 경우에
    ```
    git checkout master
    git merge <master 브랜치 자식>
    #Fast-forward Merge 방식
    ```
    - 즉, A 브랜치에서 다른 B 브랜치를 merge할 때 B 브랜치가 A 브랜치 이후의 commit을 가리키고 있으면 A 브랜치가 B 브랜치와 동일한 commit을 가리키도록 이동
2. merge할 브랜치들의 관계가 영향이 없을 때
    ```
    git checkout master
    git merge <브랜치>
    #3-way merge 방식
    ```
    - 즉, 현재 브랜치가 가리키는 commit이 merge 할 브랜치의 조상이 아니기 때문에 공통 조상을 찾아 merge
    - 이 경우에는 충돌이 발생 할 수 있다.
    merge 충돌이 일어났을 때 어떤 파일을 merge할 수 없었는지를 보려면
    ```
    git status
    ```

## 브랜치 관리
- 브랜치 목록
```
git branch      # * 기호가 붙어있는 건 현재 작업하고 있는 브랜치란 뜻
git branch -v   # 브랜치마다 마지막 커밋 메시지 보여줌
```
- 브랜치 상태
```
git branch --merged  
git branch --no-merged
```


-----------------------------------------
master 브랜치에는 안정된 코드만 두는 것이 합리적   
다른 브랜치를 만들어 테스트 후에 master 브랜치에 merge 하는것이 좋다.
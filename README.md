### Remote Repository 연결하기

<details>
<summary> 1st Day - off </summary>
<div markdown = "1">
   
1. Git
    
    버젼관리 : 실시간으로 변경사항을 기록하는 관리 시스템
    
    분산버젼관리를 하는 이유 : 서버가 터졌을 때 Legacy의 의미를 잃어버림
    
    분산버젼관리 : 분산관리를 통하여 서버에 다시 Pull_Request만 하면 되므로
    
    Git : 분산 버전 관리 프로그램 자체를 의미함
    
    GitLab : 보안이 중요한 회사에서 많이 사용 
    
    GitHub : Microsoft에 소스코드를 넣는 방식 (개인 프로젝트에서나 쓰임) ⇒ Cloud 방식
    
    Git의 장점
    
    가. 분산관리가 매우 좋음
    
    나. 잔디를 매일매일 심는지 여부를 통해 노력 / 끈기 등을 알 수 있음
    
    Gitlab에서 Commit해도 잔디 깔리나?
    
2. GUI / CLI
    
    가. GUI : 그래픽으로 컴퓨터와 상호작용 ⇒ 컴퓨터의 성능을 많이 소모함 (Window)
    
    나. CLI : 명령어를 통해 컴퓨터와 상호작용 ⇒ 백엔드 개발자가 많이 사용 (Linux)
    
3. 리눅스 (Linux)
    
    가. 여러가지 명령어
    
    | touch | 파일 생성 |
    | --- | --- |
    | mkdir a | 새폴더 생성 (a라는 폴더 사용) |
    | rm | 폴더 삭제 |
    | ls (-a) | 현재 폴더 확인 (-a를 붙여쓰면 숨겨진 파일까지 전부 나옴) |
    | cd a | a폴더로 이동 |
    | cd .. | 상위폴더로 올라간다 |
    | pwd | 현재위치 |
    | cp a b | a를 복사해서 b이름으로 붙여넣기(파일) |
    | find [검색경로] -name [파일명] | [파일명]을 [검색경로]안에 있는 모든 디렉토리에서 확인(하위) |
    | code . | 해당 Repository를 Visual Studio Code에 연결하도록 함 |
    | git clone (git Repository url) | 원격 파일 ⇒ 로컬 파일로 해당 디렉토리에 저장 |
    
4. 절대경로와 상대경로
    
    절대경로 : Html / CSS에서 절대경로를 통해 이동 (Root directory)
    
    상대경로 : 현재 작업하고 있는 디렉토리 기준으로 계산된 상대적 위치 계산(절대경로 기준점을 부여하고 그 이후에 있는 폴더만을 보여줌)
    
    1. 마크다운(markdown)
    
    텍스트 기반의 가벼운 마크업 언어 ⇒ 문서의 구조와 내용을 같이 쉽게 빠르게 작성
    
    코드가 웹에서 돌아갈 수 있도록 하는 방법
    
    tag를 이용한 문서구조화하는 방법을 의미
    
    웹 환경에서 구조를 문서화할 때 만드는 하나의 약속
    
    - [R](http://Read.md)EADME.md 파일을 통해 오픈 소스의 공식 문서 작성 ⇒ 해당 Repository의 설명글
    - 프로젝트에 대한 설명 문서 / 소프트웨어 배포 / 마크다운을 이용해 보통 작성
    - Open Library에서 사용할 때도 README.md에 작성
    
    가. Typora ⇒ 마크다운 전용 프로그램
    
    문법 (디자인적인 요소는 불가능하다.)
    
    1. # : 헤딩 ⇒ 문서의 제목이나 소제목 (h1 ~ h6)
    2. 1.2.3. : 순서가 있는 리스트
    3. 별 _ : 순서가 없는 리스트
    4. ``` python 000 ``` :  파이썬으로 표시하는 방법
    
    ```python
    print(0)
    ```
    
    1. ` ` : 텍스트 중간에 넣고 싶을 때
    
    안녕 `print(0)` 야
    
    [string] (url) : 링크를 만들 수 있음( ex : [google] (https://google.com) )
    
    [google] ([https://www.google.com](https://www.google.com/))
    
    ![string](img_url) : 이미지를 넣고 싶을 때
    
    ** dd ** : 굵게 (ex : **안녕)**
    
    __ dd __ : 굵게 (ex : **dd** )
    
    양옆에 * : 이태릭 ( *하이* )
    
    ~~dd~~ : 취소선 ( ~~ 취소선 ~~ )
    
    ___ : 수평선 
    
    - Repository : 특정 디렉토리를 버전 관리하는 저장소
    - 원격 Repo 와 로컬 Repo로 나뉘어져서 사용됨
    - git init 명령어로 로컬 저장소 생성
    - .git 디렉토리에 버전 관리에 필요한 모든 것이 담겨있음
    1. Local Repo 만드는 방법
        - git init을 이용해서 Local 위치를 명확하게 명시 (master) ⇒ 필요한 요소 생성
            - git init : .git이라는 폴더를 만들어놓음 (git으로 관리되는 Repository)
            - Git이 관리하는 Repository 안에서는 3가지 디렉토리가 있음
                - working directory : 내가 작업하고 있는 실제 디렉토리
                    
                    ⇒ 현재 git에서 추적하고 있지 않음
                    
                - staging directory : 커밋(commit)으로 남기고 싶은 특정 버젼
                    
                    ⇒ git add를 통해서 working directory ⇒ staging Area로 들고온다
                    
                        * git add . 을 하면 해당 directory의 전체 변경사항이 바뀐다.
                    
                    ⇒ git에서 관리를 시작함
                    
                    - 일부분만 commit하고 싶을 때 commit
                - Repository : commit이 저장되는곳
                    
                    ⇒ git commit ‘000’을 통해 staging Area ⇒ Repository로 들고온다.
                    
                    ⇒ Version으로 남기는 것을 의미한다. 
                    
    
    1. Git 처음 시작하기
    
    ---
    
    가. 로컬에서 Commit하기
    
    | git init | Local Directory에 git파일 추가(관리하겠다는 뜻) |
    | --- | --- |
    | git config —global user.email ‘000’ | commit 저장시 사용할 email을 저장 |
    | git config —global user.name ‘000’ | commit 저장시 사용할 이름 저장 |
    | git status  | 현재 상태 확인 |
    | git add .  | Working space ⇒ Staging Area에 Stage |
    | git commit -m ‘000’ | 000이라는 별명으로 Staging Area ⇒ Repository |
    | git push (-u) origin master | Local Repo ⇒ Remote Repo로 저장  |
    | git login —oneline | Commit 기록 확인 (Git graph로도 가능) |
    - git push -u origin master를 할 경우 이후에 git push만 해도 자동으로 사용가능
    
    ---
    
    나. 원격 Repository에 연결하기 (Remote Repository)
    
    - Github Repo Setting에서 master로 바꿔야함 ⇒ 인종차별 때문에
    
    | git remote -v | 원격저장소가 무엇인지 알 수 있음 |
    | --- | --- |
    | git remote add [별명] repository code | 원격 저장소를 등록 |
    | git pull | 원격 저장소에 변경된 내용 ⇒ Local 저장 |
    |  |  |
    
    다. Github Branch
    
    | git branch | 나무가 뭐가 있는지 확인하기 |  |
    | --- | --- | --- |
    | git switch | 브랜치를 변경한다. (최신) |  |
    | git branch ‘aa’ | aa라는 이름의 브랜치 생성 |  |
    | git checkout ‘aa’ | aa라는 나무로 이동 |  |
    
     
    
    - branch의 경우 부모가 가지고 있는 코드를 그대로 끌고온다. 부모의 코드에 일부 코드를 추가하여 넣음으로서 사용이 가능하다.
    - 3-way merging : 부모 수정사항 과 자식의 수정사항이 각각 있을 경우 부모 + 자식1로 commit을 한다. (예시 : origin 1, parent_1, child_1,2가 있을 경우 parent_1과 child_1,2가 서로 수정한다면 parent_1 + child_1, parent_2 + chile_2 이렇게 2개로 commit해서 사용함
        
        ⇒ master tree에서 git merge feature_b
</div>
</details>


<details>
<summary> 2st Day - off </summary>
<div markdown = "1">
1. 오픈소스(Open source)
    - 공개된 소프트웨어라는 의미로 무료로 사용할 수 있는 framework/Library 등을 의미한다.
    - Framework vs Library
        - Framework : 일정하게 짜여진 틀
        - Library : 여러가지 도구들 ⇒ 모든 곳에서 사용이 가능하다.
   
   

2. git ignore
    - Github에서 중요한 소스를 가리기 위해 사용하는 파일 ( 해당 파일에 .gitignore 사용 )
    - Repository를 생성하자마자 파일을 만들어야함
    - [ignore.io](http://ignore.io)라는 사이트에서 .gitignore에 들어갈 기본적인 구조 제공
        - 가능하면 하위파일에 dummy라는 파일을 만든 후 안에 중요한 자료를 넣어놓음
        - `# Cython debug symbols` 부분에 /dummy를 넣어놓으면 해당 파일 자료는 Git에 올라오지 않음
        - Git에서 한번 이미 관리했다면 이후에는 감추는 것이 불가능하므로 반드시 파일 먼저!
</div>
</details>

<details>
<summary> 3st Day - off </summary>
<div markdown = "1">
1. 기존에 Git이 연동이 되어있을 때 다른 Git으로 연동을 바꾸려고 하는 경우
   ''' python  remote: Permission to A.git denied to B.
   remote: Support for password authentication was removed on 000 으로 나올 경우에 사용 '''
   * 자격증명관리자 파일 => Windows 자격 증명 => git id, password 변경
   * git config --global [user.name + '이름', user.password + '토큰'] 입력
   * 토큰의 경우 Git Setting => developer setting => 토큰 발급하는 기관이 있음 (최근 보안 강화를 위해 Git에서는 토큰으로 발급)
</div>
</details>


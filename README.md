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
   
   '''python  remote: Permission to A.git denied to B.
   remote: Support for password authentication was removed on 000 으로 나올 경우에 사용 '''
   
   * 자격증명관리자 파일 => Windows 자격 증명 => git id, password 변경
   * git config --global [user.name + '이름', user.password + '토큰'] 입력
   * 토큰의 경우 Git Setting => developer setting => 토큰 발급하는 기관이 있음 (최근 보안 강화를 위해 Git에서는 토큰으로 발급)
   
   좋은 템플릿 사이트 : https://jekyllthemes.io/theme/creative-theme-jekyll
   * 만약 먼저 Pull된 것이 있다면 git push할 때 에러가 나므로 git pull로 상태를 체크한 후에 확인해야함
   * html에 대한 전반적인 지식을 배운 후에 Template 변경이 필요할 것으로 
</div>
</details>

<details>
<summary> 4st Day - off </summary>
<div markdown = "1">
   * 만약 git branch를 merge했으나 그 이전으로 되돌리고 싶을 경우 git reset HEAD^ 입력해서 되돌려놓을 수 있다
   * 원하는 곳으로 돌아간 후에서는 commit / push로 원하는 곳을 원격에 넣어줘야 비로소 바뀔 수 있다.
</div>
</details>

<details>
<summary> 5st Day - off </summary>
<div markdown = "1">
   1. Python이 타언어에 비해 유리한 이유
    - 알고리즘 테스트에 유리하다. (입사를 위한 코딩테스트에 매우 유리하다)
    - 구현 방식의 코딩테스트에 유리하다. (유용한 라이브러리가 매우 많다. ⇒ 정보가 매우 많다.)
    - 파이썬의 활용분야가 매우 많아지고 있다. (빅데이터 분석 / AI / 웹 프로그래밍)
    - 객체 지향 프로그래밍 ⇒ 모든 것이 객체로 구현
    - Interpreter 언어 : 사용자 Input ⇒ (기계어로 변경 ⇒ 이해 ⇒ 사용자언어로 변경 ⇒ 출력)
        - 해당 언어에서 자동으로 변경해서 사용자의 편의에 맞게 출력하는 방식을 의미
2. Visual studio 자주 쓰이는 단축키
    - Alt + 화살표 : 코드 바꾸기
    - Alt + shift :
    - 드래그 + ctrl + D :  해당 드래그 만 바꾸기
    - Alt + shit + 화살표 밑 : 복붙하기
3. 파이썬 예쁘게 쓰는법
    - 주석을 확실하고 예쁘게 달기
    - 한줄 주석(#), 여러줄 주석(드래그 + ctrk + /)
4. 변수 (Variabla)
    - 데이터를 저장하기 위해 사용
    - 변수를 사용하면 복잡한 값들을 쉽게 사용(추상화)
5. 자료형(DataType)
    - 수치형 : 정수(int), 실수(float), 복소수(complex)
        - 실수(float)의 경우에는 0.000000001단위로 달라질 수 있으므로 round(float,1) 등을 사용
    - 문자형 : 모든 문자는 기본적으로 문자형으로 나타냄 ( ⇒ Default )
        - 따옴표 안에 따옴표를 표현할 경우 : 큰 따옴표(””) 안에 작은 따옴표(’’)를 사용, 겉에 삼중따옴표(’’’ ‘’’)를 넣고 안에 추가로 넣는다.
        - Escape sequence
        
        | \n | 줄바꿈 |
        | --- | --- |
        | \t | 탭 |
        | \r | 캐리지 리턴 |
        | \0 | Null |
        | \\ | \ |
        | \’ | 단일부호사용 |
        | \” | 이중부호사용 |
    - String Inerpolation(문자열을 변수를 활용하여 반드는 법)
        - print(’Hello, %s’ %name) ⇒ %s에 %name이라는 변수 사용
        - format 함수 ⇒ ‘Hi, {0}’.format(dd)
        - f-string ⇒ print(f’{name}’) 과 같은 방식으로 사용 ( ⇒ 가장 최신 방법 )
    - type(i)를 통해서 해당 i가 어떤 자료형인지를 확인할 수 있음
6. 논리연산자
    - True / False의 경우를 의미함 ⇒ 다양하게 사용 가능
    - Falsy : False는 아니지만 False 로 취급되는 다양한 값 ⇒ 0, 0.0, (), [],{},””
        - not 일경우에만 사용 가능
    - not ⇒ and ⇒ or 순으로 우선순위가 높음
    - 논리연산자의 단축평가 ⇒ 결과가 확실한 경우 중간에 멈춘 후 값을 반환하는 방법
7. 컨테이너(자료구조)
    - List : 여러개의 데이터를 모아놓은 집합 ⇒ 여러 자료형으로 저장 가능
        - numpy의 경우에는 자료형이 하나여야 함
    - Dictionary : Hash Table로 만들어진 값으로 List와는 다르게 대부분의 시간복잡도가 O(1)
    - tuple : 여러 개의 값을 순서가 있는 구조로 저장하고 싶을 때 사용 ⇒ 변경 불가
        - tuple은 재변경이 불가능하며 index로만 접근이 가능하다. (단일 항목)
        - tuple을 만들게 된다면 반드시 마지막에 ,(Training comma) 찍는다 ⇒ ex : tuple_a = (1,)
    - set : 중복되는 요소 없이, 순서에 상관없는 데이터들의 묶음 ⇒ 중복값 제거할때만 거의 사용
        - 담고 있는 요소의 삽입 변경, 삭제가 가능하다.
        - set은 index가 없으므로 slice가 불가능하다.
            
            A_set = {1,2,3,4}
            B_set = {1,2,3,"Hello",(1,2,3)}
            
            print(A_set | B_set) # 합쳐서 set하기
            print(A_set & B_set) # 같이있는거
            print(A_set - B_set)  # A_set에만 있는거
            
            print(A_set ^ B_set) # 교집합을 뺸 나머지
            
    - 형변환
        - 파이썬에서 데이터 형태는 서로 변환할 수 있음
        - 암시적 형 변환(Implicit) : 사용자 의도없이 파이썬 내부적으로 자료형을 변환
        - 명시적 형 변환(Explicit) : 특정 함수를 활용하여 의도적으로 자료형을 변환
</div>
</details>


<details>
<summary> 6st Day - off </summary>
<div markdown = "1">
   Python fstring
   * fstring의 경우 print를 하지 않아도 자동으로 가능하다.
</div>
</details>

<details>
<summary> 7st Day - off </summary>
<div markdown = "1">
  1. 조건문
    - 특정 조건에서 특정한 부분이 나올 수 있도록 하는 문법
    - 한줄 코딩 : (True인 값) if 조건 else (false인 경우의 값)
2. 반복문
    - for / While 2가지 반복문 방식이 있음
        - for : 보통 어떤 list를 하나씩 비교하거나 전체를 돌릴 때 사용
            - for student, grade in [Dic].items(): ⇒ key, value값
            - [Dic].keys(), [Dic].values로 나타낼 수 있음
            - for idx, number in enumerate([list]): ⇒ idx(index), number(해당list)
            - List comprehension : 리스트 안에 for, if문을 넣음으로써 간결화 시도
            - Dictionay_comprehension : {i : v for number in enumerate([list)} 방식
        - while : 어떤 특정한 조건일 때 사용
        - 반복문에서 자주 사용하는 용어
            - continue : 이후의 코드는 무시하고 다음 반복으로 돌아감
            - pass : 아무런 영향이 없음 (어떤걸 넣고 싶은데 애매할 때 일단 넣는 경우)
            - break : for문 자체를 중지시키는 경우
    - Python tutor : 코드를 한줄씩 돌릴 수 있는 프로그램 사이트 이름
3. 함수의 의미
    - Decomposition(분해) : 기능을 분해하고 재사용을 가능하게 한다.
    - Abstraction(추상화) : 복잡한 내용을 모르더라도 사용할 수 있도록 하는 재사용성
    - 함수의 종류
        - 내장함수 ⇒ 파이썬에 기본적으로 포함된 함수
        - 외장함수 ⇒ import문을 사용하여 외부 라이브러리에서 제공하는 함수
        - 사용자 정의 함수 ⇒ 사용자가 직접 만드는 함수
    - 값에 따른 함수의 종류
        - Void function ⇒ 명시적인 return 값이 없는 경우 None을 반환하고 종료
        - Value returning function ⇒ 함수 실행 후 return 값을 통해 반환함(함수 바로 종료)
    - def 안에 print vs return
        - print ⇒ 변수에 지정이 불가능하다, 바로 쓴다면 가능
        - return ⇒ 변수에 넣어도 가능 (그냥 return 써라)
    - Parameter와 Argument
        - Pararmeter : 함수 시 input 이름
        - Argument : 사용할 때 명시
    - keyword Arguments ⇒ (default = position argument)
        - 위치와 상관없이 Argument에서 Parameter이름을 명시하는 것
    - 정해지지않은 여러 개의 Arguments 처리
        - 가변인자(*args) ⇒ 여러 개의 Positional Arguement를 하나의 필수 parameter로 사용
    - 패킹과 언패킹
        - 패킹 ⇒ 여러 개의 데이터를 묶어서 변수로 할당
        - 언패킹 ⇒ 시퀀스 속의 요소들을 여러 개의 변수에 나누어 할당하는 것
            - numbers = [1,2,3,4]  a,b,*c =numbers 이면 c = [3,4]가 나옴
    - 가변 키워드 인자 ⇒ **를 이용하여 사용
        - Dictionary형태로 묶이는 방법
    - Python의 Scope 범위
        - global scope ⇒ 코드 어디에서나 쓸수 있는 공간
        - local scope ⇒ 함수가 만든 scope, 함수 내부에서만 사용 가능
    - 변수 생명주기(lifecycle) ⇒ LEGB Rule
        - built-in scope ⇒ 파이썬이 실행된 이후부터 영원히 유지
        - global scope ⇒ 모듈이 호출된 시점 이후 혹은 인터프리터가 끝날 때까지 유지
            - 프로그램이 돌아가면 계속 사용 가능
        - Enclosed scope ⇒ 지역 범위 한 단계 위 범위
        - local scope ⇒ 함수가 호출되고 생성되고, 함수가 종료될 때까지 유지
            - 함수가 쓸 때만 생성되고 함수가 끝나면 사라지는 경우
    - global문 ⇒ global [변수]
        - global문을 붙이는 순간부터 global이 되며 변수를 재선언하게되면 바꿔짐
        - parameter의 경우에는 global로 사용이 불가능하다.
    - nonlocal ⇒ nonlocal [변수]
        - global을 제외하고 가장 가까운 scope 변수를 연결하도록 함
        - 가장 가까운 변수를 한번만 바꾸는 경우일 때 사용
        - 가장 가까운 변수가 없을 때 nonlocal을 사용하면 에러가 난다
4. 함수의 응용
    - map(function, iterable) ⇒ function에 가능한 것 : 자료형 / lambda x: ~~
    - filter(function, iterable) ⇒ iterab
    - zip(list_a,list_b) ⇒ list_a , list_b의 요소 하나씩을 가져오는 함수
    - lambda [parameter] : 표현식
        - return문을 가질 수 없으며 조건문 / 반복문 불가능
        - 간결한 사용
    - 재귀함수 (recursive function)
        - 자기 자신을 호출하는 함수 / 1개 이상의 base case(종료 상황)을 둬야 한다.
        - 메모리 스택(Stack overflow) , 1000번 이상 재귀 시 Recursion Error 발생
5. 모듈
    - 라이브러리(library) > 패키지 > 모듈 순으로 모임 집합
    - 프레임워크(framework) ⇒ build가 되있는 상태
    - 파이썬에서 라이브러리 / 프레임워크를 설치하는 법 ⇒ pip
    - pip list (pip에 있는 패키지 확인), pip show Somepackage (무슨 패키지인지 알아보기)
    - pip freeze > requirements.txt  ↔ pip install -r requirements.txt (다운받은 패키지를 다른 컴퓨터에서 사용하고 싶을 때)
6. 모듈
    - 외부 라이브러리(패키지, 모듈)을 사용하는 경우 pip으로 설치를 해야하는데 이 때 회사 / 사람마다 외부 라이브러리 버젼이 다를 수 있음. 이럴 경우에 에러가 생기게 되므로 가상환경을 활성화시켜서 특정 환경에서의 패키지를 관리
    - python -m venv [venv] ⇒ 가상환경의 이름을 venv로 만들겠다.
    - source [venv]/Scipts/activate ⇒ 가상환경을 activate한다.
</div>
</details>

<details>
<summary> 8st Day - off </summary>
<div markdown = "1">
</details>

....

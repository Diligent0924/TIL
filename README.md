### Remote Repository 연결하기

Remote Repo 생성하기

Github

1. 기본 브랜치 이름 master로 변경하기
2. new Repo 생성 버튼 눌러서
   1. 이름 설정
   2. 만들기

### Local

1. 새로운 디렉토리 생성:
   1. mkdir(make directory)
   2. cd (경로)
   3. git init
   4. git remote add origin (원격 레포지트리 주소(url))
   5. git remote : origin 이름으로 remote 추가된 것 확인
   6. touch README.md
2. 비전남기기(remote repository로 push하기 전 반드시 commit 있어야한다.)
   1. git add(파일명, 확장자 파일명)
      * git add . 현재 위치한 wd 의 모든 수정사항
   2. git commit -m 'first commit'
3. git remote push origin master

만약 origin의 위치를 변경하고 싶을 경우
1. git remote remove origin (바꾸기 전 파일)
2. git remote add origin [코드] (바꾸고 싶은 파일)
3. git pull origin master --rebase (바꾸고 싶은 파일) => origin root

하나의 Repository에서 여러명이 사용하는 경우
1. git pull => 항상 최신 버전으로 가져온다. (Remote에서 Local로 끌고오는것)
2. git clone [코드] => 최신 버전을 clone한다.

conflict가 나오는 상황
1. 같이 일을 했을 때 A인 사람이 먼저 push하고 B가 이후 push하면 conflict
2. git pull
3. git commit (vim 환경에서 저장되어 있음) 
4. 'wq'로 저장 => commit의 수정한다. (그냥 push해도 상관없음)

Til Remote Repository 생성
1. Local File 변경
2. 기존의 Til Clone 한 후에 git clone 

이상하다
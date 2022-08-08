# TIL (Today I learned)
- 좋은 개발자가 되기 위해 하루동안 학습한 내용이나 개발관련 경험들을 기록으로 남긴다.
- 날짜를 표시하지 않는 이유는 조급해지지 않고 꾸준하기 위함이다.

## CLI 기초

- Git이란 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템이다

- Git Bash 사용 이유
  1. 명령어의 통일 
  2. UNIX 계열 운영체제의 명령어를 더 많이 사용하기 때문에 UNIX계열 터미널 명령어를 연습해야 한다.

- CLI 용어
  - 루트 디렉토리 : /, 모든 파일과 폴더를 담고 있느 최상위 폴더이고 C 드라이브를 의미
  - 홈 디렉토리 : ~, 틸드라고 부르며 C:/Users/사용자 계정을 의미.
  - 절대 경로 : pwd 루트 디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성한 것.
  - 상대 경로 : 현재 작업하고 있는 디렉토리를 기준으로 상대적 위치를 작성한 것. 
    - ./ 현재 작업하고 있는 폴더 
    - ../ 현재 작업하고 있는 폴더의 부모폴더

- 터미널 명령어
  - touch : 파일을 생성하는 명령어 touch a.txt
  - mkdir : 디렉토리를 생성하는 명령어 mkdir a.txt
  - ls : 현재 작업 중인 디렉토리의 폴더/파일 목록을 보여주는 명령어. 
    - ls -a : 숨김 파일까지 모두 보여줌
    - ls -a -l : long 옵션, 수정 날짜, 용량까지 보여줌
  - mv : 폴더/파일을 다른 폴더 내로 이동하거나 이름을 변경하는 명령어
    - mv text.txt folder 폴더 안에 넣음
    - mv text1.txt text2.txt 이름을 바꿈
  - cd : 현재 작업중인 디렉토리를 변경
    - cd ~ : 홈 디렉토리로 이동
    - cd .. : 부모 디렉토리로 이동
    - cd - : 바로 전 디렉토리로 이동
  - rm : 폴더/파일을 지우는 명령어
    - rm -r : 묻지 않고 지움
  - start : 폴더/파일을 여는 명령어
  
  ## Visual Studio Code
  - VS Code 사용 이유 : 가볍고 빠르다. 점유율이 높다. 확장성이 좋다.
  - Extensions란 기본 기능에서 확장하여 추가적인 기능을 가능하게 하는 일종의 플러그인.
  
  ## Markdown
  - Markdown 사용 이유 : 문서화, 시각화에 도움을 주는 기능.
    - 장점 : 직관적이고 쉽다. 관리가 쉽다
    - 단점 : 표준이 없어 문법이 상이하다. 모든 HTML 마크업 기능을 대신하지 못한다.
    - 기능 종류
      - #: 제목
      - -: 목록
      - *기울임*, **굵게**, ~~취소선~~
      - `코드`, ```python, ```, ```bash```
      - 링크 : [이름](주소)
      - 이미지 : ![대체 텍스트](이미지 주소)
      - 인용문: >인용 >>인용
      - 표 : |, -, :의 조합
      - ---: 수평선

## Git의 기초
- git config --global user.name "이름"
- git config --global user.email "메일 주소"
- git config --global --list

- Working Directory : 사용자의 일반적인 작업이 일어나는 곳
- Staging Area : 커밋을 위한 파일 및 폴더가 추가되는 곳
- Repository : Staging Area에 있던 파일 및 폴더의 변경사항(커밋)을 저장하는 곳

- git init : 현재 작업 중인 디렉토리를 Git으로 관리한다는 명령어 mater권한 부여
- git status : Working Directory와 Staging Area에 있는 파일의 현재 상태를 알려주는 명령어
  - Untracked : Git가 관리하지 않는 파일(한번도 Staging Area에 올라간 적 없는 파일)
  - Tracked : Git가 관리하는 파일
    - Unmodified : 최신 상태
    - Modified : 수정되었지만 아직 Staging Area에는 반영하지 않은 상태
    - Staged : Staging Area에 올라간 상태
- git add : Working Directory에 있는 파일을 Staging Area로 올리는 명령어
  - git add .
- git commit : Staging Area에 올라온 파일의 변경 사항을 하나의 버전(커밋)으로 저장하는 명령어, 각각의 커밋은 알고리즘에 의해 반환된 고유의 ID(해시 값)을 가진다.
  - git commit -m "커밋 이유"
- git log : 커밋 내역을 조회할 수 있는 명령어
  - git log --oneline

## Github
- 깃허브란 분산 버전 관리 툴인 깃 저장소 호스팅을 지원하는 웹 서비스이다
- 원격 저장소 생성 -> 로컬 저장소와 원격 저장소 연결 -> 원격 저장소에 업로드
- 등록 : git remote add origin 사이트 주소
- 조회 : git remote -v
- 삭제 : git remote rm origin
- 업로드 : git push origin master

## Git 기초 실습 - 문제풀기

> 아래에 있는 각각의 문제에 대해 답과 이유를 작성하시오.
> 한 문제를 풀 때 마다 커밋을 저장하시오. 커밋 메시지는 "solve 문제번호 problem"의 형태로 저장하시오.

()는 내가 푼 답

1. Git과 Github는 같다. (맞으면 O, 틀리면 X)

   - 답 : x (x)
   - 이유 : Git은 분산 버전 관리 `프로그램` Github는 온라인 저장소 `서비스` 
         (Git은 버전을 작업, Github는 저장소)

   

2. 터미널 명령어 `cd .`은 현재 위치의 부모 폴더로 이동하라는 의미이다. (맞으면 O, 틀리면 X)

   - 답 : x (x)
   - 이유 : `cd .`은 현재 폴더  (`cd ..`은 부모 폴더로 이동한다.)  



3. 마크다운 문법에서 글씨의 크기를 키우고 싶다고해서 본문을 제목으로 지정하면 안된다. (맞으면 O, 틀리면 X)
   - 답 : o (x)
   - 이유 : 마크다운은 글에 `역할`을 부여한다. 
         (제목으로 글씨 크기를 키울 수 있다. )


4. Git의 3가지 공간에는 Working Directory, Staging Area, Commits이 있다. (맞으면 O, 틀리면 X)
   - 답 : x (o)
   - 이유 : Commits이 아니라 `repository(저장소)`이다.   
    (working directory에서 작업하고, staging area에서 커밋 준비, commits에서 커밋을 저장한다.)



5. Commit ID는 중복 가능하다. (맞으면 O, 틀리면 X)
   - 답 : x (x)
   - 이유 : 각 커밋마다 고유한 ID(해시값)가 부여된다. (중복 불가능.)
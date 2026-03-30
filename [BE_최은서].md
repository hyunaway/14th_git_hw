git이란 소프트웨어 개발에서 코드를 관리 및 기록하고 체계적인 개발이 가능하도록 돕는 무료 공개 소프트웨어

-> 여러 사람과 기록 및 수정 할 때 체계적으로 해결
github로 다른사람의 변경사항을 바로바로 공유 가능


**개인
GIT 사용법
1. 한번만 세팅
- github에서 개인 레포지토리 생성 (public, README ON, .gitignore NO, license NO)
- 로컬에서 폴더 생성 후 사용자 등록 (터미널 -> ctrl+shift+~, 후 git bash 선택)
- 생성한 개인 레포지토리에 연결 (git config --global user.name 깃허브 아이디 / git config --global user.email 깃허브 이메일 --> git init, git remote add origin 레포지토리 주소, git remote -v, git branch -M main)

2. 계속 쓰이는 세팅
- 폴더에서 파일 수정 및 편집 (수정 전 : git pull origin main(깃허브의 main branch의 최신사항 반영))
- 폴더에서 파일 수정사항 반영 (add, commit) (git add ., git commit -m "")
- 폴더를 push하여 개인 레포지토리에 반영 (git push origin main)


**협업
1. 한번만 세팅
- github에서 중앙레포지토리 생성
- 중앙레포지토리를 fork하여 개인 레포지토리 생성(fork : 다른 사람의 레포지토리를 내 깃허브로 복사해오는 것)
- 폴더 생성 후 중앙과 개인 연결(git init, git remote add origin 개인레포주소, git remote add upstream 중앙레포주소 / git remote -v, git branch -M main)

2. 계속 쓰이는 세팅
- !먼저 upstream에서 PULL! (git pull upstream main : 중앙레포지토리에서 최신사항 반영)
- Branch 생성, 폴더에서 파일 수정 및 편집 (git branch, git branch 이름, git switch 이름, git branch -d 이름)
- 폴더를 push하여 개인 레포지토리에 반영(git add ., git commit -m "이름", git pull upstream main, git push origin "브랜치명")
- 개인 레포지토리에서 Pull Request하기
- 중앙 레포지토리에서 코드 확인 후 Merge 받기
- 폴더의 main 브랜치에서 수정사항 반영
- 예전 브랜치 삭제


GIT 충돌(conflict)
: 똑같은 위치를 서로 다르게 고치거나 / 수정 및 삭제가 동시에 일어나거나 / pull을 받지 않고 push 했을 때 일어남


DJANGO
: python으로 작성된 웹 어플리케이션 프레임워크
FRAMEWORK
: 소프트웨어 개발을 효율적으로 만들어주는 도구

**Django 개발환경 세팅
- 세션용 레포지토리 생성(public, README OFF, .gitignore NO, license NO)
- 로컬 폴더 생성 및 터미널 열기(ctrl + shift + ~)
- 리드미 생성 후 git 연결 (echo "# likelion_14th_session">>README.md, git init)
- 가상환경 설정 (python -m venv venv , source venv/Scripts/activate , touch.gitignore)
- .gitignore 설정 (gitignore.io에서 5개 추가해서 복붙)
- settings.py 설정
- APP 생성 (python manage.py startapp[main], 코드 중 INSTALLED_APPS에 'main' 추가)
- 서버실행 (python manage.py migrate, python manage.py makemigrations, python manage.py runserver)
- git 연동(git add ., git commit -m "메세지", git branch -M main, git remote add origin "주소", git remote -v, git push origin main)
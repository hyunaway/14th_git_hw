# 1주차 세션 요약

## git 사용법(개인)
1. Github에서 개인 레포지토리 생성
2. 로컬에서 폴더 생성 후, 사용자 등록(처음에만)  
- git config --global user.name 본인 깃허브 아이디  
- git config --globla user.email 본인 깃허브 이메일  
3. 생성한 원격저장소에 연결  
- git init : 이 폴더를 깃허브랑 연동  
- git remote add origin 레포지토리 주소 : 원격저장소 연결  
- git remote -v : 연결된 원격저장소 확인  
- git branch -M main  
- git pull origin main : 깃허브의 main branch의 최신 사항 반영  
4. 파일 수정 및 편집
5. 파일 수정사항 커밋  
- git add . : 현재 디렉토리(.) 아래의 모든 변경파일을 git이 추적  
- git commit -m "커밋 메세지" : 추적한 파일들을 실제 git 이력에 기록, -m 이후의 내용은 기록될 커밋 메세지  
6. 깃허브에 반영(push)  
- git push origin main : 커밋한 수정사항들을 origin 레포(remote)의 main 브랜치에 올린다  

## git 사용법(협업) 
1. Github에서 중앙레포지토리 생성
2. 중앙레포지토리를 fork하여 개인레포지토리 생성
- fork : 다른 사람의 레포를 내 Github 계정으로 복사해오는 것
- clone : 다른 사라므이 레포를 내 로컬(pc)에 복사
3. 폴더 생성 후 중앙레포지토리와 개인레포지토리에 연결
- git init
- git remote add origin 개인레포주소
- git remote add upstream 중앙레포주소
- git remote -v
- git branch -M main
- **Vranch 생성, 파일 수정 전 upstream에서 pull 받기!!**  
git pull upstream main : 중앙레포에서 최신사항 반영
4. Branch 생성, 폴더에서 파일 수정, 편집
- git branch : branch 목록 확인
- git branch 새 브랜치 이름 : 새 브랜치 생성
- git switch 브랜치 이름 : 해당 브랜치로 이동
- git branch -d 브랜치 이름 : 해당 브랜치 삭제
5. 파일 수정사항 반영
- git add .
- git commit -m "커밋 메세지"
- git pull upstream main
6. origin레포에 반영
- git push origin "현재 브랜치명"  
push : 깃허브에 올리기
7. 개인 레포지토리에서 pull request 하기
8. 중앙 레포지토리에서 코드 확인 후 merge 받기
9. 폴더의 main 브랜치에 최신사항 반영
- git switch main : main으로 이동
- git pull upstream main : 내 폴더에 중앙레포 최신사항 반영
- git push origin main : origin main에도 변경사항 반영
10. 예전 브랜치 삭제
- git branch -d "내 브랜치 이름" : 내 폴더의 내 브랜치 삭제 (로컬 브랜치 삭제)
- git push origin --delete "브랜치명" : 원격 저장소(origin)의 브랜치 삭제

## DJANGO
장고란 python으로 작성된 웹 어플리케이션 프레임워크  

### Django 개발환경 세팅
1. 레포지토리 생성 (README Off)
2. 로컬폴더 생성, 터미널 열기
3. 리드미 생성, git 연결
- echo "#폴더명" >> README.md
- git init
4. 가상환경 설정, gitignore 생성
- 가상환경 설정하기  
django가 다른 프로젝트에 영향을 끼치는 것을 막고자 프로젝트에 독립적인 환경을 조성
    1. 가상환경 생성 : python3 -m venv venv
    2. 가상환경 활성화 : source venv/bin/activate
- .gitignore 생성  
    touch .gitignore 입력  
5. settings.py 설정
6. app 생성
- 앱설치 : python manage.py startapp [app name]  
여기서 app name은 main으로 manage.py 파일이 있는 디렉토리에서 startapp 명령어를 쳐야됨
- settings.py에 INSTALLED_APPS에 main(설치한 앱) 등록
7. 서버실행
- migrate 하기  
    python manage.py migrate  
    python manage.py makemigrations
- 서버실행하기  
    python manage.py runserver
8. git 연동, git에 올리기
- git add . 
- git commit -m "커밋메세지"
- git branch -M main
- git remote add origin "원격저장소주소"
- git remote -v
- git push origin main
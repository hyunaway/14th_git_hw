# Git
소프트웨어 개발에서 버전 관리를 도와주는 공개 소프트웨어
## 사용법
- git init</br>
git 초기화
- git remote add [레포 별명] [원격 레포 주소]</br>
원격 저장소 등록. 일반적으로 개인 레포는 origin, 중앙 레포는 upstream으로.
- git add .</br>
수정된 변경 사항 모두 스테이징
- git commit -m "커밋 메세지"</br>
수정 사항을 커밋
- git pull [레포 별명] [브랜치 이름]</br>
원격 레포의 수정 사항을 로컬에 반영.
- git push [레포 별명] [브랜치 이름]</br>
원격 레포에 해당 브랜치 커밋을 반영. 
## 협업 시 절차
1. git add .
2. git commit -m "커밋 메세지"
3. git pull upstream main
4. git push origin [브랜치명]
5. 개인 레포 -> 원격 레포 PR 생성

# Django
Python 기반 웹 어플리케이션 개발 프레임워크
## 세팅 방법
1. 프로젝트 폴더 생성 및 git init
2. 가상환경 생성 및 활성화
3. Django 설치 및 settings.py 설정
4. APP 생성
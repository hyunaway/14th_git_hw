## Git(깃)

2005년 리누스 토르발스에 의해 개발된 분산 버전 관리 시스템으로 컴퓨터 파일의 변경 사항을 추적하고 파일들의 작업을 조율함
⇒ 소프트웨어 개발에서 코드를 관리, 기록하고 소프트웨어 버전 관리를 해줌, 체계적인 개발이 가능하도록 도와주는 무료 공개 소프트웨어

- Git: 내 컴퓨터에서 버전 관리
- GITHUB: GIT을 온라인으로 공유할 수 있는 플랫폼

## Git 사용법 (개인)

1. Github에서 개인 레포지토리 생성
2. 로컬에서 폴더 생성 후, 사용자 등록 
- VSC ⇒ ctrl+shift+~
- git bash 로 바꾸기
3. 생성한 원격 저장소에 연결
- git init: 이 폴더를 깃허브랑 연동
- git remote add origin 레포지토리 주소 (원격 저장소 연결)
- git remote - v (연결된 원격 저장소 확인)
- git branch -M main (기본 브랜치 이름 변경 master→main)
4. 파일 수정 전 변경사항 받아오기
- git pull origin main
5. 파일 수정사항 커밋, 깃허브에 반영 (push)
- git add . (현재 디렉토리 . 아래의 모든 변경 파일을 git이 추적)
- git commit -m “커밋 메세지” (추적한 파일들을 실제 Git 이력에 기록, -m 이후의 내용은 기록될 커밋 메세지)
- git push origin main (커밋한 수정사항들을 origin 레포의 main 브랜치에 올린다) 

## Git 사용법 (협업)

1. 레포 관리자가 Github에서 중앙레포지토리 생성
2. 중앙레포지토리를 fork하여 개인레포지토리 생성
3. 폴더 생성 후, 중앙레포지토리와 개인레포지토리에 연결 (origin, upstream)
- git init
- git remote add origin 개인레포 주소
- git remote add upstream 중앙레포 주소
- git remote -v (연결된 원격 저장소 확인, 4줄 뜸)
- git branch -M main
- git pull upstream main
4. Branch  생성, 폴더에서 파일 수정, 편집
- git branch (브랜치 목록 확인)
- git branch 새 브랜치 이름 (새 브랜치 생성)
- git switch 브랜치 이름 (브랜치 이동)
- git branch -d 브랜치 이름 (해당 브랜치 삭제)
5. 파일 수정사항 반영 (add, commit), origin 레포에 반영
- git add .
- git commit -m “커밋 메세지”
- git pull upstream main
- git push origin “현재 브랜치명”
6. 개인 레포지토리에서 Pull Request 하기
- Add a title: 수정한 내용 간단 요약
- Add a description: 수정한 내용에 대한 자세한 설명 추가
7. 중앙 레포지토리에서 코드 확인 후 Merge 받기
8. 폴더의 main 브랜치에 최신사항 반영
- git switch main (main으로 이동)
- git pull upstream main (내 폴더에 중앙레포 최신사항 반영)
- git push origin main (origin main에도 변경사항 반영)
- git branch -d “내 브랜치 이름”: 내 폴더의 내 브랜치 삭제 (로컬 브랜치 삭제)
- git branch origin —delete “브랜치명” (원격 저장소의 브랜치 삭제)
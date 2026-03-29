# 14th_git_hw
14기 깃 과제레포 
BE_권현서
멋사 1주차 

-git 사용법

1. Github에서 개인 레포지토리 생성
2. 로컬에서 폴더 생성 후, 사용자 등록
-1. 레포지토리와 똑같은 폴더 workspace 안에 생성
-2. vscode켜서 폴더 열기
-3. crtl + shift + ~ : 터미널 여는 명령어
-4. 아래 화살표 클릭 후 git bash 열기

3. 사용자 등록
-1. git config —global user.name 내 깃허브 아이디
-2. git config —global user.email 내 깃허브 이메일
내 컴퓨터에서 한 번만 설정해두면 다음 레포지토리 만들 때부터는 안 해도 됨

4. 생성한 원격 저장소에 연결
-1. git init : 이 폴더를 깃 허브와 연동
-2. git remote add origin 레포지토리 주소 : 원격 저장소 연결
-3. git remote –v : 연결된 원격 저장소 확인
-4. git branch –M main : 기본 브랜치 이름 master  main으로 변경

5. 파일 수정 전 변경 사항 받아오기
-1. git pull origin main : 깃허브의 main branch의 최신 사항 반영

6. 파일 수정, 편집(저장)
-1. git add . : 현재 디렉토리(.) 아래의 모든 변경 파일을 git이 추적
-2. git commit –m “커밋 메시지” : 추적한 파일들을 실제 Git 이력에 기록, -m 이후의 내용은 기록될 커밋 메시지
+pull 한 번 push 전에 해주는 것 추천!
-3. git push origin main : 커밋한 수정 사항들을 Origin 레포(remote)의 main 브랜치에 올림 (push)
-Ctrl + S : 저장

*깃허브(remote = 원격 = 깃허브에 올라간거) = Origin 레포

-git 협업

1. Github에서 레포지토리 생성(=중앙레포지토리)
2. 각 팀원들은 중앙레포지토리를 fork하여 개인 레포지토리 생성
3. 폴더 생성 후, 중앙레포지토리와 개인레포지토리에 연결(origin=개인 레포, upstream=중앙 레포)
위 과정들은 프로젝트 처음에 한번만 설정

4. 작업 시작하기 전 upstream에서 pull
5. Branch 생성, 폴더에서 파일 수정, 편집
6. 폴더에서 파일 수정 사항 반영(add, commit)
7. 폴더를 push하여 개인 레포지토리에 반영
8. 개인 레포지토리에서 Pull Request하기
9. 중앙 레포지토리에서 코드 확인 후 Merge 받기
10. 폴더의 main 브랜치에 수정사항 반영
11. 예전 브랜치 삭제(위 과정 반복)
위 과정들은 프로젝트 내내 반복

-fork : 다른 사람의 레포지토리를 내 계정으로 복사해 오는 것
중앙 레포지토리를 fork하여 개인 레포지토리 생성

*순서 정리
1. 레포 관리자가 Github에서 중앙 레포지토리 생성
2. 중앙 레포지토리를 fork하여 개인 레포지토리 생성
3. 폴더 생성 후, 중앙 레포지토리와 개인 래포지토리 연결(origin, upstream)
-1. 폴더 생성(만들어 둔 workspace 안에 만들기, 폴더명은 깃허브와 통일)
-2. VSCode로 해당 폴더 열기
-3. 상단 Terminal -> new Terminal (cntr ++ shift + ~)
4. git init : 이 폴더를 깃허브랑 연동(아직 연동할 깃허브 경로는 설정되지 않음)
5. git remote add origin 개인레포주소
6. git remote add upstream 중앙레포주소
7. git remote –v (연결된 원격 저장소 확인, 4줄 다 뜨면 good)
8. git branch –M main (기본 브랜치 이름 master  main으로 변경)
9. ✰ Branch 생성, 파일 수정 전 upstream에서 Pull 받기
10. Branch 생성, 폴더에서 파일 수정, 편집
-1. git branch 새 브랜치 이름 : 새 브랜치 생성
-2. git branch : branch 목록 확인
-3. git switch 브랜치 이름 : 브랜치 이동
-4. git branch –d 브랜치 이름 : 해당 브랜치 삭제
11. 폴더의 main 브랜치에 최신사항 반영
12. 예전 브랜치 삭제 
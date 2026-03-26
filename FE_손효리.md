GIT 사용법 (개인)

1. Github에서 개인 레포지토리 생성
2. 로컬에서 폴더 생성 후, 사용자 등록
    --> git config --global user.name 깃허브 아이디
    --> git config --global user.name 깃허브 이메일
    을 통해서 사용자 등록! 본인 컴퓨터에서 한 번 해두면 다음 레포만들 때 하지 않아도 됨.
3. 생성한 개인 레포지토리에 연결
    --> git init 로 이 폴더를 깃허브랑 연동
    --> git remote add origin 레포 주소를 통해 깃허브에 연결
3.5 파일 수정전 변경사항 받아오기
    --> git pull origin main
4. 파일 수정, 편집
5,6. 파일 수정사항 커밋, 깃허브에 반영
    --> git add . 현재 디렉토리 아래 모든 변경 파일을 git이 추적
    --> git commit -m "커밋메시지" 추적한 파일들 git이력에 등록 후 메시지와 함께 기록
    --> git push origin main 커밋 수정사항들 orgin레포의 main 브랜치에 올림

GIT 사용법 (협업)

1. 레포 관리자가 Github에서 중앙레포 생성
2. 중앙레포를 fork하여 개인레포 생성
3. 폴더 생성 후, 중앙레포와 개인 레포에 연결
    --> git init
    --> git remote add oring 개인레포주소
    --> git remote add upstream 중앙레포주소
    --> git remote -V 연결된 원격 저장소 확인
    --> git branch -M main 
3.5 Branch 생성, 파일 수정 전 upstream에서 pull받기
    --> git branch 새 브랜치 이름
    --> git switch 브랜치 이름  브랜치 이동
4. Branch 생성, 폴더에서 파일 수정, 편집
5,6. 파일 수정 사항 반영, origin레포에 반영
    --> git add .
    --> git commit -m "커밋메시지"
    --> git push orign "현재 브랜치명"
7. 개인 레포에서 Pull Request하기
8. 중앙레포에서 코드 확인 후 Merge받기
9. 폴더의 main브랜치에 최신사항 반영
    --> git switch main
    --> git pull upstream main
    --> git push origin main
10. 예전 브랜치 삭제
    --> git branch -d "내 브랜치 이름"
    --> git push origin --delete "브랜치명"
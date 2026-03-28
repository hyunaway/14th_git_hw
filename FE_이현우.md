3/25 1주차 세션 내용 요약

Git : 분산 버전 관리 시스템으로 컴퓨터 파일의 변경 사항을 추적하고 작업을 조율하는 프로그램
-> 이는 소프트웨어 개발에서 코드의 관리, 기록에 용이하고 버전도 알아서 관리 해주기 때문에 협업에 효율적인 공개 소프트웨어다

Github : Git 저장소 호스팅 서비스 및 공동 협업 플랫폼

Github없이 Git만 사용하여 여러 사람과 개발을 하게 되면?
-> 개인의 컴퓨터에서만 기록을 관리하기 때문에 하나의 노트북으로 돌려가며 개발하기 or 아주 사소한 수정사항에도 일일히 공유해야 하고 직접 반영해기

= Git과 Github는 같이 사용해야 최적의 환경에서 협업 개발이 가능하다

how to use Git and Github

1. 개인

1) Github에서 개인 레포지토리를 생성한다
   레포지토리 이름, 설명, 공개 여부, readme 생성 여부, license 등을 설정하고 생성
2) 초기 환경 세팅(사용자 등록)
   로컬에서 폴더를 생성하고 본인의 이름과 가입 이메일을 입력한다
   -> 본인 컴퓨터에서 한번만 해두면 그 이후에는 따로 진행하지 않아도 된다
3) 생성한 원격저장소에 연결
   git init : 이 폴더를 깃허브에 연동
   git remote add origin 레포지토리 주소(복붙) : 원격 저장소 연결
   git remote add -v : 연결된 원격 저장소 확인
   git branch -M main (기본 브랜치 이름을 main으로 변경)
   **모든 작업을 수정하기 전에 변경사항을 받아오는 것을 습관화 하자**
   git pull origin main : 최신 변동 사항을 반영 (pull)
4) 수정 사항 반영
   git add . : 현재 디렉토리(.) 아래의 모든 변경 파일을 Git이 추적
   git commit -m “커밋 메세지" 변경한 사항을 텍스트로 작성
   git push origin main : 수정사항들을 Origin 레포(remote)의 main 브랜치에 올린다(push)

2. 협업(중앙, 개인 레포지토리로 구분됨)

1) 개인 레포지토리 생성
   중앙 레포지토리(현재까지 작업이 완료된 파일이 들어있는 레포지토리) fork(복사)
   -> 개인 작업 환경 생성
2) 폴더 생성 후 중앙,개인 레포지토리에 연결
   git init : 해당 폴더를 깃허브랑 연동
   git remote add origin 개인레포주소
   git remote add upstream 중앙레포주소
   git remote -v : 연결된 원격 저장소 확인
3) 중앙 레포지토리 pull 받기
   git pull upstream main : 최신 변동 사항을 반영 (pull)
   git branch : 목록 확인
4) 수정 사항 반영
   git add .
   git commit -m “커밋 메세지”
   _git pull upstream main_ -> 내가 수정하는 사이에 다른 개발자가 수정한 사항이 있을 수 있으므로!
   git push origin “현재 브랜치명"
5) 개인 레포지토리에서 Pull Request 하기
6) 중앙 레포지토리에서 확인 후 merge(합병)
7) main branch에 최신 사항 반영 및 기존 브랜치 삭제

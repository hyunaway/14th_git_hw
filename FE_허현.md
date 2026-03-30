Git -> 개인의 분산버전 관리 시스템
Github -> Git의 온라인 공유 플랫폼

개인
1. Githib에서 개인 레포 생성
2. 로컬에 폴더 생성 및 vs로 열기 (이때 터미널을 git bash로 변경)
3. 로컬폴더를 깃허브와 연동/ git init
4. 깃허브랑 연동은 시켯지만 어떤 레포랑 연결할지 정해지지않아 경로를 설정/ git remote add origin ~
5. 최신사항 가져오기/ git pull origin main
(먼저 git branch -M main 기존브랜치 이름 main으로변경)
6. 저장 및 브랜치 올리기/ git add . -> git commit -m "~" -> git push origin main

협업
개인과 유사하지만 fork,upstraming개념 도입
1. 중앙레포를 개인레포로 가져옴/ fork사용
2. 개인의 4번까지 진행 + 중앙레포 주소 연결/ git remotr add upstream ~
3. 개인의 5번까지 실행 + 브랜치(main의 복사본 생성 및 이동)/ git branch ~ -> git switch ~
4. 개인의 6번까지 실행 + push전에 pull을해 충돌 문제 예방
5. 중앙레포에 머지하기

충돌
1. 같은파일 같은줄 다른수정
2. 한명 수정,한명 삭제
3. pull받지않고 push시

자료의 예시
1. 업스트림에서 무빙건 -> 프짱으로 변경
2. 로컬에서 pull을 받지 않고 내용을 수정함 (로컬은 무빙건인 상태에서 푸근짱으로)
3. 이로인한 위3의 충돌 발생

해결법
1. Github를 통한 해결(pull안하고 push)
-> 현재변경사항 승인 (Accept current change)
-> 다시 머지 이후 pull을 통한 충돌해결 반영
2. VS를 통한 해결(push 전에 pull할때)
-> Rebase와 Merge를 추천해줌 이때 Merge를 사용
-> pull받고 직접수정
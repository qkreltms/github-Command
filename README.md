# 깃 명령어 정리 <br>
git init<br>
git --help<br> 
git log (종료 q)<br>
git clone<br>
# branch가 2개 이상일 경우 git pull할 시,<br>
There is no tracking information for the current branch.<br>
Please specify which branch you want to merge with. 가 뜰 수 있다.<br>
로컬 branch에서 어느 branch로 pull 해야할지 모르는 경우 뜸으로<br>
git pull origin master<br>
또는<br>
git branch --set-upstream-to=origin/master master<br>
git pull<br>
# 깃 허브 커밋 방법
git add * <br>
git commit -m "first commit!" //git add * 없이 하고싶다면, git commit -all -m "first commit!"<br>
git push origin master <br>
# 깃 허브에서 파일 가져오기
git clone <url><br>
# 깃 허브 유저 등록
git config credential.helper store<br>
를 입력후 push 할 때 비밀번호, 아이디를 입력하면 다음에 묻지 않는다.<br>
# 새로운 branch 생성 후 branch 변경
git branch testing<br>
git branch //branch 생겼는지 확인<br>
git checkout testing// git checkout -b testing 으로 한번에 할 수도 있다.<br>
# branch 이동
git checkout testing //head가 testing branch로 이동한다.<br>
# branch 삭제
git branch -d testing
# branch 합치기
git merge master //testing branch에서







# branch가 2개 이상일 경우 git pull할 시<br>
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
# conflict 처리 방법
다른 branch와 같은 파일을 수정할 경우 conflict가 발생한다.<br>
"<<<<<<< HEAD" 이 부분이 현재 작업하고있는 branch 시작이고,<br>
"=======" 끝을 가리킨다. 이 다음 바로아래에는 병합하려는 대상 branch의 중복된 부분이 나온다.<br>
">>>>>>> master" 이 부분은 병합하려는 대상 branch의 중복된 부분의 끝 지점이다.<br>
충돌 부분을 처리하고 git add *, git status를 입력 후<br>
"All conflicts fixed but you are still merging."이 뜨는지 확인하자.<br>
뜨는것을 확인 후 git commit -m "test"<br>
참고로 자동으로 conflict를 처리해주는 git mergetool 이라는 것도있다.<br>
# 현재 branch 상태 그래프로 보기
git log --oneline --decorate --graph --all
# branch 이름 변경하기
git branch -m 변경전_branch_name 새로운_branch_name
# merge vs rebase
참고 주소<br>
<https://git-scm.com/book/ko/v1/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-Rebase%ED%95%98%EA%B8%B0><br>
# pull vs fetch
pull = fetch + merge<br>
fetch: 새로운 fetch_head branch를 만들어주고, 이것과 merge 해야 됨
# reset 이미 깃허브에 push 한 것을 이전으로 되돌리기
git reset 483452d //원하는 커밋 위치로 되돌리기 (이전 소스코드 내용은 그대로 둔체로)
git commit -m "..."  //되돌린 부분에서 커밋
git push origin +master //remote repository를 강제로 revert
참고: http://hochulshin.com/git-revert-changes/





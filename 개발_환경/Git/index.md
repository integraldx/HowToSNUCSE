# Git
[공식 사이트](https://git-scm.com/)

Git은, 개발중인 프로그램의 소스코드를 관리하고, 더 나아가 팀원들과 공유하기 위한 분산형 버전 관리 시스템(Distributed Version Control System)입니다.  
이를 사용하면 소스코드 분할을 이용한 팀원 간의 협업이 더욱 원활해지고, 작업 기록을 명시적으로 남길 수 있으며, 작업 도중에 있는 코드를 프로덕션 코드(실제 서비스에 사용될 코드)와 분리할 수 있습니다.

## 설치하기
 - 윈도우 / 맥: 공식 사이트에서 설치 파일을 제공합니다
 - 리눅스: 사용하는 배포판의 패키지 매니저에 포함되어 있습니다.

## 간단한 기초 사용법
`※ 터미널 사용을 가정합니다. Github Desktop, GitKraken과 같은 클라이언트들에 대한 사용법은 다른 문서들을 참고해주세요.※`
### add와 commit
1. 새로운 폴더를 만들고, 폴더 안으로 이동 후 `git init`을 실행합니다.
   - 이를 실행하고 나면, 새로운 폴더는 git repository가 됩니다.
2. `git status` 를 실행해 보면 현재 상태가 나타납니다.
   1. `On branch master` : 현재 `master` 브랜치에 있다는 뜻
   2. `No commits yet` : 아직 아무런 커밋이 없다는 뜻
   3. `nothing to commit` : 커밋할 파일이 없다는 뜻
3. 새로운 파일 `hello.c`를 생성해봅시다. 이후 `git status`를 실행하면 정보가 바뀝니다.
   1. `Untracked files, hello.c` : git 리포지토리에 등록되지 않은 파일 `hello.c`가 존재한다는 뜻
4. 이제 `git add hello.c`를 실행하면, `hello.c`가 커밋을 위해 *스테이지*됩니다. `git status`로 확인해볼 수 있습니다.
5. `git commit`을 실행하면, 현재 *스테이지*된 파일들이 *커밋*됩니다.
   1. 사용자 정보가 설정되지 않았다면, `git config`를 하라는 메세지가 나옵니다. 메세지에 나온 명령어대로 자신의 이메일과 이름을 입력하면 됩니다.
   2. 명령어 실행 후, *커밋 메세지*를 수정하는 창이 나타납니다(보통 vim입니다. 따로 설정을 거치지 않았다면 한글이 입력되지 않을 수 있습니다.). 메세지를 수정하고 종료하면 커밋이 완료됩니다.
   3. 만약 커밋 메세지를 짧게 한 줄로 나타내고 싶다면, `git commit -m "COMMIT MESSAGE"`를 실행하면 됩니다.
6. 커밋이 완료되고 나면, `git log`를 통해 커밋 로그를 확인할 수 있습니다.

### branch와 merge
1. `git branch new-branch` 를 통해 **현재 존재하는 브랜치로부터** 새 브랜치 `new-branch`를 만들 수 있습니다. 지금은 `master`로부터 만들어졌을 것입니다.
2. `git checkout new-branch` 를 통해 브랜치를 넘어갈 수 있습니다. `git status`로 현재 어느 브랜치에 있는지 체크할 수 있습니다.
3. 위에 적힌 방식대로, `new-branch`에서 몇개의 파일을 추가하고 커밋해봅시다.
4. 추가된 파일들은, `new-branch`에는 존재하지만, `master`에는 존재하지 않습니다.
5. 이제 `git checkout master` 를 통해 `master` 브랜치로 돌아와봅시다. 만든 파일이 사라집니다.
6. `merge`를 통해 `new-branch`에 있는 수정사항들("커밋"들)을 반영할 수 있습니다. `master`브랜치 위에서 `git merge new-branch`를 실행합니다.
7. 폴더를 확인해보면, 만든 파일들이 다시 생겨난 것을 볼 수 있습니다. `new-branch`에 있던 수정사항들이 `master`에 반영되었기 때문입니다.
8. `git log` 를 실행하여, 반영한 수정사항들을 볼 수 있습니다.

## Git의 이해를 위한 세부 사항들
- [.gitconfig](gitconfig.md)
- [파일의 상태](files.md)
- [커밋](commit.md)
- [브랜치](branch.md)
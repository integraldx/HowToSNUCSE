# 파일의 상태
Git Repository 안의 파일들은 모두 어떠한 상태를 가지게 됩니다.
그 목록은 다음과 같습니다.  
- Untracked
- Unmodified
- Modified
- Staged

## Untracked
Untracked 파일들은 git의 관리를 받지 않는 파일들을 말합니다.
이 파일들은 .gitignore에 의해 무시된 파일일수도 있고, 그저 새로 만들고 커밋되지 않은 파일일수도 있습니다.
이 파일들은 `git add <file>` 명령을 통해 **Staged** 상태로 넘어갈 수 있습니다.

## Unmodified
Unmodified 파일들은 git의 관리를 받고 있지만, 가장 마지막 커밋으로부터 아무런 수정사항도 가해지지 않은 파일을 말합니다.
만약 이 파일을 수정하게 된다면, 자동으로 **Modified** 상태로 넘어가게 됩니다.
또는, `git rm <file>` 명령을 통해 더 이상 git의 관리를 받지 않도록 **Untracked** 상태로 만들 수도 있습니다.

## Modified
Modified 파일들은 git의 관리를 받고 있고, 가장 마지막 커밋 이후로 어떠한 수정사항이 가해진 파일을 말합니다.
이런 파일들은 `git add <file>` 명렁을 통해 **Staged** 상태로 넘어갈 수 있습니다.
또는, 만약 가한 수정사항을 이전으로 되돌리고 싶다면, `git checkout -- <file>`명렁을 통해 **Unmodified** 상태로 되돌릴 수 있습니다.

## Staged
Staged 파일들은 `git add <file>` 명령 등을 통해 index에 추가되어있는 파일들을 말합니다.
이 파일들은 `git commit` 명령을 통해 index에 들어있는 정보를 토대로 새 커밋을 작성함으로써 **Unmodified** 상태가 될 수 있습니다.
또는, `git reset HEAD <file>` 명령을 통해 **Modified** 상태로 되돌릴 수 있습니다.
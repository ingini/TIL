# Git

> git은 소스코드 현상(버전)관리 도구이다. 

## 기본명령어 

1. 저장소(`repository`) 만들기

   ```bash
   $ Git init
   Initialized empty Git repository in
   c:/Users/user/Desktop/TIL/.git/
   
   user@teacher MINGW64 ~/Dsektop/TIL (master)
   $ 
   ```

   ```bash
   내가 원하는 폴더를 git으로 관리하는 저장소로 초기화한다.
   (`master`) 라는 표기를 통해 해당 폴더가 git repository라는 것을 확인할수 있다.
   (더 정화학하게는 해당 폴더에 숨김 폴더에 .git이 있다.)
   ```

   

2.  `git add` - 커밋할 목록에 추가하기

   git add . 에서 . 은 현재 디렉토리를 뜻하는 리눅스 표기법이다. 현재 디렉토리의 변경 사항들을 모두 커밋할 목록에 담아둔다는 뜻이다.

   git add git.md 라고 하면, 특정 파일만 올릴 수도 있고, git add myfolder/ 라고 하면, 특정 폴더를 모두 담아둘 수도 있다.

   ``` bash
   $ git add .
   
   Changes to be committed:
     (use "git rm --cached <file>..." to unstage)
   
           new file:   Git.md
   
   ```

3.  커밋

   커밋은 버전의 이력을 남기는 것이다. 커밋할 목록에 있는 내용들을 버전에 포함시킨다. (untracked / 목록에 없는 것은 포함 안됨.)

   ```bash
   $ git commit -m '커밋메세지'
   ```

4.  커밋 이력 확인하기

   ```bash
   $ git log
   commit 073eb95bc65e6c19b710347c5eb71739fc113c1a (HEAD -> master)
   Author: ingini <ingini@gmail.com>
   Date:   Tue May 21 12:40:52 2019 +0900
   
       Git 기초 명령어 정리
   
   ```

5. ##  git 상태 확인하기

   ```bash
   $ git status 
   ```

   CLI(Command Line Interface)에서는 현재 상태를 확인하기 위해서 지속적으로 확인해야 한다.

## 원격 저장소 활용하기 (Github)

1. 원격 저장소 등록하기

   ```bash
   $git remote add origin
   https://github.com/ingini/TIL.git
   ```

    https://github.com/edutak/TIL.git 라는 주소를 `origin` 이라는 원격 저장소 이름으로 추가(`add`) 한다.

   

2. 원격 저장소 등록은 최초에 한번만 하면 된다.

   ```bash
   $ git remote -v 
   ```

   

   2. 원격 저장소 올리기

      ```
      $ git push origin master
      ```

      `origin` 이라는 이름의 원격저장소에 올린다(push)

   

3. 저장소로부터 복제하기

   ```
   $ git clone
   https://github.com/ingini/TIL.git
   ```

    주소는 github에서 우측에 있는 초록색 버튼(clone)을 눌러서 얻을 수 있음.

    해당 명령어는 집 혹은 노트북에서 작업하려고 할 때 받아서 쓸 수 있다.

tip ! 마크다운 사용법 총정리

[링크](<https://heropy.blog/2017/09/30/markdown/>)
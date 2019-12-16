## Git 기초

### 0.준비 사항

- [git bash](http://it.chosun.com/site/data/html_dir/2019/07/07/2019070700064.html)
- git을 활용하기 위한 CLI(Command Line Interface)를 제공한다. 
  - source tree, github desktop등을 통해 GUI 환경에서도 활용가능하다. 
  
## 1. 로컬저장소 활용하기

### 1. 저장소 초기화

```bash
$git init
Initialized empty Git repository in C:/Users/student/Desktop/TIL/.git/
```

  저장소(repository)를 초기화 하게 되면, .git 폴더가 해당 디렉토리가 생성된다. 

- bash 창에서는 (master) 라고 표기된다. 
  - 현재 브랜치가 master라는 것을 의미함.

### 2. add - staging area

> git으로 관리되는 파일들은 Working directory(작업환경), Staging Area, commit 단계를 거쳐 이력에 저장된다. 

```
$ git add a.txt # 파일명
$ git add images/ # 폴더명
$ git add . # 현재 디렉토리의 모든 파일 및 폴더  
```

- add 전 상태

  ```bash
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        image/
        markdown.md

nothing added to commit but untracked files present (use "git add" to track)

student@M16022 MINGW64 ~/Desktop/TIL (master)

  
  ```

 

## 3. commit

> 커밋은 코드의 이력을 남기는 과정이다. 

```bash
$ git commit -m 'commit message'
```

- 커밋 메세지는 항상 해당 이력에 대한 정보를 담을 수 있도록 작성하는 것이 좋다. 
- 일관적인 커밋 메세지를 작성하는 습관을 들이자. 
- 이력 확인을 위해서는 아래의 명령어를 활용한다. 
- 항상 status 명령어를 통해 git의 상태를 항상 확인하자. 

```
git remote add origin https://github.com/peterschoice/gitclass.git
git push -u origin master
```



## 원격 저장소 활용하기 

> 원격 저장소를 제공하는 서비스는 다양하게 존재한다. github을 기준으로 설명한다. 



### 1. 원격저장소 설정

```bash
$ git remote add origin {github url}
```

- {github url} 부분에는 원격저장소 url을 작성한다. 
- 원격 저장소(remote)로 {github url}을 origin 이라는 이름으로 추가(add)하는 명령어이다. 
- 원격 저장소 목록을 보기 위해서는 아래의 명령어를 활용한다. 

```bash
$ git remote -v
origin  https://github.com/peterschoice/gitclass.git (fetch)
origin  https://github.com/peterschoice/gitclass.git (push)
```

### 2. push

```bash
$git push origin master 
```


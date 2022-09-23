# Git-for-Archaeologists / 고고학자를 위한 깃

* 본 레포지토리는 고고학 연구자에게 Git과 Github를 소개하고자 작성되었습니다.
* Git과 Github를 활용하여 개인연구, 공동연구를 관리하는 방법을 살펴봅니다.
* 문의는 Issue 혹은 E-mail을 통해 연락주세요.

## 목차

1. [Git?, Github?](#git?,-github?)
2. [기본 터미널 명령어](#기본-터미널-명령어)
3. [Git 기본용어](#git-기본용어)
4. [Git 기본 명령어](#git-기본-명령어)
5. [Git을 활용한 개인연구 관리](#git을-활용한-개인연구-관리)
6. [Git을 활용한 협업](#git을-활용한-협업)

## Git?, Github?

&nbsp; Git은 Linus Torvalds에 의해 개발된 **분산 버전 관리 시스템**입니다. 다양한 파일의 변경사항을 기록하여, 추후 필요할 때 이를 확인하거나 되돌릴 수 있습니다. 또한 여러 사람이 함께 하나의 프로젝트, 연구, 개발을 진행할 때 효율적으로 협업을 할 수 있게 해줍니다. Git을 사용하면 인터넷이 불가능한 지역에서도 작업이 가능하며, 자연스럽게 백업이 되어 컴퓨터가 분실 혹은 고장나도 복구가 가능합니다(Push까지 무사히 끝낸 경우). 무엇보다 가장 큰 장점은 다양한 사람들이 함께 협업하는 상황속에서도 깔끔하게 프로젝트, 연구, 개발을 진행할 수 있다는 것입니다.

&nbsp; **Github**는 Git을 사용하는 프로젝트를 지원하는 웹 호스팅 서비스입니다. 즉 Git을 사용하는 **프로젝트의 서버** 역할을 담당해줍니다. Git을 웹에서 편히 사용할 수 있게 해주는 도구로 버전 관리, 코드 확인, 버그 정리를 할 수 있으며 블로그, SNS, 포트폴리오 정리의 기능을 해주기도 합니다.

*깃허브 가입 및 세팅은 아래의 링크를 참조해주시기 바랍니다.<br>
[Github 가입](https://www.lainyzine.com/ko/article/how-to-create-github-account/) / [Git 설치(Windows)](https://goddaehee.tistory.com/216) / [Git 설치(MacOS)](https://velog.io/@wijoonwu/Mac-OS-%EC%97%90%EC%84%9C-Git-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0)

## 기본 터미널 명령어

&nbsp; Git을 사용하는 방법은 크게 두 가지가 있습니다. 첫 번째, **GUI 프로그램** 입니다. GUI 프로그램은 우리가 평소에 사용하는 프로그램처럼 GUI로 되어 있어 사용이 간편합니다. 하지만 할 수 있는 작업이 적다는 치명적인 단점이 있습니다. 두 번째, **터미널 명령어(CLI)를 활용하는 방법**입니다. 이 방법의 경우, 모든 기능을 사용할 수 있습니다. 하지만 어렵다는 단점이 있습니다(물론 숙달되면 간단합니다.)

&nbsp; 본문에서는 **두 번째 방법(터미널 명령어를 활용한 방법)**을 사용하고자 합니다. 다소 생소하여 어렵게 느껴질 수 있지만, 작업 흐름을 익히시면 금방 적응되실겁니다. 본문에는 자주 사용하는 명령어만 기재한 것입니다. 실제로는 훨씬 많은 명령어가 있습니다.

&nbsp; 모든 명령어는 대상 파일 혹은 폴더의 상위 디렉토리에서 사용되거나, 대상 파일 혹은 폴더의 정확한 주소를 기입하여 사용해야합니다.

### 1) cd / 디렉토리 이동
```bash
cd 디렉토리 주소

Ex) cd /chantore/Research


cd .. / 상위 디렉토리로 이동

Ex) cd..
```
디렉토리를 이동하는 명령어. 'cd ..' 의 경우 현재 디렉토리의 상위 디렉토리로 이동합니다.

### 2) ls / 디렉토리 확인
```bash
ls

Ex) ls
```
디렉토리를 확인하는 명령어.

### 3) cp / 복사
```bash
cp 복사할-대상-주소 복사될-주소

Ex) cp /Desktop/masterdata.csv /chantore/research/data
```
파일 혹은 폴더를 복사하는 명령어.

### 4) mv / 파일 혹은 폴더 위치 변경
```bash
mv 이동-대상-주소 이동될-주소

Ex) mv /Desktop/masterdata.csv /chantore/research/data
```
파일 혹은 폴더의 위치를 변경하는 명령어. 우리가 흔히 사용하는 ctrl + c, ctrl + v 라고 생각하면 됩니다.

### 5) pwd / 주소 확인
```bash
pwd

Ex) pwd
```
현재 위치의 주소를 확인하는 명령어.

### 6) clear / 터미널 창 초기화
```bash
clear

Ex) clear
```
터미널 창을 깨끗하게 초기화. 명령어를 많이 입력하여 터미널 창이 지저분할 때 사용하시면 됩니다.

### 7) mkdir / 디렉토리 생성
```bash
mkdir 새로운-디렉토리-이름

Ex) mkdir new-research
```
폴더를 생성하는 명령어.

### 8) cat / 파일 확인
```bash
cat

Ex) cat script.R
```
파일의 내용을 출력하는 명령어. 단순 출력이기 때문에 편집은 불가능합니다.

### 9) rm / 파일 혹은 폴더 삭제
```bash
rm 삭제할-파일-혹은-폴더

Ex) rm trashfile.txt


rm -rf 삭제할-파일-혹은-폴더

Ex) rm -rf trashfile.txt
```

### 10) vi / vi 에디터로 열기
```bash
vi 파일명

Ex) vi /chantore/research/script.py
```
vi 에디터로 파일을 편집할 수 있게 해주는 명령어.

## Git 기본용어

&nbsp; Git의 기본적인 용어에 대해 살펴봅니다. 이러한 용어는 뒤이어 살펴볼 Git의 기본 명령어에서 그대로 사용되는 경우가 많기 때문에 숙지가 필요합니다.

**1. Repository**<br>
	&nbsp;**- Remote Repository** : **원격 서버**에 위치하는 저장소(일종의 중앙 저장소)<br>
	&nbsp;**- Local Repository** : 개발자가 작업하는 **개인 PC의 저장소**<br>
	
**2. Clone** : 원격 저장소의 내용을 로컬 저장소로 복사하는 행위<br>

**3. Branch** : **독립적인 작업을 위한 분기점,** 작업을 할 때는 Branch를 생성하여 작업한다. 작업이 끝난 경우, 이를 병합하고 사용한 Branch를 삭제하여 마무리한다. Branch를 통해 협업시 충돌을 방지할 수 있으며, 작업 흐름을 한눈에 파악할 수 있다.<br>

**4. Head** : 현재 작업 중인 Branch <br>

**5. Staging Area** : **임시 저장 영역**으로 Git에 의해 관리 및 추적이 이루어짐, 커밋될 것들이 계류하는 장소<br>

**6. Working Directory** : 작업 중인 디렉토리, Git에 의해 관리되지만 추적되지는 않음<br>

**7. Commit** : 변경된 작업을 확정하고 로컬 저장소에 저장하는 작업, 작업 내용에 대한 메세지(Commit Message)를 작성해줘야하며 메세지의 형식은 통일시켜 정해주어야한다.<br>

**8. Merge** : 다른 Branch의 변경 내용을 현재 Branch에 합치는 작업<br>

**9. Push** : 변경된 로컬 저장소의 내용(Commit)을 **중앙 저장소에 반영**시키는 작업<br>

**10. Pull** : 변경된 중앙 저장소의 내용을 **로컬 저장소에 반영**시키는 작업

## Git 기본 명령어

### 1) clone
```git
git clone 원격-저장소-주소

Ex) git clone https://github.com/ChanToRe/Git-for-Archaeologists.git
```
원격 저장소의 데이터를 로컬 저장소로 복사해오는 작업. 작업을 처음 시작할 때 사용. cd 명령어로 원하는 위치로 이동한 후 clone을 실행할 것.

### 2) init
```git
git init

Ex) git init
```
저장소를 최초 사용상태로 초기화하는 명령어. 이 명령어를 입력해야 추가적인 명령어를 실행할 수 있음.

### 3) status
```git
git status

Ex) git status
```
저장소의 상태를 확인하는 명령어. 작업 중인 브랜치, 저장소 내부의 파일, 변경 사항 등의 정보를 확인할 수 있음.

### 4) add
```git
git add 파일명-혹은-디렉토리명

Ex)
git add changefile.R
git add .
```
변경 사항을 Staging Area에 등록하는 명령어. Commit 전 단계. git add . 을 통해 전체를 등록할 수 있음.

### 5) commit
```git
git commit -m "커밋-메세지-내용"

Ex) git commit -m "Update : New data"
```
Staging Area에 있는 변경 내용들을 정의하고 간략히 설명하는 메세지를 남김.

### 6) push
```git
git push

Ex) git push
```
로컬 저장소에서 원격 저장소로 변경사항을 반영시킴.

### 7) pull
```git
git pull

Ex) git pull
```
원격 저장소에서 로컬 저장소로 변경사항을 가져옴(최신 버전을 가져옴).

### 8) branch
```git
git branch 생성할-브랜치-이름
git branch -d 삭제할-브랜치-이름

Ex)
git branch develop
git branch -d develop
```
branch를 생성하고 삭제하는 명령어. 작업할 때 만들어 사용하고, 작업이 끝났을 경우 삭제해야함.

### 9) switch
```git
git switch 이동할-브랜치-이름

Ex) git switch develop
```
원하는 branch로 이동하는 명령어.

### 10) merge
```git
git merge 합칠-브랜치-이름

Ex) git merge develop
```
각 branch에서 마무리된 작업을 master branch로 합치는 작업. merge는 반드시 master branch에서 이루어져야함.

## Git을 활용한 개인연구 관리

&nbsp; Git을 사용한 버전 관리는, 개인연구에서도 유용하게 사용될 수 있다. 장점으로는 (1)연구에 활용되는 코드를 체계적으로 관리할 수 있다. (2)README.md를 작성하여 논문을 소개하는 페이지로 활용할 수 있다 (3)github로 데이터를 공유할 경우, 논문의 지면을 할애하여 부록형식으로 첨부할 필요가 없으며, 이를 활용하는 다른 연구자 또한 훨씬 간단하게 데이터를 활용할 수 있다. 최근 고고학에서 프로그래밍을 활용한 분석을 시도하는 경우가 많아지고 있는데, Github에 이를 등록하여 코드와 데이터를 간편하게 공유할 수 있다. [Enrico R. Crema의 예시](https://github.com/ercrema/NeolithicKoreaDemography)

```git
#혼자 작업할 때 Workflow

1. Github에서 저장소 생성
2. cd 저장-위치    # 저장 위치로 이동
3. git init    # 저장소 초기화
4. git remote add origin 저장소-주소    # 원격 저장소 추가
5. git remote -v    # 원격 저장소 상세 정보 확인
---------- 위의 작업은 가장 처음에만 실시 ----------
6. ~~~ 작업 ~~~
7.  git status    # 저장소 상태 확인
8. git add 파일명 or git add .    # Staging Area에 등록
9. git commit -m "커밋-메세지-내용"    # Staging Area -> Local Repository
10. git push
```
&nbsp; 가장 먼저 Github에서 저장소를 생성해준다. 이후 작업할 PC에서 작업 위치로 이동한 후 3~5의 작업을 실행하여 저장소를 셋팅해준다. 작업을 한 뒤에는 add 명령어를 통해 Staging Area에 올린 뒤, commit을 하고 push를 통해 원격 저장소에 최종적으로 올린다.

## Git을 활용한 협업

&nbsp; Git의 진가는 여러 사용자들이 함께 협업할 때 드러난다. (1)충돌없이 다양한 사용자들이 프로젝트를 진행해갈 수 있다. (2)Issue Tracker를 통해 Issue를 체계적으로 관리할 수 있다. (3)일종의 메신저처럼 활용할 수 있다. 이외에도 여러 기능을 통해 프로젝트를 체계적으로 관리할 수 있다. 협업할 경우 구성원끼리 사전에 Commit message를 어떻게 작성할 것인지 논의하고 이후 형식에 맞게 Commit message를 작성해야한다. 최근 고고학 자료의 양이 극단적으로 많아지고 있는 상황속에서 다양한 연구자들이 협업을 통해 함께 자료를 관리한다면 더욱 양질의 자료를 간편하게 활용할 수 있을 것으로 예상된다.

```git
# 협업 할 때 Workflow
1. Github에서 저장소 생성
2. cd 저장-위치    # 저장 위치로 이동
3. git init    # 저장소 초기화
4. git remote add origin 저장소-주소    # 원격 저장소 추가
5. git remote -v    # 원격 저장소 상세 정보 확인
---------- 위의 작업은 가장 처음에만 실시 ----------
6. cd 작업-위치    # 작업 및 관리 위치로 이동
7. git branch 브랜치-이름    # 브랜치 생성
8. git switch 브랜치-이름    # 생성한 브랜치로 이동
9. ~~~ 작업 ~~~
10. git add 파일명 or git add .    # Staging Area에 등록
11. git commit -m "커밋-메세지-내용"    # Staging Area -> Local Repository
12. git switch master    # master branch로 이동
13. git pull     # 충돌 방지를 위해 최신 상태로 업데이트
14. git merge 브랜치-이름     # 브랜치에서 작업한 내용을 master branch에 병합
15. git push    # Local repository -> Remote repository
16. git branch -d 브랜치-이름    # 사용한 브랜치 삭제
```

&nbsp; 가장 먼저 Github에서 저장소를 생성해준다. 이후 작업할 PC에서 작업 위치로 이동한 후 3~5의 작업을 실행하여 저장소를 셋팅해준다. 이후 저장 위치로 이동하고 작업할 브랜치를 생성한 뒤 해당 브랜치로 이동한다. 이후 작업을 한 뒤 작업이 마무리 된다면 add 명령어를 통해 Staging Area에 올리고, commit을 하여 로컬 저장소에 올린다. 이어서 master branch로 이동한 뒤 pull을 통해 로컬 저장소를 최신 상태로 업데이트 해주고, 작업한 브랜치를 master branch에 병합한다. 이후 이를 push하여 원격 저장소에 올린 뒤, 사용한 브랜치는 삭제한다.

## * .gitignore

&nbsp; Github에 올리고 싶지 않은 보완 관련 파일, 개인정보 파일, 미공개 파일 등은 **.gitignore**에 등록하여 Github에 올라가지 않게 관리할 수 있다. 생성 방법은 아래와 같다.

`.gitignore` 라는 이름의 파일 생성
내부에 아래와 같이 작성

```git
*.파일확장자    # 해당 파일 확장자 전부 제외
Ex) *.hwp

name.파일확장자    # 해당 name의 파일 제외
Ex) 고고학자를 위한 git.hwp

name/    # 해당 name의 폴더 제외
Ex) 참고문헌/
```
&nbsp; 필자의 경우 (1)본문 파일(한글, 워드 등), (2)참고문헌, (3)미공개 데이터 등을 gitignore에 등록하여 사용하고 있습니다.
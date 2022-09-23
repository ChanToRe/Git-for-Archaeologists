# Git-for-Archaeologists

* 본 레포지토리는 고고학 연구자에게 Git과 Github를 소개하고자 작성되었습니다.
* Git과 Github를 활용하여 개인연구, 공동연구를 관리하는 방법을 살펴봅니다.
* 문의는 Issue 혹은 E-mail을 통해 연락주세요.

## 목차

[1. Git?, Github?](# 1. Git?, Github?) <br>
[2. Teminal Command](# 2. Teminal Command) <br>
[3. Git 기본용어](# 3. Git 기본용어) <br>
[4. Git 기본 명령어](# 4. Git 기본 명령어) <br>
[5. Git을 활용한 개인연구 관리](# 3. Git를 활용한 개인연구 관리) <br>
[6. Git을 활용한 협업](# 4. Github를 활용한 협업)

## 1. Git?, Github?

&nbsp; Git은 Linus Torvalds에 의해 개발된 **분산 버전 관리 시스템**입니다. 다양한 파일의 변경사항을 기록하여, 추후 필요할 때 이를 확인하거나 되돌릴 수 있습니다. 또한 여러 사람이 함께 하나의 프로젝트, 연구, 개발을 진행할 때 효율적으로 협업을 할 수 있게 해줍니다. Git을 사용하면 인터넷이 불가능한 지역에서도 작업이 가능하며, 자연스럽게 백업이 되어 컴퓨터가 분실 혹은 고장나도 복구가 가능합니다(Push까지 무사히 끝낸 경우). 무엇보다 가장 큰 장점은 다양한 사람들이 함께 협업하는 상황속에서도 깔끔하게 프로젝트, 연구, 개발을 진행할 수 있다는 것입니다.

&nbsp; Github는 Git을 사용하는 프로젝트를 지원하는 웹 호스팅 서비스입니다. 즉 Git을 사용하는 프로젝트의 서버 역할을 담당해줍니다. Git을 웹에서 편히 사용할 수 있게 해주는 도구로 버전 관리, 코드 확인, 버그 정리를 할 수 있으며 블로그, SNS, 포트폴리오 정리의 기능을 해주기도 합니다.

*깃허브 가입 및 세팅은 아래의 링크를 참조해주시기 바랍니다.<br>
[Github 가입](https://www.lainyzine.com/ko/article/how-to-create-github-account/) / [Git 설치(Windows)](https://goddaehee.tistory.com/216) / [Git 설치(MacOS)](https://velog.io/@wijoonwu/Mac-OS-%EC%97%90%EC%84%9C-Git-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0)

## 2. 기본 터미널 명령어

&nbsp; Git을 사용하는 방법은 크게 두 가지가 있습니다. 첫 번째, GUI 프로그램 입니다. GUI 프로그램은 우리가 평소에 사용하는 프로그램처럼 GUI로 되어 있어 사용이 간편합니다. 하지만 할 수 있는 작업이 적다는 치명적인 단점이 있습니다. 두 번째, 터미널 명령어를 활용하는 방법입니다. 이 방법의 경우, 모든 기능을 사용할 수 있습니다. 하지만 어렵다는 단점이 있습니다(물론 숙달되면 간단합니다.)

&nbsp; 본문에서는 두 번째 방법(터미널 명령어를 활용한 방법)을 사용하고자 합니다. 다소 생소하여 어렵게 느껴질 수 있지만, 작업 흐름을 익히시면 금방 적응되실겁니다. 본문에는 자주 사용하는 명령어만 기재한 것입니다. 실제로는 훨씬 많은 명령어가 있습니다.

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

### 10) vi / 디렉토리 생성
```bash
vi 파일명

Ex) vi /chantore/research/script.py
```
vi 에디터로 파일을 편집할 수 있게 해주는 명령어.

## 3. Git 기본용어

&nbsp; Git의 기본적인 용어에 대해 살펴봅니다. 이러한 용어는 뒤이어 살펴볼 Git의 기본 명령어에서 그대로 사용되는 경우가 많기 때문에 숙지가 필요합니다.

**1. Repository**<br>
	&nbsp;**- Remote Repository** : 원격 서버에 위치하는 저장소(일종의 중앙 저장소)<br>
	&nbsp;**- Local Repository** : 개발자가 작업하는 개인 PC의 저장소<br>
**2. Clone** : 원격 저장소의 내용을 로컬 저장소로 복사하는 행위<br>
**3. Branch** : 독립적인 작업을 위한 분기점, 작업을 할 때는 Branch를 생성하여 작업한다. 작업이 끝난 경우, 이를 병합하고 사용한 Branch를 삭제하여 마무리한다. Branch를 통해 협업시 충돌을 방지할 수 있으며, 작업 흐름을 한눈에 파악할 수 있다.<br>
**4. Head** : 현재 작업 중인 Branch <br>
**5. Staging Area** : 임시 저장 영역으로 Git에 의해 관리 및 추적이 이루어짐, 커밋될 것들이 계류하는 장소<br>
**6. Working Directory** : 작업 중인 디렉토리, Git에 의해 관리되지만 추적되지는 않음<br>
**7. Commit** : 변경된 작업을 확정하고 로컬 저장소에 저장하는 작업, 작업 내용에 대한 메세지(Commit Message)를 작성해줘야하며 메세지의 형식은 통일시켜 정해주어야한다.<br>
**8. Merge** : 다른 Branch의 변경 내용을 현재 Branch에 합치는 작업<br>
**9. Push** : 변경된 로컬 저장소의 내용(Commit)을 중앙 저장소에 반영시키는 작업<br>
**10. Pull** : 변경된 중앙 저장소의 내용을 로컬 저장소에 반영시키는 작업

## 4. Git 기본 명령어

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

## 5. Git을 활용한 개인연구 관리

## 6. Git을 활용한 협업
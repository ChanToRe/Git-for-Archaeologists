# Git-for-Archaeologists

* 본 레포지토리는 고고학 연구자에게 Git과 Github를 소개하고자 작성되었습니다.
* Git과 Github를 활용하여 개인연구, 공동연구를 관리하는 방법을 살펴봅니다.
* 문의는 Issue 혹은 E-mail을 통해 연락주세요.

## 목차

[1. Git?, Github?](## 1. Git?, Github?)<br>
[2. Teminal Command](## 2. Teminal Command)<br>
[3. Git 기본용어](## 3. Git 기본용어)<br>
[4. Git 기본 명령어](## 4. Git 기본 명령어)<br>
[5. Git을 활용한 개인연구 관리](## 3. Git를 활용한 개인연구 관리)<br>
[6. Git을 활용한 협업](## 4. Github를 활용한 협업)

## 1. Git?, Github?

&nbsp; Git은 Linus Torvalds에 의해 개발된 **분산 버전 관리 시스템**입니다. 다양한 파일의 변경사항을 기록하여, 추후 필요할 때 이를 확인하거나 되돌릴 수 있습니다. 또한 여러 사람이 함께 하나의 프로젝트, 연구, 개발을 진행할 때 효율적으로 협업을 할 수 있게 해줍니다. Git을 사용하면 인터넷이 불가능한 지역에서도 작업이 가능하며, 자연스럽게 백업이 되어 컴퓨터가 분실 혹은 고장나도 복구가 가능합니다(Push까지 무사히 끝낸 경우). 무엇보다 가장 큰 장점은 다양한 사람들이 함께 협업하는 상황속에서도 깔끔하게 프로젝트, 연구, 개발을 진행할 수 있다는 것입니다.

&nbsp; Github는 Git을 사용하는 프로젝트를 지원하는 웹 호스팅 서비스입니다. 즉 Git을 사용하는 프로젝트의 서버 역할을 담당해줍니다. Git을 웹에서 편히 사용할 수 있게 해주는 도구로 버전 관리, 코드 확인, 버그 정리를 할 수 있으며 블로그, SNS, 포트폴리오 정리의 기능을 해주기도 합니다.

*깃허브 가입 및 세팅은 아래의 링크를 참조해주시기 바랍니다.<br>
[Github 가입](https://www.lainyzine.com/ko/article/how-to-create-github-account/) / [Git 설치(Windows)](https://goddaehee.tistory.com/216) / [Git 설치(MacOS)](https://velog.io/@wijoonwu/Mac-OS-%EC%97%90%EC%84%9C-Git-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0)

## 2. 기본 터미널 명령어

&nbsp; Git을 사용하는 방법은 크게 두 가지가 있습니다. 첫 번째, GUI 프로그램 입니다. GUI 프로그램은 우리가 평소에 사용하는 프로그램처럼 GUI로 되어 있어 사용이 간편합니다. 하지만 할 수 있는 작업이 적다는 치명적인 단점이 있습니다. 두 번째, 터미널 명령어를 활용하는 방법입니다. 이 방법의 경우, 모든 기능을 사용할 수 있습니다. 하지만 어렵다는 단점이 있습니다(물론 숙달되면 간단합니다.)

&nbsp; 본문에서는 두 번째 방법(터미널 명령어를 활용한 방법)을 사용하고자 합니다. 다소 생소하여 어렵게 느껴질 수 있지만, Workflow를 익히시면 금방 적응되실겁니다. 본문에는 자주 사용하는 명령어만 기재한 것입니다. 실제로는 훨씬 많은 명령어가 있습니다.

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

## 4. Git 기본 명령어

## 5. Git을 활용한 개인연구 관리

## 6. Git을 활용한 협업
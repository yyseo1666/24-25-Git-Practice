# LV000 - 깃/깃허브 새싹세션 

## 세션 목표
1. Docker 컨테이너 환경에서 Git을 설치하고 설정하는 방법을 배우며, GitHub 레포지토리를 클론하여 실습에 활용할 준비를 합니다.
2. Visual Studio Code 에서 Docker 컨테이너와의 연동 방법을 익힐 수 있습니다. 

## Step 0. 필수 소프트웨어 설치

### 1. Docker 설치

https://www.docker.com/

### 2. VSC 설치

https://code.visualstudio.com/

## Step 1. git session 실습을 위한 Ubuntu Docker 컨테이너 생성 및 Git 설치 실습

### 1. Ubuntu Docker 이미지 설치 및 실행

먼저 Ubuntu Docker 이미지를 가져오고 실행합니다:

```bash
docker pull ubuntu:latest
docker run -it --name ${컨테이너 이름} ubuntu
```

이 명령어는 최신 Ubuntu 이미지를 가져와 대화형 터미널(`-it`)로 실행하고, 컨테이너 이름을 `my_ubuntu`로 지정합니다.

### 2. Ubuntu 컨테이너 접속(1번이 성공할 경우 건너뜁니다)

컨테이너가 실행 중이 아니라면 다음 명령어로 시작하고 접속합니다:

```bash
docker start ${컨테이너 이름}
docker exec -it ${컨테이너 이름} /bin/bash
```

### 3. Git 설치

```bash
apt-get update
apt-get install -y git
```

### 4. Git 설치 확인

```bash
git --version
```

## Step 2. Docker ubuntu와 VSC를 연결하기

### 1. Docker container 활성화 확인

아래 명령어로 실행되고 있는 도커 컨테이너의 상태를 확인합니다.

```bash
docker ps
```
만약, 실행되고 있지 않을 경우 [Step 1. git session 실습을 위한 Ubuntu Docker 컨테이너 생성 및 Git 설치 실습](#step-1-git-session-실습을-위한-ubuntu-docker-컨테이너-생성-및-git-설치-실습) 의 2번을 실행해보세요.



### 2. VSC에서 Docker Extension 설치

### 3. Docker Extension → ubuntu 우클릭 → Attach VSC 클릭

### 4. Terminal 열기

`Ctrl + Shift + ~` 으로 터미널을 엽니다.

## Step 3. git clone

### 1. 깃허브에서 레포지토리 클론

[깃허브 링크](https://github.com/GDSC-Gachon/24-25-Git-Practice)

```bash
git clone https://github.com/GDSC-Gachon/24-25-Git-Practice.git
```
---
이제 Git 및 Docker 설정을 마쳤습니다. 실습을 완료하신 분들은 다음 세션으로 이동해 주세요. 계속해서 GitHub 활용법에 대해 알아볼 예정입니다.

<div style="display: flex; justify-content: space-between;">
  <a href="이전세션링크" style="font-size: 18px; color: transparent; pointer-events: none;">Prev</a>
  <a href="다음세션링크" style="font-size: 18px;">Next: LV100</a>
</div>
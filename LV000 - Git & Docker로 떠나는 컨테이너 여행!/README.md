# 🚀 [LV000] Git & Docker로 떠나는 컨테이너 여행!

**🗺️ 이번 여행의 목표:**

1. 도커 컨테이너 안에 직접 깃을 설치하고 설정하는 법을 배우고 깃허브 저장소를 가져와 실습 준비를 마칩니다.
2. Visual Studio Code (VSCode)를 이용하여 컨테이너 내부에서 편리하게 작업하는 방법을 익힙니다. 

## 🎒 0단계:  여행 준비는 다 되었나요? 필수 준비물 확인!

### 🧰 1. Docker 설치: 컨테이너 여행의 필수품!

아직 Docker가 설치되어 있지 않다면, 아래 링크를 통해 설치를 진행해주세요.

[https://www.docker.com/](https://www.docker.com/)

### 💻 2. VSCode 설치: 똑똑하고 편리한 여행 동반자!

VSCode는 다양한 기능으로 개발을 도와주는 강력한 도구입니다. 아직 설치하지 않았다면, 아래 링크에서 다운로드 받을 수 있습니다.

[https://code.visualstudio.com/](https://code.visualstudio.com/)

## 🚂 1단계: Ubuntu 컨테이너 탑승! 

### 🚄 1. Ubuntu 컨테이너 설치 & 실행: 

```bash
docker pull ubuntu:latest
docker run -it --name ${컨테이너 이름} ubuntu
```

위 명령어는 최신 Ubuntu 이미지를 다운로드하고 `my_ubuntu` 라는 이름의 컨테이너를 실행합니다. `-it` 옵션은 컨테이너 내부에 대화형 터미널을 통해 접속할 수 있도록 해줍니다.

### 🚆 2. 컨테이너 재탑승:  이미 컨테이너를 생성했다면?

이미 컨테이너를 생성했지만 실행 중이 아니라면 다음 명령어를 통해 컨테이너를 시작하고 접속할 수 있습니다.

```bash
docker start ${컨테이너 이름}
docker exec -it ${컨테이너 이름} /bin/bash
```

### 🧰 3. Git 설치: 컨테이너 안에 Git 챙기기!

컨테이너 내부에서 다음 명령어를 실행하여 Git을 설치합니다.

```bash
apt-get update
apt-get install -y git
```

### ✅ 4. Git 설치 확인:  제대로 설치되었는지 확인!

```bash
git --version
```

## 🔌 2단계:  VSCode와 컨테이너 연결하기

### 🔍 1. Docker 컨테이너 활성화 확인:

아래 명령어를 통해 현재 실행 중인 Docker 컨테이너 목록을 확인합니다.

```bash
docker ps
```

만약 컨테이너가 실행 중이 아니라면, [1단계: Ubuntu 컨테이너 탑승!](#-1단계-ubuntu-컨테이너-탑승) 의 2번 과정을 참고하여 컨테이너를 시작해주세요.

### 🔌  2. VSCode Docker Extension 설치: 

VSCode 좌측 Extensions 메뉴에서 'Docker'를 검색하여 설치합니다.

### 🖱️  3. Docker Extension → ubuntu 우클릭 → Attach VSCode 클릭:

설치된 Docker Extension을 통해, 실행 중인 Ubuntu 컨테이너에 VSCode를 연결합니다.

### 💻 4. Terminal 열기 (`Ctrl + Shift + ~`):  

VSCode 터미널을 열어 컨테이너 내부에서 명령어를 실행할 준비를 마칩니다.

---

🎉 이제 Git 및 Docker 설정을 마쳤습니다! 다음 여정에서는 Git/Github의 기본적인 개념을 알아보고, 여러 명령어로 본격적인 협업을 시작해 봅시다!

<div style="display: flex; justify-content: space-between;">
  <a href="이전세션링크" style="font-size: 18px; color: transparent; pointer-events: none;">Prev</a>
  <a href="다음세션링크" style="font-size: 18px;">Next: LV100</a>
</div>

# Ubuntu 24.04 noVNC Docker for 오픈소스SW기초 
<img src="https://github.com/user-attachments/assets/018a008d-c310-4ed5-93e6-1c9b6859f7a9" width="900" height="550" />

브라우저만으로 Ubuntu 24.04 데스크톱 환경에 접속할 수 있는 Docker 이미지입니다. (리눅스 수업 실습용)

## 실행 전 도커 설치 필수

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (Windows / Mac)

설치 확인:
```bash
docker --version
docker compose version
```
설치후 반드시 Docker Desktop 실행:
```
win키 + Docker Desktop 검색 후 실행
```

## 실행 방법

```bash
git clone https://github.com/cire21st/ubuntu-novnc.git
```
```bash
cd ubuntu-novnc
```
```bash
docker compose up -d
```

브라우저에서 `http://localhost/` 접속하면 데스크톱 화면이 뜹니다.
noVNC의 연결 버튼을 클릭하여 Ubuntu를 자유롭게 사용합니다.

## 종료 방법

```bash
docker compose down
```

## 실습 파일 저장 위치(중요!!)

`workspace` 폴더가 컨테이너 바탕화면(`~/Desktop`)과 연결되어 있습니다. 
(`~/Desktop`) 밖에 디렉토리에 정보는 저장되지 않습니다!! 실습 코드는 (`~/Desktop`) 안에 저장하세요.

## 포함된 프로그램

- Terminator (터미널)
- VSCodium (코드 에디터)
- Firefox
- gcc / g++ / make

## 직접 빌드하려면

```bash
docker compose -f docker-compose-build.yaml up --build
```

---
*아직 작업 중인 임시 버전입니다.*

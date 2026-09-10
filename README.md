# Ubuntu 24.04 noVNC Docker
<img src="https://github.com/user-attachments/assets/018a008d-c310-4ed5-93e6-1c9b6859f7a9" width="175" height="90" />

브라우저만으로 Ubuntu 24.04 데스크톱 환경에 접속할 수 있는 Docker 이미지입니다. (리눅스 수업 실습용)

## 실행 방법

```bash
git clone https://github.com/cire21st/ubuntu-novnc-docker.git
cd ubuntu-novnc-docker
docker compose up
```

브라우저에서 `http://localhost/` 접속하면 데스크톱 화면이 뜹니다.

종료:
```bash
docker compose down
```

## 직접 빌드하려면

```bash
docker compose -f docker-compose-build.yaml up --build
```

## 실습 파일 저장 위치

`workspace` 폴더가 컨테이너 바탕화면(`~/Desktop`)과 연결되어 있습니다. 실습 코드는 여기에 저장하세요.

## 포함된 프로그램

- Terminator (터미널)
- VSCodium (코드 에디터)
- Firefox
- gcc / g++ / make

---
*아직 작업 중인 임시 버전입니다.*

# DOCKER

## 명령어

### 도움말

```dockerfile
docker run --help
```

### image 가져오기

```dockerfile
docker pull <image name>
```

ex)

```
docker pull continuumio/miniconda3
```



### image 실행

```dockerfile
docker run <option> <image name> <run file>
```

-i(interactive), -t(Pseudo-tty) 옵션을 사용하면 실행된 Bash Shell에 입력 및 출력을 할 수 있습니다. 그리고 --name 옵션으로 컨테이너의 이름을 지정할 수 있습니다. 이름을 지정하지 않으면 Docker가 자동으로 이름을 생성하여 지정합니다.

| 옵션   | 설명                                                         |
| ------ | ------------------------------------------------------------ |
| -i, -t | -interactive -tty i와 t는 터미널 입력을 위한 옵션으로 일반적으로 *-it* 혹은 *-i -t* |
| -d     | detached mode 흔히 말하는 백그라운드 모드                    |
| --name | 컨테이너 이름 설정                                           |
| -p     | 호스트와 컨테이너 포트의 연결 : 포워딩                       |
| -e     | 컨테이너 내에서 사용할 환경변수 설정                         |
| -rm    | 프로세스 종료시 컨테이너 자동 삭제                           |
| --link | 컨테이너 연결 [컨테이너명:별칭]                              |
| -v     | 호스트와 컨테이너의 디렉토리 연결 (마운트)                   |
| -e     | 컨테이너 내에서 사용할 환경변수 설정                         |

ex)

```dockerfile
docker run -i -t --name hello ubuntu /bin/bash
```

### 이미지 종료

```dockerfile
exit
```

### 컨테이너 실행 기록

```dockerfile
docker ps -a
```

### 이미지 변경 사항 저장

```dockerfile
 docker commit <container id> <image name>
```

컨테이너 아이디와 공백 입력 후 해당 이미지를 사용할 때 쓸 이름을 입력해줍니다.

### 컨테이너 아이디 확인

```dockerfile
docker ps -a
```

### 이미지 실행 시 로컬 폴더를 마운트해 사용하기

```dockerfile
docker run -i -t -v <로컬 경로>:<컨테이너 경로> <이미지 이름>
```


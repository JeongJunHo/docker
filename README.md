# DOCKER

## 명령어

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

ex)

```dockerfile
docker run -i -t --name hello ubuntu /bin/bash
```

## 실습

### miniconda3 설치

```dockerfile
docker pull continuumio/miniconda3
```

### miniconda3 실행

```dockerfile
docker run -i -t continuumio/miniconda3 /bin/bash
```

### python 사용

```python
python3 -c "print(3*5)"
# 결과 15
```

 -c는 인터프리터 모드이다 즉각 결과를 반환해준다.

-i는 대화형 모드이다. ctrl + d

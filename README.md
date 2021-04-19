# CPU 사용량을 늘리기 위한 샘플

## Artillery 를 이용한 부하테스트 [링크](https://artillery.io/)
- artillery 설치
```shell
npm install -g artillery
```
  

- 작성 스크립트 실행 (yaml 파일)  
 yaml 파일을 만든 후 해당 파일의 폴더에서 아래의 스크립트 실행

```shell
artillery.cmd run --ouput report.json .\cpu-test.yaml
```

- 테스트 완료 후 생성된 ouput 파일 html 로 변경
```shell
artillery.cmd report .\report.json
```

## Docker 빌드 및 push

### build
```shell
docker build -t 사용자이름/도커허브레파지토리

ex) docker build -t kimkuma/springboot-cpu-bound
```
### push
```shell
docker push 사용자이름/도커허브레파지토리

ex) docker push kimkuma/springboot-cpu-bound
```

### pull
```shell
docker pull 사용자이름/도커허브레파지토리

ex) docker pull kimkuma/springboot-cpu-bound
```

### run
```shell
docker run -p [호스트port]:[컨테이너port] 사용자이름/도커허브레파지토리

ex) docker run -p 80:80 kimkuma/springboot-cpu-bound
```

## Jenkins 설치(CentOS 기준)

### jenkins 인스턴스에서 실행하는 명령어
```shell
sudo yum install wget
sudo yum install maven
sudo yum install git
sudo yum install docker

sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum install jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```
### 여기까지 실행하면 설치는 완료

### 초기 Password 확인
```shell
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```



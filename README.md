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
# How_to_deploy_WebGl_with_ApacheTomcat
## WebGl로 빌드한 유니티 프로젝트를 톰캣에 배포하는 방법(확실하지 않음)

### 1. 톰캣 JDK 호환성
    톰캣 11은 Jakarta EE 10을 기반으로 하며, Java 17 이상을 요구함.
    톰캣 9는 Java 8 이상만 있으면 동작할 수 있음.


### 2. 톰캣 다운로드 
    https://tomcat.apache.org/
    
### 3. 서버 컴퓨터 방화벽 인바운드 설정
    이건 외부에서 해당 포트로 접속할 수 있도록 설정할 수 있음

### 3. 서버 내부 배포파일 설정
    유니티로 빌드한 WebGL 기준으로는 
        Build 폴더
        TemplateData 폴더
        index
    이 세 종류의 파일을 톰캣 서버 디렉토리 webapps 내부 새로운 폴더를 생성한 후 파일 삽입

### 4. 3번까지 했을 시 로컬 서버 배포
    http://localhost:{포트}/{webapps폴더명} 이렇게 접속하면 들어갈 수 있음
    인바운드 설정 후 : http://{서버IP}:{포트}/{webapps폴더명}


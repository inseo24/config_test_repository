# config_test_repository


1. study_msa 레포지터리의 config-server-test/config-test-server 에 있는 서버 1개, test 폴더 안의 first-service 서버 1개씩 총 2개르 띄운다.

2. config server를 먼저 띄우고 그 다음 first-service를 실행한다.

3. yaml profile을 default, dev, prod, stage 각기 다른 yaml 파일을 레포지터리에서 가져오는지 테스트해보 수 있다!


repo 안의 yml에 eureka 설정이 있어서 discovery-server가 안돌면 error가 로그로 찍힘

study_msa repo의 test/discovery-server를 같이 돌려주면 에러 안뜸! ㅇㅁ<


## config name 변경하기 고군분투기

spring-cloud-starter-config 의존성 추가 후, yml config name 을 지정해봤자 application name을 따라간다.

즉, config server가 config repository에서 해당 서비스의 yml 파일을 찾을 때 /[spring.applicaiton.name]/[spring.profiles/active] 로 찾음

application name 이 first-service 에 active profile 이 dev라면 first-service-dev.yml(yaml) 을 찾음

여기서 config.name 을 아무리 지정해봤자 소용 없다!-!

profile마다 이름을 다르게 지정할거면 해당 yml에 application-name을 다르게 지정해야 하는데, 그 경우 eureka에 등록되는 이름도 같이 변경되니 discovery service 처리가 (...)



기존 bootstrap의 경우 config name을 따로 지정하고 application name은 따로 쓰는게 됐던 거 같은데 현재 import + starter-config 조합으로는 힘든 거 같다.

혹시 방법을 아시는 분 help me!!

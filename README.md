# config_test_repository


1. study_msa 레포지터리의 config-server-test/config-test-server 에 있는 서버 1개, test 폴더 안의 first-service 서버 1개씩 총 2개르 띄운다.

2. config server를 먼저 띄우고 그 다음 first-service를 실행한다.

3. yaml profile을 default, dev, prod, stage 각기 다른 yaml 파일을 레포지터리에서 가져오는지 테스트해보 수 있다!


repo 안의 yml에 eureka 설정이 있어서 discovery-server가 안돌면 error가 로그로 찍힘
study_msa repo의 test/discovery-server를 같이 돌려주면 에러 안뜸! ㅇㅁ<

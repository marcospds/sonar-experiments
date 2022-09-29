Este exemplo demonstra como gerar cobertura de código para testes executados por [maven-invoker-plugin](http://maven.apache.org/plugins/maven-invoker-plugin/) (_This example demonstrates how to collect code coverage by tests, which executed by maven-invoker-plugin_).

1.  Compila o projeto e executa todos os testes (_Build project and execute all tests_):

        mvn clean install
2.  Subir o Sonar local com Docker (_Up local Sonar by Docker_):

        docker run -d -it --rm -e SONAR_FORCEAUTHENTICATION=false -p 9000:9000 --pull always sonarqube
3.  Envia para o Sonar local (_Analyse by Sonar_):

        mvn sonar:sonar
4.  Acessar projeto no Sonar local (_Access the project in local Sonar_):

        http://localhost:9000/dashboard?id=org.example%3Amaven-invoker-plugin-example

- Esse projeto do tipo packaging maven-plugin gera cobertura para o Sonar tanto do teste unitário com Junit em target/site/jacoco, quanto do teste integrado usando maven-invoker-plugin em target/site/jacoco-it (_This packaging maven-plugin project generates coverage for Sonar for both unit testing with Junit at target/site/jacoco and integrated testing using maven-invoker-plugin at target/site/jacoco-it_).

- Links que me levaram até aqui (_Links that took me here_):
  - https://blog.sandra-parsick.de/2021/05/31/how-to-measure-test-coverage-in-invoker-tests-with-jacoco/
  - https://stackoverflow.com/questions/15141915/running-code-coverage-with-cobertura-and-jacoco
  - https://github.com/Godin/sonar-experiments/tree/master/jacoco-examples/maven-invoker-plugin-example (Thx @Godin!)

This example demonstrates how to collect code coverage by tests, which executed by [maven-invoker-plugin](http://maven.apache.org/plugins/maven-invoker-plugin/).

1.  Build project and execute all tests:

        mvn clean install

2.  Analyse by Sonar :

        mvn sonar:sonar

** This packaging maven-plugin project generates coverage for Sonar for both unit testing with Junit at target/site/jacoco and integrated testing using maven-invoker-plugin at target/site/jacoco-it
** Esse projeto do tipo packaging maven-plugin gera cobertura para o Sonar tanto do teste unitário com Junit em target/site/jacoco, quanto do teste integrado usando maven-invoker-plugin em target/site/jacoco-it

** Links that took me here:
** Links que me levaram até aqui:
https://blog.sandra-parsick.de/2021/05/31/how-to-measure-test-coverage-in-invoker-tests-with-jacoco/
https://stackoverflow.com/questions/15141915/running-code-coverage-with-cobertura-and-jacoco
https://github.com/Godin/sonar-experiments/tree/master/jacoco-examples/maven-invoker-plugin-example

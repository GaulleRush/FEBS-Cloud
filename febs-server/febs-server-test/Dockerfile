FROM openjdk:8u212-jre
MAINTAINER MrBird 852252810@qq.com

COPY ./target/febs-server-test-1.3-SNAPSHOT.jar /febs/febs-server-test-1.3-SNAPSHOT.jar
ADD agent/ /agent

ENTRYPOINT ["java", "-javaagent:/agent/skywalking-agent.jar", "-Dskywalking.agent.service_name=febs-server-test", "-Dskywalking.collector.backend_service=${skywalking.url}:11800", "-jar", "/febs/febs-server-test-1.3-SNAPSHOT.jar"]
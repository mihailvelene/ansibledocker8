FROM tomcat
MAINTAINER mihailvelene@gmail.com
RUN apt-get update && apt-get install -y git && apt-get install -y maven
EXPOSE 8080
RUN cd / && mkdir test && cd test && git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git && cd boxfuse-sample-java-war-hello && mvn package && cp target/hello-1.0.war /usr/local/tomcat/webapps
CMD ["catalina.sh", "run"]
###

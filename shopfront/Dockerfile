FROM openjdk:8-jre
COPY pom.xml .
ENV MAVEN_CONFIG=''
RUN mvn clean install
ADD target/shopfront-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8010
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]

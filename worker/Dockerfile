FROM maven:3.5-jdk-8-alpine
RUN mkdir /app
COPY . /app
WORKDIR /app
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
COPY --from=0 /app/target/worker-jar-with-dependencies.jar /app.jar
CMD java -jar /app.jar

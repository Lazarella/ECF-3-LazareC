FROM maven:3.8.1-openjdk-11 as build

COPY . /usr/src/myapp
COPY pom.xml /usr/src/myapp

WORKDIR /usr/src/myapp

RUN mvn package -DskipTests

FROM openjdk:11

COPY --from=build /usr/src/myapp/target/*.jar /usr/app/app.jar

WORKDIR /usr/app

CMD ["java", "-jar", "app.jar"]


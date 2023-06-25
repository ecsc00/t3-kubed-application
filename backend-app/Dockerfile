FROM maven:3.8.3-openjdk-17 as base
WORKDIR /app
COPY pom.xml ./
RUN mvn dependency:resolve
COPY src ./src
RUN mvn package
EXPOSE 8080
CMD ["mvn", "spring-boot:run"]
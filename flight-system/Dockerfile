FROM maven:3.9.6-eclipse-temurin-21 AS build
COPY . .
RUN mvn clean package -DeskipTests
COPY --from=build /target/*.jar app.jar
EXPOSE 8080
CMD ["java", "-jar", "target","/app.jar"]

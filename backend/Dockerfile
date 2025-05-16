# Build stage
FROM eclipse-temurin:21-jdk-alpine AS build
WORKDIR /opt/app
COPY src/Main.java .
RUN javac Main.java

# Run stage
FROM eclipse-temurin:21-jre-alpine
WORKDIR /opt/app
COPY --from=build /opt/app/Main.class .
CMD ["java", "Main"]
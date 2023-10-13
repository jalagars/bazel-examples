FROM openjdk:13-jdk-alpine3.10

RUN addgroup -S demogroup && adduser -S demo -G demogroup
USER demo

# Inform Docker that the container is listening on the specified port at runtime.
EXPOSE 8080

WORKDIR /usr/app

RUN pwd
# copy the jar file
COPY .java-tutorial/bazel-bin/src/main/java/com/example/cmdline/runner_deploy.jar .

RUN ls -hl

ENTRYPOINT ["java","-jar","runner_deploy.jar"]
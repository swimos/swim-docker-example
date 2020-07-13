# swim-docker-example

This is a small example application demonstrating how to build a Java project into a Docker image using the [Gradle docker plugin](https://github.com/bmuschko/gradle-docker-plugin).

The application itself is composed of two parts: 
- A basic plane that stores some arbitrary information using a Value Lane and contains a Command Lane for updating it.
- A client application that is used for reading and writing to the plane.

The Docker image exposes port 9001 as this is what the server is configured to use in the `resources/server.recon` configuration file.

This project can be built into a Docker image as follows:
```
./gradlew dockerBuildImage

$ docker image ls
REPOSITORY                       TAG                 IMAGE ID            CREATED             SIZE
org.swimos/swim-docker-example   1.2                 17d69579cdf8        1 second ago        342MB
```


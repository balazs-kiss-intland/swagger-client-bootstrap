# CodeBeamer Swagger client bootstrap project

This project is meant to be the starting point for Java based client projects which are connecting to the codeBeamer ALM system.

## Requirements

Building the API client SDK requires:
1. Java 1.8+
2. Gradle
3. Running codeBeamer instance

## Installation

To regenerate the API client SDK, open the /build.gradle file and modify the codeBeamerBaseUrl definition to your codeBeamer instance:

```groovy
def codeBeamerBaseUrl = "{your codeBeamer instance base URL}"
```

After this setup you can use the following gradle task to download the latest API definition:

```shell script
./gradlew downloadSwaggerJson
```

This command should update the swagger_api.json file in the project directory.

Based on the swagger_api.json file, now you can regenerate the client SDK library to represent the latest state of the API:

```shell script
./gradlew generateSwaggerClient
```

To build your client code you can use:

```shell script
./gradlew swagger-client:build
```

## Getting started

Please follow the [installation](#installation) instruction and execute the [Main.java](swagger-client/src/main/java/com/example/swagger/client/Main.java) file.
# Task manager application with Kotlin Multiplatform

A task manager application built with Ktor and Kotlin Multiplatform
by following the steps in the [Full-stack development with Kotlin Multiplatform
](https://ktor.io/docs/full-stack-development-with-kotlin-multiplatform.html) tutorial.

## Set the localhost IP address

Because it's not possible to make calls to `0.0.0.0` or `localhost` from code running on an Android Virtual Device or the
iPhone simulator, you need to specify a host address for the HTTP client.

1. Navigate to the `HttpClientManager.kt` file in `composeApp/src/commonMain/kotlin/com/example/ktor/full_stack_task_manager/network`.
2. In the `defaultRequest` function replace the value of the `host` property with the IP address of your machine.

## Run the server

Use the following command to start the server:

```shell
./gradlew :server:run
```

The server will then run at [http://0.0.0.0:8080/](). To test the endpoints, navigate to the following URLs:

- [http://0.0.0.0:8080/tasks](http://0.0.0.0:8080/tasks) to see a complete list of tasks in JSON format.
- [http://0.0.0.0:8080/tasks/byPriority/Medium](http://0.0.0.0:8080/tasks/byPriority/Medium) to see tasks filtered
  by `Medium` priority.

## Run the client

In IntelliJ IDEA, choose from the following run configurations:

- `iOSApp` to run the app on iOS
- `composeApp` to run the app on Android
- `composeApp [desktop]` to run the app on Desktop
- `composeApp [wasmJs]` to run the app on Web
# test

## Project Overview

This repository is a Gradle-based Java application named `test`.

It contains a simple CLI application in the `app` subproject that prints a greeting message and includes a basic JUnit test.

## Repository Structure

- `app/`
  - `build.gradle` - Gradle build script for the application module.
  - `src/main/java/org/example/App.java` - Main application source file.
  - `src/test/java/org/example/AppTest.java` - Unit test for the application.
- `build/` - Gradle build outputs and reports.
- `gradle/` - Gradle wrapper configuration and version catalog.
- `gradle.properties` - Gradle build properties and cache settings.
- `settings.gradle` - Root settings file for the Gradle multi-project build.

## Build and Run

### Prerequisites

- Java 21 compatible JDK
- Gradle wrapper is included, so you can use `./gradlew`

### Build

```bash
./gradlew clean build
```

### Run

```bash
./gradlew :app:run
```

This prints the greeting message from `org.example.App`.

## Application Behavior

The application prints `Hello World!` when executed.

The main class is configured in `app/build.gradle` as `org.example.App`.

## Testing

Run unit tests with:

```bash
./gradlew test
```

The repository includes a JUnit Jupiter test that verifies `App.getGreeting()` returns a non-null greeting.

## Notes

- The project uses the Gradle application plugin.
- The Java toolchain is configured for Java 21.
- The `app` module depends on Guava via the version catalog defined in `gradle/libs.versions.toml`.

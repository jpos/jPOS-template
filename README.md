## jPOS Template

Clone this project in order to create your own jPOS based application.

This branch also includes a `.sdkmanrc` that pins Java 25.0.1-amzn and Gradle 9.4.0, so `sdk env install && sdk env` keeps everyone on the same toolchain.
Each service module applies the `org.jpos.jposapp` Gradle plugin (v0.0.16), replacing the legacy `jpos-app.gradle` helper and providing the `installApp`, `dist`, `distnc`, `zip`, and `run` tasks per module.

We recommend that you install [Gradle](http://gradle.org/) in order to build your jPOS projects, but if you don't have it installed, you can use the Gradle wrapper scripts `gradlew` and `gradlew.bat`. In the following instructions, when we say `gradle` we really mean either your installed Gradle or one of the wrapper scripts (depending if you are on Unix or DOS based platforms).

### Build an eclipse project
````
gradle eclipse
````

### Build an IDEA project
````
gradle idea
````

### Build your own jar
````
gradle jar
````

### Check the jPOS version
````
gradle version
````

### Create a distribution of your application
````
gradle dist
````
This creates a tar gzipped file in the `build/distributions` directory.

### Install application in 'build/install' directory
````
gradle installApp
````
Installs application in `build/install` with everything you need to run jPOS. Once the directory is created, you can `cd build/install` and call `java -jar your-project-version.jar` or the `bin/q2` (or `q2.bat`) script available in the `bin` directory.

### Publish Maven artifacts
````
gradle publish
````

### List available Gradle tasks
````
gradle tasks
````


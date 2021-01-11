## Sample JavaFX Maven Application

A simple JavaFX application based off the [OpenJFX getting started documentation](https://openjfx.io/openjfx-docs/) that uses Maven as the build file.

I tried two different approaches based on the documentation to get the project running from both the command line and from IntelliJ IDEA, and this one works with both.

The project was created using the [JavaFX Maven Archetype](https://openjfx.io/openjfx-docs/#maven) via the IntelliJ IDEA project wizard. 

Despite the fact that the instructions seemed to suggest this is not modular (i.e. does not use the Java Module System), it actually does. It has a module-info.java and uses the module path instead of the classpath. This appears to be the main difference between this project and my other [JavaFX Maven project](https://github.com/trishagee/javafx-maven), and since this one runs correctly without needing any additional downloads or configuration, other than what was set up via Maven, at this time I would recommend this approach.

This application will run if you:
 - Call `mvn clean javafx:run` from the command line, with `JAVA_HOME` set to JDK 15
 - Run `App.java` from inside IntelliJ IDEA using the usual run configurations, e.g. Ctrl+Shift+R (Mac) / Ctrl+Shift+F10 (Window) or the run gutter icons

This application will **not** run from the Maven Tool Window or from "Run Anything" using the Maven command`mvn clean javafx:run` inside IntelliJ IDEA:

>Note: In case JAVA_HOME is not set to 15, running from the Maven Projects window might fail. To avoid it, you can add the correct java command to the javafx-maven-plugin: &lt;configuration>&lt;executable>/path/to/jdk-12/bin/java&lt;/executable>&lt;/configuration>. 

(from https://openjfx.io/openjfx-docs/#IDEA-Maven)

I've [opened an issue for this](https://youtrack.jetbrains.com/issue/IDEA-259216). I couldn't get the workaround mentioned above to work, so I will either be running the application the usual IntelliJ IDEA way, or via the terminal.

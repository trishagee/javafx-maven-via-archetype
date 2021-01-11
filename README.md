## Sample JavaFX Maven Application

A simple JavaFX application based off the [OpenJFX getting started documentation](https://openjfx.io/openjfx-docs/) that uses Maven as the build file.

I tried two different approaches based on the documentation to get the project running from both the command line and from IntelliJ IDEA, and this one works with both.

The project was created using the [JavaFX Maven Archetype](https://openjfx.io/openjfx-docs/#maven) via the IntelliJ IDEA project wizard. 

Despite the fact that the instructions seemed to suggest this is not modular (i.e. does not use the Java Module System), it actually does. It has a module-info.java and uses the module path instead of the classpath. This appears to be the main difference between this project and my other [JavaFX Maven project](https://github.com/trishagee/javafx-maven), and since this one runs correctly without needing any additional downloads or configuration, other than what was set up via Maven, at this time I would recommend this approach.
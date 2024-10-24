## KdbInsideBrains

**Version**: 5.6.0
- Requires IntelliJ build 241.* or older

**Code changes**: [e2ccb342e391393c883476571dacad20f7fb82c5](https://github.com/mwsmws22/KdbInsideBrains/commit/e2ccb342e391393c883476571dacad20f7fb82c5)

**Edits**:
- Default space after comma
- Default space around assignment operator
  - Edited this style so that it's space after not 'around'
  - E.g. `myTable: select from data` not `myTable : select from data`

**Steps**:
1. Clone [forked repo](https://github.com/mwsmws22/KdbInsideBrains) and checkout [5.6.0 branch](https://github.com/mwsmws22/KdbInsideBrains/tree/5.6.0)
2. Open project in IntelliJ
3. Set project SDK to JDK 17
    - Make sure to download [directly from Oracle](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
4. Set Gradle JVM to JDK 17
    - `Settings > Build, Execution, Deployment > Build Tools > Gradle > Gradle JVM`
5. From the Gradle tool window run `KdbInsideBrains > Tasks > build > build`
6. Find packaged JAR at `build\libs\KdbInsideBrains-5.6.0.jar`
7. Extract the following files:
    - `org\kdb\inside\brains\lang\formatting\QCodeStyleSettings.class`
    - `org\kdb\inside\brains\lang\formatting\QSpacingStrategy.class`
8. Download IntelliJ plugin zip [5.6.0](https://plugins.jetbrains.com/plugin/download?rel=true&updateId=520027) from JetBrains
    - [All plugin versions](https://plugins.jetbrains.com/plugin/16746-kdbinsidebrains/versions)
    - Alternatively you can also use the plugin zip locally built by Gradle for testing purposes:
      - `build\distributions\KdbInsideBrains-5.6.0.zip`
9. Patch JAR file contained in plugin zip with above class files

## google-java-format

**Version**: 1.13.0

**Code changes**: [123f00950f6aca3fdc96eb0f21c9553f21101706](https://github.com/mwsmws22/google-java-format/commit/123f00950f6aca3fdc96eb0f21c9553f21101706)

**Edits**:
- Change max line length from 100 to 120
- Fix comment wrapping

**Steps**:
1. Clone [forked repo](https://github.com/mwsmws22/google-java-format) and checkout [1.13.0 branch](https://github.com/mwsmws22/google-java-format/tree/1.13.0)
2. Open project in IntelliJ
3. Set project SDK to JDK 11
    - Make sure to download [directly from Oracle](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html) 
4. From the Maven tool window run `Google Java Format Parent > Lifecycle > package`
    - Make sure to enable 'Skip Tests' mode
    - ![image](https://github.com/user-attachments/assets/54c6a6ba-b926-4bc9-a742-dd7e093d6d31)
5. Find packaged JAR at `core\target\google-java-format-1.13.0.jar`
6. Extract the following files:
    - `com\google\googlejavaformat\java\Formatter.class`
    - `com\google\googlejavaformat\java\JavaCommentsHelper.class`
    - `com\google\googlejavaformat\java\javadoc\JavadocFormatter.class`
7. Download IntelliJ plugin zip [1.13.0](https://plugins.jetbrains.com/plugin/download?rel=true&updateId=146903) from JetBrains
    - [All plugin versions](https://plugins.jetbrains.com/plugin/8527-google-java-format/versions/stable)
8. Patch JAR file contained in plugin zip with above class files

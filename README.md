# android_plugin
Android Gradle Plugin

This plugin will maintain version updated across different projects

It works making a copy of the file Versions.kt into the folder buildSrc/main/java
so all the libraries here should keep updated every time we do a new release

Version bump should be done in this repository, then every project should add the plugin


```
    id("com.nmarsollier.versionplugin") version "+"
```

and the mavenLocal() or the company repository.

Every time we sync with gradle files will download the last version of libraries an will apply those libraries.


# Execution

bump this library version in build.gradle.kts to the next version

version = ***

run

```
./gradlew clean build publishToMavenLocal
```
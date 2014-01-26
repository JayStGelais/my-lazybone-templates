Java Library Project Template
-----------------------------

You have just created a Java library project. This project can be built using Gradle.

What all has been already taken care for you:

* A boilerplate `build.gradle`
* Easily generate IntelliJ Idea project files with `gradle idea`
* Checkstyle configuration
* Jacoco code coverage
* Bintray maven publish integration for your library (.jar)
* Release plugin will walk you through publishing you library (.jar)
* Comprehensive `.gitignore` - so that unnecessary files don't get checked in. (generated if --with-git is used)
* Uses jcenter (faster) maven repo

You project looks like :

```
  project/
    |--+ src/              (put your Java source files here)
    |--+ config/
           |--+ checkstyle/
                  |--+ checkstyle.xml              (checkstyle rule config)
                  |--+ checkstyle-suppressions.xml (suppressions for unit tests)
                  |--+ checkstyle.xsl              (stylesheet to produce HTML report)
	|--+ gradle/           (contains binaries for gradle wrapper)
	|--+ gradlew           (gradle warpper script for unix/linux/mac)
	|--+ gradlew.bat       (gradle warpper script for windows)
    |--+ build.gradle      (build script)
    |--+ quality.gradle    (additional build script implementing jacoco and checkstyle)
	|--+ gradle.properties (build properties, including project version)
    |--+ README.md         (This README)
    |--+ LICENSE.txt       (Apache 2.0 License text) 
```


Notes:

* A simpler directory structure is suitable for a library where you don't have webapp/resources etc.
* When you need to publish your library to Bintray, set bintrayUser & bintrayKey in gradle.properties
* Generate wrapper using `gradle wrapper`
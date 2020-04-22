# JUnit 5 Plugin 

Adds support to pitest for JUnit 5 and the Jupiter api.

## Versions

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.pitest/pitest-junit5-plugin/badge.svg?style=flat)](https://maven-badges.herokuapp.com/maven-central/org.pitest/pitest-junit5-plugin)

* 0.5-0.11 requires pitest 1.4.0 or above
* 0.4 requires pitest 1.3.2 or above
* 0.3 requires pitest 1.3.0 or 1.3.1
* 0.2 requires pitest 1.2.5 

## Usage

The plugin has been built against JUnit platform 1.5.0 - you may encounter issues if you use it with a different version. 

To activate the plugin it must be placed on the classpath of the pitest tool (**not** on the classpath of the project being mutated).

### Maven

```xml
    <plugins>
      <plugin>
        <groupId>org.pitest</groupId>
        <artifactId>pitest-maven</artifactId>
        <version>1.4.9</version>
        <dependencies>
          <dependency>
            <groupId>org.pitest</groupId>
            <artifactId>pitest-junit5-plugin</artifactId>
            <version>0.10-SNAPSHOT</version>
          </dependency>
        </dependencies>
      </plugin>
   </plugins>
```
For Pitest configuration options, have a look at http://pitest.org/quickstart/maven/.

### Gradle

```
plugins {
    id 'java'
    id 'info.solidsoft.pitest' version '1.4.9'
}

pitest {
    //adds dependency to org.pitest:pitest-junit5-plugin and sets "testPlugin" to "junit5"
    junit5PluginVersion = '0.12'
    // ...
}
```

See [gradle-pitest-plugin documentation](https://github.com/szpak/gradle-pitest-plugin#pit-test-plugins-support) for more configuration options.

## About

Plugin originally created by @tobiasstadler.

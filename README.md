# project-import-issue

Requires the following or similar script in `init.d` in order to reproduce the project import issue:

```Groovy
initscript {
    repositories {
        maven {
            url "https://plugins.gradle.org/m2"
        }
    }
    dependencies {
        classpath "com.gradle:build-scan-plugin:1.8"
    }
}

rootProject {
    apply plugin: com.gradle.scan.plugin.BuildScanPlugin
    buildScan {
        publishAlways()
    }
}
```

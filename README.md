# sample-gradle-multi
Generate a Gradle Multi-project by following the procedure described on the following site, and verify whether Dependabot can detect library updates.  
https://docs.gradle.org/current/samples/sample_building_java_applications_multi_project.html

## How it was created
Here are the commands I actually executed and the choices I made at that time.
```
$ ./gradlew init

Select type of project to generate:
  1: basic
  2: application
  3: library
  4: Gradle plugin
Enter selection (default: basic) [1..4] 2

Select implementation language:
  1: C++
  2: Groovy
  3: Java
  4: Kotlin
  5: Scala
  6: Swift
Enter selection (default: Java) [1..6] 3

Split functionality across multiple subprojects?:
  1: no - only one application project
  2: yes - application and library projects
Enter selection (default: no - only one application project) [1..2] 2

Select build script DSL:
  1: Groovy
  2: Kotlin
Enter selection (default: Groovy) [1..2] 1

Project name (default: sample-gradle-multi):

Source package (default: sample.gradle.multi):


> Task :init
Get more help with your project: https://docs.gradle.org/6.8.3/samples/sample_building_java_applications_multi_project.html

BUILD SUCCESSFUL in 14s
2 actionable tasks: 1 executed, 1 up-to-date
```

After that, I'm deliberately lowering the version of the library it depends on to see if Dependabot works.

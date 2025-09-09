Setup of basic Gradle using cli :
```chatinput
gradle init --use-defaults --type java-applications
```
The above command will setup a basic gradle project
```chatinput
 ./gradlew build
```
To prepare a jar which is executable you need to setup manifest property in `build.gradle` to identify what is the main class to execute
```groovy
jar {
    manifest {
        attributes(
                'Main-Class':'org.example.Main'
        )
    }
}
```


The above command can build your project
```chatinput
 ./gradlew jar
```
The above command creates a new jar file in `build/libs` folder
```chatinput
java -jar build/libs/filename.jar
```
The above command will execute your code


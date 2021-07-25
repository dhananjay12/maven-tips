# Maven Tips


## Create maven plugin

### Generate

```
mvn archetype:generate \
-DgroupId=com.djcodes.mvn.tips \
-DartifactId=check-maven-plugin \
-Dversion=0.0.1 \
-DarchetypeGroupId=org.apache.maven.archetypes \
-DarchetypeArtifactId=maven-archetype-mojo
```

### Install

```
mvn clean install
```

### Run
```
mvn com.djcodes.mvn.tips:check-maven-plugin:0.0.1:check-dependency
```

### Use in Other projects

```
<build>
    <plugins>
        <plugin>
            <groupId>com.djcodes.mvn.tips</groupId>
            <artifactId>check-maven-plugin</artifactId>
            <version>0.0.1</version>
            <executions>
                <execution>
                    <goals>
                        <goal>count-dependency</goal>
                    </goals>
                </execution>
            </executions>
            <configuration>
                <scope>test</scope>
            </configuration>
        </plugin>
    </plugins>
</build>
```




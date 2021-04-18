# Notes

## Creating the maven project via archtype

The initial project was created by running the following code:

```
mvn archetype:generate \
        -DarchetypeGroupId=org.openjfx \
        -DarchetypeArtifactId=javafx-archetype-simple \
        -DarchetypeVersion=0.0.3 \
        -DgroupId=com.partosb \
        -DartifactId=book-model-reader \
        -Dversion=1.0.0 \
        -Djavafx-version=15.0.1
```

## Configuring the `javafx-maven-plugin` plugin

The following parameters were added to the plugin configuration:

```
<noHeaderFiles>true</noHeaderFiles>
<stripDebug>true</stripDebug>
<noManPages>true</noManPages>
<launcher>book-model-reader</launcher>
<jlinkImageName>book-model-reader</jlinkImageName>
<jlinkZipName>book-model-reader</jlinkZipName>
```

The first 3 items strip the final image from currently unneeded parts.

The second 3 items configure the name of the created launcher file, 
image folder and zip file respectively.

## Maven 


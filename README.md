# README

This archetype is a quick start template that provides Guava, Lombok, JUnit, Mockito, and SLF4J.

## Usage

```shell
$ mvn archetype:generate -DarchetypeGroupId=dk.swissarmyronin -DarchetypeArtifactId=guava-lombok-mockito-archetype -DarchetypeVersion=1.2
```

## Troubleshooting

If the archetype generation fails, check the code out and build it, then add it to the local archetype catalog.

### Clone and build

Clone the repository's ``master`` branch and build it.

```shell
$ git clone -b master https://github.com/SwissArmyRonin/guava-lombok-mockito-archetype.git
$ cd guava-lombok-mockito-archetype
$ mvn install
```

### Add to catalog

Open ``~/.m2/archetype-catalog.xml`` and add the snippet below. Remember to set the version to the same version that you just built:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<archetype-catalog  xmlns="http://maven.apache.org/plugins/maven-archetype-plugin/archetype-catalog/1.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/plugins/maven-archetype-plugin/archetype-catalog/1.0.0 http://maven.apache.org/xsd/archetype-catalog-1.0.0.xsd">
  <archetypes>
    <archetype>
      <groupId>dk.swissarmyronin</groupId>
      <artifactId>guava-lombok-mockito-archetype</artifactId>
      <version>1.2</version>
      <description>A quick start template that provides Guava, Lombok, JUnit, Mockito, and SLF4J.</description>
    </archetype>
  </archetypes>
</archetype-catalog>
```

Now the archetype is avaialable from the command line and in your IDE.
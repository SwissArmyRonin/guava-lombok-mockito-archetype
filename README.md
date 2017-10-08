# Archetype installation & use

Clone the repository's ``master`` branch and build it.

```shell
$ git clone -b master https://github.com/mhvelplund/maven-quickstart.git
$ cd maven-quickstart
$ mvn install
```

Next, add the archetype to ``~/.m2/archetype-catalog.xml`` (remember to set the
version to the same version that you just built):

```xml
<?xml version="1.0" encoding="UTF-8"?>
<archetype-catalog  xmlns="http://maven.apache.org/plugins/maven-archetype-plugin/archetype-catalog/1.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/plugins/maven-archetype-plugin/archetype-catalog/1.0.0 http://maven.apache.org/xsd/archetype-catalog-1.0.0.xsd">
  <archetypes>
    <archetype>
      <groupId>dk.darknight</groupId>
      <artifactId>quickstart</artifactId>
      <version>1.1.0</version>
      <description>A quick start template that provides Guava, Lombok, JUnit, Mockito, and SLF4J.</description>
    </archetype>
  </archetypes>
</archetype-catalog>
```

Now the archetype is avaialable from the command line and in your IDE. To test
it, go to your project directory and run:

```shell
$ mvn archetype:generate -DarchetypeGroupId=dk.darknight -DarchetypeArtifactId=quickstart -DarchetypeVersion=1.1.0
```
# spring-boot-kotlin-basic-archetype

## How to use?

This archetype is published to Maven central. 
You can generate project using this archetype using `mvn archetype:generate` and select the archetype number.

### Install archetype locally

```bash
git clone https://github.com/sivalabs/spring-boot-kotlin-basic-archetype.git
cd spring-boot-kotlin-basic-archetype
./mvnw clean install
```

### Generate application from archetype

```
mvn archetype:generate \
    -B -DarchetypeGroupId=io.github.sivalabs.maven.archetypes \
    -DarchetypeArtifactId=spring-boot-kotlin-basic-archetype \
    -DarchetypeVersion=0.0.1 \
    -DgroupId=com.mycompany \
    -DartifactId=myapp \
    -Dversion=1.0-SNAPSHOT \
    -Dpackage=com.mycompany.myapp
```

## Developer Notes

Procedure for deploying to Maven Central https://central.sonatype.org/pages/apache-maven.html

Create or update archetypes and set version to SNAPSHOT (ex: 1.0.0-SNAPSHOT)

Deploy SNAPSHOT version to https://oss.sonatype.org/content/repositories/snapshots/

`spring-boot-kotlin-basic-archetype> ./mvnw clean deploy -P release`

Deploy release version to Maven Central

```
spring-boot-kotlin-basic-archetype> ./mvnw release:clean release:prepare -P release
spring-boot-kotlin-basic-archetype> ./mvnw release:perform -P release
```

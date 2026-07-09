# Preferences Spring Boot Starter

A Spring Boot starter for the [OpenWMS.org CORE Preferences library](https://github.com/openwms/org.openwms.core.preferences.lib).
Adding this starter to a Spring Boot application activates all Preferences components through auto-configuration, no component scanning
of the `org.openwms` package is required.

## Usage

```xml
<dependency>
    <groupId>io.interface21</groupId>
    <artifactId>preferences-spring-boot-starter</artifactId>
    <version>1.0.0-SNAPSHOT</version>
</dependency>
```

With the default (JPA) persistence backend the consuming application additionally configures the ORM mapping file:

```yaml
spring:
  jpa:
    mapping-resources:
      - META-INF/preferences-orm.xml
```

To use the MongoDB persistence backend instead, activate the `MONGODB` Spring profile.

## Build

```bash
./mvnw clean install
```

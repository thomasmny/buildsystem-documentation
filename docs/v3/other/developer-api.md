---
description: >-
  This page explains how to integrate the BuildSystem developer API into your
  project.
---

# Developer API

## Adding BuildSystem to your project

### **Maven:**

```xml
<dependency>
  <groupId>de.eintosti</groupId>
  <artifactId>buildsystem-api</artifactId>
  <version>version</version>
</dependency>
```

### **Or alternatively, with Gradle:**

```kotlin
repositories {
  mavenCentral()
}
dependencies {
  compileOnly("de.eintosti:buildsystem-api:version")
}
```

## Obtaining an instance of the API

### **Using the singleton**

Note: this method will throw an `IllegalStateException` if the API is not loaded.

```java
BuildSystem api = BuildSystemProvider.get();
...
```

### **Using the Bukkit ServicesManager**

```java
RegisteredServiceProvider<BuildSystem> provider = Bukkit.getServicesManager().getRegistration(BuildSystem.class);
if (provider != null) {
    BuildSystem api = provider.getProvider();
    ...
}
```

## Facebook Android SDK for Maven & Gradle

Current port is based on the v3.7.0 available at https://developers.facebook.com/android/  
The API is packaged as an **aar** and available from Maven Central Repository for use with **Maven** or **Gradle**.

###How to use

####Maven

The **aar** dependency requires the use of the maven-android-plugin 3.8.1+ with maven 3.1.1+ :

```xml
<dependency>
  <groupId>fr.avianey</groupId>
  <artifactId>facebook-android-api</artifactId>
  <version>3.7.0</version>
  <type>aar</type>
</dependency>
```

If you want to use a newer version of the android-support-v4 dependency, exclude the old one with this line :    

```xml
<dependency>
  <groupId>fr.avianey</groupId>
  <artifactId>facebook-android-api</artifactId>
  ...
  <exclusions>
    <exclusion>
      <artifactId>support-v4</artifactId>
      <groupId>com.google.android</groupId>
    </exclusion>
  </exclusions>
</dependency>
```

####Gradle

Add the following dependency to your build.gradle

```javascript
dependencies {
  compile 'fr.avianey:facebook-android-api:+@aar'
  // other dependencies
}
```

If you want to use a newer version of the android-support-v4 dependency, exclude the old one with this line :  

```javascript
configurations.all {
  exclude group: 'com.google.android', module: 'support-v4', version: 'r7'
  // other configurations
}
```

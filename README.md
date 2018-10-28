# Bintray
Script for publishing libraries to Bintray

Usage
--------
1. Add those lines in the end of your `build.gradle` and change values of extension properties to actual.
```groovy
ext {
    publishGroupId = 'ru.digipeople.logger'
    publishArtifactId = 'logger'
    publishVersion = '1.0.0'
    publishDesc = "Logger implementation for Android"
    publishVcsUrl = "https://github.com/DigiPeopleInc/Logger"
}

apply from: 'https://raw.githubusercontent.com/DigiPeopleInc/Bintray/master/publish_v1.gradle'
```
2.  Add bintray credentials to your `local.properties`
```properties
# Bintray credentials
bintray.user=<user_mame>
bintray.apikey=<api_key>
```

3. Publish library
```
gradlew cleanAssemblePublish
```
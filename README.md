Gradle Play Publisher Demo 
========================================

This is very useful plugin for building, uploading, and then promoting your App Bundle or APK to publishing app listings and other metadata in google play console.

Step 1 - Add Gradle Play Publisher Dependencies
-----

Open your app/build.gradle (Module: app) file, add the following to the very top.

```gradle

buildscript {
    repositories {
         maven { url 'https://oss.sonatype.org/content/repositories/snapshots' }
    }
    dependencies {
          classpath 'com.github.triplet.gradle:play-publisher:2.8.0-SNAPSHOT'
    }
}

apply plugin: 'com.github.triplet.play'

play {
    serviceAccountCredentials = file("your-server-acount-key.json")
}

```

Step 2 - For Retrieve the play store listing such as icon, screenshot, title, description, etc..
------
```gradle

./gradlew bootstrap --product

```

Step 3 - For Updating the play store listing such as icon, screenshot, title, description, etc..
------
```gradle

./gradlew publishProducts

```


LIMITATION
-----
The first APK or App Bundle needs to be uploaded via the Google Play Console because registering the app with the Play Store cannot be done using the Play Developer API. For all subsequent uploads and changes, GPP may be used.

SUPPORT ❤️
-----

Find this demo useful? Support it by joining [**stargazers**](https://github.com/aman-jham/google-gradle-play-publisher-demo/stargazers) for this repository ⭐️
<br/>
And [**follow me**](https://github.com/aman-jham?tab=followers) for my next creations 👍

LICENCE
-----

Google-Play-gradle-play-publisher-demo by [Aman Jham](https://www.linkedin.com/in/aman-jham-9436276a/) is licensed under a [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0).
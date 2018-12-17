
# bugsavvy-android
In-App Feedback and bug-reporting SDK for Android Apps 

## Installation
### Gradle

in  project level build.gradle.

```groovy
allprojects {
    repositories {
        maven { url "https://dl.bintray.com/ahmed56734/maven" }
        maven { url "https://jitpack.io" }
    }
}
```
in app module build.gradle
```groovy
implementation 'com.bugsavvy:bugsavvy:1.0.0-alpha02'
```



## Usage


```kotlin
class App : Application(){
    override fun onCreate() {
        BugSavvy.Builder(this)
                .setInvocationEvents(BugSavvyInvocationEvent.SHAKE)
                .setPrimaryColor(R.color.colorPrimary)
                .setColorTheme(BugSavvyColorTheme.BugSavvyColorThemeLight)
                .build()
    }
}
```

##### invoke
```kotlin
BugSavvy.invoke()
```
##### Logs
```kotlin
BugSavvyLogger.i("tag", "message")
```

## screenshots
<img src="https://github.com/ahmed56734/bugsavvy-android-sample/blob/master/screenshots/1.png" width="150"> <img src="https://github.com/ahmed56734/bugsavvy-android-sample/blob/master/screenshots/2.png" width="150"> <img src="https://github.com/ahmed56734/bugsavvy-android-sample/blob/master/screenshots/3.png" width="150"> <img src="https://github.com/ahmed56734/bugsavvy-android-sample/blob/master/screenshots/4.png" width="150">

## notes
- app has to be migrated to androidx if not migrated already.
- sample app code will be published soon.

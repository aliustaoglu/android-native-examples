1. Create a new project with No Activity
2. Add new Java File as "MainActivity.java"
3. Add a new layout called main_activity.xml
And make MainActivity as the launcher
```xml
<application>
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>

        </activity>
<application>
```
4. Add gradle dependencies for navigation
  https://developer.android.com/guide/navigation/navigation-getting-started
5. If you want to generate safeargs add below to buildscript>dependencies in build.gradle (Project file)
  classpath "androidx.navigation:navigation-safe-args-gradle-plugin:$nav_version"
6. Also add plugin to build.gradle (app)
  apply plugin: "androidx.navigation.safeargs"
7. Create 2 empty fragments (eg. ListFragment, DetailFragment). Include layouts but do not include factory methods
8. Add new Android Resource File with resource type of Navigation and name it (eg. main_navigation.xml)
9. Add a NavHostFragment into main_activity.xml and refer to the resource you added above
10. Add 2 fragments into main_navigation
11. Create an action from listFragment to detailFragment
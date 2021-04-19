---
title: Adding Custom Fonts in Android Apps 
last_modified_at: 2019-06-21
categories: 
   - Blog
tags: 
   - Android
   - Font 
   - Custom
   - Fonts
---

This is the most important thing in Android development for making UI really beautiful and understandable for user expecially for Persian or arabic language users.

To add a custom font easily, (*which I prefer using [Calligraphy](https://github.com/InflationX/Calligraphy) library*). First, paste your font in `Assets` folder and then, add these dependencies in app `Build.gradle`:

```
dependencies {
    implementation 'io.github.inflationx:calligraphy3:3.1.1'
    implementation 'io.github.inflationx:viewpump:1.0.0'
}
```

After that, you'll need to hit `sync now` from above. After syncing the `gradle`, create a class called `CustomFont` with following codes. You might consider adding `fonts` folder inside `/Assets`. So -> `/Assets/fonts`. 

**Kotlin class:**

```kotlin
class CustomFont : Application() {

    override fun onCreate() {
        super.onCreate()
        ViewPump.init(ViewPump.builder()
                .addInterceptor(CalligraphyInterceptor(
                  CalligraphyConfig.Builder()
                    .setDefaultFontPath("fonts/myFont.ttf")
                    .setFontAttrId(R.attr.fontPath)
                    .build()))
                .build())
    }
}
```

Here I pasted my font (*called `myFont.ttf`*) inside `/Assets/fonts` folder and link it inside `setDefaultFontPath` double quotation.
So, we did the whole thing but, the class is unusable and for preventing that, go to `AndroidManifest.xml` and inside `application` tag, link your class in `android:name` attribute like this:

```xml
<application
        android:name=".CustomFont"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:supportsRtl="true">
```

And that's it. So for using in each `class` or `Activity` you want, the only thing you should do is adding following codes after `class` - `Activity` definition:

```kotlin
class MainActivity : AppCompatActivity() {

   override fun attachBaseContext(newBase: Context) {
      super.attachBaseContext(ViewPumpContextWrapper.wrap(newBase))
   }
```
That's all of it.




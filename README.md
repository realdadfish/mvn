A repository of assorted (Android) libraries.

Android Test Kit is packaged here with a local build that utilized [Dagger 1.2.1](https://square.github.io/dagger/), as an alternative of Jake Wharton's own [Double Espresso](https://github.com/JakeWharton/double-espresso), which does not play nicely with Robolectric tests in the same source tree ([more information](http://stackoverflow.com/questions/23989278)).

To use this repository in your Gradle-based project, include it so:

    repositories {
        ...
        maven { url "https://raw.github.com/tommyd3mdi/mvn/master" }
    }

Then, provide the dependency like so:

    androidTestCompile("com.google.android.apps.common.testing.ui.espresso:espresso:1.1") {
        exclude group: "com.squareup.dagger"
        ...
    }

There is also a repackaged version of okio / okhttp that works with
Android L build LVP79. Use these artifacts:

    compile 'com.squareup.okio:okio:1.0.0-REPACKAGED'

and

    compile 'com.squareup.okhttp:okhttp:2.0.0-REPACKAGED-OKIO'

respectively.

Finally, this repository contains a patched version of [ACRA 4.5.0](http://www.acra.ch) that make it work
on Android Devices using ART until https://github.com/ACRA/acra/issues/136 is properly fixed. Include it like this:

    compile 'ch.acra:acra:4.5.0-ART-FIX'

- Thomas

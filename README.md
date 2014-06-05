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

- Thomas

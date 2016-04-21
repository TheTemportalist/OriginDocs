Setup
==========================

After setting up your Forge workspace, you will first want to add Origin as a dependency.

If you plan to use the API as a true API, then the API may not exist when you run your mod in a mod-pack.
If you do not plan on actauly relying on any of the classes in the API package,
then you should setup your Origin dependency as an API.
Otherwise, should you decide to rely on the classes in either the API or Foundation packages,
you MUST setup Origin as a foundation dependency (compile time).
Follow the instructions below depending on if you are using Origin as an API or as a Foundation.

Both
--------------------

For both setups you will need to find your `build.gradle` file. This holds the build script from Forge.
From there, add the following block of code to your gradle file:

```
repositories {
    mavenCentral()
    jcenter()
    maven {
        name "dsiriusArt"
        url "http://box1.dmodoomsirius.me:8081/artifactory/libs-release/"
    }
}
```

This code will allow Forge/Gradle to pull from the online repository in order to setup Origin

API
--------------------

1. Find your `build.gradle` file
2. Add this to it:
```
dependencies {
    deobfProvided "temportalist.origin:Origin:9.+"
}
```

Foundation
--------------------

1. Find your `build.gradle` file
2. Add this to it:
```
dependencies {
    deobfCompile "temportalist.origin:Origin:9.0.+"
}
```

!!! note
When using a Foundation setup, the second digit (for Origin) in SemVer notation indicates the foundation release.
If you want to setup with OriginFoundation 2.0.0, use Origin version 9.2.0

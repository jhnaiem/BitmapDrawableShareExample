# BitmapDrawableShareExample
[![](https://jitpack.io/v/jhnaiem/BitmapDrawableShareExample.svg)](https://jitpack.io/#jhnaiem/BitmapDrawableShareExample)

This Android library provides functionality to share BitmapDrawable objects, sourced from XML or Composable, across different parts of your application.

## Features
- Share BitmapDrawable objects from XML or Composable.
- Easy to integrate with minimal code changes.

## Install

In settings.gradle, add maven { url 'https://jitpack.io' }

### Groovy

```groovy
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()

        maven { url 'https://jitpack.io' }
    }
}
```

Include the JitPack.io Maven repo in your project's build.gradle file

```groovy
allprojects {
 repositories {
    maven { url "https://jitpack.io" }
 }
}
```

Then add this dependency to your app's build.gradle file

```groovy
dependencies {
	        implementation 'com.github.jhnaiem:BitmapDrawableSharer:$current-version'
	}
``````


## Usage

**From XML**

To share a BitmapDrawable from XML, use the following code:

```kotlin xml

val bitmapDrawable = binding.imgPhoto.drawable as BitmapDrawable
    BitmapDrawableSharer.shareImage(requireContext(), photoId, bitmapDrawable)
```

In this example, imgPhoto is the ID of the drawable resource.

**From Composable**

To share a BitmapDrawable from Composable, use the following code:

```kotlin xml
BitmapDrawableSharer.shareImage( context, photoId, bitmapDrawable)
```
After obtaining the bitmapDrawable, you can use it in your application as needed.

## Contributing
We welcome contributions to this library. If you find a bug or have a feature request, please open an issue on our GitHub repository.

## License
This library is licensed under the Apache License, Version 2.0. See the LICENSE file for details.

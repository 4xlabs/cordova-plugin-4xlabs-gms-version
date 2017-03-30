Cordova GMS library version sync plugin for Android
===================================================
This plugin is a Google APIs for Android library version sync.
Both [PhoneGap](http://phonegap.com/) and [Apache Cordova](http://cordova.apache.org/) are supported.

---------------------------------------------------

## Installation

Cordova plugin installation guide, https://cordova.apache.org/docs/en/latest/platform_plugin_versioning_ref/index.html#plugin-versioning

*Github (current master, potentially unstable)*
```bash
$> cordova plugin add https://github.com/4xlabs/cordova-plugin-4xlabs-gms-version
```

If you re-install the plugin, please always remove the plugin first, then remove the SDK

```bash
$> cordova plugin rm cordova-plugin-4xlabs-gms-version
$> cordova plugin add https://github.com/4xlabs/cordova-plugin-4xlabs-gms-version
```

## Last release information

**v0.0.1 - 31/Mar/2017**
- Initial version.
- Google APIs for Android version 10.2.1, [Release notes February 2017 - v.10.2](https://developers.google.com/android/guides/releases#february_2017_-_v102)
- [Set Up Google Play Services](https://developers.google.com/android/guides/setup)

```
com.google.android.gms:play-services-auth:10.2.1
com.google.android.gms:play-services-identity:10.2.1
com.google.android.gms:play-services-gcm:10.2.1
com.google.android.gms:play-services-location:10.2.1
com.google.android.gms:play-services-maps:10.2.1
```

## Notes
To resolve conflict version from other different plugins

File: platforms/android/project.properties

```ini
cordova.system.library.3=com.google.android.gms:play-services-gcm:10.2+
cordova.system.library.5=com.google.android.gms:play-services-maps:9.8.0
cordova.system.library.6=com.google.android.gms:play-services-location:9.8.0
cordova.system.library.7=com.google.android.gms:play-services-auth:+
cordova.system.library.8=com.google.android.gms:play-services-identity:+
```

Build failed

```
FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':compileDebugJavaWithJavac'.
> Compilation failed; see the compiler error output for details.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.

Error: cmd: Command failed with exit code 1 Error output:
Note: Some input files use or override a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
Note: Some input files use or override a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
C:\projects\mobileapp\platforms\android\src\plugin\google\maps\PluginUtil.java:135: error: cannot access AbstractSafeParcelable
    Builder builder = LatLngBounds.builder();
                                  ^
  class file for com.google.android.gms.common.internal.safeparcel.AbstractSafeParcelable not found
Note: Some input files use or override a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
Note: Some input files use unchecked or unsafe operations.
Note: Recompile with -Xlint:unchecked for details.
1 error

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':compileDebugJavaWithJavac'.
> Compilation failed; see the compiler error output for details.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.
```
Cordova GMS library version sync plugin for Android
===================================================
This plugin is a Google APIs for Android library version sync.
Both [PhoneGap](http://phonegap.com/) and [Apache Cordova](http://cordova.apache.org/) are supported.

---------------------------------------------------

## Installation

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
- Google APIs for Android version 10.2.1
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

```xml
<framework src="com.google.android.gms:play-services-auth:+" />
<framework src="com.google.android.gms:play-services-identity:+" />
<framework src="com.google.android.gms:play-services-auth:9.8.0" />
<framework src="com.google.android.gms:play-services-identity:9.8.0" />
```
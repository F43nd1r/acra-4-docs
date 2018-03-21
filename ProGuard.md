# Using ACRA with ProGuard

## Introduction

This Wiki will show you how to use ACRA with ProGuard enabled.  It does not try to explain all the details of using ProGuard as there are many other good resources for that including:

http://proguard.sourceforge.net/index.html

http://developer.android.com/guide/developing/tools/proguard.html

http://android-developers.blogspot.com/2010/09/proguard-android-and-licensing-server.html

It also assumes you have ACRA installed in your project and setup correctly.  If you don't have ACRA setup please read the [how to](BasicSetup) first.

## Details

ProGuard is a tool that shrinks, optimizes and obfuscates your code and is included when you create a new Android project in Eclipse.  In order to use ProGuard with ACRA you will need to enable ProGuard by making a change to your `project.properties` file and by making a few small changes to your ProGuard configuration file (`proguard-project.txt`).

****NB as of ACRA 4.8.0, the ACRA AAR ships with a proguard.cfg containing all the rules required by ACRA, so you don't need to specify any ACRA specific rules. ****

But in order to enable ProGuard, add the appropriate build config to your project.
For Maven this would mean adding a `src/main/proguard/proguard.cfg` file and the following to the android-maven-plugin config of your pom.xml:
```
<proguard>
    <skip>false</skip>
    <config>src/main/proguard/proguard.cfg</config>
</proguard>
```

Your proguard.cfg should contain those Proguard rules that you wish to apply to your project. A good starting point are those below.

```
-optimizationpasses 5
-dontusemixedcaseclassnames
-dontskipnonpubliclibraryclasses
-dontpreverify
-verbose
-optimizations !code/simplification/arithmetic,!field/*,!class/merging/*
-keep public class * extends android.app.Activity
-keep public class * extends android.app.Application
-keep public class * extends android.app.Service
-keep public class * extends android.content.BroadcastReceiver
-keep public class * extends android.content.ContentProvider
-keep public class com.android.vending.licensing.ILicensingService
-keepclasseswithmembernames class * {
    native <methods>;
}
-keepclasseswithmembernames class * {
    public <init>(android.content.Context, android.util.AttributeSet);
}
-keepclasseswithmembernames class * {
    public <init>(android.content.Context, android.util.AttributeSet, int);
}
-keepclassmembers enum * {
    public static **[] values();
    public static ** valueOf(java.lang.String);
}
-keep class * implements android.os.Parcelable {
  public static final android.os.Parcelable$Creator *;
}
```

As mentioned above, since 4.8.0 ACRA has shipped with it's own proguard.cfg, but if for some reason you want to override ACRA's config then these are the values that ACRA is recommending.

```
#ACRA specifics
# Restore some Source file names and restore approximate line numbers in the stack traces,
# otherwise the stack traces are pretty useless
-keepattributes SourceFile,LineNumberTable

# ACRA needs "annotations" so add this... 
# Note: This may already be defined in the default "proguard-android-optimize.txt"
# file in the SDK. If it is, then you don't need to duplicate it. See your
# "project.properties" file to get the path to the default "proguard-android-optimize.txt".
-keepattributes *Annotation*

# Keep all the ACRA classes
-keep class org.acra.** { *; }

# Don't warn about removed methods from AppCompat
-dontwarn android.support.v4.app.NotificationCompat*
```

I recommend keep all the ACRA classes so that your Proguard config remains simple.
You don't really need to trim or obfuscate the ACRA classes do you?
It's not like ACRA is a big library or especially secret.


But if you really feel you need to pare them down as much as possible then use the following:
```
# keep this class so that logging will show 'ACRA' and not a obfuscated name like 'a'.
# Note: if you are removing log messages elsewhere in this file then this isn't necessary
-keep class org.acra.ACRA {
	*;
}

# keep this around for some enums that ACRA needs
-keep class org.acra.ReportingInteractionMode {
    *;
}

-keepnames class org.acra.sender.HttpSender$** {
    *;
}

-keepnames enum org.acra.ReportField {
    *;
}

# keep this otherwise it is removed by ProGuard
-keep public class org.acra.ErrorReporter
{
    public void addCustomData(java.lang.String,java.lang.String);
    public void putCustomData(java.lang.String,java.lang.String);
    public void removeCustomData(java.lang.String);
}

# keep this otherwise it is removed by ProGuard
-keep public class org.acra.ErrorReporter
{
    public void handleSilentException(java.lang.Throwable);
}
```

## Testing ACRA with ProGuard

Don't forget to test the crash reporting capability of your app after you have Proguarded to make sure that you haven't accidentally excluded something.

Do so by putting code in your application that causes an 'un-caught crash' which is outside of any try/catch blocks you have (temporarily of course.)  Since ProGuard may remove 'un-needed code', make sure your crash logic is complex enough where it won't be stripped out by the ProGuard optimizer.  For example:

```java
// cause a crash...
String sCrashString = null;
Log.e("MyApp", sCrashString.toString() );
```
or

```java
// cause a crash...
throw new NullPointerException();
```

If ACRA is working properly, you should see the results populated in your Google document that you created.  It should give you a stack trace with the file name and the line number where the crash happened.  Also, you should see something like this in your LogCat viewer (assuming you haven't stripped out logging):

```
12-22 10:54:20.533: DEBUG/ACRA(25633): Retrieve application default SharedPreferences.
12-22 10:54:20.533: DEBUG/ACRA(25633): Set OnSharedPreferenceChangeListener.
12-22 10:54:20.533: DEBUG/ACRA(25633): ACRA is enabled for com.yourdoman.yourapp, intializing...
12-22 10:54:20.553: DEBUG/ACRA(25633): Looking for error files in /data/data/com.yourdomain.yourapp/files
12-22 10:54:20.583: DEBUG/ACRA(25633): Writing crash report file.
12-22 10:54:20.603: DEBUG/ACRA(25633): Looking for error files in /data/data/com.yourdomain.yourapp/files
12-22 10:54:20.613: DEBUG/ACRA(25633): Connect to https://your.crashserver.com?formUri="your form key here" &amp;ifq
12-22 10:54:20.843: DEBUG/ACRA(25633): Posting crash report data
12-22 10:54:20.843: DEBUG/ACRA(25633): Reading response
12-22 10:54:21.153: DEBUG/ACRA(25633): <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd"><html><head><meta http-equiv="Content-type" content="text/html; charset=utf-8">
12-22 10:54:21.153: DEBUG/ACRA(25633): <title>Thanks!</title>
```

If the LogCat output stops after the "Connect to `https://your.crashserver.com?formUri="your form key here"' line then most likely your emulator or device is unable to reach the Internet.

**Remember to remove your crash code when you are done testing!**

Happy debugging.
## ACRA-4.10.0 (13-JUN-2017)
* https://github.com/ACRA/acra/pull/542 & https://github.com/ACRA/acra/pull/576 Fix internal crashes 
* https://github.com/ACRA/acra/pull/545 & https://github.com/ACRA/acra/pull/557 & https://github.com/ACRA/acra/pull/577 Improve extensibility of default senders
* https://github.com/ACRA/acra/pull/560 & https://github.com/ACRA/acra/pull/566 File attachment support

## ACRA-4.9.2 (7-JAN-2017)
* https://github.com/ACRA/acra/pull/524 Only attempt to resend error report on HTTP 408 (client timeout) or HTTP 500+ (server error).
* https://github.com/ACRA/acra/pull/526 & https://github.com/ACRA/acra/pull/535 Fixed order of collections.
* https://github.com/ACRA/acra/pull/528 Fix a rare runtime error caused by proguard
* https://github.com/ACRA/acra/pull/523 Switched internal structure to json - May cause breaking changes in classes interacting with CrashReportData, as its superclass was changed.
* https://github.com/ACRA/acra/issues/539 Added /res folder and R.txt to AAR.

## ACRA-4.9.1 (12-OCT-2016)
* https://github.com/ACRA/acra/pull/465 Cleanup last Activity from UI thread.
* https://github.com/ACRA/acra/pull/462 Added RetryPolicy.
* https://github.com/ACRA/acra/pull/506 Added applicationLogFileDir to allow specification of relative application log paths.
* https://github.com/ACRA/acra/pull/509 Don't ship Jar as part of the release. ACRA needs to be referenced as an AAR.
* https://github.com/ACRA/acra/pull/501 Handling null intent on SenderService restart.
* https://github.com/ACRA/acra/pull/504 Simplified logcat collector.
* https://github.com/ACRA/acra/pull/496 Simplified Collectors.
* https://github.com/ACRA/acra/pull/495 Better handling of application end when a debugger is attached.
* https://github.com/ACRA/acra/pull/488 Make BaseCrashReportDialog extend FragmentActivity to increase its versatility
* https://github.com/ACRA/acra/pull/487 Add a preInit() method to BaseCrashReportDialog for e.g. AppCompatDelegate setup
* https://github.com/ACRA/acra/pull/511 Using AppCompat classes where appropriate.
* https://github.com/ACRA/acra/pull/466 Allowing LogcatCollector to be configured to block for at most 3 seconds.
* https://github.com/ACRA/acra/pull/521 Change LastModifiedComparator implementation to be identical with Long.compare()

## ACRA-4.9.0 (4-JUN-2016)
* https://github.com/ACRA/acra/pull/460 Discard messages if HTTP 401 or 405 received from server.

## ACRA-4.9.0-RC-2 (9-MAY-2016)
* https://github.com/ACRA/acra/pull/453 Fix NullPointerException if no reporting mode is set.
* https://github.com/ACRA/acra/pull/457 Fix annotation default mistaken as custom value.
* https://github.com/ACRA/acra/pull/458 Never return null for BuildConfig class.

## ACRA-4.9.0-RC-1 (2-MAY-2016)
**NB there are API changes in this release which may require code changes IF you are configuring ACRA programmatically**
* https://github.com/ACRA/acra/pull/407 Updating to Android Support library 23.2.1
* https://github.com/ACRA/acra/pull/411 Exposing ACRA.isACRASenderServiceProcess()
* https://github.com/ACRA/acra/pull/412 Only start SenderService on startup IF there are approved reports to send.
* https://github.com/ACRA/acra/pull/413 Hardened construction of BaseCrashReportDialog so that automated test robots can't use it to break an app. **NB Breaking change:** override `init` instead of `onCreate` in subclasses.
* https://github.com/ACRA/acra/pull/425 Fix potential NPE getting process name.
* https://github.com/ACRA/acra/pull/427 More robust implementation of getProcessName.
* https://github.com/ACRA/acra/pull/436 Set the theme for the Notification dialog using the `resDialogTheme` attribute or config method.
* https://github.com/ACRA/acra/pull/432 **NB Breaking change** Configure KeyStore using a KeyStoreFactory class instead of a KeyStoreFactory instance so KeyStoreFactory classes don't have to be serializable. 
* https://github.com/ACRA/acra/pull/440 UserAgent for HTTP reports changed from "Android" to "Android ACRA <versionNr>"
* https://github.com/ACRA/acra/pull/439 **NB Breaking change** ACRAConfig is now `final`. Ie all setters have been removed. Configuration should be done via annotations or (if programmatic) via the `ConfigurationBuilder`.
* https://github.com/ACRA/acra/pull/438 Renamed `ACRAConfiguration.forceCloseDialogAfterToast()` to `ACRAConfiguration.alsoReportToAndroidFramework()` for better clarity on behaviour.
* https://github.com/ACRA/acra/pull/445 Moved checkCrashResources into `ConfigurationBuilder.build()` which nows throws a checked Exception. To mitigate, we have added `ACRA.init()` methods that take ConfigurationBuilder and handle that Exception.


## ACRA-4.8.5 (17-MAR-2016)
* https://github.com/ACRA/acra/pull/401 Fix NPE sending HTTPS when a KeyStoreFactory is not defined.
* https://github.com/ACRA/acra/pull/403 Fix TrustManagerFactory not initialized when no KeyStore provided.

## ACRA-4.8.3 (16-MAR-2016) DON'T USE - problem with HTTPS send.
* https://github.com/ACRA/acra/pull/373 Added Proguard rule to keep ReportSenderFactory constructors.
* https://github.com/ACRA/acra/pull/388 Instead of KeyStore pass a KeyStoreFactory around.
* https://github.com/ACRA/acra/pull/399 Removing ability to configure reports to NOT send at shutdown.

## ACRA-4.8.2 (16-FEB-2016)
* https://github.com/ACRA/acra/issues/366 Fix for NPE on ConfigurationBuilder.build() when there is no ReportCrashes annotation on Application.
* https://github.com/ACRA/acra/pull/370 Fix for NPE on startup deleting unsent reports from old app version.
* https://github.com/ACRA/acra/pull/368 Addition of Android-Support annotations. Thanks https://github.com/F43nd1r

## ACRA-4.8.1 (3-FEB-2016)
* https://github.com/ACRA/acra/issues/354 Fix for SenderService crashing on Android 19 and earlier.
* https://github.com/ACRA/acra/pull/359 Looking for BuildConfig class in the package defined in AndroidManifest.
* https://github.com/ACRA/acra/pull/360 Moving towards making ACRAConfiguration immutable
* https://github.com/ACRA/acra/pull/357 Hide all ACRA debug log unless ACRA.DEV_LOGGING is switched on.

## ACRA-4.8.0 (30-JAN-2016)

***WARNING*** ACRA-4.8.0 service crashes on Android 19 and earlier. See https://github.com/ACRA/acra/issues/354. Wait for 4.8.1

***The 4.8.0 AAR ships with an AndroidManifest containing config for SenderService and CrashReportDialog. It also contains a proguard.cfg with ACRA specific proguard rules which should be consumed automagically by your build tool.***

**Breaking changes**
* ReportSender API has changed. See https://github.com/ACRA/acra/wiki/Report-Destinations#implementing-your-own-sender
* ReportSenders need to be configured **BEFORE** ACRA is initialised. See https://github.com/ACRA/acra/wiki/Report-Destinations#implementing-your-own-sender
* ACRAConfiguration has moved to the org.acra.config package. 

**Other Changes**
* https://github.com/ACRA/acra/pull/339 Capturing logcat earlier so avoid logs being filled with ACRA output.
* https://github.com/ACRA/acra/pull/336 Handling log files that are contained within sub folders of the application files folder.
* https://github.com/ACRA/acra/pull/341 Making Dialog easy to extend.
* https://github.com/ACRA/acra/pull/344 Reports are sent via the SenderService in a separate process.
  NB This introduces a ***BREAKING API change***. ReportSenders can no longer be configured directly. You must configure a ReportSenderFactory that is responsible for constructing and configuring the ReportSender. You can do so programmatically or declaratively. Many thanks to https://github.com/romansl for making the start on this.
  See https://github.com/ACRA/acra/wiki/Report-Destinations#implementing-your-own-sender for details.
* https://github.com/ACRA/acra/pull/346 ACRA nows ships with its own proguard.cfg so you don't need to specifiy ACRA specific rules (unless you want to override the defaults).
* https://github.com/ACRA/acra/pull/347 Don't send reports on startup unless `acra.enable` is true.
* https://github.com/ACRA/acra/pull/345 Report 2nd stacktrace report. Only log the error once.

## ACRA-4.7.0 (3-DEC-2015)
  * Known Issue https://github.com/ACRA/acra/issues/332 Due to the non-deterministic way in which OkHttp creates Threads it is possible that ACRA itself will crash when trying to send a report on shutdown. The report should still be sent on app restart. If you really want to avoid then set *sendReportsAtShutdown* == *false*.

## ACRA-4.7.0-RC3 (23-NOV-2015) - NB this is a release candidate - use at own risk
  * https://github.com/ACRA/acra/pull/330 Removing use of inet.harder library. ACRA now requires Froyo or greater. If no Froyo then ACRA disables itself.

## ACRA-4.7.0-RC2 (14-NOV-2015)
  * https://github.com/ACRA/acra/pull/315 Allowing authentication with crash server in pre Gingerbread apps.
  * https://github.com/ACRA/acra/pull/316 HTTP response code >= 200 and < 300 indicates the report was sent.
  * https://github.com/ACRA/acra/pull/317 Removing SYSTEM, SECURE and GLOBAL SETTINGS from the *default* report fields due to privacy concerns.
  * https://github.com/ACRA/acra/pull/310 Configuring request length instead of using chunked streaming mode to support servers that can't handled chunked mode.

## ACRA-4.7.0-RC1 (20-SEP-2015)
  * https://github.com/ACRA/acra/pull/279 Fixed bug when poorly configured application log filename.
  * https://github.com/ACRA/acra/issues/273 Fixed potential crash when retrieving media data.
  * https://github.com/ACRA/acra/issues/268 NoSuchMethod StringUtils.isEmpty for API less than 9.
    ACRA now supports back to API 3 once again.
  * https://github.com/ACRA/acra/pull/293 if multiple senders and the first Sender fails that the others are attempted.
  * https://github.com/ACRA/acra/pull/294 Removed capability of OOM errors by streaming report instead of reading the entire report into memory.
  * **Breaking Change** - removed *ACRA#setConfig()*. This method should have been removed some time ago. Manually supplied ACRA config should be supplied into *ACRA#init()*.

## ACRA-4.6.2 (28-APR-2015)
  * https://github.com/ACRA/acra/pull/242 Fix for user email address being cleared when using crash report dialog.
  * https://github.com/ACRA/acra/pull/241 Fix check for whether to gather read logs.
  * https://github.com/ACRA/acra/issues/262 Silent mode wouldn't wait for ACRA to send report.

## ACRA-4.6.1 (15-FEB-2015)
  * PR#237 Don't require build config class in ACRA config

## ACRA-4.6.0 (7-FEB-2015)
  * PR#233 PR#235 Allowing the location of BuildConfig to be configurable to support Gradle build flavours.
**NB This is a breaking change IF your are capturing BuildConfig AND your Application class does not reside in the Java package defined in your original AndroidManifest manifest:package attribute.** In that scenario you will need to explicitly configure 'buildConfigClass' in your ACRA config.

## ACRA-4.6.0RC2 (24-JAN-2015)
  * PR#216 Fix for NPE on ```endApplication()``` when calling ```handleException(th, true)```
  * PR#215 Removed backwards incompatible change introduced by #210
  * PR#221 Switched to using TlsSniSocketFactory as default for SSL.
  * PR#222 Ability to configure a custom Crash Report Dialog via ```reportDialogClass```
  * PR#227 Bugfix - Notification now opens dialog.

## ACRA-4.6.0RC1 (8-JAN-2015):

### Breaking changes:
  * GoogleFormSender has been removed.

### Other changes:
  * PR#202 Return immediately if sending silently and not ending application.
  * PR#199 Make send reports on shutdown configurable.
  * Use RFC822 for timezone
  * Fixed #174 ACRA crashes when converting SHARED_PREFERENCES to JSON
  * PR#173 Ability to customize the CrashReportDialog button text
  * Logging Exceptions as soon as they are received
  * Ensuring that ACRA never retains a strong reference to an Activity
  * PR#87 to allow interceptor to inject additional data on each exception report.
  * Fixed #136 SendWorker failing because it cannot start a Thread on App destruction
  * PR#158 to keep custom variables ordered by entry order
  * PR#155 to clear out custom parameters
  * PR#154 Use ACTION_SEND_TO in EailIntentSender
  * PR#132 Added support for a custom key store
  * PR#98 Additional ACRA init methods.
  * PR#89 Added STACKTRACE_HASH attribute to ErrorReport
  * PR#83 ReportBuilder and ability to send error with no stacktrace.
    
## ACRA-4.5.0:
  * When receiving 403 errors from server, discard report.

## ACRA-4.5.0RC3:
  * Fixed Issue #84: new `CrashReportDialog` was missing check for empty resource ids.

## ACRA-4.5.0RC2:
  * Merged PR #76: add support for defining HTTP Headers.
  * Fixed Issue #59: `customReportContent` could not be set programmatically after `ACRA.init()`.
  * Fixed Issues #73 and #78: `CrashReportDialog` not shown on Android 4.2.2
  * Fixed Issue #77: report building was failing if a Key/null pair was added to `CUSTOM_DATA`
  * Fixed Issue #75: JSON type was hardcoded with PUT method

## ACRA-4.5.0RC:
  * Fixed Issue #38: delete reports when notification is cancelled.
  * Fixed Issue #37: now use `AlertDialog.Builder` to create a dialog with button ordered according to the platform UI guidelines. We can also remove the theme from the manifest for the `CrashReportDialog` activity so the platform uses its preferred theme.
  * Fixed Issue #60: HTTP 409 return codes (conflict) are not considered as errors anymore. Report is considered as already received and is discarded.
  * Fixed Issue #66 and acra/acralyzer#23 - Escape special characters to prevent new lines in values from being interpreted as new keys in CUSTOM_DATA.
  * Fixed issue #42 (infinite-acra-crash) by explicitly finishing the last Activity
  * Fixed Issue #3 - do not throw an exception when init is called more than once. Just issue a warning log and don't do anything else.
  * `HttpPostSender` has been replaced with a `HttpSender`, more versatile:
    * new option `httpMethod`: to allow to send via `PUT` or `POST` method. When using `PUT`, the report UUID is appended at the end of the `formURI`.
    * new option `reportType`: can be set to `FORM` or `JSON` to encode report data in either one of these formats.
  * Creation of a `DisplayManagerCollector` which is able to collect display(s) data with or without the new `DisplayManager` introduced with Android 4.2
  * Addition of a new configuration item `excludeMatchingSettingsKeys` to allow filtering out sensitive data from `Settings.System`, `Settings.Secure` and `Settings.Global`.
  * Addition of a new field `SETTINGS_GLOBAL` which collects data from the new `android.provider.Settings.Global` introduced in Android 4.2 to handle multiple user accounts with common settings.

## ACRA-4.4.0:
  * Sending reports over HTTPS is now more secure with SSL certificates validation. If you need to post to a server with a self-signed certificate, set the option `disableSSLCertValidation` to true

## ACRA-4.3.1:
  * Issue 11: put `ErrorReporter.checkReportsOnApplicationStart()` back in the public API
  * Issue 147: handle back button like a Cancel on the crash dialog
  * Issue 148: Comment field of CrashReportDialog is lost after device rotation 
  * Issue 149: CrashReportDialog content is now scrollable.
  * Issue 138: Crash on application start
  * Fix for issue 143: DIALOG is displayed even if acra.alwaysaccept is true

## ACRA-4.3.0:
## ACRA-4.3.0RC:
  * Removed a few unnecessary Log.d traces.
  * Changed old spreadsheet.google.com default form post URL for the newer one docs.google.com/spreadsheet
  * After new discussion around Issue 111, GoogleFormSender and HttpPostSender get their former constructors back in addition to the new constructor without formKey/formUri. So, if the sender is initialized without formUri/formKey provided, it will always look at ACRA.getConfig() to get its destination so it can be changed dynamically. If the formKey/formUri is provided, then it is set once and never changed.
  * Various changes due to discussion on Issue 111:
    * Creation of a setDefaultReportSenders() method on ErrorReporter. This is the method which is called by ACRA.init() to instanciate the relevant default ReportSenders depending on the provision of mailTo, formUri and formKey parameters.
      The method should now be called whenever you wish to change the configuration by switching from one of these 3 parameter to the others.
    * HTTPPostSender and GoogleFormSender do not take their formURI/formKey as a constructor parameter anymore. They get the value from ACRA.getConfig() instead. If their parameters are changed programmatically, they don't need to be reinstanciated.
    * Addition of a warning message if ACRA.getConfig() is called before ACRA.init(). ACRA.getNewDefaultConfig() should be used instead.
    * ACRA.getNewDefaultConfig() now requires an Application as a parameter. This allows to create a new ACRAConfiguration instance with @ReportsCrashes defined values BEFORE calling ACRA.init()
  * added: new configuration item googleFormUrlFormat to allow, if Google Docs/Drive services evolve, to modify the Form URL structure without releasing a new ACRA version in emergency.

## ACRA-4.3.0b2:
  * fixed: issue 137 - with JellyBean, we now send only logcat traces related to our app. But this does not require the READ_LOGS permission 

## ACRA-4.3.0b1:
  * modified: MediaCodecListCollector now displays codec profiles and levels names instead of abstract int values.
  * added: issue 135 - 'deleteOldUnsentReportsOnApplicationStart' annotation to control whether to delete old reports (defaults to true).
  * modified: removed DEVICE_ID from the default fields. INSTALLATION_ID should be enough and is not a sensible private data.
  * modified: issue 111 - ACRAConfiguration is not a static fields container anymore. Each instance holds its own set of values, this allow to define various configuration instances and switch between one or the other with a single object reference switch (ACRA.setConfig()))
  * added: MediaCodecListCollector to retrieve the list of supported codecs and capabilities for the device. Field name: MEDIA_CODEC_LIST. (Since API Level 16 - Jelly Beans)
  * added: ThreadCollector to retrieve the broken thread Id and Name. Field name: THREAD_DETAILS
  * modified: Refactored Configuration collection class, was not in the collectors package.
  * added back an handleException(Throwable e) without the endApplication boolean to enhance backward API compatibility.
  * added: new ReportField.APPLICATION_LOGFILE including the latest ReportsCrashes.applicationLogFileLines lines from the file ReportsCrashes.applicationLogFile. Allows to collect application specific log file data.
  * added: issue 70 - option excludeMatchingSharedPreferencesKeys to exclude sensible data from collected SharedPreferences.
  * added: issue 80 - option sendReportsInDevMode can now be set to false to disable sending reports in development mode. Reports will be sent only by signed applications.
  * fixed: issue 60 - ACRA crashes in NOTIFICATION mode without user comments.
  * added: logcatFilterByPid configuration item. When set to true, logcat field collects only lines related to the application process.
  * modified: Issue 66 - ReportsCrashes annotation is now @Inherited.
  * modified: handleException() method do not need to return the worker thread anymore
  * fixed: issue 69
  * modified: reduced TOAST wait from 4s to 3s.
  * fixed: stop calling ACRA when ACRA throws an exception but let the native exception handler do its job. Should fix Issue 72.
  * fixed: don't call dumpsys meminfo after on OutOfMemroryError. It looks like it hangs the app. 
  * modified: trying to clarify the logic of deleting/notifying reports on application start.
  * fixed: direct DIALOG mode is working again. The dialog creation has to be the last thing to do before killing the app.
  * fixed: the async wait for toast and sender thread termination was... crap. It is now fixed but the direct DIALOG does not work anymore. Must be a timing issue, which lets me think that this might not be a future proof solution.
  * fixed Issue 84: all email reports got "null crash report" as a title... 
  * modified: removed the DROPBOX, RADIOLOG and EVENTSLOG fields from default report templates. They should be activated only by devs who really need them.
  * new: full dynamic configuration
  * modified: asynchronous wait for Toast display and sender thread termination. No more chance to cause ANR.
  * modified: handleException and handleSilentException do not return the sender Thread anymore.
  * New: direct DIALOG mode, thanks to Julia Segal.
  * modified: lowered the default number of logcat lines to 100
  * New: configuration of resources now possible via setters. This is to fix Issue 85 with ADT 14 from which we can't pass Android Library Projects resources ids to ACRA as they are not final anymore.
  * Overall code cleaning and refactoring (William Ferguson)

## ACRA-4.2.3:
## ACRA-4.2.3RC:
  * Code cleaning and better files handling => should fix most report duplicates issues. (William Ferguson)

## ACRA-4.2.2RC:
  * Fixed: prevent persistent IS_SILENT
  * Fixed: prevent some report duplicates
  * Fixed: prevent persistent USER_COMMENT
  * Fixed: prevent ACRA Crash if getCrashReportFileList() is called without initializing ACRA
  * Fixed: handle 4xx and 5xx http response codes as errors => throw exception and keep report and retry later

## ACRA-4.2.1b:
  * Fixed: NOTIFICATION + mailTo was broken

## ACRA-4.2.0b:
  * New: Added a SHARED_PREFERENCES field containing K/V pairs of the application default shared preferences + sharedPreferences provided by developer with @ReportsCrashes(additionalSharedPreferences={"my.own.prefs","a.second.prefs"})
  * Fixed: do not send silent reports if acra.enabled or acra.disabled SharedProperties have been set to disable ACRA.
  * Fixed: after application restart with ACRA disabled from SharedPreferences settings, ACRA was not able to detect a change on this setting and reactivate. 
  
## ACRA-4.1.0b:
  * Issue 53: new @ReportsCrashes option to let the developer choose to display the Force Close dialog after the Toast.

## ACRA-4.0.1b:
  * Forced HttpClient SocketBufferSize to 8192 bytes as it appears that on some devices, the default size is set to a huge 2Mb.
  * Refactoring: extract constants from @ReportsCrashes. This was causing compilations issues with javac.
  * Issue 52: log substring was crashing when using http post with a response < 200 chars.

## ACRA-4.0.0b:
  * Fixed: Prevent ACRA from sending report duplicates when sending silent reports in simultaneous threads.
  * New: Added a IS_SILENT field.
  * New: socketTimeout configuration item in ReportsCrashes annotation.
  * Changed: Replaced URLConnection POST implementation with HttpClient HttpPost. Fixes timeouts with Basic Http Auth. Might fix https stability issues.
  * Changed: removed includeDropBox, includeEventsLog and includeRadioLog configuration items. This is now done by customizing reports content. Final default report template will not include these fields.
  * New: Added a SETTINGS_SECURE field for http://developer.android.com/reference/android/provider/Settings.Secure.html content
  * New: Added a SETTINGS_SYSTEM field http://developer.android.com/reference/android/provider/Settings.System.html content
  * New: Added an ENVIRONMENT field for state and details about external storage http://developer.android.com/intl/fr/reference/android/os/Environment.html
  * WontDo: PackageStats could be interesting but there is no public API to retrieve it.
  * New: Added an INSTALLATION_ID field containing http://android-developers.blogspot.com/2011/03/identifying-app-installations.html
  * New: Added a REPORT_ID field based on UUID.
  * New: All reports content can now be customized using ReportsCrashes.customReportContent. It replaces the mailReportFields that had been implemented only for mail reports before. This requires to create your own .csv and import it in GoogleCode.
  * Changed: Build data are now put together in a single column except for data about device model/manufacturer
  * Changed: Moved some report columns to put user related data together
  * New: Issue 46 - added an optional field for user email input in crash dialog. Retrieves and stores value from already implemented SharedPreferene. Field activation similar to user comment (provide a resourceId for its label). 
  * New: Added a DEVICE_FEATURES field http://developer.android.com/intl/fr/reference/android/content/pm/PackageManager.html#getSystemAvailableFeatures()
  * New: Added an USER_APP_START_DATE field
  * New: Added an includeDropBoxSystemTags config option
  * New: added an includeDropBox configuration item with default value to false. This is to avoid any performance issue due to DropBox events collection for people who don't need them.
  * Changed: removed debugging log event when examining SharedPreference update.
  * New: ACRA project has been mavenized: building and releasing is now handled with maven. See [Releasing] and [Maven] pages for details. 
  * Fixed: Issue 42 - prevent ACRA 3.2 from crashing because of pending reports from previous ACRA versions.
  * Fixed: in NOTIFICATION mode, user comments could be attached to wrong reports.
  * Fixed: in SILENT mode, only explicit SILENT exceptions (cast with handleSilentException) were sent on application crash. Standard exception were sent on application restart.
  * Fixed: possible NPE when enabling/disabling ACRA with SharedPreferences.
  * New: Added SharedPreferences items for:
  	* include system logs (may contain private data)
  	* include Device ID (IMEI) (this a private identifier)
  	* include user email (the user inputs his email address in the preference field)
  	* always accept sending reports
  * Changed: default behavior in NOTIFICATION mode when notif has been ignored: on next application start do not respawn the notification and delete non approved reports. A config item has been added to enable the old behaviour back.
  * Changed: renamed some report field names which could be confusing (related to android build)
  * New: added a Toast before collecting crash data
  * New: added 2 fields in reports: application version code (some devs don't always update
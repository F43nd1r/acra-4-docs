_**IN WORK**_
***


**Table of Contents**

- [additionalDropBoxTags](Configuration-A-Z#additionaldropboxtags)
- [additionalSharedPreferences](Configuration-A-Z#additionalsharedpreferences)
- [alsoReportToAndroidFramework](Configuration-A-Z#alsoreporttoandroidframework)
- [applicationLogFile](Configuration-A-Z#applicationlogfile)
- [applicationLogFileLines](Configuration-A-Z#applicationlogfilelines)
- [buildConfigClass](Configuration-A-Z#buildconfigclass)
- [connectionTimeout](Configuration-A-Z#connectiontimeout)
- [customReportContent](Configuration-A-Z#customreportcontent)
- [deleteOldUnsentReportsOnApplicationStart](Configuration-A-Z#deleteoldunsentreportsonapplicationstart)
- [deleteUnapprovedReportsOnApplicationStart](Configuration-A-Z#deleteunapprovedreportsonapplicationstart)
- [dropboxCollectionMinutes](Configuration-A-Z#dropboxcollectionminutes)
- [excludeMatchingSharedPreferencesKeys](Configuration-A-Z#excludematchingsharedpreferenceskeys)
- [excludeMatchingSettingsKeys](Configuration-A-Z#excludematchingsettingskeys)
- [formUri](Configuration-A-Z#formuri)
- [formUriBasicAuthLogin](Configuration-A-Z#formuribasicauthlogin)
- [formUriBasicAuthPassword](Configuration-A-Z#formuribasicauthpassword)
- [includeDropBoxSystemTags](Configuration-A-Z#includedropboxsystemtags)
- [logcatArguments](Configuration-A-Z#logcatarguments)
- [logcatFilterByPid](Configuration-A-Z#logcatfilterbypid)
- [mailTo](Configuration-A-Z#mailto)
- [mode](Configuration-A-Z#mode)
- [reportDialogClass](Configuration-A-Z#reportdialogclass)
- [reportSenderFactoryClasses](Configuration-A-Z#reportsenderfactoryclasses)
- [resDialogCommentPrompt](Configuration-A-Z#resdialogcommentprompt)
- [resDialogEmailPrompt](Configuration-A-Z#resdialogemailprompt)
- [resDialogIcon](Configuration-A-Z#resdialogicon)
- [resDialogNegativeButtonText](Configuration-A-Z#resdialognegativebuttontext)
- [resDialogOkToast](Configuration-A-Z#resdialogoktoast)
- [resDialogPositiveButtonText](Configuration-A-Z#resdialogpositivebuttontext)
- [resDialogText](Configuration-A-Z#resdialogtext)
- [resDialogTheme](Configuration-A-Z#resdialogtheme)
- [resDialogTitle](Configuration-A-Z#resdialogtitle)
- [resNotifIcon](Configuration-A-Z#resnotificon)
- [resNotifText](Configuration-A-Z#resnotiftext)
- [resNotifTickerText](Configuration-A-Z#resnotiftickertext)
- [resNotifTitle](Configuration-A-Z#resnotiftitle)
- [resToastText](Configuration-A-Z#restoasttext)
- [sendReportsInDevMode](Configuration-A-Z#sendreportsindevmode)
- [sharedPreferencesName](Configuration-A-Z#sharedpreferencesname)
- [sharedPreferencesMode](Configuration-A-Z#sharedpreferencesmode)
- [socketTimeout](Configuration-A-Z#sockettimeout)

## formUri

Specify the report destination. See also [Backends](Backends)

Equivalent `ConfigurationBuilder.setFormUri`

## mode

See [User Interaction](AdvancedUsage#user-interaction)

Equivalent `ConfigurationBuilder.setReportingInteractionMode`

## resDialogPositiveButtonText

Use with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION`

Resource id for the label of positive button in the crash dialog.

If not provided, defaults to `android.R.string.ok`.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogPositiveButtonText`

## resDialogNegativeButtonText

Use with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION`

Resource id for the label of negative button in the crash dialog.

If not provided, defaults to `android.R.string.cancel`.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogNegativeButtonText`

## resDialogCommentPrompt

Use with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION`

Resource id for the user comment input label in the crash dialog.

If not provided, the input field is not shown.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogCommentPrompt`

## resDialogEmailPrompt

Use with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION`

Resource id for the user email adress input label in the crash dialog.

If not provided, the input field is not shown.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogEmailPrompt`

## resDialogIcon

Use with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION`

Resource id for the icon in the crash dialog.

If not provided, defaults to `android.R.drawable.ic_dialog_alert`.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogIcon`

## resDialogOkToast

Use with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION`

Resource id for the Toast text triggered when the user accepts to send a report in the crash dialog.

If not provided, the Toast is not shown.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogOkToast`

## resDialogText

**Required** for `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION` if `reportDialogClass` is not set or extends from `CrashReportDialog`.

Resource id for the text in the crash dialog.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogText`

## resDialogTitle

Use with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION`

Resource id for the title in the crash dialog.

If not provided, does not show any title.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogTitle`

## resDialogTheme

Use with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION`

Resource id for the theme of the crash dialog.

If not provided, defaults to `android.R.style.Theme_Dialog`.

See also [Dialog](AdvancedUsage#dialog)

Equivalent `ConfigurationBuilder.setResDialogTheme`

## resNotifIcon

Use with `ReportingInteractionMode.NOTIFICATION`

Resource id for the icon in the status bar notification.

If not provided, defaults to `android.R.drawable.stat_notify_error`.

See also [Notification](AdvancedUsage#status-bar-notification)

Equivalent `ConfigurationBuilder.setResNotifIcon`

## resNotifText

**Required** for `ReportingInteractionMode.NOTIFICATION`

Resource id for the text in the status bar notification.

See also [Notification](AdvancedUsage#status-bar-notification)

Equivalent `ConfigurationBuilder.setResNotifText`

## resNotifTickerText

**Required** for `ReportingInteractionMode.NOTIFICATION`

Resource id for the ticker text in the status bar notification.

See also [Notification](AdvancedUsage#status-bar-notification)

Equivalent `ConfigurationBuilder.setResNotifTickerText`

## resNotifTitle

**Required** for `ReportingInteractionMode.NOTIFICATION`

Resource id for the title in the status bar notification.

See also [Notification](AdvancedUsage#status-bar-notification)

Equivalent `ConfigurationBuilder.setResNotifTitle`

## resToastText

**Required** for `ReportingInteractionMode.TOAST`. May be used with `ReportingInteractionMode.DIALOG` or `ReportingInteractionMode.NOTIFICATION` 

Resource id for the Toast text triggered when the application crashes. This is displayed while the report is being created, before a possible dialog/notification appears. This allows the user to know what is happening just before the application is terminated.

See also [Toast](AdvancedUsage#toast-notification)

Equivalent `ConfigurationBuilder.setResNotifTitle`

## sharedPreferencesName

Name of the SharedPreferences that will host ACRA settings you can make accessible to your users through a preferences screen:
* `ACRA.PREF_DISABLE_ACRA` or `ACRA.PREF_ENABLE_ACRA`
* `ACRA.PREF_ALWAYS_ACCEPT`
* `ACRA.PREF_ENABLE_DEVICE_ID`
* `ACRA.PREF_ENABLE_SYSTEM_LOGS`

If not provided, defaults to the application default SharedPreferences, as retrieved with `PreferenceManager.getDefaultSharedPreferences(Context)`.

See also [User control](AdvancedUsage#letting-your-users-control-acra)

Equivalent `ConfigurationBuilder.setSharedPreferencesName`

## sharedPreferencesMode

Use **only** in conjunction with `sharedPreferencesName`.

Mode of the custom SharedPreference.

If not provided, defaults to `Context.MODE_PRIVATE`.

See also [User control](AdvancedUsage#letting-your-users-control-acra)

Equivalent `ConfigurationBuilder.setSharedPreferencesMode`

## includeDropBoxSystemTags

If enabled, DropBox events collection will include system tags:
* system_app_anr
* system_app_wtf
* system_app_crash
* system_server_anr
* system_server_wtf
* system_server_crash
* BATTERY_DISCHARGE_INFO
* SYSTEM_RECOVERY_LOG
* SYSTEM_BOOT
* SYSTEM_LAST_KMSG
* APANIC_CONSOLE
* APANIC_THREADS
* SYSTEM_RESTART
* SYSTEM_TOMBSTONE
* data_app_strictmode

If not provided, defaults to `false`.

See also [DropBoxManager](AdvancedUsage#adding-dropboxmanager-events-to-your-reports)

Equivalent `ConfigurationBuilder.setIncludeDropboxSystemTags`

## additionalDropBoxTags

Array of tags that you want to be fetched when collecting DropBox entries.

See also [DropBoxManager](AdvancedUsage#adding-dropboxmanager-events-to-your-reports)

Equivalent `ConfigurationBuilder.setAdditionalDropBoxTags`

## dropboxCollectionMinutes

Number of minutes to look back when collecting events from DropBoxManager.

If not provided, defaults to 5 minutes.

See also [DropBoxManager](AdvancedUsage#adding-dropboxmanager-events-to-your-reports)

Equivalent `ConfigurationBuilder.setDropboxCollectionMinutes`

## logcatArguments

Arguments to be passed to the logcat command line. 

If not provided, defaults to { "-t", "100", "-v", "time" }.

Do not include -b arguments for buffer selection, include ``ReportField.EVENTSLOG` and `ReportField.RADIOLOG` in `customReportContent` to activate alternative logcat buffers reporting. They will use the same other arguments as those provided here.

Equivalent `ConfigurationBuilder.setLogcatArguments`

## formUriBasicAuthLogin

Use **only** with `formUri` and `formUriBasicAuthPassword`.

Specifies a username for basic HTTP authentication. 

See also [Authentication](Report-Destinations#sending-reports-to-your-own-self-hosted-script)

Equivalent `ConfigurationBuilder.setFormUriBasicAuthLogin`

## formUriBasicAuthPassword

Use **only** with `formUri` and `formUriBasicAuthLogin`.

Specifies a username for basic HTTP authentication. 

See also [Authentication](Report-Destinations#sending-reports-to-your-own-self-hosted-script)

Equivalent `ConfigurationBuilder.setFormUriBasicAuthPassword`

## customReportContent

See [Report Content](AdvancedUsage#choosing-which-fields-to-be-included-in-reports)

Equivalent `ConfigurationBuilder.setCustomReportContent`

To toggle single fields use `ConfigurationBuilder.setReportField`.

## mailTo

Add your crash reports mailbox here if you want to send reports via email. This allows to get rid of the `INTERNET` permission.

Note that email mode uses different default Report Content.

See also [Sending by Email](Report-Destinations#sending-reports-by-email)

Equivalent `ConfigurationBuilder.setMailTo`

## deleteUnapprovedReportsOnApplicationStart

Controls whether unapproved reports are deleted on application start or not.

If not provided, defaults to `true`.

Silent and Toast reports are automatically approved.
Dialog and Notification reports required explicit approval by the user before they are sent.
On application restart the user is prompted with approval for any unsent reports.
So you generally don't want to accumulate unapproved reports, otherwise you will prompt them multiple times.

If this is set to true then all unapproved reports bar one will be deleted on application start.
The last report is always retained because that is the report that probably just happened.

If set to false then on restart the user will be prompted with approval for each unapproved report.

Equivalent `ConfigurationBuilder.setDeleteUnapprovedReportsOnApplicationStart`

## deleteOldUnsentReportsOnApplicationStart

This property can be used to determine whether old (out of date) reports should be sent or not.
Reports are considered old if the application has been updated since the last run.

If not provided, defaults to `true`.

Equivalent `ConfigurationBuilder.setDeleteOldUnsentReportsOnApplicationStart`

## connectionTimeout

Value in milliseconds for timeout attempting to connect to a network.

If not provided, defaults to 5 seconds.

Equivalent `ConfigurationBuilder.setConnectionTimeout`

## socketTimeout

Value in milliseconds for timeout receiving a response to a network request.

If the request is retried due to timeout, the socketTimeout will double before retrying the request.

If not provided, defaults to 8 seconds.

Equivalent `ConfigurationBuilder.setSocketTimeout`

## alsoReportToAndroidFramework

Set this to true if you prefer displaying the native force close dialog after the ACRA is done.

Recommended: Keep this set to false if using `ReportingInteractionMode.DIALOG`.

If not provided, defaults to `false`.

Equivalent `ConfigurationBuilder.setAlsoReportToAndroidFramework`

## additionalSharedPreferences

Add here your `SharedPreferences` identifier Strings if you use others than your application's default. They will be added to the `ReportField.SHARED_PREFERENCES` field.

See also [Custom SharedPreferences](AdvancedUsage#adding-custom-sharedpreferences-names)

Equivalent `ConfigurationBuilder.setAdditionalSharedPreferences`

## logcatFilterByPid

Set this to true if you want to include only logcat lines related to your Application process.

If not provided, defaults to `false`.

See also [Logcat](AdvancedUsage#adding-logcat-eventlog-or-radiolog-extracts-to-reports)

Equivalent `ConfigurationBuilder.setLogcatFilterByPid`

## sendReportsInDevMode

If disabled only signed packages will send reports.

If not provided, defaults to `true`. 

Equivalent `ConfigurationBuilder.setSendReportsInDevMode`

## excludeMatchingSharedPreferencesKeys

All preferences with a key that matches one of the here provided regex patterns will be excluded from collection.

See also [Excluding preferences](AdvancedUsage#exclude-sharedpreferences-keys)

Equivalent `ConfigurationBuilder.setExcludeMatchingSharedPreferencesKeys`

## excludeMatchingSettingsKeys

All keys of Settings.System, Settings.Secure and Settings.Global matching one of the here provided regex patterns will be excluded from collection.

See also [Excluding settings](AdvancedUsage#exclude-settings-keys)

Equivalent `ConfigurationBuilder.setExcludeMatchingSettinsKeys`

## buildConfigClass

ACRA tries to dicover this automatically, so you probably won't have to set this. 

Attributes of this class will be collected in the `BUILD_CONFIG` step.

See also [BUILD_CONFIG](ReportCOntent#build_config)

Equivalent `ConfigurationBuilder.setBuildConfigClass`

## reportSenderFactoryClasses

All ReportSenders generated by the factories provided here will receive crash reports.

If not provided, defaults to `DefaultReportSenderFactory`, which either creates an `EmailIntentSender` if `mailTo` is provided, or a `HttpSender` if `formUri` is provided.

See also [ReportSenders](Report-Destinations)

Equivalent `ConfigurationBuilder.setReportSenderFactoryClasses`

## applicationLogFile

To use in combination with [APPLICATION_LOG](ReportContent#application_log) to set the path/name of your application log file. If the string does not contain any path separator, the file is assumed as being in the default files directory.

See also [Custom Logs](AdvancedUsage#adding-your-own-log-file-extracts-to-reports)

## applicationLogFileLines

To use in combination with [APPLICATION_LOG](ReportContent#application_log) to set the number of latest lines of your application log file to be collected.

If not provided, defaults to 100.

See also [Custom Logs](AdvancedUsage#adding-your-own-log-file-extracts-to-reports)

## reportDialogClass

Custom Dialog class used when prompting the user for crash details.

If not provided, defaults to org.acra.dialog.CrashReportDialog



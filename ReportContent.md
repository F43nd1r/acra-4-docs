**Table of Contents**

- [ANDROID_VERSION](ReportContent#android_version)
- [APP_VERSION_CODE](ReportContent#app_version_code)
- [APP_VERSION_NAME](ReportContent#app_version_name)
- [APPLICATION_LOG](ReportContent#application_log)
- [AVAILABLE_MEM_SIZE](ReportContent#available_mem_size)
- [BRAND](ReportContent#brand)
- [BUILD](ReportContent#build)
- [BUILD_CONFIG](ReportCOntent#build_config)
- [CRASH_CONFIGURATION](ReportContent#crash_configuration)
- [CUSTOM_DATA](ReportContent#custom_data)
- [DEVICE_FEATURES](ReportContent#device_features)
- [DEVICE_ID](ReportContent#device_id)
- [DISPLAY](ReportContent#display)
- [DROPBOX](ReportContent#dropbox)
- [DUMPSYS_MEMINFO](ReportContent#dumpsys_meminfo)
- [ENVIRONMENT](ReportContent#environment)
- [EVENTSLOG](ReportContent#eventslog)
- [FILE_PATH](ReportContent#file_path)
- [INITIAL_CONFIGURATION](ReportContent#initial_configuration)
- [INSTALLATION_ID](ReportContent#installation_id)
- [IS_SILENT](ReportContent#is_silent)
- [LOGCAT](ReportContent#logcat)
- [MEDIA_CODEC_LIST](ReportContent#media_codec_list)
- [PACKAGE_NAME](ReportContent#package_name)
- [PHONE_MODEL](ReportContent#phone_model)
- [PRODUCT](ReportContent#product)
- [RADIOLOG](ReportContent#radiolog)
- [REPORT_ID](ReportContent#report_id)
- [SETTINGS_GLOBAL](ReportContent#settings_global)
- [SETTINGS_SECURE](ReportContent#settings_secure)
- [SETTINGS_SYSTEM](ReportContent#settings_system)
- [SHARED_PREFERENCES](ReportContent#shared_preferences)
- [STACK_TRACE](ReportContent#stack_trace)
- [THREAD_DETAILS](ReportContent#thread_details)
- [TOTAL_MEM_SIZE](ReportContent#total_mem_size)
- [USER_APP_START_DATE](ReportContent#user_app_start_date)
- [USER_COMMENT](ReportContent#user_comment)
- [USER_CRASH_DATE](ReportContent#user_crash_date)
- [USER_EMAIL](ReportContent#user_email)


## REPORT_ID
_**Since: 4.0 - Default: Yes**_

A unique identifier for this report. If you receive 2 reports with the same ID then ACRA sent the same report twice. Most of the time this happens on poor network conditions.

## APP_VERSION_CODE
_**Since: 1.0 - Default: Yes**_

Application version code. This is the incremental integer version code
used to differentiate versions on the android market.
  
See [`PackageInfo.versionCode`](http://developer.android.com/reference/android/content/pm/PackageInfo.html#versionCode).

## APP_VERSION_NAME
_**Since: 1.0 - Default: Yes**_
  
Application version name.
  
See [`PackageInfo.versionName`](http://developer.android.com/reference/android/content/pm/PackageInfo.html#versionName).
  
## PACKAGE_NAME
_**Since: 1.0 - Default: Yes**_

Application package name.
  
See [`Context.getPackageName()`](http://developer.android.com/reference/android/content/Context.html#getPackageName%28%29).




## FILE_PATH
_**Since: 1.0 - Default: Yes**_

  Base path of the application's private file folder.
  
  See  [`Context.getFilesDir()`](http://developer.android.com/reference/android/content/Context.html#getFilesDir%28%29)

## PHONE_MODEL
_**Since: 1.0 - Default: Yes**_

  Device model name.
  
  See [`Build.MODEL`](http://developer.android.com/reference/android/os/Build.html#MODEL).

## BRAND
_**Since: 1.0 - Default: Yes**_

  Device brand (manufacturer or carrier).
  
  See [`Build.BRAND`](http://developer.android.com/reference/android/os/Build.html#BRAND).

## PRODUCT
_**Since: 1.0 - Default: Yes**_

  Device overall product code.
  
  See [`Build.PRODUCT`](http://developer.android.com/reference/android/os/Build.html#PRODUCT).

## ANDROID_VERSION
_**Since: 1.0 - Default: Yes**_

  Device android version name. 
  
  See [`Build.VERSION.RELEASE`](http://developer.android.com/reference/android/os/Build.VERSION.html#RELEASE)

## BUILD
_**Since: 4.0 - Default: Yes**_

  Android build details. Here is an example for the NexusOne with official Android 2.3.3: 
  
```
BOARD=mahimahi
BOOTLOADER=0.35.0017
BRAND=google
CPU_ABI=armeabi-v7a
CPU_ABI2=armeabi
DEVICE=passion
DISPLAY=GRI40
FINGERPRINT=google/passion/passion:2.3.3/GRI40/102588:user/release-keys
HARDWARE=mahimahi
HOST=android-test-1.mtv.corp.google.com
ID=GRI40
MANUFACTURER=HTC
MODEL=Nexus One
PRODUCT=passion
RADIO=unknown
SERIAL=HT019P801851
TAGS=release-keys
TIME=1297306326000
TYPE=user
UNKNOWN=unknown
USER=android-build
```
  
  See [`Build`](http://developer.android.com/reference/android/os/Build.html).

## TOTAL_MEM_SIZE
_**Since: 1.0 - Default: Yes**_

  Estimation of the total device memory size based on filesystem stats.

## AVAILABLE_MEM_SIZE
_**Since: 1.0 - Default: Yes**_

  Estimation of the available device memory size based on filesystem stats.

## CUSTOM_DATA
_**Since: 1.0 - Default: Yes**_

  Contains key = value pairs defined by the application developer during
  the application execution.

## STACK_TRACE
_**Since: 1.0 - Default: Yes**_

  The Holy Stack Trace. Details of the exception that caused the application to crash.

## INITIAL_CONFIGURATION
_**Since: 3.0 - Default: Yes**_

  [`Configuration`](http://developer.android.com/intl/fr/reference/android/content/res/Configuration.html) fields state on the application start.
  
  Example:
  
```
locale=fr_FR
hardKeyboardHidden=HARDKEYBOARDHIDDEN_YES
keyboard=KEYBOARD_NOKEYS
keyboardHidden=KEYBOARDHIDDEN_NO
fontScale=1.0
mcc=208
mnc=10
navigation=NAVIGATION_TRACKBALL
navigationHidden=NAVIGATIONHIDDEN_NO
orientation=ORIENTATION_PORTRAIT
screenLayout=SCREENLAYOUT_SIZE_NORMAL+SCREENLAYOUT_LONG_YES
seq=117
touchscreen=TOUCHSCREEN_FINGER
uiMode=UI_MODE_TYPE_NORMAL+UI_MODE_NIGHT_NO
userSetLocale=false
```

## CRASH_CONFIGURATION
_**Since: 3.0 - Default: Yes**_

  [`Configuration`](http://developer.android.com/intl/fr/reference/android/content/res/Configuration.html) fields state on the application crash.

  Example :
  
```
locale=fr_FR
hardKeyboardHidden=HARDKEYBOARDHIDDEN_YES
keyboard=KEYBOARD_NOKEYS
keyboardHidden=KEYBOARDHIDDEN_NO
fontScale=1.0
mcc=208
mnc=10
navigation=NAVIGATION_TRACKBALL
navigationHidden=NAVIGATIONHIDDEN_NO
orientation=ORIENTATION_LANDSCAPE
screenLayout=SCREENLAYOUT_SIZE_NORMAL+SCREENLAYOUT_LONG_YES
seq=120
touchscreen=TOUCHSCREEN_FINGER
uiMode=UI_MODE_TYPE_NORMAL+UI_MODE_NIGHT_NO
userSetLocale=false
```

  As an example of how this field combined with [initial_configuration](ReportContent#INITIAL_CONFIGURATION) can help you debug your application,
  you can see here that the "seq" field has been increased from 117 to120.
  This means that 3 configuration changes occurred between the
  Application start and the crash. You can also see that the orientation
  changed from PORTRAIT to LANDSCAPE. There could be lots of issues
  regarding orientation (and other configuration) changes handling, so
  if you don't understand how a bug happens, having a look at this values
  can help you understand what the user did with his device.
  
  Though, having seq value increased does not mean that these changes
  occured while your application was active. There can be lots of things
  happening between your application start and the crash. For example, a
  user can start your application and use it on day 1 without any issue,
  use many other applications in between, reopen your application on day
  2 (which was still started but paused) and then the crash occurs.
  All the configuration changes that happened in between introduce a
  change in the seq value.  

## DISPLAY
_**Since: 3.0 - Default: Yes**_

  Device display specifications.
  
  See [`WindowManager.getDefaultDisplay()`](http://developer.android.com/reference/android/view/WindowManager.html#getDefaultDisplay%28%29)
  
  Example:

```
width=480
height=800
pixelFormat=1
refreshRate=60.0fps
metrics.density=x1.5
metrics.scaledDensity=x1.5
metrics.widthPixels=480
metrics.heightPixels=800
metrics.xdpi=254.0
metrics.ydpi=254.0
```

## USER_COMMENT
_**Since: 3.0 - Default: Yes**_

  Comment added by the user in the dialog displayed in NOTIFICATION mode.

## USER_APP_START_DATE
_**Since: 4.0 - Default: Yes**_

  User date on application start.

## USER_CRASH_DATE
_**Since: 3.0 - Default: Yes**_

  User date immediately after the crash occurred.

## DUMPSYS_MEMINFO
_**Since: 4.0 - Default: Yes (?)**_
_**Requires DUMP permission for device running Android 4.0 (ICS) and later.**_

  Memory state details for your application process.
  
Example (taken from android 2.3.3, content may vary with android versions):

```none
Applications Memory Usage (kB):
Uptime: 75158991 Realtime: 192859224

** MEMINFO in pid 18806 [org.acra.sampleapp] **
                    native   dalvik    other    total
            size:     4216     5447      N/A     9663
       allocated:     4208     2818      N/A     7026
            free:        7     2629      N/A     2636
           (Pss):      759      211     2118     3088
  (shared dirty):     2296     1860     5052     9208
    (priv dirty):      684       64     1436     2184
 
 Objects
           Views:        0        ViewRoots:        0
     AppContexts:        0       Activities:        0
          Assets:        2    AssetManagers:        2
   Local Binders:        7    Proxy Binders:       14
Death Recipients:        1
 OpenSSL Sockets:        0
 
 SQL
               heap:        0         MEMORY_USED:        0
 PAGECACHE_OVERFLOW:        0         MALLOC_SIZE:        0
 
 
 Asset Allocations
    zip:/data/app/org.acra.sampleapp-1.apk:/resources.arsc: 5K
```

Analysis of these data require a high knowledge of internal system
memory handling. You can get some clues in [this StackOverflow answer from Dianne Hackborn](http://stackoverflow.com/questions/2298208/how-to-discover-memory-usage-of-my-application-in-android/2299813#2299813).

## DROPBOX
_**Since: 4.0 - Default: No**_

_**Requires READ_LOGS permission.**_

  Content of the `android.os.DropBoxManager` (introduced in API level 8).

  
  The DropBoxManager is an alternative logging system which allows platform
  developers to persist data (text ot binary). There is small chance that
  these logging events are really useful for debugging your app... but you 
  can add your own tags to be retrieved by ACRA. So if you ever can find
  some usage for it (maybe related with StrictMode?) then ACRA is already
  ready to collect them.
  
  A few details were given about the usage of the DropBox by [Brad Fitzpatrick in this StackOverflow answer](http://stackoverflow.com/questions/4434192/dropboxmanager-use-cases/4445105#4445105).
    
  If [properly configured to retrieve system tags](AdvancedUsage#adding-dropboxmanager-events-to-your-reports), here is the kind of content you can retrieve after a fresh boot on a Nexus One (with android 2.3.3):

```none
Tag: system_app_anr
Nothing.
Tag: system_app_wtf
Nothing.
Tag: system_app_crash
Nothing.
Tag: system_server_anr
Nothing.
Tag: system_server_wtf
Nothing.
Tag: system_server_crash
Nothing.
Tag: BATTERY_DISCHARGE_INFO
Nothing.
Tag: SYSTEM_RECOVERY_LOG
Nothing.
Tag: SYSTEM_BOOT
@20110327T163719
Text: Build: google/passion/passion:2.3.3/GRI40/102588:user/release-keys
Hardware: mahimahi
Bootloader: 0.35.0017
Radio: unknown
Kernel: Linux version 2.6.35.7-59423-g08607d4 (android-build@apa28.mtv.corp.google.com) (gcc version 4.4.3 (GCC) ) #1 PREEMPT Tue Dec 28 09:34:38 PST 2010


Tag: SYSTEM_LAST_KMSG
@20110327T163720
Text: Build: google/passion/passion:2.3.3/GRI40/102588:user/release-keys
Hardware: mahimahi
Bootloader: 0.35.0017
Radio: unknown
Kernel: Linux version 2.6.35.7-59423-g08607d4 (android-build@apa28.mtv.corp.google.com) (gcc version 4.4.3 (GCC) ) #1 PREEMPT Tue Dec 28 09:34:38 PST 2010

[[TRUNCATED]]
nd
[75771.250976] wake lock alarm_rtc, expired
[75771.256195] suspend: enter suspend
[75771.256378] PM: Syncing filesystems ... done.
[75771.257965] Freezing user space processes ... (elapsed 0.02 seconds) d
Tag: APANIC_CONSOLE
Nothing.
Tag: APANIC_THREADS
Nothing.
Tag: SYSTEM_RESTART
Nothing.
Tag: SYSTEM_TOMBSTONE
Nothing.
Tag: data_app_strictmode
Nothing.
```

    

## LOGCAT
_**Since: 4.0 - Default: Yes**_

_**Requires READ_LOGS permission.**_

  Logcat default extract.
    
  The [`logcat`](http://developer.android.com/intl/fr/guide/developing/tools/logcat.html)
  is the Android Developer's best friend. This is where all applications
  and the system write their debug traces. Retrieving logcat events in
  your reports will allow you to retrieve your own debugging traces.
  
  See [configuration details](AdvancedUsage#adding-logcat-eventlog-or-radiolog-extracts-to-reports).

## EVENTSLOG
_**Since: 4.0 - Default: No**_

_**Requires READ_LOGS permission.**_

  Logcat eventslog extract.
    
  The eventslog is a lower level logging buffer. Its content looks like this:
  
```none
03-27 16:37:45.230 I/content_update_sample(  428): [content://gmail-downloads/download,delete,_id IN (),2328,,100]
03-27 16:37:45.550 I/dvm_gc_info(  203): [7017575181485061379,-9057997136484935626,-3939377503288981465,9365717]
03-27 16:37:45.560 I/am_create_task(  103): 4
03-27 16:37:45.560 I/am_create_activity(  103): [1083121280,4,org.acra.sampleapp/.CrashTestLauncher,android.intent.action.MAIN,NULL,NULL,270532608]
03-27 16:37:45.570 I/am_pause_activity(  103): [1079760528,org.adwfreak.launcher/.Launcher]
03-27 16:37:45.760 I/am_on_paused_called(  203): org.adwfreak.launcher.Launcher
03-27 16:37:45.770 I/am_proc_start(  103): [559,10059,org.acra.sampleapp,activity,org.acra.sampleapp/.CrashTestLauncher]
03-27 16:37:45.810 I/dvm_gc_madvise_info(  559): [1290240,1056768]
03-27 16:37:45.850 I/am_proc_bound(  103): [559,org.acra.sampleapp]
03-27 16:37:45.850 I/am_restart_activity(  103): [1083121280,4,org.acra.sampleapp/.CrashTestLauncher]
03-27 16:37:45.980 I/db_sample(  428): [/data/data/com.google.android.gm/databases/XX@YY,COMMIT;DELETE FROM attachments WHERE _id IN (),695,,100]
03-27 16:37:46.080 I/db_sample(  428): [/data/data/com.google.android.gm/databases/XX@YY,GETLOCK:SELECT * FROM custom_label_color_prefs,8122,,100]
03-27 16:37:46.150 I/binder_sample(  176): [android.view.IWindowSession,4,7,com.joko.lightgridpro,1]
03-27 16:37:46.410 I/db_sample(  428): [/data/data/com.google.android.gm/databases/XX@YY,SELECT * FROM custom_label_color_prefs,8453,,100]
03-27 16:37:46.410 I/db_sample(  428): [/data/data/com.google.android.gm/databases/downloads.db,SELECT _id FROM downloads WHERE (status >= '200') ORDER BY lastm,1134,,100]
03-27 16:37:46.410 I/content_query_sample(  428): [content://gmail-downloads/download,_id,status >= '200',lastmod,2036,,100]
03-27 16:37:46.450 I/db_sample(  428): [/data/data/com.google.android.gm/databases/XX@YY,BEGIN EXCLUSIVE;,42,,9]
03-27 16:37:46.570 I/notification_cancel(  103): [com.handcent.nextsms,321,0]
03-27 16:37:46.580 I/am_destroy_service(  103): [1084025168,com.handcent.nextsms/com.handcent.sms.transaction.SmsReceiverService,540]
03-27 16:37:46.590 I/am_kill (  103): [300,com.android.settings,14,too many background]
03-27 16:37:46.590 I/am_proc_died(  103): [300,com.android.settings]
03-27 16:37:46.600 I/db_sample(  428): [/data/data/com.google.android.gm/databases/XX@YY,COMMIT;SELECT _id FROM attachments WHERE downloadId == 0,102,,21]
03-27 16:37:46.620 I/gmail_perf_end(  428): [ME.constructor,132,11014,1]
03-27 16:37:46.630 I/content_query_sample(  411): [content://gmail-ls/labels/XX@YY,canonicalName/numUnreadConversations,,,17123,,100]
03-27 16:37:46.660 I/am_on_resume_called(  559): org.acra.sampleapp.CrashTestLauncher
03-27 16:37:46.720 I/activity_launch_time(  103): [1083121280,org.acra.sampleapp/.CrashTestLauncher,949,29542]
03-27 16:37:46.840 I/am_destroy_service(  103): [1083808248,com.google.android.gm/.downloadprovider.DownloadService,428]
03-27 16:37:46.900 I/db_sample(  428): [/data/data/com.google.android.gm/databases/XX@YY,BEGIN EXCLUSIVE;,268,,54]
03-27 16:37:46.970 I/am_create_service(  103): [1084806080,com.nitrodesk.droid20.nitroid/com.nitrodesk.daemon.ExchangeListenerSvc,,275]
03-27 16:37:46.990 I/am_proc_start(  103): [572,10049,com.levelup.beautifulwidgets,broadcast,com.levelup.beautifulwidgets/.HomeWidget14]
03-27 16:37:47.030 I/dvm_gc_madvise_info(  572): [1290240,1056768]
03-27 16:37:47.070 I/am_proc_bound(  103): [572,com.levelup.beautifulwidgets]
03-27 16:37:47.160 I/dvm_gc_info(  103): [8320808730291807962,-8924856104238569357,-3969495325797021657,8620078]
03-27 16:37:47.180 I/db_sample(  428): [/data/data/com.google.android.gm/databases/XX@YY,SELECT IFNULL((SELECT _id FROM conversations WHERE syncRationale,266,,54]
03-27 16:37:47.290 I/db_sample(  275): [/data/data/com.nitrodesk.droid20.nitroid/databases/windroid.db,BEGIN EXCLUSIVE;,149,com.nitrodesk.droid20.nitroid,30]
03-27 16:37:47.300 I/am_kill (  103): [308,com.google.android.partnersetup,14,too many background]
03-27 16:37:47.300 I/am_proc_died(  103): [308,com.google.android.partnersetup]
03-27 16:37:47.550 I/dvm_gc_info(  559): [8314046716718409527,-8925986472288581587,-4000739048211904473,8525718]
03-27 16:37:47.650 I/dvm_gc_info(  559): [8314046716718413429,-8925704997311875024,-3999894623281772505,8525718]
03-27 16:37:47.720 I/db_sample(  275): [/data/data/com.nitrodesk.droid20.nitroid/databases/windroid.db,COMMIT;SELECT _id, AccountID, DeviceID, ServerName, UserID, Doma,111,com.nitrodesk.droid20.nitroid,23]
03-27 16:37:47.980 I/db_sample(  275): [/data/data/com.nitrodesk.droid20.nitroid/databases/windroid.db,BEGIN EXCLUSIVE;,249,com.nitrodesk.droid20.nitroid,50]
03-27 16:37:48.100 I/dvm_gc_info(  559): [8314046716718417551,-9042798587623495631,-3999331673328351193,8525718]
```

## RADIOLOG
_**Since: 4.0 - Default: No**_

_**Requires READ_LOGS permission.**_

  Logcat radio extract.
    
  The third buffer managed by logcat contains radio events. It looks like this:

```
03-27 16:37:28.960 D/GSM     (  195): [DSAC DEB] trySetupData with mIsPsRestricted=false
03-27 16:37:28.960 I/GSM     (  195): Preferred APN:20810:20810:SFR, 8, 20810, sl2sfr, , null, , , , -1, default, supl
03-27 16:37:28.960 I/GSM     (  195): Waiting APN set to preferred APN
03-27 16:37:28.960 D/GSM     (  195): [GsmDataConnectionTracker] Create from allApns : [SFR, 8, 20810, sl2sfr, , null, , , , -1, default, supl][SFR-MMS, 9, 20810, mmssfr, , http://mms1, 10.151.0.1, 8080, , -1, mms]
03-27 16:37:28.960 D/GSM     (  195): [GsmDataConnection-1] DcInactiveState msg.what=EVENT_CONNECT
03-27 16:37:28.960 D/GSM     (  195): [GsmDataConnection-1] Connecting to carrier: 'SFR' APN: 'sl2sfr' proxy: '' port: '
03-27 16:37:28.960 D/RILJ    (  195): [0094]> SETUP_DATA_CALL 1 0 sl2sfr   3
03-27 16:37:29.020 D/RILJ    (  195): [0095]> REQUEST_GET_NEIGHBORING_CELL_IDS
03-27 16:37:29.260 D/RILJ    (  195): [0095]< REQUEST_GET_NEIGHBORING_CELL_IDS  
03-27 16:37:32.760 D/RILJ    (  195): [UNSL]< UNSOL_DATA_CALL_LIST_CHANGED [DataCallState: { cid: 1, active: 2, type: IP, apn: sl2sfr, address: 10.114.107.85 }, DataCallState: { cid: -1, active: 0, type: , apn: , address:  }, DataCallState: { cid: -1, active: 0, type: , apn: , address:  }]
03-27 16:37:32.770 D/RILJ    (  195): [0094]< SETUP_DATA_CALL {1, rmnet0, 10.114.107.XX}
03-27 16:37:32.770 D/GSM     (  195): [GsmDataConnection-1] DcActivatingState msg.what=EVENT_SETUP_DATA_CONNECTION_DONE
03-27 16:37:32.770 D/GSM     (  195): [GsmDataConnection-1] interface=rmnet0 ipAddress=10.114.107.XX gateway=10.114.107.86 DNS1=172.20.2.39 DNS2=172.20.2.10
03-27 16:37:32.770 D/GSM     (  195): [GsmDataConnection-1] DataConnection setup result='SUCCESS' on cid=1
03-27 16:37:32.770 D/GSM     (  195): [GsmDataConnection-1] DcInactiveState: setEnterNoticationParams cp,cause
03-27 16:37:32.770 D/GSM     (  195): [GsmDataConnection-1] DcActiveState: enter notifyConnectCompleted
03-27 16:37:32.770 D/GSM     (  195): [GsmDataConnection-1] notifyConnection at 1301236652781 cause=No Error
03-27 16:37:32.790 D/GSM     (  195): [DataConnection] Start poll NetStat
03-27 16:37:33.730 D/RILJ    (  195): [UNSL]< UNSOL_RESPONSE_NETWORK_STATE_CHANGED
03-27 16:37:33.730 D/RILJ    (  195): [0096]> OPERATOR
03-27 16:37:33.730 D/RILJ    (  195): [0097]> GPRS_REGISTRATION_STATE
03-27 16:37:33.730 D/RILJ    (  195): [0098]> REGISTRATION_STATE
03-27 16:37:33.730 D/RILJ    (  195): [0099]> QUERY_NETWORK_SELECTION_MODE
03-27 16:37:33.740 D/RILJ    (  195): [0096]< OPERATOR {F SFR, (N/A), 20810}
03-27 16:37:33.760 D/RILJ    (  195): [0097]< GPRS_REGISTRATION_STATE {1, null, null, 9}
03-27 16:37:33.780 D/RILJ    (  195): [0098]< REGISTRATION_STATE {1, 4654, 0084EC08, 9, null, null, null, null, null, null, null, null, null, null, A5}
03-27 16:37:33.790 D/RILJ    (  195): [0099]< QUERY_NETWORK_SELECTION_MODE {0}
03-27 16:37:33.790 D/GSM     (  195): Poll ServiceState done:  oldSS=[0 home F SFR (N/A) 20810  UMTS CSS not supported -1 -1RoamInd: -1DefRoamInd: -1EmergOnly: false] newSS=[0 home F SFR (N/A) 20810  HSDPA CSS not supported -1 -1RoamInd: -1DefRoamInd: -1EmergOnly: false] oldGprs=0 newGprs=0 oldType=UMTS newType=HSDPA
03-27 16:37:33.790 D/GSM     (  195): RAT switched UMTS -> HSDPA at cell 8711176
03-27 16:37:41.270 D/RILJ    (  195): [UNSL]< UNSOL_RESPONSE_NETWORK_STATE_CHANGED
03-27 16:37:41.270 D/RILJ    (  195): [0100]> OPERATOR
03-27 16:37:41.270 D/RILJ    (  195): [0101]> GPRS_REGISTRATION_STATE
03-27 16:37:41.270 D/RILJ    (  195): [0102]> REGISTRATION_STATE
03-27 16:37:41.270 D/RILJ    (  195): [0103]> QUERY_NETWORK_SELECTION_MODE
03-27 16:37:41.290 D/RILJ    (  195): [0100]< OPERATOR {F SFR, (N/A), 20810}
03-27 16:37:41.310 D/RILJ    (  195): [0101]< GPRS_REGISTRATION_STATE {1, null, null, 3}
03-27 16:37:41.340 D/RILJ    (  195): [0102]< REGISTRATION_STATE {1, 4654, 0084EC08, 3, null, null, null, null, null, null, null, null, null, null, A5}
03-27 16:37:41.350 D/RILJ    (  195): [0103]< QUERY_NETWORK_SELECTION_MODE {0}
03-27 16:37:41.350 D/GSM     (  195): Poll ServiceState done:  oldSS=[0 home F SFR (N/A) 20810  HSDPA CSS not supported -1 -1RoamInd: -1DefRoamInd: -1EmergOnly: false] newSS=[0 home F SFR (N/A) 20810  UMTS CSS not supported -1 -1RoamInd: -1DefRoamInd: -1EmergOnly: false] oldGprs=0 newGprs=0 oldType=HSDPA newType=UMTS
03-27 16:37:41.350 D/GSM     (  195): RAT switched HSDPA -> UMTS at cell 8711176
03-27 16:37:44.140 D/RILJ    (  195): [0104]> SIGNAL_STRENGTH
03-27 16:37:44.150 D/RILJ    (  195): [0104]< SIGNAL_STRENGTH {4, 99, -1, -1, -1, -1, 0}
```

## IS_SILENT
_**Since: 4.0 - Default: Yes**_

True if the report has been explicitly sent silently by the developer.

## DEVICE_ID
_**Since: 4.0 - Default: No**_

_**Requires READ_PHONE_STATE permission.**_

  Device unique ID (IMEI for GSM and the MEID or ESN for CDMA phones).
  
  If you need to know if reports come from single or multiple users without using the READ_PHONE_STATE permission, you should use [#INSTALLATION_ID] instead.
  
  See [`TelephonyManager.getDeviceId()`](http://developer.android.com/reference/android/telephony/TelephonyManager.html#getDeviceId%28%29)

## INSTALLATION_ID
_**Since: 4.0 - Default: Yes**_

  Installation unique ID. This identifier allow you to track a specific
  user application installation without using any personal data.
  Implemented following the guidelines from the [Android Developers Blog](http://android-developers.blogspot.com/2011/03/identifying-app-installations.html).

## USER_EMAIL
_**Since: 4.0 - Default: Yes**_

  User email address. Can be provided by the user in the `acra.user.email` SharedPreference field.

## DEVICE_FEATURES
_**Since: 4.0 - Default: Yes**_

  Features declared as available on this device by the system.
  These features are those that are used by the android market
  to filter apps according to `<uses-feature>` directives from applications manifests.
  
  Example from a NexusOne:

```
android.hardware.location.network
android.hardware.wifi
com.google.android.feature.GOOGLE_BUILD
android.hardware.telephony
android.hardware.location
android.software.sip
android.hardware.touchscreen.multitouch
android.hardware.sensor.compass
android.hardware.camera
android.hardware.bluetooth
android.hardware.sensor.proximity
android.software.sip.voip
android.hardware.microphone
android.hardware.sensor.light
android.hardware.location.gps
android.hardware.camera.autofocus
android.hardware.telephony.gsm
android.hardware.sensor.accelerometer
android.hardware.touchscreen
android.software.live_wallpaper
android.hardware.camera.flash
glEsVersion = 2.0
```

## ENVIRONMENT
_**Since: 4.0 - Default: Yes**_

  External storage state and standard directories.

  Example from a NexusOne:
  
```
getDataDirectory=/data
getDownloadCacheDirectory=/cache
getExternalStorageAndroidDataDir=/mnt/sdcard/Android/data
getExternalStorageDirectory=/mnt/sdcard
getExternalStorageState=mounted
getRootDirectory=/system
getSecureDataDirectory=/data
getSystemSecureDirectory=/data/system
isEncryptedFilesystemEnabled=false
isExternalStorageRemovable=true
```

## SHARED_PREFERENCES
_**Since: 4.2 - Default: Yes**_

  Collects your application's SharedPreferences. By default it will just collect the values in the ["default" SharedPreferences file](http://developer.android.com/reference/android/preference/PreferenceManager.html#getDefaultSharedPreferences(android.content.Context)).

  If your app contains multiple SharedPreference files, or if you are using a non-default name, you can add them by providing their names with `@ReportsCrashes(additionalSharedPreferences={"my_own_prefs","a_second_prefs"})`.

  "empty" often means that the user did not change anything so all values are default.
  

## SETTINGS_SYSTEM
_**Since: 4.0 - Default: Yes (No, since 4.7.0-RC2)**_

  System settings.
  
  Example from Nexus One:
  
```
ACCELEROMETER_ROTATION=1
AIRPLANE_MODE_ON=0
AIRPLANE_MODE_RADIOS=cell,bluetooth,wifi
AIRPLANE_MODE_TOGGLEABLE_RADIOS=bluetooth,wifi
ALARM_ALERT=content://media/internal/audio/media/81
AUTO_TIME=0
CALL_AUTO_RETRY=0
CAR_DOCK_SOUND=/system/media/audio/ui/Dock.ogg
CAR_UNDOCK_SOUND=/system/media/audio/ui/Undock.ogg
DESK_DOCK_SOUND=/system/media/audio/ui/Dock.ogg
DESK_UNDOCK_SOUND=/system/media/audio/ui/Undock.ogg
DIM_SCREEN=1
DOCK_SOUNDS_ENABLED=0
DTMF_TONE_TYPE_WHEN_DIALING=0
EMERGENCY_TONE=0
FONT_SCALE=1.0
HAPTIC_FEEDBACK_ENABLED=1
HEARING_AID=0
LOCKSCREEN_SOUNDS_ENABLED=0
LOCK_SOUND=/system/media/audio/ui/Lock.ogg
LOW_BATTERY_SOUND=/system/media/audio/ui/LowBattery.ogg
MODE_RINGER=2
MODE_RINGER_STREAMS_AFFECTED=166
MUTE_STREAMS_AFFECTED=46
NEXT_ALARM_FORMATTED=sam. 6:45
NOTIFICATIONS_USE_RING_VOLUME=1
NOTIFICATION_LIGHT_PULSE=1
NOTIFICATION_SOUND=content://media/external/audio/media/85
POWER_SOUNDS_ENABLED=1
RINGTONE=content://media/internal/audio/media/11
SCREEN_BRIGHTNESS=76
SCREEN_BRIGHTNESS_MODE=1
SCREEN_OFF_TIMEOUT=60000
SHOW_WEB_SUGGESTIONS=1
STAY_ON_WHILE_PLUGGED_IN=0
TRANSITION_ANIMATION_SCALE=1.0
TTY_MODE=0
UNLOCK_SOUND=/system/media/audio/ui/Unlock.ogg
VIBRATE_IN_SILENT=1
VIBRATE_ON=5
VOLUME_ALARM=5
VOLUME_BLUETOOTH_SCO=9
VOLUME_MUSIC=15
VOLUME_NOTIFICATION=5
VOLUME_RING=6
VOLUME_SYSTEM=7
VOLUME_VOICE=4
WIFI_SLEEP_POLICY=2
WIFI_USE_STATIC_IP=0
WINDOW_ANIMATION_SCALE=1.0
```

## SETTINGS_SECURE
_**Since: 4.0 - Default: Yes (No, since 4.7.0-RC2)**_

  Secure settings, applications can't modify them, only the user.
  
  Example from Nexus One:
  
```
ADB_ENABLED=1
ALLOWED_GEOLOCATION_ORIGINS=http://www.google.co.uk http://www.google.com
ALLOW_MOCK_LOCATION=0
ANDROID_ID=200142d4dfd4e641
ASSISTED_GPS_ENABLED=1
BACKGROUND_DATA=1
BACKUP_ENABLED=1
BACKUP_PROVISIONED=1
BACKUP_TRANSPORT=com.google.android.backup/.BackupTransportService
BLUETOOTH_ON=1
CDMA_CELL_BROADCAST_SMS=1
DATA_ROAMING=0
DEFAULT_INPUT_METHOD=com.touchtype.swiftkey/.KeyboardService
DEVICE_PROVISIONED=1
DISABLED_SYSTEM_INPUT_METHODS=
ENABLED_ACCESSIBILITY_SERVICES=
ENABLED_INPUT_METHODS=com.google.android.inputmethod.latin/com.android.inputmethod.latin.LatinIME:com.touchtype.swiftkey/.KeyboardService
INSTALL_NON_MARKET_APPS=1
LAST_SETUP_SHOWN=eclair_1
LOCATION_PROVIDERS_ALLOWED=network,gps
MOBILE_DATA=1
MOUNT_PLAY_NOTIFICATION_SND=1
MOUNT_UMS_AUTOSTART=0
MOUNT_UMS_NOTIFY_ENABLED=1
MOUNT_UMS_PROMPT=1
NETWORK_PREFERENCE=1
PREFERRED_CDMA_SUBSCRIPTION=1
PREFERRED_NETWORK_MODE=0
SEND_ACTION_APP_ERROR=1
THROTTLE_RESET_DAY=14
TTS_DEFAULT_COUNTRY=FRA
TTS_DEFAULT_LANG=fra
TTS_DEFAULT_RATE=100
TTS_DEFAULT_SYNTH=com.svox.pico
TTS_DEFAULT_VARIANT=
TTS_ENABLED_PLUGINS=
TTS_USE_DEFAULTS=0
USB_MASS_STORAGE_ENABLED=1
VOICE_RECOGNITION_SERVICE=com.google.android.voicesearch/.GoogleRecognitionService
WIFI_NETWORKS_AVAILABLE_NOTIFICATION_ON=1
WIFI_ON=0
WIFI_SAVED_STATE=0
WIFI_WATCHDOG_WATCH_LIST=GoogleGuest
```

## SETTINGS_GLOBAL
_**Since: 4.5 - Default: Yes (No, since 4.7.0-RC2)**_

  Global settings, introduced in Android 4.2.

  Example from 4.2 emulator:

```
AIRPLANE_MODE_ON=0
AIRPLANE_MODE_RADIOS=cell,bluetooth,wifi,nfc,wimax
AIRPLANE_MODE_TOGGLEABLE_RADIOS=bluetooth,wifi,nfc
ASSISTED_GPS_ENABLED=1
AUDIO_SAFE_VOLUME_STATE=1
AUTO_TIME=1
AUTO_TIME_ZONE=1
BLUETOOTH_ON=0
CALL_AUTO_RETRY=0
CAR_DOCK_SOUND=/system/media/audio/ui/Dock.ogg
CAR_UNDOCK_SOUND=/system/media/audio/ui/Undock.ogg
CDMA_CELL_BROADCAST_SMS=1
DATA_ROAMING=0
DEFAULT_INSTALL_LOCATION=0
DESK_DOCK_SOUND=/system/media/audio/ui/Dock.ogg
DESK_UNDOCK_SOUND=/system/media/audio/ui/Undock.ogg
DEVICE_PROVISIONED=1
DOCK_SOUNDS_ENABLED=0
EMERGENCY_TONE=0
INSTALL_NON_MARKET_APPS=1
LOCK_SOUND=/system/media/audio/ui/Lock.ogg
LOW_BATTERY_SOUND=/system/media/audio/ui/LowBattery.ogg
MOBILE_DATA=1
MODE_RINGER=2
NETSTATS_ENABLED=1
NETWORK_PREFERENCE=1
PACKAGE_VERIFIER_ENABLE=1
POWER_SOUNDS_ENABLED=1
PREFERRED_NETWORK_MODE=0
SET_INSTALL_LOCATION=0
STAY_ON_WHILE_PLUGGED_IN=1
THROTTLE_RESET_DAY=22
UNLOCK_SOUND=/system/media/audio/ui/Unlock.ogg
USB_MASS_STORAGE_ENABLED=1
WIFI_COUNTRY_CODE=us
WIFI_DISPLAY_ON=0
WIFI_MAX_DHCP_RETRY_COUNT=9
WIFI_NETWORKS_AVAILABLE_NOTIFICATION_ON=1
WIFI_ON=0
WIFI_SLEEP_POLICY=2
WIFI_WATCHDOG_ON=1
WIRELESS_CHARGING_STARTED_SOUND=/system/media/audio/ui/WirelessChargingStarted.ogg
```


## APPLICATION_LOG
_**Since: 4.3 - Default: No**_

  Content of your own application log file. To be configured with
  `@ReportsCrashes(applicationLogFile = "applog.log")` to define the path/name of
  the log file and `@ReportsCrashes.applicationLogFileLines(150)` to set
  the number of latest lines you want to be retrieved (default is 100).
  
## MEDIA_CODEC_LIST
_**Since: 4.3 - Default: No**_
  
  Since Android API Level 16 (Android 4.1 - Jelly Beans), retrieve the list of supported Media codecs and their capabilities (color format, profile and level).

Sample collected from Android 4.1 emulator:

```
0: OMX.google.mp3.decoder
isEncoder: false
Supported types: [audio/mpeg]
1: OMX.google.amrnb.decoder
isEncoder: false
Supported types: [audio/3gpp]
2: OMX.google.amrwb.decoder
isEncoder: false
Supported types: [audio/amr-wb]
3: OMX.google.aac.decoder
isEncoder: false
Supported types: [audio/mp4a-latm]
4: OMX.google.g711.alaw.decoder
isEncoder: false
Supported types: [audio/g711-alaw]
5: OMX.google.g711.mlaw.decoder
isEncoder: false
Supported types: [audio/g711-mlaw]
6: OMX.google.vorbis.decoder
isEncoder: false
Supported types: [audio/vorbis]
7: OMX.google.mpeg4.decoder
isEncoder: false
Supported types: [video/mp4v-es]
video/mp4v-es color formats:COLOR_FormatYUV420Planar
video/mp4v-es profile levels:MPEG4ProfileSimple-MPEG4Level0,MPEG4ProfileSimple-MPEG4Level0b,MPEG4ProfileSimple-MPEG4Level1,MPEG4ProfileSimple-MPEG4Level2,MPEG4ProfileSimple-MPEG4Level3
8: OMX.google.h263.decoder
isEncoder: false
Supported types: [video/3gpp]
video/3gpp color formats:COLOR_FormatYUV420Planar
video/3gpp profile levels:H263ProfileBaseline-H263Level10,H263ProfileBaseline-H263Level20,H263ProfileBaseline-H263Level30,H263ProfileBaseline-H263Level45,H263ProfileISWV2-H263Level10,H263ProfileISWV2-H263Level20,H263ProfileISWV2-H263Level30,H263ProfileISWV2-H263Level45
9: OMX.google.h264.decoder
isEncoder: false
Supported types: [video/avc]
video/avc color formats:COLOR_FormatYUV420Planar
video/avc profile levels:1AVCProfileBaseline-AVCLevel1,1AVCProfileBaseline-AVCLevel1b,1AVCProfileBaseline-AVCLevel11,1AVCProfileBaseline-AVCLevel12,1AVCProfileBaseline-AVCLevel13,1AVCProfileBaseline-AVCLevel2,1AVCProfileBaseline-AVCLevel21,1AVCProfileBaseline-AVCLevel22,1AVCProfileBaseline-AVCLevel3,1AVCProfileBaseline-AVCLevel31,1AVCProfileBaseline-AVCLevel32,1AVCProfileBaseline-AVCLevel4,1AVCProfileBaseline-AVCLevel41,1AVCProfileBaseline-AVCLevel42,1AVCProfileBaseline-AVCLevel5,1AVCProfileBaseline-AVCLevel51
10: OMX.google.vpx.decoder
isEncoder: false
Supported types: [video/x-vnd.on2.vp8]
video/x-vnd.on2.vp8 color formats:COLOR_FormatYUV420Planar
11: OMX.google.aac.encoder
isEncoder: true
Supported types: [audio/mp4a-latm]
12: OMX.google.amrnb.encoder
isEncoder: true
Supported types: [audio/3gpp]
13: OMX.google.amrwb.encoder
isEncoder: true
Supported types: [audio/amr-wb]
14: OMX.google.h263.encoder
isEncoder: true
Supported types: [video/3gpp]
video/3gpp color formats:COLOR_FormatYUV420Planar,COLOR_FormatYUV420SemiPlanar
video/3gpp profile levels:H263ProfileBaseline-H263Level45
15: OMX.google.h264.encoder
isEncoder: true
Supported types: [video/avc]
video/avc color formats:COLOR_FormatYUV420Planar,COLOR_FormatYUV420SemiPlanar
video/avc profile levels:1AVCProfileBaseline-AVCLevel1,1AVCProfileBaseline-AVCLevel1b,1AVCProfileBaseline-AVCLevel11,1AVCProfileBaseline-AVCLevel12,1AVCProfileBaseline-AVCLevel13,1AVCProfileBaseline-AVCLevel2
16: OMX.google.mpeg4.encoder
isEncoder: true
Supported types: [video/mp4v-es]
video/mp4v-es color formats:COLOR_FormatYUV420Planar,COLOR_FormatYUV420SemiPlanar
video/mp4v-es profile levels:MPEG4ProfileCore-MPEG4Level2
17: OMX.google.flac.encoder
isEncoder: true
Supported types: [audio/flac]
18: AACEncoder
isEncoder: true
Supported types: [audio/mp4a-latm]
19: OMX.google.raw.decoder
isEncoder: false
Supported types: [audio/raw]
```

## THREAD_DETAILS
_**Since: 4.3 - Default: No**_
  
  Retrieves details of the failing thread (id, name, group name).

Here's what is provided when the main thread crashes:
  
```
id=1
name=main
priority=5
groupName=main
```

And here is when a secondary thread which has been given a name (DoSomeBackgroundStuff) crashes:

```
id=91
name=DoSomeBackgroundStuff
priority=5
groupName=main
```

## BUILD_CONFIG
_**Since: 5.0 - Default: Yes**_

All constants defined on the BuildConfig class as a list of constant name=value pairs. This will at a minimum contain a boolean DEBUG constant that states whether this is a debug or release build. The Gradle Android Plugin populates several other constants and provides a way to add custom constants during the build.

Here is an example:

```
BUILD_TYPE=debug
DEBUG=true
FLAVOR=
PACKAGE_NAME=com.android.sample
VERSION_CODE=10
VERSION_NAME=5.0
CUSTOM_FIELD=custom value
```
With the corresponding Gradle script fragment to set the value for CUSTOM_FIELD:

```
android {
    defaultConfig {
        buildConfigField 'String', 'CUSTOM_FIELD, '\"custom value\"'
    }
```
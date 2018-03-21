Welcome to the acra wiki!

**If you found a bug in ACRA, please file an issue in the [Issues Tracker](https://github.com/ACRA/acra/issues). You can also post your questions or suggestions to the [Discussion Group](http://groups.google.com/group/acra-discuss).**

**Please Note** : As of ACRA-4.8.0, ACRA uses the `SenderService` to send crash reports. The `SenderService` runs in a **separate process** to ensure that reports can be sent even when your own VM is dying from an unhandled exception. This means that a new instance of your application will be started and your `Application.onCreate()` will be called again. If you are performing once only tasks in `Application.onCreate()` then check the name of the current process and don't do them if the process name is `:acra`. You can use `ACRA.isSenderService()` for this.
As of ACRA-4.9.0 `ACRA.isSenderService()` is not available, use `ACRA.isACRASenderServiceProcess()` instead.

* [Overview](wiki/Overview)
* [Setup instructions](wiki/BasicSetup)
* [Advanced Usage](wiki/AdvancedUsage)
* [Reports fields description](wiki/ReportContent)
* [Backends](wiki/Backends)
* [ProGuard configuration](wiki/ProGuard)
* [Change log](wiki/ChangeLog)

* [Notice on using Google Docs Spreadsheets to store reports](wiki/Notice-on-Google-Form-Spreadsheet-usage)

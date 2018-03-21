ACRA allows your Android application to send Crash Reports to various destinations:

  * your own server-side HTTP POST script
  * [various existing backends](Backends)
  * any other possible destination by implementing your own report sender
  * an email

When a crash occurs, you can choose and configure 4 different ways of interacting with the user:

  * Silent (default): ACRA actions are not visible. The crash report is sent and then the default android crash system does its job (Force Close dialog)
  * Toast: When the crash occurs, ACRA displays a [toast](http://developer.android.com/intl/fr/guide/topics/ui/notifiers/toasts.html) and simultaneously sends the report.
  * Notification: An optional toast is displayed on application crash, but the report is not sent immediately. A status bar notification is published warning the user that he should send a report. When selected, the notification displays a dialog asking for the authorization to send the report, with an optional user comment.
  * Dialog: allows display of a crash dialog without the need of a status bar notification. 

This tutorial will guide you through installing ACRA in your application project.

If you have any question or comment regarding ACRA, post a message on the [Discussion Group](http://groups.google.com/group/acra-discuss).

## Is that all?

First of all, you should read [Reports content](AdvancedUsage#reports-content) for an explanation of the data collected
by ACRA.

ACRA is designed to work with the simplest possible setup. But there are lots of configurable items, all described in
the [Advanced Usage Guide](AdvancedUsage). Among them:

  * **[User interaction mode](AdvancedUsage#user-interaction)**:
    * **SILENT (default)**: with the basic setup, ACRA sends reports silently, without warning your users, and lets the system display the native Force Close dialog (which may include Android Market Send Report button on android 2.1+ devices... if your app has been downloaded from the market).
    * **[TOAST](AdvancedUsage#toast-notification)**: displays a [Toast](http://developer.android.com/intl/fr/reference/android/widget/Toast.html) with the text of your choice when the app crashes but doesn't allow your user to prevent reports from being sent (but you can setup a SharedPreference item).
    * **[NOTIFICATION](AdvancedUsage#status-bar-notification )**: displays a Toast when the app crashes, then a notification in the status bar asking your user to send a report. When the notification is selected, a Dialog asks for authorization + optional user comment.
    * **[DIALOG](AdvancedUsage#dialog )**: displays a Toast when the app crashes, then displays a Dialog on application restart asking for authorization + optional user comment.

  * **[Reports destination](AdvancedUsage#reports-destination)**:
    * **[Custom server script](AdvancedUsage#sending-reports_to_your_own_self-hosted_script)**: if you want to have better control over the reports, you can implement your own server-side script to handle reports and host it somewhere else. Then you can configure ACRA to send reports to this script.
    * **[E-mail](AdvancedUsage#sending-reports-by-email)**: if your application does not require internet permission and you don't want to add it only for crash reporting, you can configure ACRA to send reports by e-mail. This means that when a crash occurs, the user has to choose the e-mail app he prefers before reviewing the crash report and sending it.
    * **[Any destination you can imagine](AdvancedUsage#implementing-your-own-sender)**: there is a simple Interface you can implement to provide your own report sender to ACRA. ACRA gives your class the report data, you do whatever you want with it.

  * **[Reports content](AdvancedUsage#reports-content)**: ACRA provides extensive device information and state data in default reports. In addition, you can:
    * [Add custom variable states or traces](AdvancedUsage#adding-your-own-variables-content-or-traces-in-crash-reports)
    * [Add logcat, eventlog or radiolog extracts](AdvancedUsage#adding-logcat-eventlog-or-radiolog-extracts-to-reports)
    * [Add DropBoxManager events](AdvancedUsage#adding-dropboxmanager-events-to-your-reports)
    * [Add Device unique ID](AdvancedUsage#adding-the-device-unique-id-to-your-reports)
    * [Choosing which fields to be included in reports](AdvancedUsage#choosing-which-fields-to-be-included-in-reports)

  * **[User preferences](AdvancedUsage#letting-your-users-control-acra)**: you can add to your app preferences screen some items to let users control ACRA's behavior and reports content:
    * [Enable/disable sending reports](AdvancedUsage#enabledisable-acra)
    * [Enable/disable sending system logs](AdvancedUsage#enabledisable-system-logs)
    * [Enable/disable sending device unique id](AdvancedUsage#enabledisable-including-deviceid)
    * [Add an e-mail address to allow the developer to contact the user](AdvancedUsage#set-an-email-address-to-be-added-to-reports)
    * [Always accept sending reports](AdvancedUsage#enabledisable-auto-accept-reports) (for `NOTIFICATION` mode)

  * **[Dynamic Configuration](AdvancedUsage#dynamic-configuration)**
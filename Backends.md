## No more Google Forms

Using Google Forms as an ACRA backend has been a nice free solution when starting android development.
Though, Google asked us to stop using this solution and it won't be supported in future releases.

[You can read more details on this topic here.](Notice-on-Google-Form-Spreadsheet-usage)

Selecting your backend for collecting ACRA reports may be the most difficult task.
[Here is a review of various solutions](http://blog.antoche.com/2013/03/05/crash-reports-and-logs-aggregation-for-android/)
by [Antoine Bouthors](https://plus.google.com/118220830246810519317)

## Official backend

[Acralyzer](http://github.com/ACRA/acralyzer) is the new **open source** backend created by the author of ACRA.

Its main advantages:
* Can be hosted for free on [Cloudant](http://www.cloudant.com), [IrisCouch](http://www.iriscouch.com) or [Couchappy](https://www.couchappy.com)  (reasonable
  pricing plan based on your usage of both services, you'll most likely stay in the free zone)  
**Note:** if the backend is hosted on cloudant and facing **Host returned error code 400** issue while posting report. Refer to the solution in the following link. [Host returned error code 400](https://github.com/ACRA/acra/issues/376)
* Based on a full open source stack, it can also be hosted on **your own servers** with the only requirement of installing
  CouchDB. **Your data is yours**.
* Guarantees to display ALL possible data collected by ACRA.

## Alternative backends

Being an open source project, ACRA welcomes all initiatives to integrate its reports in any other backend/analysis tool.

Here is a list of solutions we are aware of.

### Commercial solutions

Their UI is often more polished than Acralyzer and they can provide some more handy features or integration with other
bug tracking / project management tools.

* [Sentry](https://getsentry.com/welcome/) also released an [ACRA Sender](https://github.com/dz0ny/acra)
* [Hockeyapp](http://support.hockeyapp.net/kb/client-integration-android/how-to-use-acra-with-hockeyapp) OSX, iOS and Android beta distribution platform and crash reports collection. There is a [more complete sender](https://gist.github.com/antoche/5123357) contributed by [Antoine Bouthors](https://plus.google.com/118220830246810519317)
* [Bugify](http://www.bugify.com) - commercial PHP bug and issue tracker [published an ACRA sender](https://gist.github.com/mateberlin/5540392)
* [LogEntries](http://www.vaudaux-ruth.com/android-log-collecting-with-acra-and-logentries), log management service you can eventually use to collect crash reports.
* [Tracepot](http://www.tracepot.com) - backend made directly for ACRA 

### Open source solutions

We did not test any of the following backends. Some are in early development stage. Support is provided by their respective developers.

#### Google AppEngine hosting:
* [acra-reporter](https://code.google.com/p/acra-reporter/) - java AppEngine backend by [Matthew Winters](https://plus.google.com/107003339094747431332).
* [sdimmick's android crash reports](https://github.com/sdimmick/android_crash_reports) - python AppEngine backend

#### PHP Hosting:
* [BrokenOpenApp](http://www.brokenopenapp.org/2015/05/24/first-post.html), a multi-project and user Symfony2 app with ProGuard support seeks testers
* The [Simplest PHP ACRA backend](https://gist.github.com/KevinGaudin/5560305) - 10 lines of code to just write each received report to a
  single file.
* [ACRAViz](https://github.com/vaibhavpandeyvpz/acraviz) Open-source, Silex/Doctrine powered backend for visualizing crash reports from ACRA library for Android.
* [Medialoha](http://www.medialoha.net/) are developing their own opensource backend[MAB-LAB](http://medialoha.net/index.php/fr/menu-mablab-fr). Source will be [available on GitHub](https://github.com/Medialoha/MAB-LAB) soon.
* [Marvinlabs](http://www.marvinlabs.com/) are developing their own opensource backend, [acra-server](https://github.com/marvinlabs/acra-server) [a demo server is available](http://acra-server-demo.marvinlabs.com/dashboard) to let you discover its features. 
* [CrashReportsViewer](https://github.com/BenoitDuffez/crashreportsviewer) opensource PHP backend by [Benoit Duffez](https://plus.google.com/108948613775343769413)
* [Crash Report Dashboard](https://github.com/thamilvanan/CrashReportDashboard) FORK open source PHP backend for ACRA, originally by [Arvid Gerstmann](https://plus.google.com/107977664598327468897).
* [X2ON's Android ACRA Server](https://github.com/x2on/android-acra-server) + [sender](https://github.com/x2on/android-acra-json-sender) by [Felix Schulze](https://www.felixschulze.de/) / [X2ON](http://www.x2on.de/)
* [ACRA Mailer](https://github.com/d-a-n/acra-mailer) forwards reports to an email address in a nicely formatted email. Allows to receive reports by mail without going through an intent (and user action to send the mail)
* [TBSFactory ACRA Server](https://github.com/tbsfivangarcia/TBSFACTORY-ACRA-SERVER)
* [ACRA PHP Mailer](https://github.com/fassor/acra-php-mailer) simple JSON report receiver which forwards the crash report to an email address
* [The simplest PHP SQL backend](https://github.com/GamersCave/The-Simplest-ACRA-PHP-SQL-Backend) a simple backend with SQL compability.
* [Android app with server component to view your errors](https://github.com/GamersCave/ACRA-Android-PHP-backend). A backend as an app, which retrieves error logs from a server component

#### Ruby Hosting:
* [Acracadabra](http://livefront.github.com/acracadabra/) forwards reports to an email address. Allows to receive reports by mail without going through an intent (and user action to send the mail)
* [Johnny Crash](https://github.com/avarteqgmbh/johnny_crash)

#### Python Hosting:
* [ACRA Web.py](https://github.com/chengbo/ACRA-webpy)
* [Django ACRA](https://github.com/Simpsonpt/django-acra) Ready To Go Helper! Django Model, View and Admin Panel for ACRA.

#### Node.js Hosting:
* [node acra reporter](https://github.com/halkeye/node-acra-reporter) provided by [Gavin Mogan](https://plus.google.com/107775609316541886610) who is also contributing to Acralyzer.
* [acra node server](https://github.com/warsclon/acra-node-server)

### JVM Hosting:
* [Vaadin-Spring-based Backend](https://github.com/F43nd1r/acra-backend)

#### Standalone:
* [acra-go](https://github.com/gen2brain/acra-go) Backend written in Go language, comes with dashboard, no external dependencies.
* [acra-collector](https://github.com/dbrgn/acra-collector) Backend written in Rust. Very simple, no dashboard. Logs the crash to a file and sends an e-mail.
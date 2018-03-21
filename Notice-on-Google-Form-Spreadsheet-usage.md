# Notice on using Google Form/Spreadsheet for reports storage

In its initial configuration, ACRA offers to send reports to a Google Docs (Drive) Form which stores reports data in a
Google Docs spreadsheet.

This was coming really handy when you start developing an app and can't afford spending time and/or money on hosting a
reports storage engine yourself. It is free and you could rely on Google's infrastructure.

**Unfortunately this usage of Google Forms has gone beyond the limits of what is acceptable for Google. They shared with
us their concern about it and kindly asked us to stop using Google Forms for automatic reporting storage.**

There are some limitations to the usage of Google Documents anyway, detailed here:
http://support.google.com/drive/bin/answer.py?hl=en&answer=37603

Spreadsheets are limited to 400,000 (four hundred thousands) cells, which lets you imagine receiving approximately
11,000 (eleven thousands) reports before reaching the limit.

Even if this looks like a huge number of reports, you should know that:
* the **UI of the spreadsheet tends to become rather slow** when a large amount of data is contained in the spreadsheet
* **an overloaded spreadsheet can't be opened anymore**
* you won't receive any help from Google's teams to recover your spreadsheet's data

If your application is used by a large number of users, the delivery of a faulty update with a single bug experienced by
a large portion of them can quickly lead to an overloaded spreadsheet.

As a consequence, **using Google Drive Forms as the ACRA reporting endpoint will not be supported anymore with the next
releases**. You have to consider one of these solutions:
* implement and host your own reports storage engine. Even a simple script writing reports to a text file or in a
  database table can be enough. [Instructions are provided](AdvancedUsage#reports-destination)
  to let you configure ACRA to send its data the way you want to receive it.
  A possible solution can be as simple as this [minimalistic PHP script](https://gist.github.com/KevinGaudin/5560305):
```php
<?php
    // Outputs all POST parameters to a text file. The file name is the date_time of the report reception
    $fileName = date('Y-m-d_H-i-s').'.txt';
	$file = fopen($fileName,'w') or die('Could not create report file: ' . $fileName);
    foreach($_POST as $key => $value) {
      $reportLine = $key." = ".$value."\n";
	  fwrite($file, $reportLine) or die ('Could not write to report file ' . $reportLine);
    }
	fclose($file);
?>
```
* host an already existing open source reports storage engine. [Acralyzer](http://github.com/ACRA/acralyzer) is the new
  official ACRA backend, you can also read [[Backends]] for other possible solutions.
* subscribe to a plan on a third-party service like [Bugsense](http://www.bugsense.com/docs/android#acra), [Zubhium](https://www.zubhium.com/docs/crashreporting/) or [HockeyApp](http://support.hockeyapp.net/kb/client-integration-android/how-to-use-acra-with-hockeyapp) which provide instructions to let ACRA send them its reports. You'll get insightful analysis tools on top of a robust reports storage engine. Starter plans are usually free of charge.

We are aware that all these solutions have some inconvenience, requiring you to either develop and/or host a new
server-side component or to send your crash reports to a third-party service that may charge you or use your data to
sell global app quality stats.



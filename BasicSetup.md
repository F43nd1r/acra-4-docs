Step by step installation of the ACRA library in an existing application project, with the simplest settings:
  * Add the dependency on [`acra-4.X.Y.aar`](http://search.maven.org/#search%7Cga%7C1%7Cch.acra) to your application.
  * Configure your Application class either declaratively (recommended) or programmatically.
  * Update your AndroidManifest

# Add the dependency

ACRA is available on Maven central and can, as such, easily be integrated as a dependency of your project using the usual dependency management of your favorite build system.

**Maven**
```xml
<dependency> 
    <groupId>ch.acra</groupId> 
    <artifactId>acra</artifactId> 
    <version>4.9.2</version> 
    <type>aar</type> 
</dependency>
```

**Gradle**
```groovy
compile 'ch.acra:acra:4.9.2'
```

# Configure your Application class

If you don't already have an Application class, then create one. 
Apply the configuration to your Application class.

**Creating an Application class**
  * Create a new class in your package root.
  * Give it a name like: `MyApplication` extending from `android.app.Application` (or another subclass of that)
  * Update the `application` element in your AndroidManifest to reference the new class.

## Configuring ACRA - Declaratively

Add a `@ReportsCrashes` annotation to your Application class and then override the `attachBaseContext()` method to add `ACRA.init(this);`. In our newly created class, it looks like:

```java
    import org.acra.*;
    import org.acra.annotation.*;

    @ReportsCrashes(
        formUri = "http://www.backendofyourchoice.com/reportpath"
    )
    public class MyApplication extends Application {
        @Override
        protected void attachBaseContext(Context base) {
            super.attachBaseContext(base);

            // The following line triggers the initialization of ACRA
            ACRA.init(this);
        }
    }
```

## Configuring ACRA - Programmatically

You can also configure ACRA programmatically, or even partially declaratively and partially programmatically.


```java
    import org.acra.ACRA;
    import org.acra.configuration.*;

    public class MyApplication extends Application {
        @Override
        protected void attachBaseContext(Context base) {
            super.attachBaseContext(base);

            // Create an ConfigurationBuilder. It is prepopulated with values specified via annotation.
            // Set any additional value of the builder and then use it to construct an ACRAConfiguration.
            final ACRAConfiguration config = new ConfigurationBuilder(this)
                .setFoo(foo)
                .setBar(bar)
                .build();

            // Initialise ACRA
            ACRA.init(this, config);
        }
    }
```

---

**NB if you are starting services or other tasks in `Application.onCreate`, you should test to see if the current process is the `:acra` process. If it is then you probably don't want to start your service.**

In ACRA 4.9.0+ you can do that via `ACRA.isACRASenderServiceProcess(Application)`, in prior versions you will need to check the name of the process yourself.

# Update AndroidManifest

AndroidManifest needs to have the following modified
  * Application element needs to point to your Application class.
  * `Internet` permission needs to be declared if you are sending other than by email.

## Configuring the Application element

Edit `AndroidManifest.xml`, it will have an `application` element. You need to configure the `android:name` attribute to point to your Application class (put the full name with package if the application class package is not the same as manifest root element declared package):
```xml
<application android:icon="@drawable/icon" android:label="@string/app_name"
                android:name="MyApplication">
```

## Declaring the `internet` permission

If any of your senders require internet permission to deliver reports then add that to the manifest. NB if you have specified a target URL then you will be using the HttpSender and will **require** the internet permission.

```xml
<uses-permission android:name="android.permission.INTERNET"/>
```

> Please note that depending on the backend you selected, some additional parameters may be required. Please refer to
> the backend documentation.
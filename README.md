AndroidManifest.xml :
```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    package="com.andromojo.internetconnectivity">

    <uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.InternetConnectivity"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>

```

/res/drawable/try_again_button.xml :

```xml

<?xml version="1.0" encoding="utf-8"?>
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape android:shape="rectangle">
            <solid android:color="@color/purple_700" />
            <corners android:radius="50dp" />
        </shape>
    </item>
</selector>

```

/res/layout/activity_main.xml :

```xml

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Internet Connectivity"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>

```

/res/layout/connection_status.xml :

```xml

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:orientation="vertical"
    android:gravity="center"
    android:background="@color/purple_200"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ImageView
        android:layout_width="150dp"
        android:layout_height="150dp"
        android:src="@drawable/ic_baseline_signal_wifi_off_24"
        android:layout_gravity="center"
        app:tint="@color/purple_700"/>

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="OOPS!"
        android:textStyle="bold"
        android:textSize="40sp"
        android:gravity="center"
        android:textColor="@color/purple_700"/>

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textColor="@color/purple_700"
        android:textSize="25sp"
        android:text="No Internet Connection"
        android:gravity="center"/>

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textColor="@color/purple_700"
        android:textSize="18sp"
        android:text="Please Check Your Connection"
        android:gravity="center"/>

    <androidx.appcompat.widget.AppCompatButton
        android:id="@+id/btnTryAgain"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="50dp"
        android:textAllCaps="true"
        android:text="Try Again"
        android:textColor="@color/white"
        android:background="@drawable/try_again_button"/>

</LinearLayout>

```

# Ex_5_Send-SMS-Using-Intent

Develop program to create and design an android application to Send SMS using Intent in Android Studio.

## AIM:
To create and design an android application Send SMS using Intent in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details given in the MainActivity file.

Step 7: Save and run the application.


## Program:
 ```
/*
Program to create and design an android application for Sending  SMS using Intent.
Developed by: 212220230048
RegisterNumber:  Srinivasan S
*/
```

## MainActivity.java:
```java
package com.firstapp.ex05;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle; import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent; import android.net.Uri; import android.os.Bundle; import android.view.View; import android.widget.Button; public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    Button mbutton=(Button) findViewById(R.id.smsButton);
    mbutton.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View view) {
            Intent intent =new Intent(Intent.ACTION_VIEW, Uri.fromParts("sms","9840155373",null));
            intent.putExtra("sms_body","SMS using Intent");
            startActivity(intent);
        }
    });


}
}
```
## activity_main.xml:
```java
<Button
    android:id="@+id/smsButton"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:backgroundTint="@color/design_default_color_secondary"
    android:text="send sms"
    android:layout_centerHorizontal="true"
    android:layout_centerVertical="true"/>
```

## AndroidMainfest.xml
```java
<application
    android:allowBackup="true"
    android:dataExtractionRules="@xml/data_extraction_rules"
    android:fullBackupContent="@xml/backup_rules"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:supportsRtl="true"
    android:theme="@style/Theme.Ex05"
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
```

## Output:
![image](https://github.com/SrinivasanAIDS/Ex_5_Send-SMS-Using-Intent/assets/103049243/8688f9f6-756a-4ad6-bd49-1535ecb01c29)

![image](https://github.com/SrinivasanAIDS/Ex_5_Send-SMS-Using-Intent/assets/103049243/9cc18ce4-1882-4e0f-9ffd-7807603309d2)

## Result:
Thus a Simple Android Application to create and design an android application for Sending SMS using Intent in Android Studio was developed and executed successfully.

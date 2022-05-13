
# Ex.No:4 Design an android application Send SMS using Intent.


## AIM:

To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “ex.no.4″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application Send SMS using Intent.
Developed by: S. Sanjna Priya
Registeration Number : 212220230043
*/
```

### MainActivity.java
```
package com.example.ex04;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button mButton= (Button) findViewById(R.id.send_sms);
        mButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(Intent.ACTION_VIEW, Uri.fromParts("sms","9443354213",null));
                intent.putExtra("sms_body","Welcome to Android Studio");
                startActivity(intent);
            }
        });
    }
}
```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingLeft="16dp"
    android:paddingRight="16dp"
    android:paddingBottom="16dp"
    android:paddingTop="16dp"
    tools:context=".MainActivity">

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/send_sms"
        android:text="click_here_to_send_sms"/>

</RelativeLayout>
```

## OUTPUT
![4 1](https://user-images.githubusercontent.com/75234965/168219370-bb399655-9c92-4ea8-bf58-9e19746de0c7.png)

![4 3](https://user-images.githubusercontent.com/75234965/168219375-ee75d0f9-11bb-4efd-9e35-37170812c0f5.png)

![4 4](https://user-images.githubusercontent.com/75234965/168219380-3ad65b79-0481-4757-9eb0-ddd0cb37a9e9.png)

## RESULT
Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is developed and executed successfully.

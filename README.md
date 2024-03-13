# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.
Step 2: Then type the Application name as HelloWorld and click Next.
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml
Step 6: Display message give in MainActivity file.
Step 7: Save and run the application

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: YUVARAJ.B
Registeration Number : 212221040187
*/
```
## ACTIVITY_MAIN.XML
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:autofillHints="enterlink"
        android:id="@+id/editTextText"
        android:layout_width="290dp"
        android:layout_height="48dp"
        android:hint="@string/hint_web"
        android:inputType="text"
        android:textAlignment="center"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.495"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.935" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="324dp"
        android:text="@string/search_btn"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## MAINACTIVITY.JAVA
```
package com.example.buttons;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.EditText;
import android.widget.Button;
import android.net.Uri;
import android.content.Intent;
import android.view.View;

public class MainActivity extends AppCompatActivity {
    EditText editText;
    Button button;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url = editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }

   });
}
}
```

## OUTPUT

![Fimplicit](https://github.com/yuvaraj-csk/ImplicitIntent-MAD/assets/134052574/b0792962-c0d4-40ef-a49f-bbbb4f034168)

![impli-gmail](https://github.com/yuvaraj-csk/ImplicitIntent-MAD/assets/134052574/50e4ab25-5c43-49a2-8de9-189399bafc4d)


![signin-gmail](https://github.com/yuvaraj-csk/ImplicitIntent-MAD/assets/134052574/fe3ea95a-3691-4105-8cb4-ba8c90d7fdf1)






## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.



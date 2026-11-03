# Implicit_Intent
# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. Start the project: Create a new Android project in Android Studio.
2. Design the UI: In activity_main.xml, add an EditText (to accept the URL input) and a Button (to trigger the navigation).
3. Initialize components: In MainActivity.java, map the EditText and Button variables to their respective XML IDs using findViewById().
4. Set click listener: Attach an OnClickListener to the button to listen for user click events.
5. Get input: Inside the onClick method, extract the text entered in the EditText and convert it to a string.
6. Create implicit intent: Instantiate an Intent with the action Intent.ACTION_VIEW and pass the parsed URL string using Uri.parse().
7. Start activity: Call startActivity(intent) to trigger the OS to open the webpage in an available web browser.
8. Execution: Run and test the application.

## PROGRAM:
```
/*
Program
Developed by: Karthik J
Registeration Number : 212225040176
*/
```
**MainActivity**
```java
package com.example.implicit_intent;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.btn);
        editText = (EditText) findViewById(R.id.editText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```
**Activity_main.xml**
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="322dp"
        android:layout_height="67dp"
        android:fontFamily="sans-serif-condensed"
        android:hint="Enter the url"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.494"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.486" />

    <Button
        android:id="@+id/btn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@color/white"
        android:onClick="search"
        android:text="Search"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editText" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@android:color/holo_blue_bright"
        android:fontFamily="casual"
        android:text="Type website name"
        android:textSize="30sp"
        app:layout_constraintBottom_toTopOf="@+id/editText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="serif"
        android:text="Welcome To Android Studio"
        android:textAppearance="@style/TextAppearance.AppCompat.Body2"
        android:textSize="22sp"
        app:layout_constraintBottom_toTopOf="@+id/textView"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />


</androidx.constraintlayout.widget.ConstraintLayout>
```


## OUTPUT

<img width="1917" height="1073" alt="Screenshot 2026-11-03 225909" src="https://github.com/user-attachments/assets/f751e8c6-17da-4da3-bb40-9d434d9963c1" />

<img width="1917" height="1078" alt="Screenshot 2026-11-03 225901" src="https://github.com/user-attachments/assets/def5af28-e054-43ea-b76d-466faba8b7ae" />

<img width="1917" height="1078" alt="Screenshot 2026-11-03 225855" src="https://github.com/user-attachments/assets/513e3105-180d-4ff3-a316-d098b708f240" />

<img width="1917" height="1065" alt="Screenshot 2026-11-03 225816" src="https://github.com/user-attachments/assets/38b6ff47-b91e-4a04-9262-dd520d9589be" />


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.



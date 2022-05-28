### Ex.No:5 Develop a program to accept username and password from the end user using Text View and Edit Text and display personal information of the student.
### AIM :
To develop a program to accept username and password from the end user using Text View and Edit Text and display personal information of the student using Android Studio
### EQUIPMENTS REQUIRED :
Android Studio(Min.required Artic Fox)
### ALGORITHM :
## Step 1: 
Open Android Stdio and then click on File -> New -> New project.
## Step 2: 
Then type the Application name as studentinfo and click Next.
## Step 3: 
Then select the Minimum SDK as shown below and click Next.
## Step 4: 
Then select the Empty Activity and click Next. Finally click Finish.
## Step 5: 
Design layout in activity_main.xml.
## Step 6: 
Accept username and password from the end user and the display information give in MainActivity file.
## Step 7: 
Save and run the application.
### PROGRAM :
```java
Developed by: ASHWIN A O
Registeration Number : 212220230005
```

## activity main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/button4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="16dp"
        android:text="Name"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toStartOf="@+id/e1"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.224" />

    <Button
        android:id="@+id/button3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="16dp"
        android:text="password"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toStartOf="@+id/e2"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.351" />

    <EditText
        android:id="@+id/e1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:text=" "
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/buttonSubmit"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.354" />

    <Button
        android:id="@+id/buttonSubmit"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="16dp"
        android:text=" submit"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.499" />

    <Button
        android:id="@+id/buttonReset"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="reset"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.523"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.499" />

    <EditText
        android:id="@+id/e2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:text=""
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.781"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.223" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="186dp"
        android:layout_height="116dp"
        android:text=" "
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.422"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/buttonSubmit"
        app:layout_constraintVertical_bias="0.362" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## activity main.java
```java
package com.example.userpass;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
//import android.support.v7.app.AppCompatActivity;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity {

    // These are the global variables
    EditText editName, editPassword;
    TextView result;
    Button buttonSubmit, buttonReset;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        editName = (EditText) findViewById(R.id.e2);
        editPassword = (EditText) findViewById(R.id.e1);
        result = (TextView) findViewById(R.id.textView);
        buttonSubmit = (Button) findViewById(R.id.buttonSubmit);
        buttonReset = (Button) findViewById(R.id.buttonReset);
/*
Submit Button
*/
        buttonSubmit.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String name = editName.getText().toString();
                String password = editPassword.getText().toString();
                result.setText("Name:\t" + name + "\nPassword:\t" + password );
            }
        });

        buttonReset.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editName.setText("");
                editPassword.setText("");
                result.setText("");
                editName.requestFocus();
            }
        });
    }
}
```
### OUTPUT :
![Screenshot 2022-05-28 114330](https://user-images.githubusercontent.com/75235601/170813377-40c0f76d-3142-4888-aa54-b9c3f5e64ff4.jpg)
![Screenshot 2022-05-28 114501](https://user-images.githubusercontent.com/75235601/170813381-761c6b8c-57e2-48fc-9f0f-1550a43f40ba.jpg)

### RESULT :
Thus a Simple Android Application develop a program to accept username and password from the end user using Text View and Edit Text and display personal information of the student using Android Studio is developed and executed successfully.




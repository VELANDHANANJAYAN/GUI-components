# Ex.No: 1 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1.Start a new project in Android Studio.

2.Design a simple layout(.xml File).

3.Inside MainActivity.java , create the button function

4.Create button for colors and fonts while clicking color or font button should change the color and font.

5.Display corresponding changes in application.

## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by: VELAN D
Registeration Number : 212222040176
*/
```
### In activitymain.xml:
~~~
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="sans-serif-black"
        android:text="Hello World!"
        android:textSize="48sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toTopOf="@+id/button1"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.496"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.623" />

    <Button
        android:id="@+id/button2"
        android:layout_width="304dp"
        android:layout_height="56dp"
        android:layout_marginBottom="308dp"
        android:backgroundTint="#9DA2A3"
        android:text="CHANGE COLOR"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.532"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/button1"
        android:layout_width="297dp"
        android:layout_height="56dp"
        android:layout_marginBottom="32dp"
        android:backgroundTint="#9DA2A3"
        android:text="CHANGE FONT SIZE"
        android:textSize="20sp"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
~~~
### In MainActivity.java:
~~~
package com.example.gui_component;

import android.graphics.Color;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

import com.example.gui_component.R;

public class MainActivity extends AppCompatActivity
{
    int ch=1;
    float font=30;
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t= (TextView) findViewById(R.id.textView);
        Button b1= (Button) findViewById(R.id.button1);
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                t.setTextSize(font);
                font = font + 5;
                if (font == 50)
                    font = 30;
            }
        });
        Button b2= (Button) findViewById(R.id.button2);
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                switch (ch) {
                    case 1:
                        t.setTextColor(Color.RED);
                        break;
                    case 2:
                        t.setTextColor(Color.GREEN);
                        break;
                    case 3:
                        t.setTextColor(Color.BLUE);
                        break;
                    case 4:
                        t.setTextColor(Color.CYAN);
                        break;
                    case 5:
                        t.setTextColor(Color.YELLOW);
                        break;
                    case 6:
                        t.setTextColor(Color.MAGENTA);
                        break;
                }
                ch++;
                if (ch == 7)
                    ch = 1;
            }
        });
    }
}
~~~
## OUTPUT

![Screenshot 2024-05-07 174708](https://github.com/VELANDHANANJAYAN/GUI-components/assets/119405038/9ce64f45-f1f3-4893-ba5c-939416dffb8e)
![Screenshot 2024-05-07 174722](https://github.com/VELANDHANANJAYAN/GUI-components/assets/119405038/9ed60dbb-9b0f-4bb7-b9ba-4f3411207e1d)
![Screenshot 2024-05-07 174742](https://github.com/VELANDHANANJAYAN/GUI-components/assets/119405038/1adea5eb-231b-4512-a7cb-8c53e85db0de)
![Screenshot 2024-05-07 174759](https://github.com/VELANDHANANJAYAN/GUI-components/assets/119405038/1bde93f4-2731-42a6-9373-6f93040c16c6)

## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.



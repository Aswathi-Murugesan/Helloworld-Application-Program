MainActivity.java: 

package com.example.helloworld; 

import androidx.appcompat.app.AppCompatActivity; 

import android.os.Bundle; import android.view.View;

import android.widget.Button; 

import android.widget.EditText; 

import android.widget.TextView; 

public class MainActivity extends AppCompatActivity { 

@Override 

protected void onCreate(Bundle savedInstanceState) 

{ 

super.onCreate(savedInstanceState); 

setContentView(R.layout.activity_main); 

} 

public void doSomething(View v) { 

final TextView outputText = (TextView) findViewById(R.id.textView); 

final EditText nameText = (EditText) findViewById(R.id.editText); 

Button b = (Button)findViewById(R.id.button); 

b.setOnClickListener(new View.OnClickListener() 

{ 

public void onClick(View v)

{ 

outputText.setText("Hello " + nameText.getText()); 

} 

}); 

} 

} 

ActivityMain.xml: 

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout 

xmlns:android="http://schemas.android.com/apk/res/android" 

xmlns:app="http://schemas.android.com/apk/res-auto" 

xmlns:tools="http://schemas.android.com/tools" 

android:layout_width="match_parent" 

android:layout_height="match_parent" 

android:paddingBottom="16dp" 

android:paddingLeft="16dp" 

android:paddingRight="16dp" 

android:paddingTop="16dp" 

tools:context=".MainActivity" 

tools:showIn="@layout/activity_main">

<TextView 

android:layout_width="wrap_content" 

android:layout_height="wrap_content" 

android:text="Hello World!" 

android:id="@+id/textView" 

app:layout_constraintBottom_toBottomOf="parent" 

app:layout_constraintEnd_toEndOf="parent" 

app:layout_constraintStart_toStartOf="parent" 

app:layout_constraintTop_toTopOf="parent" />

<EditText 

android:layout_width="wrap_content" 

android:layout_height="wrap_content" 

android:inputType="textPersonName" 

android:text="Enter Name" 

android:ems="10" 

android:id="@+id/editText" 

android:layout_below="@+id/textView" 

android:layout_centerHorizontal="true" 

android:layout_marginTop="57dp"/>
<Button 

android:layout_width="wrap_content" 

android:layout_height="wrap_content" 

android:text="Click Me" 

android:id="@+id/button" 

android:layout_below="@+id/editText" 

android:layout_toRightOf="@+id/textView" 

android:layout_toEndOf="@+id/textView" 

android:layout_marginTop="104dp" 

android:onClick="doSomething" />

</RelativeLayout>

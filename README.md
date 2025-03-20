# MAD-10
# Ex.No:10 Develop an android application to create a option menu to display menu items using android studio.


## AIM:
To create a option menu to display menu items using Android Studio.

## EQUIPMENTS REQUIRED:
Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

## Program to print the text “optionmenu”.
## Developed by: KISHORE M
## Registeration Number : 212221043003



## Activity_main.xml


```C

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <androidx.appcompat.widget.Toolbar
        android:id="@+id/toolbar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:title="Options Menu"
        app:layout_constraintTop_toTopOf="parent"
        android:background="?android:attr/colorPrimary" />

    <TextView
        android:id="@+id/helloTextView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>

```

## MainActivity.java

```C

package com.example.ex_10;

import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;
import androidx.appcompat.widget.Toolbar;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Set up the toolbar
        Toolbar toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar); // Set the toolbar as the action bar
    }

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.options_menu, menu); // Inflate the menu
        return true;
    }

    @Override
    public boolean onOptionsItemSelected(MenuItem item) {
        Toast.makeText(this, "Selected Item: " + item.getTitle(), Toast.LENGTH_SHORT).show();
        return super.onOptionsItemSelected(item);
    }
}
```

## options_menu.xml

```C

<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">
    <item
        android:id="@+id/search_item"
        android:title="@string/search" />
    <item
        android:id="@+id/upload_item"
        android:title="@string/upload" />
    <item
        android:id="@+id/copy_item"
        android:title="@string/copy" />
    <item
        android:id="@+id/print_item"
        android:title="@string/print" />
    <item
        android:id="@+id/share_item"
        android:title="@string/share" />
    <item
        android:id="@+id/bookmark_item"
        android:title="@string/bookmark" />
</menu>
```
## OUTPUT

<img src="https://github.com/user-attachments/assets/6f088aa0-5a03-46a5-b929-e75c0ecb4ab0" width=200>


## RESULT

The application successfully displays an options menu with various items, and upon selecting any item, a toast message shows the selected item.

# workshop1

### AIM :

 To Create a application for addition of two numbers

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “calculator operation”.
Developed by: I S ISHITA
Registeration Number : 212224220038
*/
```

### activity main_xml :

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="24dp"
    android:gravity="center">
    <TextView
        android:id="@+id/workshop"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Workshop1"
        android:textSize="18sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginTop="20dp" />
    <TextView
        android:id="@+id/addition"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Addition Of Two Numbers"
        android:textSize="18sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginTop="20dp" />
    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="number" />

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="number"
        android:layout_marginTop="12dp" />

    <Button
        android:id="@+id/btnSum"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Calculate Sum "
        android:layout_marginTop="16dp" />

    <TextView
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Result will appear here"
        android:textSize="18sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginTop="20dp" />

</LinearLayout>

```

### main activity java :

```

package com.example.workshop1;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button btnSum;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Link UI elements
        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        btnSum = findViewById(R.id.btnSum);
        result = findViewById(R.id.result);

        btnSum.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // Get numbers from EditText
                String s1 = num1.getText().toString();
                String s2 = num2.getText().toString();

                if (s1.isEmpty() || s2.isEmpty()) {
                    result.setText("Please enter both numbers!");
                    return;
                }

                // Convert to integers
                int a = Integer.parseInt(s1);
                int b = Integer.parseInt(s2);

                // Calculate sum
                int sum = a + b;

                // Display result
                result.setText("Sum: " + sum);
            }
        });
    }
}

```

### output:

<img width="1729" height="1064" alt="image" src="https://github.com/user-attachments/assets/dbd82d37-426f-4e61-9d36-be5a342000fd" />

### result:

Thus a Simple Android Application create  to get addition of two numbers  using Android Studio is developed and executed successfully.




 

# My-first-app
First working app I created. with Youtube instructions
package com.example.loginapp.myfirstapplication;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
// I created  a place to enter the numbers, and a button for results//

        Button addbutton = (Button)findViewById(R.id.addbutton);
        addbutton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                EditText firstnumEditText = (EditText) findViewById(R.id.firstNumEditText);
                EditText numedittext2 =  (EditText)findViewById(R.id.numeditText2);
                TextView resulttextView = (TextView) findViewById(R.id.resulttextView);
 // created a expression to enter the 2 numbers and add them. and  a result to show the sum of those numbers//                

                        int num1 = Integer.parseInt(firstnumEditText.getText().toString());
                int num2 = Integer.parseInt(numedittext2.getText().toString());
                int result = num1 + num2 ;
                resulttextView.setText(result + "");
            }
        });
    }
}

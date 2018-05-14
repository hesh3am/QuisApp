package com.example.hesham.quisapp;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.CheckBox;
import android.widget.EditText;
import android.widget.RadioButton;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    int score = 0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    public void submit(View view) {
        EditTexteQuestion1();
        checkboxQuestion2();
        checkboxQuestion3();
        radioButtonQuestion4();
        radioButtonQuestion5();
        Toast.makeText(this, "You score is : " + score, Toast.LENGTH_LONG).show();
        score = 0;
    }

    /////////////////////////////// question 1
    public void EditTexteQuestion1() {
        EditText Answer300 = (EditText) findViewById(R.id.Answer300);
        String value = Answer300.getText().toString();
        if (value.contentEquals("300"))
            score += 2;
    }

    /////////////////////////////// question 2
    public void checkboxQuestion2() {
        CheckBox four1CheckBox = (CheckBox) findViewById(R.id.four1);
        boolean four1 = four1CheckBox.isChecked();
        if (four1)
            score -= 1;

        CheckBox four2CheckBox = (CheckBox) findViewById(R.id.four2);
        boolean four2 = four2CheckBox.isChecked();
        if (four2)
            score += 1;

        CheckBox four3CheckBox = (CheckBox) findViewById(R.id.four3);
        boolean four3 = four3CheckBox.isChecked();
        if (four3)
            score += 1;

        CheckBox four4CheckBox = (CheckBox) findViewById(R.id.four4);
        boolean four4 = four4CheckBox.isChecked();
        if (four4)
            score -= 1;
    }

    /////////////////////////////// question 3
    public void checkboxQuestion3() {
        CheckBox eigth1CheckBox = (CheckBox) findViewById(R.id.eigth1);
        boolean eigth1 = eigth1CheckBox.isChecked();
        if (eigth1)
            score += 1;

        CheckBox eigth2CheckBox = (CheckBox) findViewById(R.id.eigth2);
        boolean eigth2 = eigth2CheckBox.isChecked();
        if (eigth2)
            score -= 1;

        CheckBox eigth3CheckBox = (CheckBox) findViewById(R.id.eigth3);
        boolean eigth3 = eigth3CheckBox.isChecked();
        if (eigth3)
            score -= 1;

        CheckBox eigth4CheckBox = (CheckBox) findViewById(R.id.eigth4);
        boolean eigth4 = eigth4CheckBox.isChecked();
        if (eigth4)
            score += 1;
    }

    /////////////////////////////// question 4
    public void radioButtonQuestion4() {
        RadioButton radioButtonAnswer36 = (RadioButton) findViewById(R.id.Answer36);
        boolean Answer36 = radioButtonAnswer36.isChecked();
        if (Answer36)
            score += 2;
    }

    /////////////////////////////// question 5
    public void radioButtonQuestion5() {
        RadioButton radioButtonAnswer22 = (RadioButton) findViewById(R.id.Answer22);
        boolean Answer22 = radioButtonAnswer22.isChecked();
        if (Answer22)
            score += 2;
    }
}

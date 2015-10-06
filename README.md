# Work1
Java MAIN ACTIVITY
package com.example.vladyslav.mywork1;

import android.app.Activity;
import android.app.ListActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.ExpandableListView;
import android.widget.ListView;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends Activity implements View.OnClickListener {
        TextView soch;
    TextView hlib;
    TextView maca;
    TextView silhlib;

        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_main);
            soch = (TextView)findViewById(R.id.soch);
            soch.setOnClickListener(this);
            hlib = (TextView)findViewById(R.id.hlib);
            hlib.setOnClickListener(this);
            maca = (TextView)findViewById(R.id.maca);
            maca.setOnClickListener(this);
            silhlib = (TextView)findViewById(R.id.silhlib);
            silhlib.setOnClickListener(this);



        }





        @Override
        public boolean onCreateOptionsMenu(Menu menu) {
            // Inflate the menu; this adds items to the action bar if it is present.
            getMenuInflater().inflate(R.menu.menu_main, menu);
            return true;
        }

        @Override
        public boolean onOptionsItemSelected(MenuItem item) {
            // Handle action bar item clicks here. The action bar will
            // automatically handle clicks on the Home/Up button, so long
            // as you specify a parent activity in AndroidManifest.xml.
            int id = item.getItemId();

            //noinspection SimplifiableIfStatement
            if (id == R.id.action_settings) {
                return true;
            }

            return super.onOptionsItemSelected(item);
        }


    @Override
    public void onClick(View v) {

        switch (v.getId()){
            case R.id.soch:
              Intent intent = new Intent(this,Main2Activity.class);
                startActivity(intent);
                break;
            default:
                break;


        }
        switch (v.getId()) {
            case R.id.hlib:
                Intent intent = new Intent(this, Hlibzyacamu.class);
                startActivity(intent);
                break;
            default:
                break;
        }
        switch (v.getId()) {
            case R.id.maca:
                Intent intent = new Intent(this, Maca.class);
                startActivity(intent);
                break;
            default:
                break;
        }
        switch (v.getId()) {
            case R.id.silhlib:
                Intent intent = new Intent(this, Silhlib.class);
                startActivity(intent);
                break;
            default:
                break;
        }

    }
}



# ListView 1
untuk menampilkan list

> ini xmlnya 
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <ListView
        android:id="@+id/listview"
        android:layout_width="360dp"
        android:layout_height="592dp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
> ini kotlin
```kt
package com.example.latihan3_listview

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.ArrayAdapter
import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        var daftarNama =  ArrayList<String>()
        daftarNama.add("machiatto")
        daftarNama.add("cafucino")
        daftarNama.add("kapal api")
        daftarNama.add("americano")
        daftarNama.add("chocalate")

        val arrayAdapter = ArrayAdapter(applicationContext,android.R.layout.simple_list_item_1,daftarNama)
        listview.adapter = arrayAdapter;

    }
}

```

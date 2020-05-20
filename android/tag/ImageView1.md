# ImageView 1
kalo dihtml tag <img/> gunanya untuk menampilkan gambar
```xml
            <ImageView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:src="@drawable/user_1"/>
```
user1 disini adalah nama gambarnya dengan tipe ``png``


```xml
   <ImageView
      android:id="@+id/images_dice"
      android:src="@drawable/empty_dice"
      android:layout_gravity="center_horizontal"
      android:layout_width="wrap_content"
      tools:src="@drawable/dice_3"
      android:layout_height="wrap_content"/>
```

1. tools:src -> hanya untuk menampilkan tampilan di android studio saja karena saat dijalankan gambarnya yaitu yg tidak ada
2. android:src -> ini untuk menamilkan gambar disi empty_dice yg berarti gambarnya kosong

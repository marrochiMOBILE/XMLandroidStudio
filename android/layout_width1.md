# layout_width 1
untuk lebar tampilan

#### syntax
```xml
android:layout_width="...isi ukuran....."
```

contoh :
```xml
 android:layout_width="170dp"
```

|opsi|arti|penjelasan|
|---|---|--|
| **`wrap_content`**||sesuai ukuran format teks|
| **`match_parent`** || peleberan secara max |
| **`dp`** |  density independent pixels  | Jumlah piksel diwakili dalam satu unit dp akan meningkat sesuai resolusi layar ( bila Anda memiliki banyak titik per pixel per inci ) . Sebaliknya pada perangkat dengan resolusi lebih rendah , jumlah piksel diwakili dalam unit yang dp akan menurun . Karena ini adalah unit relatif , perlu memiliki ukuran dasar yang bisa dibandingkan dengannya . Misal dasar ukuran adalah layar 160 dpi . Berikut ini adalah persamaannya : px = dp * ( dpi / 160 ) .|
|**`dip`**|density independent pixels| sama ke yg atas |
|**`px `**| pixel | sesuai dengan piksel yang sebenarnya pada layar |
|**`pt`**|point|sesuai dengan 1/72 dari satu inci di layar|
|**`in`**|inch|sesuai dengan inci pada layar|
|**`mm`**|milimeter|sesuai dengan milimeter di layar|
|**`sp `**|scale independent pixels|Unit ini skala menurut dpi layar (mirip dengan dp) serta preferensi ukuran font pengguna.|

Pada dasarnya , Android membuat lebih mudah dalam menangani ukuran layar yang berbeda. Selama Anda menggunakan dp untuk semua : views ( TextView , ImageView , EditView , dll ) , layout , dll. Hal ini akan memastikan aplikasi Anda akan mebuat  skala sesuai sebagai perubahan resolusi layar dari perangkat ke perangkat lain. Anda harus menggunakan sp untuk semua teks, ini akan membawa ke preferensi font account pengguna.

Contoh :

Katakanlah Anda memiliki view dengan width 10px.
Pada layar yang memiliki 160dpi, apa yang Anda amati secara visual adalah bahwa 10dp = 10px , dan mengubah unit file .xml Anda. Dari dp ke px atau sebaliknya tidak akan mengubah apa yang Anda amati di layar.

Sekarang, katakanlah Anda memiliki layar dengan dua kali resolusi : 320dpi ( asumsi kedua layar memiliki dimensi fisik yang sama ). Anda akan melihat tampilan yang persis setengah ( yaitu jika Anda mengukur dengan penggaris ) dari apa yang terlihat di layar 160dpi . Namun, jika Anda mengubah unit dalam file .xml untuk 10dp , ukuran pada layar 320dpi akan sama dengan ukuran pada layar 160dpi .

Lihatlah distribusi ukuran layar dan density di sini :

http://developer.android.com/about/dashboards/index.html#Screens

Dan panduan tentang Dimensi di android :

http://developer.android.com/guide/topics/resources/more-resources.html#Dimensi

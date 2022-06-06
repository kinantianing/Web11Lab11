# Web11Lab11

**Nama    : Aning Kinanti** <br>
**NIM     : 312010364** <br>
**Kelas   : TI.20.A2** <br>
**Matkul  : Pemrograman Web** <br>

# Belajar PHP Framework (Codeigneter)
1. Konfigurasi Webserver dengan mengaktifkan beberapa ekstensi, mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian Apache klik Config -> PHP.ini. Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server seperti dibawah ini : <br>
![Gambar 1](screenshot/ss1.PNG) <br>

2. Instalasi Codeigneter 4 dari website https://codeigniter.com/download.
Extrak file zip Codeigniter ke direktori htdocs/lab11ci.
Ubah nama direktory menjadi ci4. Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/

3. Menjalankan CLI (Command Line Interface). Untuk mengakses CLI buka terminal/command prompt. Seperti dibawah ini : <br>
![Gambar 2](screenshot/ss2.PNG) <br>

4. Mengaktifkan Mode Debugging untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable CI_ENVIRINMENT menjadi development.
Contoh error yang terjadi apabila mengubah kode pada file app/Controller/Home.php hilangkan titik koma pada akhir kode.
![Gambar 3](screenshot/ss3.PNG) <br>



## A. Program Sederhana Menggunakan Framework Codeigneter 4
### 1. Membuat Route Baru
Tambahkan kode berikut pada file `Routes.php` yang terletak pada `app/config/Routes.php` seperti contoh dibawah ini : <br>
```
$routes->get('/about', 'Page::about');
$routes->get('/contact', 'Page::contact');
$routes->get('/faqs', 'Page::faqs');
```
<br>

### 2. Membuat Controller
Buatlah file PHP baru dengan nama `Page.php` yang terletak pada `app/Controllers/Routes.php` lalu isi dengan sintaks seperti contoh dibawah ini : <br>
```
<?php

namespace App\Controllers;

class Page extends BaseController
{
    public function about()
    {
       echo "Ini adalah halaman About";

    }

    public function contact()
    {
        echo "Ini adalah halaman Contact";

    }

    public function faqs()
    {
        echo "Ini adalah halaman Faqs";
    }
}
```
<br>

Selanjutnya coba akses dengan alamat url http://localhost:8080/about
![Gambar 4](screenshot/ss4.PNG) <br>

### 3. Membuat View
Buatlah file PHP baru dengan nama `about.php` yang terletak pada `app/Views/about.php` lalu isi dengan sintaks seperti contoh dibawah ini : <br>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title><?= $title; ?></title>
</head>
<body>
    <?= $this->include('template/header'); ?>

    <h1><?= $title; ?></h1>
    <hr>
    <p><?= $content; ?></p>

    <?= $this->include('template/footer'); ?>
</body>
</html>
```
<br>

Ubah method about pada class Controllers Page menjadi seperti berikut : <br>
```
public function about()
    {
        return view('about', [
            'title' => 'Halaman About', 
            'content' => 'Ini adalah paragraf yang menjelaskan tentang halaman about.'
        ]);
    }

```
<br>

Setelah halaman direfresh maka akan menjadi seperti dibawah ini :
![Gambar 5](screenshot/ss5.PNG) <br>


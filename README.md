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

4. Mengaktifkan Mode Debugging untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development. Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable CI_ENVIRINMENT menjadi development.
![Gambar 3](screenshot/ss3.PNG) <br>

Contoh error yang terjadi apabila mengubah kode pada file 
app/Controller/Home.php hilangkan titik koma pada akhir kode.



## A. Modularisasi Program
### 1. Membuat File Header Php
Buatlah dokumen PHP dengan nama `header.php` seperti contoh dibawah ini : <br>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="style.css" rel="stylesheet" type="text/stylesheet" media="screen" />
    <title>Contoh Modularisasi</title>
</head>
<body>
    <div class="container">
        <header>
            <h1>Modularisasi</h1>
        </header>
        <nav>
            <a href="home.php">HOME</a>
            <a href="about.php">ABOUT</a>
            <a href="kontak.php">CONTACT</a>
        </nav>
```
<br>

### 2. Membuat File Footer Php
Buatlah file PHP baru dengan nama `footer.php` seperti contoh dibawah ini : <br>
```
        <footer>
            <p>&copy; 2021, Informatika, Universitas 
        </footer>
    </div>
</body>
</html>
```
<br>
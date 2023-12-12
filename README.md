# Labweb9
|Nama | Rifa Andiani Meilawati|
| :--| :--|
|NIM|312210377|
|Matkul|pemograman web 1|
|Dosen| agung nugroho S.Kom.,M.Kom|
|Kelas| TI22A4|
# PHP MODULAR
PHP modular mengacu pada pendekatan pengembangan web yang memecah aplikasi PHP menjadi modul atau bagian-bagian yang lebih kecil dan mandiri. Pendekatan ini bertujuan untuk meningkatkan keterbacaan kode, mempermudah pemeliharaan, dan memfasilitasi pengembangan yang berskala lebih besar. Beberapa konsep yang terkait dengan PHP modular melibatkan penggunaan fungsi, kelas, dan namespace untuk memisahkan fungsionalitas ke dalam unit yang lebih kecil.
# Instruksi Praktikum
Persiapkan text editor misalnya VSCode.
Buat folder baru dengan nama lab9_php_modular pada docroot webserver (htdocs)
Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya.
## 1.  Buat file baru dengan nama header.php
```PHP
<?php
include("koneksi.php");

// query untuk menampilkan data
$sql = 'SELECT * FROM data_barang';
$result = mysqli_query($conn, $sql);

?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Contoh Modularisasi</title>
    <link href="style.css" rel="stylesheet" type="text/stylesheet" media="screen" />
</head>
<body>
        <div class="container">
        <header>
        <center>
            <h2 style="color: #000080;">Modularisasi Menggunakan Require</h2>
        </center>
        </header>
        <nav>
            <a href="tambah.php">Tambah Barang</a>
            <a href="home.php">Home</a>
            <a href="about.php">Tentang</a>
            <a href="kontak.php">Kontak</a>
        </nav>
```

## OUTPUT

# 2.  Buat file baru dengan nama footer.php

```PHP
        <footer>
            <center>
            <p>&copy; 2023, Informatika, Liskania Aprilia</p>
    </center>
        </footer>
    </div>
</body>
</html>
```

## OUTPUT

# 3. Buat file baru dengan nama home.php

```PHP
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
</head>
<div class="container">
<div class="title-container">
            <h1 style="color: #FFFFFF;">Home</h1>
        </div>
<div class="content">
    <center>
    <h2 style="color: #000080;">Situs Jual Beli Barang Elektronik</h2>
</center>
</div>
        <b>
    <p>Jual beli barang elektronik kini semakin mudah dan terjangkau. Anda bisa menemukan berbagai macam barang elektronik yang Anda butuhkan di sini, mulai dari smartphone, laptop, hingga televisi.</p>

<p>Selain itu, Anda juga bisa mendapatkan berbagai macam promo dan diskon menarik.</p>

<p>Yuk, mulai jual beli barang elektronik di sini sekarang juga!</p>
<b>
</div>
<?php require('footer.php'); ?>
</html>
```
## OUTPUT

# 4. Buat file baru dengan nama about.php

```PHP
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
</head>
<div class="container">
<div class="title-container">
            <h1 style="color: #FFFFFF;">About</h1>
        </div>
<div class="content">
    <center>
    <h2 style="color: #000080;">Tentang Kami</h2>
</center>
</div>
        <b>

<p>Situs ini adalah situs jual beli barang elektronik yang terpercaya dan terjangkau. Kami menyediakan berbagai macam barang elektronik, mulai dari smartphone, laptop, hingga televisi.</p>

<p>Kami berkomitmen untuk memberikan pengalaman jual beli yang terbaik bagi pelanggan. Kami memiliki tim customer service yang siap membantu Anda 24/7. Kami juga menawarkan berbagai macam promo dan diskon menarik untuk pelanggan setia kami.</p>

<p>Visi dan Misi</p>

<p>Visi: Menjadi situs jual beli barang elektronik terpercaya dan terjangkau di Indonesia.</p>

<p>Misi:</p>

<p>1. Menyediakan berbagai macam barang elektronik berkualitas dengan harga terjangkau</p>
<p>2. Memberikan pengalaman jual beli yang terbaik bagi pelanggan</p>
<p>3. Menjadi mitra terpercaya bagi penjual dan pembeli</p>


<p>Jika Anda memiliki pertanyaan atau ingin memberikan masukan, Anda bisa menghubungi kami melalui:</p>

<p>Email: databarang@gmail.com</p>
<p>Telepon: 08997645667787</p>
<p>WhatsApp: 09874536896</p>
              
</b>
</div>
<?php require('footer.php'); ?>
</html>
```
## OUTPUT

# PERTANYAAN & TUGAS
Implementasikan konsep modularisasi pada kode program praktikum 8 tentang database, sehingga setiap halamannya memiliki template tampilan yang sama.

1. Membuat file index untuk menampilkan data (Read)

```HTML
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Data Barang</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
    
</head>

<body>
    <div class="container">
    <div class="title-container">
            <h1 style="color: #FFFFFF;">Data Barang</h1>
        </div>
        <div class="main"> 
             <?php require('header.php'); ?>          
            <table>
                <tr>
                    <th>Gambar</th>
                    <th>Nama Barang</th>
                    <th>Kategori</th>
                    <th>Harga Jual</th>
                    <th>Harga Beli</th>
                    <th>Stok</th>
                    <th>Aksi</th>
                </tr>
                <?php if ($result) : ?>
                    <?php while ($row = mysqli_fetch_array($result)) : ?>
                        <tr>
                            <td><img src="gambar/<?= $row['gambar']; ?>" alt="<?=$row['nama']; ?>"></td>
                            <td><?= $row['nama']; ?></td>
                            <td><?= $row['kategori']; ?></td>
                            <td><?= $row['harga_beli']; ?></td>
                            <td><?= $row['harga_jual']; ?></td>
                            <td><?= $row['stok']; ?></td>
                            <td>
                                <a href="ubah.php?id=<?= $row['id_barang']; ?>">Ubah</a>
                                <a href="hapus.php?id=<?= $row['id_barang']; ?>">Hapus</a>
                            </td>
                        </tr>
                    <?php endwhile; else : ?>
                    <tr>
                        <td colspan="7">Belum ada data</td>
                    </tr>
                <?php endif; ?>
            </table>
        </div>
    </div>
    <?php require('footer.php'); ?>
</body>
</html>
```
# 2. Menambah Data (Create)

```php
<?php
error_reporting(E_ALL);
include_once 'koneksi.php';

if (isset($_POST['submit']))
{
    $nama = $_POST['nama'];
    $kategori = $_POST['kategori'];
    $harga_jual = $_POST['harga_jual'];
    $harga_beli = $_POST['harga_beli'];
    $stok = $_POST['stok'];
    $file_gambar = $_FILES['file_gambar'];
    $gambar = null;
    if ($file_gambar['error'] == 0)
    {
        $filename = str_replace(' ', '_',$file_gambar['name']);
        $destination = dirname(__FILE__) .'/gambar/' . $filename;
        if(move_uploaded_file($file_gambar['tmp_name'], $destination))
        {
            $gambar = 'gambar/' . $filename;;
        }
    }
    $sql = 'INSERT INTO data_barang (nama, kategori,harga_jual, harga_beli, stok, gambar) ';
    $sql .= "VALUE ('{$nama}', '{$kategori}','{$harga_jual}','{$harga_beli}', '{$stok}', '{$gambar}')";
    $result = mysqli_query($conn, $sql);
    header('location: index.php'); 
}
?>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tambah Barang</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
</head>

<body>
    <div class="container">
    <div class="title-container">
            <h1 style="color: #FFFFFF;">Tambah Barang</h1>
        </div>
        <div class="main">
            <form method="post" action="tambah.php" enctype="multipart/form-data">
                <div class="input">
                    <label> Nama Barang</label>
                    <input type="text" name="nama"/>
                </div>
                <div class="input">
                    <label>Kategori</label>
                    <select name="kategori">
                        <option value="Komputer">Komputer</option>
                        <option value="Elektronik">Elektronik</option>
                        <option value="HandPhone">HandPhone</option>
                    </select>
                </div>
                <div class="input">
                    <label>Harga Jual</label>
                    <input type="text" name="harga_jual" />
                </div>
                <div class="input">
                    <label>Harga Beli</label>
                    <input type="text" name="harga_beli" />
                </div>
                <div class="input">
                    <label>Stok</label>
                    <input type="text" name="stok" />
                </div>
                <div class="input">
                    <label>File Gambar</label>
                    <input type="file" name="file_gambar" />
                </div>
                <div class="submit">
                    <input type="submit" name="submit" value="Simpan" />
                </div>
            </form>
        </div>
    </div>
</body>
</html>
```
# 3. Mengubah Data (Update)

```php
<?php
error_reporting(E_ALL);
include_once 'koneksi.php';

if (isset($_POST['submit']))
{
    $id = $_POST['id'];
    $nama = $_POST['nama'];
    $kategori = $_POST['kategori'];
    $harga_jual = $_POST['harga_jual'];
    $harga_beli = $_POST['harga_beli'];
    $stok = $_POST['stok'];
    $file_gambar = $_FILES['file_gambar'];
    $gambar = null;

    if ($file_gambar['error'] == 0)
    {
        $filename = str_replace(' ', '_', $file_gambar['name']);
        $destination = dirname(__FILE__) . '/gambar/' . $filename;
        if (move_uploaded_file($file_gambar['tmp_name'], $destination))
        {
            $gambar = 'gambar/' . $filename;;
        }    
    }

    $sql = 'UPDATE data_barang SET ';
    $sql .= "nama = '{$nama}', kategori = '{$kategori}', ";
    $sql .= "harga_jual = '{$harga_jual}', harga_beli = '{$harga_beli}', stok = '{$stok}' ";
    if (!empty($gambar))
        $sql .= ", gambar = '{$gambar}' ";
    $sql .= "WHERE id_barang = '{$id}'";
    $result = mysqli_query($conn, $sql);   
    
    header('location: index.php');
}

$id = $_GET['id'];
$sql = "SELECT * FROM data_barang WHERE id_barang = '{$id}'";
$result = mysqli_query($conn, $sql);
if (!$result) die('Error: Data tidak tersedia');
$data = mysqli_fetch_array($result);

function is_select($var, $val) {
    if ($var == $val) return 'selected="selected"';
    return false;
}

?>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ubah Barang</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
</head>

<body>
    <div class="container">
    <div class="title-container">
            <h1 style="color: #FFFFFF;">Ubah Barang</h1>
        </div>
        <div class="main">
            <form method="post" action="ubah.php" enctype="multipart/form-data">
            <div class="input">
                <label>Nama Barang</label>
                <input type="text" name="nama" value="<?php echo $data['nama'];?>" />
            </div>
                <div class="input">
                    <label>Kategori</label>
                    <select name="kategori">
                        <option <?php echo is_select ('Komputer', $data['kategori']);?> value="Komputer">Komputer</option>
                        <option <?php echo is_select ('Komputer', $data['kategori']);?> value="Elektronik">Elektronik</option>
                        <option <?php echo is_select ('Komputer', $data['kategori']);?> value="Hand Phone">Hand Phone</option>
                    </select>
                </div>
                <div class="input">
                    <label>Harga Jual</label>
                    <input type="text" name="harga_jual" value="<?php echo $data['harga_jual'];?>" />
                </div>
                <div class="input">
                    <label>Harga Beli</label>
                    <input type="text" name="harga_beli" value="<?php echo $data['harga_beli'];?>" />
                </div>
                <div class="input">
                    <label>Stok</label>
                    <input type="text" name="stok" value="<?php echo $data['stok'];?>" />
                </div>
                <div class="input">
                    <label>File Gambar</label>
                    <input type="file" name="file_gambar" />
                </div>
                <div class="submit">
                    <input type="hidden" name="id" value="<?php echo $data['id_barang'];?>" />
                    <input type="submit" name="submit" value="Simpan" />
                </div>
            </form> 
        </div>
    </div>
</body>
</html>
```
# 4. Menghapus data (delete)

```php
<?php
include_once 'koneksi.php';
$id = $_GET['id'];
$sql = "DELETE FROM data_barang WHERE id_barang = '{$id}'";
$result = mysqli_query($conn, $sql);
header('location: index.php');
?>
```
# FINISH


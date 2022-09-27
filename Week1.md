# Skilvull-Writing Task

# **Unix Command Line**
Unix command line adalah tool untuk kita berinteraksi dengan komputer dengan hanya menggunakan text (biasa dikenal dengan text interface)

## Shell
Shell merupakan program perintah yang diketikkan melalui keyboard dan menyampaikannya kepada sistem operasi untuk diproses.

## Command Line interface
CLI atau yang dikenal dengan Command Line Interface adalah suatu program yang akan memerintahkan suatu komputer untuk melakukan tugasnya dengan inputan teks dan akan menampilkan suatu informasi berupa teks juga.

## Mengakses CLI dan Penggunaan Terminal
Cara mengakses CLI pada setiap sistem operasi berbeda contohnya pada sistem operasi pada Windows kita bisa menggunakan yang namanya CMD atau command prompt sedangkan pada sistem operasi Linux kita bisa menggunakan yang namanya Shell hanya saja pada linux dinamakan Shell Bash tapi pada dasarnya sama saja.

Ada beberapa cara menggunaka terminal di sistem operasi windows, antara lain:
- Dengan membuka aplikasi terminal di start
- Dengan membuka run dan ketik cmd
- Dengan membuka folder lalu klik kanan lalu pilih " open in terminal "

## Menambahkan File
Kita dapat membuat file kosong dengan cara mengetik pada terminal '' **touch file_name** ''. Contohnya seperti :
```
$ touch athif.txt
```
## Menampilkan Sebuah Konten
Kita dapat menampilkan konten dari sebuah file dengan command " **cat file_name** ". Contohnya seperti :
```
$ cat athif.text
```

## Membuat Direktori
Direktori atau biasa yang disebut dengan folder dapat dibuat melalui command line dengan cara " **mkdir file_name** ". Contohnya seperti :
```
$ mkdir alya
```

## **Struktur File** 
## Berpindah Diantara File
Saat kita menggunakan komputer, pasti struktur file kita sangat banyak, dengan menggunakan command line kita dapat berpindah file ke file lainnya. Dengan menggunakan command " **cd** " maka dapat berpindah pada suatu file/direktori secara spesifik. Contohnya seperti:
```
$ cd alya
```

## Memeriksa Direktori Saat Ini
Saat kita menggunakan command line, sangatlah penting untuk mengetahui posisi direktori di mana kita bekerja. Untuk mengeceknya sangatlah mudah kita bisa menggunakan:
```
$ pwd
```

## Menampilkan Konten/Daftar File
Pada proses berpindah direktori akan sangat mudah apabila kita dapat melihat daftar file pada direktori saat ini. Untuk melakukannya anda bisa mengetik command:
```
$ ls
```

## Direktori Induk
Kita sudah mengerti cara menggunakan cd untuk berpindah diantara direktori, namun kita belum mengetahui cara untuk berpindah ke direktori induk kembali. Kita dapat menggunakan simbol khusus " **..** ", seperti " **cd ..** ". Contohnya seperti:
```
alya $ cd .. 
skilvul $ 
```

## Direktori Awal
Jika kita menggunakan command " **cd** " tanpa menetapkan sebuah direktori, maka kita akan dikembalikan pada direktori awal/home. Hal ini ditandakan seperti:
```
alya $ cd
~ $ 
```

## **Mengelola File Direktori**
## Memindahkan File dan Direktori
Kita dapat memindahkan file yang ada di sebuah folder ke dalam folder lainnya. Caranya sangat mudah kita bisa menggunakan command " **mv file_yang_ingin_dipindahkan direktori_tujuan** ". Contohnya seperti
```
$ mv athif.txt alya
```

## Mengganti Nama File dan Direktori
Command mv selain untuk memindahkan file dapat juga digunakan untuk mengubah nama file dan direktori caranya " **mv NamaFileLama NamaFileBaru** ". Contohnya seperti:
```
$ mv athif.txt pacarAlya.txt
```

## Menyalin File dan Direktori
Kita dapat menyalin sebuah file di dalam folder dengan menggunakan command " **cp NamaFileYangDisalin NamaFileBaru** ". Contohnya seperti :
```
alya $ pacarAlya.txt sayangAlya.txt
```

## Menghapus File dan Direktori
Selain dapat menyalin kita juga dapat menghapus suatu file dengan menggunakan command " rm NamaFile ". Contohnya seperti:
```
alya $ rm sayangAlya.txt
```


# **Git & Github**
## Kenapa harus Git dan Github?
Saat kita membuat website, kemungkinan besar akan berkolaborasi dengan orang lain pada proses project nanti untuk hal ini diperlukan suatu tools yang berguna dan memudahkan kita berkolaborasi dengan orang lain.

**Git** adalah tool yang memudahkan Anda untuk melakukan pengembangan dan berkolaborasi dengan tim selain itu kegunaan git adalah suatu kendali sistem yang terdistribusi yang artinya semua riwayat code kita akan terekam dengan jelas setiap kita melakukan perubahan, pembuatan branch, dan penggabungan. 

**Github** adalah suatu website layan berbasis cloud untuk para developer mengelola dan mengubah code mereka serta melakukan perubahan yang dapat dikontrol yang artinya Github merupakan suatu platform untuk kita bekerjama sama dengan developer lainnya.

## Bagaimana alur proses dalam penggunaan Git?
Alur menggunakan git ada yang harus dilalui, antara lain:
1. Kita harus membuat sebuah repository terlebih dahulu.
2. Setelah meng-create repo server, selanjutnya adalah membuat clone repo untuk tim lain agar dapat berkolaborasi dengan repo yang sama.
3. Selanjutnya kita bisa melakukan code add, edit, delete, dll untuk proses pengerjaan proyeknya, tergantung kebutuhan masing-masing.
4. Setelah melakukan code di atas, jangan lupa untuk dicommit dan berikan suatu message agar apa yang telah dikerjakan jelas serta diketahui dengan tim lainnya.
5. Setelah kita commit kita bisa push untuk mengunggah file ke remote.
6. Setelah salah satu orang melakukan code push maka tim lainnya dapat mengunduh dengan cara melakukan code pull.
7. Alur simplenya antara lain : Add -> Commit -> Push -> Pull.

## Inisialisasi Git
Untuk pertama kali git harus kita inisialisasi, caranya gampang cukup mengetik:
``` 
$ git init
```

## Memilih File
Jika anda sudah membuat suatu file selanjut kita dapat memilih file untuk dibagikan dengan cara:
```
$ git add NamaFile
```

## Menyimpan File Perubahan
Jika sudah memilih file yang diubah maka kita harus menyimpan file tersebut, dengan menambahkan suatu pesan agar tidak membingungkan tim lainnya. Menyimpan perubahan ini biasa disebut dengan commit, caranya:
```
$ git commit -m "Pesan"
```
## Menambah Remote Repository
Git menggunakan remote (remote repository) untuk menyimpan file yang akan dibagikan. Developer melakukan mengunduh dan mengunggah file dari remote dalam proses berbagi. Kita dapat melakukannya dengan cara:
```
$ git remote add RemoteName UrlRemote
```
## Mengunggah File
Kita dapat mengunggah file yang sudah kita commit dengan cara:
```
$ git push -u origin main/master
```

## Mengunduh File 
Setelah salah satu pengembang mengunggah file ke remote kita harus mengunggah file tersebut dengan cara:
```
$ git pull origin main/master
```

## Cloning Github ke Local
Kita dapat mengeclone suatu repository ke file local di dalam komputer kita, salah satu caranya adalah kita dapat menggunakan git clone. Pertama kita bisa membuka direktori atau folder yang kita inginkan untuk menyimpan clone reponya. Setelah dibuka kita bisa menggunakan git bash lalu ketik code:
```
$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```

# **HTML**


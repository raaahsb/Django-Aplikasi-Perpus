## NAMA : Sahara Hasibuan
## NIM  : 20.01.013.067
## MK   : Pemrograman Mobile
#
# RANGKUMAN PLAYLIST DJANGO
Django merupakan salah satu web framework yang menggunakan bahasa pemrograman python, django berbasis MVT adalah kependekan dari Model, View, dan Template. Pengertian Web framework adalah sebuah tools yang berguna untuk memudahkan programmer ketika membuat aplikasi berbasis web.

## Apa itu MVT ?
Jika biasanya sebuah framework itu berbasis MVC (Model View Controller), pada djanggo ini aga sedikit berbeda yaitu menggunakan model MTV dimana pengertian dari MTV adalah sebagai berikut :
1. Model, merupakan bagian yang berfungsi untuk melakukan iteraksi dengan basis data.
2. View, merupakan bagian yang memuat logika biasanya digunakan untuk mengolah data dari model kemudian dapat dikirimkan ke dalam Template.
3. Template, merupakan bagian yang berfungsi untuk mengatur tampilan dalam bentuk XML atau HTML

## Ada beberapa skill dasar yang diperlukan untuk belajar Django seperti :
1. Memahami Python
2. Memahami Konsep OOP / PBO
3. Memahami Query SQL
4. Mengerti HTML

## Peralatan Yang Dibutuhkan Belajar Django
1. CMD / Terminal Berfungsi untuk menginstall Django, membuat project, menjalankan
server, dll
2. Text Editor (VSCode) Untuk menulis kode program
3. Web Browser Untuk menampilkan Aplikasi web yang telah dibuat
4. Install Python
5. PIP adalah sebuah tool yang akan kita gunakan untuk manajemen paket python. Termasuk juga menginstall Django. 

## MEMBUAT PROJECT APLIKASI PERPUSTAKAAN
1. cd Desktop / #Untuk menyimpan Project di Halaman Desktop
2. Django-admin startproject perpus #Perintah ini untuk membuat Project baru Bernama Perpus
3. Didalam Folder Project Perpus terdapat :
  -Manage.py #Ini adalah file Perintah untuk berinteraksi dengan Project Django
  - __init__.py #Untuk memberitahukan Python bahwa Perpus adalah sebuah Package
  - Setting.py #Berisikan File Konfigurasi / Pengaturan seperti Konfigurasi Template, Database, dll
  - Urls.py #Berisikan pola – pola URL
  - Wsgi.py #Untuk development Project yang melibatkan Web server yang kompetibel dengan Wsgi / Mengonline-kan Project
4. Python manage.py runserver #Untuk menjalankan Project dan mendapatkan alamat Project Django yang akan dibuat

## Apa Itu Basic Routing
1. Client memberikan Request untuk mengakses Halaman Buku pada Server Django namun
PAGE NOT FOUND. Karena URL Buku yang di Request belum ada di Server.
2. Untuk dapat melayani Request dari Client, harus dibuatkan URL baru
3. Jika sudah, maka Request dari Client akan dapat terpenuhi

## Membuat Apps
Apps adalah sebuah aplikasi pada Django yang mempunyai Model Database, View, Template, dan URLCons. Setiap Project di Django mempunyai Apps dan bisa lebih dari satu
Apps

## Membuat Views
Alur yang digunakan untuk membuat Views ini adalah Client, URLConf, View dan memberikan Response kepada Client. Views diciptakan untuk memenuhi Request dari Client. 

## Template
1. Pada tahap ini, Alur yang digunakan mulai berkembang. Dimulai dari Client, URLConf, View, dan Template.
2. Pada bagian Settings.py Line 58. Tambahkan ‘DIRS’ : [‘template’]
3. Buat Folder templates satu Level dengan settings, lalu buiat buku.html
4. Membuat HTML sederhana 

## Template Extending
Pada tahap ini, kita akan membuat Base Template / Template dasar untuk semua Halaman.
2. Template utama yang isinya Base.html adalah file html utama yang akan menampung
konten – konten dari Template Apps
3. Didalam Apps akan dibuat folder template yang isinya hanya bagian – bagian konten
4. Bagian Konten akan diextend / dimasukkan kedalam Base.html

## Static File
Static File adalah kumpulan File CSS, Java Script, dan gambar. Static File ini digunakan untuk mempercantik / memperindah tampilan Aplikasi yang dibuat dan memerikan pengalaman kenyamanan saat Aplikasi digunakan.

## Setup Bootstrap
1. Tahap ini cukup mudah dilakukan karena kita hanya perlu memindahkan file – file CSS
dan Java Script kedalam Folder static yang telah di Set Up.
2. Download Bootstrap dan JQuery yang akan digunakan.
3. Selanjutnya panggil file – file tersebut di Base.html

## Setup DataBase
1. Secara default Django menggunakan Mysql dengan nama 'data.sql'. Ini bisa di Rename sesuai dengan keinginan kita seperti ‘perpustakaan.sql’
2. Pada saat pertama kali melakukan Runserver, ini akan mengcreate database saja tidak termasuk tabel – tabel nya database
3. Selanjutnya dilakukan Migrasi dilakukan untuk menyebarkan / menginisialisasi tabel – tabel kedalam db.sqlite3 terhadap database project yang akan dibuat.
4. Jika berhasil melakukan Migrasi, maka akan tampil seperti dibawah ini

## Setup Mysql
1. Pada tahap ini, melakukan Konfigurasi MySql sebagai DBMS untuk project Django yang akan dibuat.
2. Tahap ini bersifat Opsional, bisa tidak digunakan jika ingin menggunakan sqlite3 sebagai DBMS
3. Jika ingin menggunakan MySql sebagai DBMS, selanjutnya install MySql Installer
4. Jika berhasil diinstall, selanjutnya buka MySql Command Line lalu create Database
5. Konfigurasikan Database ke settings.py

## Model
  Models merupakan definitive dari database atau representasi tabel pada database. Dengan menggunakan models ini, kita tidak perlu lagi menggunakan Query SQL untuk membuat tabel di database.
  Ketika melakukan Migrasi pada model buku, maka Django akan melakukan Create Tabel Buku sesuai dengan field – field yang ada pada model buku ini. Maka jadilah Tabel pada Database yaitu Tabel Buku.

## Foreign Key
1. Foreign Key digunakan untuk membuat Relasi antar tabel dalam database Relational.
2. Kelompok_id merupakan Foreign Key yang nanti nya akan diisi oleh id tabel kelompok

## Django Admin
  Django Admin merupakan salah satu fitur yang powerfull yang ada pada Django. Dikatakan Powerfull karena dapat melakukan CRUD sederhana untuk mengelola data pada
model yang kita buat. Model – Model yang kita buat akan ditambahkan kedalam Django Admin. Django admin ini bersifat Private karena diperlukan Login terlebih dahulu untuk dapat mengakses nya. Django admin Sederhana namun sangat membantu. Pertanyaannya ada dua :
1. Bagaimana cara kita log in django admin ini?
2. Bagaimana model-model kita di daftarkan ke dalam django admin ini?
Sebenarnya saat kita membuat projek ada URL yang sudah dibuatkan oleh djangonya yaitu admin, URL inilah untuk mengakses django admin, apabila ingin akses langsung /admin tampilannya langsung django admin log in. Lalu buat akun buka terminal buat username nya dengan nama admin, lalu email addres, dan password 2 kali. Jalankan kembali servernya jika sudah membuat akun. Akun tersebut di masukkan ke dalam log in. Apabila sudah masuk ke dalam akun selanjutnya kita menampilkan model yang sudah kita buat di dalam django admin. Lalu save, model-model yang kita sudah buat sudah masuk sudah terdaftar. Perpustakaan adalah nama X nya, Buku dan kelompok adalah model nya. Power fullnya terdapat di tombol add kalau di klik akan menampilkan ada sebuah form untuk menambahkan data dalam Buku, kita hanya membuat kelas model saja di datakan di dalam django admin. Mengisi judul,penulis,penerbit,jumlah,dan kelompok id dengan mengisi nama dan keterangan dan save. Ini udah termasuk ke database. Kita buka lagi di model kelompok yang sudah terdapat 3 kelompok seperti adaptif,normatif,dan produktif. 
  
## Model Admin
Pada tahap ini, kita akan melakukan custom sederhana terhadap tampilan data buku, fill-fill apa saja yang ditampilkan sebagai informasi seperti judul,penulis,penerbit dan lain-lain. Kita akan menampilkan kotak pencarian dan filter kelompok buku.

## ORM (Object Relational Mapping)
ORM (object relational mapping) merupakan teknik yang digunakan dalam pemrograman untuk menggunakan basis data relasional sebagai penyimpanan data dengan bentuk objek. Perlu diketahui django menggunakan teknik ini untuk menggunakan database relasional.
Kenapa? Agar kode python yang ditulis tidak campur aduk dengan query sql. Jadi, ORM ini bertugas sebagai penghubung aplikasi yang dibuat menggunakan database relasional.

## Model form
1. Form biasanya ditulis dengan HTML. Namun di Django tidak wajib menggunakan HTML, bisa saja menggunakan Models
2. Input Type harus disesuaikan dengan Type data pada tabel database.
3. Selanjutnya Membuat file baru di perpustakaan dengan nama form. Lalu membuat viewsnya untuk menghasilkan seperti gambar dibawah ini

## Form Widged
1. Pada tahap ini, kita menambahkan atribut dengan menggunakan widged pada output yang telah dibuat sebelumnya.
2. Didalam forms.py ditambahkan widgets, text Input merupakan typenya.
3. Tambahkan atribut kelas didalamnya.

## CRUD : Menambah Data
1. Pada tahap ini, kita masuk ke dalam queryset. Disini kita menambah data, menampilkan, mengubah dan mengapus data Dari data yang sudah dibuat.
2. Selanjutnya kita akan menyimpannya ke dalam database. Prosesnya ada di views yang nantinya akan mengecek apakah data yang di submit oleh user sudah benar atau sudah valid.
3. Apabila sudah maka akan di simpan ke database.
4. Lalu buka text editor, buka file views. Fungsi dari csrf sendiri adalah untuk mngamankan form yang dibuat.

## CRUD : Menampilkan Data
1. Menampilkan data buku yang sudah dibuat, seperti menampilkan nilai 90/100 danmenampilkan kelompok seperti produktif maka hasilnya pasti error karena kelompok_id merupakan type integer.
2. Namun Apabila menambah __nama, maka akan bisa mengeluarkan hasilnya.
3. Penggunaan queryset tidak sepanjang query. Untuk menampilkan limit pada queryset cukup ditambah diujungnya [:3], sedangkan dalam query limit 3.

## CRUD : Mengubah Data
1. Tahap Mengubah data ini perannya sangat penting karena saat kita salah dalam melakukan input data, maka kita harus mengubahnya atau mengeditnya dengan menggunakan fitur update atau fitur ubah data ini. Ini lebih efektif dibandingkan dengan hapus, lalu input ulang
2. Ubah data sebenarnya sama dengan form menambah data. Bedanya form ubah data sudah terisi oleh data yang ingin kita ubah, misalnya seperti ingin mengubah judul yang dari Bhs.Indonesia menjadi IPA, lalu klik simpan dan selesai. 

## CRUD : Hapus Data
1. Hapus data juga penting dalam aplikasi, karena apabila data tersebut tidak lagi digunakan kita dapat menghapus nya. Karena Fungsi fitur ini sendiri adalah untuk menghapus data yang sudah tidak digunakan oleh user.
2. Sebelum menggunakan action/aksi hapus, terlebih dahulu membuat konfirmasi yang berisi apakah yakin ingin menghapus atau tidak untuk menghindari ketidaksengajaan user dalam menghapus data.

## Login / LogOut
Authentication merupakan proses verifikasi/validasi identitas user yang terdaftar sebelum mengakses system. Dengan ini kita jadi bisa membatasi user mana saja yang boleh manambah data, mengubah data, dan menghapus data. Jadi tidak sembarang user mengakses halaman-halaman tersebut . django ada system authentication yang akan kita gunakan yang bernama class LoginView untuk membuat namanya sama seperti membuat log in django admin. Berarti saat ingin membuat yang baru bisa mambuat di terminal.

## Sign Up
Pada tahap ini kita akan membuat form sign up, agar user bisa login ke aplikasi perpustakaan yang dibuat. Tahap ini berhubungan dengan django admin karena di dalamnya terdapat username django adminnya. Jika lihat di dokumentasi resmi Django, ada sebuah user form yang bernama UserCreationForm untuk membuat user baru

## Upload & export File
Pada tahap ini kita membuat tools upload file, seperti mengupload cover buku. Kita akan menambahkan file baru pada model buku yang bernama cover sehingga di dalam tambah buku nanti akan muncul yang baru seperti cover atau muncul di ubah buku. Di buku kita akan menambahkan kolom baru yaitu cover sebagai informasi buku yang kita masukkan.

Pada tahap ini akan membuat export file. Export file ini biasa digunakan untuk membuat report atau laporan ke dalam bentuk file excel, pdf, atau file lainnya. Dalam aplikasi biasanya terdapat fitur laporan yang harus di export data yang terdapat dalam database ke dalam file excel contohnya. Cara menggunakan export ini bisa menggunakan django-importexport.

## Virtual Environment
Pada tahap ini akan membahas tentang virtual environment atau lingkungan virtual, dalam kasus ini lingkungan virtual berguna untuk mengisolasi projek yang kita buat. Setiap kita membuat projek didalam lingkungan virtual ini, projek tersebut akan terisolasi dari direktori system dan memiliki paket python sendiri yang terinstal di lingkugan virtual tersebut. Lingkungan system operasi lebih besar yang didalam nya sudah ada django versi 2.2.12,pillow versi 7.1.2, dan django-import-export versi 2.2.0. kita juga sudah membuat aplikasi perspustakaan di lingkungan system tersebut dengan menggunakan django versi 2.2.12. apabila kita membuat projek di dalam lingkungan virtual environment 1 dan virtual environment 2. Di dalam virtual env 1 terdapat aplikasi perpustakaan yang dibangun dengan django 1.11 sedangkan di dalam virtual env 2 terdapat juga aplikasi yang dibangun dengan django 3.0.8 mysqlclient.

## Persiapan deploy
Deployment adalah kegiatann untuk menyebarkan aplikasi yang telah dikerjakan oleh developer (pengembang). Artinya kita mempublish projekk atau aplikasi yang kita buat untuk dilihat oleh ornang lain. Kita juga melewati siklus pembuatan aplikasi yaitu :
a. Development : mengerjakan projek aplikasi kita atau proses pembuatan, pengembangan . kita di awal-awal akan membuat form,model,view,tampilan itu adalah tahapan development atau pengembangan.
b. Testing : setelah dilakukan pembuatan otomatis kita akan melakukan uji coba agar mengetahui kekurangan dari kegiatan tersebut. Mengecek apakah sudah sesuai atau apakah ada bug. Testing ini juga dilakukan saat production.
c. Production : aplikasi kita yang sudah di buat sudah di deploy / sudah bisa di publish / sudah bisa digunakan oleh orang lain. Bisa juga user melakukan testing pada saat tahap ini. 
Alur kerja nya dari client yang melakukan request langsung ditangani oleh web server lalu ke wsgi lalu terakhir ke django atau perputaran yang sudah kita buat yaitu aplikasi perpustakaan tersebut.
  Yang perlu disiapkan adalah app (github,writelab,perpus), terminal, server, domain
  
## Deployment
Pada tahap ini, kita akan mendeploymen aplikasi yang telah dibuat ke server. Dengan awalan mengcoding di local lalu mengupload ke github lalu di clon atau ditarik ke computer server untuk dideploy disana.
Saat aplikasi kita dalam mode production disetting dan debug masih nilainya masih dalam true jadi kalau misalkan salah menuju ke halaman pasti akan eror . Saat kita dalam mode production kita tidak boleh dibiasakan mengubah tampilan saat mode dalam production, apabila terjadi eror akan berakibat fatal maka itu kalau kita ingin mengambangkan aplikasi yang dalam production kita hanya perlu mengembangkannya di local dan kita masuk ke tahap development atau tahap pengembangan lagi seperti mengubah tampilan atau menambah fitur yang diinginkan. 

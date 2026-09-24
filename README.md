# 💍 Sistem Manajemen Wedding Organizer

## Houry Do Wedds

#### Alya Hauranisa Nugroho | 2509116005 | Sistem Informasi A 2025

#### Mata Kuliah: Pemrograman Berorientasi Objek

---

## Deskripsi Program

Sistem Manajemen Wedding Organizer merupakan program berbasis bahasa pemrograman Java yang digunakan untuk mengelola data pada usaha Wedding Organizer "Houry Do Wedds" secara sederhana.

Program ini dibuat dengan menerapkan konsep Object Oriented Programming atau OOP, serta fitur fitur sederhana yang mendukung CRUD yang meliputi _Create, Read, Update, Delete_. Program ini memungkinkan pengguna untuk mengelola dan mencatat informasi seperti pada data pelanggan, paket wedding, pemesanan wedding, serta vendor.

---

## Struktur Package, Class, dan MVC sebagai Nilai Tambah

<img width="503" height="464" alt="image" src="https://github.com/user-attachments/assets/8c88af55-4520-4904-95b4-7084dd271c73" />

Program Sistem Manajemen Wedding Organizer, setiap class disusun dalam beberapa package yang menerapkan struktur MVC, yaitu _Model_, _Controller_, dan _View_ yang saya terapkan untuk nilai tambah. Setiap package memiliki fungsi dan classnya masing masing, diantaranya:

---

### Package `com.mycompany.weddingorganizerminpro2` sebagai Main
Package ini merupakan package utama yang berisi class WeddingOrganizerMinpro2.java sebagai _entry point_program melalui method main().

#### 1. `WeddingOrganizerMinpro2.java`

Class ini merupakan class utama yang menjadi *entry point* program. Class ini digunakan untuk menjalankan program dan menampilkan menu utama.

Menu utama pada program ini terdiri dari:

1. Tambah
2. Tampilkan
3. Update
4. Hapus
5. Keluar >>>

---

### Package `model` sebagai Model
Package ini merupakan bagian Model dalam penerapan struktur  MVC. Model berfungsi untuk menyimpan dan mengelola data yang digunakan dalam Sistem Manajemen Wedding Organizer. Setiap class di dalam package ini mewakili objek yang ada dalam sistem dan memiliki atribut serta method untuk mengelola datanya. Class yang terdapat dalam package ini, diantaranya:

#### 1. `Pelanggan.java`

Class ini merupakan class data yang merepresentasikan pelanggan yang melakukan pemesanan pada Wedding Organizer.

Atribut yang digunakan meliputi:

* `idPelanggan`
* `nama`
* `noHp`

#### 2. `PaketWedding.java`

Class ini merupakan class data yang merepresentasikan paket wedding yang tersedia.

Atribut yang digunakan meliputi:

* `idPaket`
* `namaPaket`
* `harga`

#### 3. `PemesananWedding.java`

Class ini merupakan class data yang merepresentasikan data pemesanan wedding.

Atribut yang digunakan meliputi:

* `idBooking`
* `pelanggan`
* `paketWedding`
* `venue`
* `tanggalAcara`
* `pax`

#### 4. `Vendor.java`

Class ini merupakan superclass yang digunakan sebagai class induk untuk jenis-jenis vendor yang diolah pada Wedding Organizer.

Class ini menyimpan atribut umum yang dimiliki oleh setiap vendor, yaitu:

* `idVendor`
* `namaVendor`
* `noTelepon`

Atribut dan method umum yang terdapat dalam class ini kemudian akan digunakan oleh subclass yang mewarisi class `Vendor`.

#### 5. `VendorCatering.java`

Class ini merupakan subclass atau class anak yang mewarisi sifat dari dari class `Vendor`. Class ini mewarisi informasi umum vendor dari superclass dan memiliki atribut tambahan yang khusus digunakan untuk vendor catering, yaitu:

* `jenisMasakan`
* `sistemPenyajian`
* `hargaPerPax`

#### 6. `VendorDekorasi.java`

Class ini merupakan subclass atau class anak yang mewarisi sifat dari dari class `Vendor`. Class ini mewarisi informasi umum vendor dari superclass dan memiliki atribut tambahan yang khusus digunakan untuk vendor dekorasi, yaitu:

* `temaDekorasi`
* `jenisDekorasi`
* `hargaPaketDekorasi`

---

### Package `controller` sebagai Controller

Package ini merupakan bagian Controller dalam penerapan struktur MVC. Controller berfungsi untuk mengatur alur program dan menghubungkan antara Model dengan View. Package ini berisi class yang menangani operasi CRUD serta validasi input dari pengguna sebelum data diproses. Class yang terdapat dalam package ini diantaranya:

#### 1. `WeddingCRUD.java`

Class ini merupakan class yang menangani seluruh proses utama CRUD pada program.

Data yang dikelola pada class ini meliputi:

* Pelanggan
* Paket Wedding
* Pemesanan Wedding
* Vendor

Pada class ini, ditambahkan juga ArrayList dan data _dummy_ untuk setiap data yang dikelola pada Sistem Manajemen Wedding Organizer.

#### 2. `InputValidator.java`

Class InputValidator digunakan untuk membantu memvalidasi input yang dimasukkan oleh pengguna agar sesuai dengan format yang dibutuhkan program. Class ini memiliki beberapa method, yaitu:

* bacaInt(), yaitu method yang berfungsi membaca dan memvalidasi input berupa angka.
* bacaPilihan(), yaitu method yang berfungsi untuk membaca pilihan menu dari pengguna.
* bacaTeks(), yaitu method membaca dan memvalidasi input berupa teks.

---

### Package `view` sebagai View

Package ini merupakan bagian View dalam penerapan struktur MVC. View berfungsi untuk menampilkan informasi kepada pengguna. Package ini mengatur tampilan menu dan pesan yang muncul saat program dijalankan. Class yang terdapat dalam package ini, di antaranya:

#### 1. `Menu.java`

Class ini digunakan untuk menampilkan menu yang terdapat pada program, baik menu utama maupun submenu yang ada didalamnya. Class ini memiliki beberapa method yang digunakan untuk tampilan program, yaitu:

* tampilkanMenuUtama()
* tampilkanMenuTambah()
* tampilkanMenuTampilkan()
* tampilkanMenuUpdate()
* tampilkanMenuHapus()
* tampilkanMenuJenisVendor()

#### 2. `Pesan.java`

Class ini digunakan untuk menampilkan pesan kepada pengguna, seperti pesan berhasil, pesan kesalahan, atau informasi lainnya selama program berjalan. Pada class ini terdapat method tampilkanPesan() yang digunakan untuk menampilkan pesan dengan format "> [ pesan ] <".


---

## Penerapan Encapsulation

<img width="476" height="129" alt="image" src="https://github.com/user-attachments/assets/20a36d1b-129c-4073-b2fb-5937629edaf9" />

Pada program ini, saya menerapkan konsep encapsulation dengan menyembunyikan atribut menggunakan access modifier private, lalu menyediakan method getter dan setter sebagai jalur akses untuk membaca atau mengubah data. Konsep encapsulation saya terapkan pada seluruh class data pada model. Hal ini bertujuan agar data dalam object tidak dapat diakses atau diubah secara langsung dari luar class.

Sebagai contoh, pada class PaketWedding terdapat beberapa method berikut:

<img width="443" height="306" alt="image" src="https://github.com/user-attachments/assets/0ec01a73-2fc4-4af3-9a07-988e424a7045" />

Pada gambar di atas digunakan method getter, yaitu getIdPaket(), getNamaPaket(), dan getHarga(), digunakan untuk mengambil nilai atribut idPaket, namaPaket, dan harga.

<img width="987" height="202" alt="image" src="https://github.com/user-attachments/assets/5fb83b6b-fe46-4c61-893e-11f28170b762" />

Selain menerapkan getter, saya juga menerapkan method setter yaitu setHarga() yang digunakan untuk mengubah nilai atribut harga. Pada method setHarga(), saya juga menambahkan validasi data jika nilai harga yang dimasukkan kurang dari atau sama dengan 0, maka akan menampilkan pesan seperti pada gambar di atas.

---

## Penerapan Inheritance

Pada program ini, saya menerapkan konsep inheritence dengan menjadikan class Vendor sebagai superclass atau class induk dari subclass VendorCatering dan VendorDekorasi.

Atribut yang bersifat umum seperti ID vendor, nama vendor, dan nomor telepon ditempatkan pada superclass Vendor. Kedua subclass kemudian mewarisi atribut dan method tersebut serta menambahkan atribut khusus sesuai dengan jenis vendornya. Penerapan inheritance bertujuan agar atribut dan method yang sama tidak perlu ditulis kembali pada masing-masing subclass, sehingga dapat digunakan untuk efisiensi. Penerapan inheritence pada class VendorCatering dan VendorDekorasi digunakan untuk mengelola data vendor berdasarkan jenisnya.

Implementasi inheritance pada kode dapat dilihat pada gambar berikut:

<img width="1724" height="314" alt="image" src="https://github.com/user-attachments/assets/85a24a50-5dfd-4c35-adc2-778cbe1aa6f6" />

<img width="1188" height="344" alt="image" src="https://github.com/user-attachments/assets/ceabd1a2-747c-4f69-8e75-87b569fb2702" />


Pada gambar di atas, diketahui bahwa konsep inheritance diterapkan pada VendorCatering dan VendorDekorasi yang merupakan subclass dari Vendor menggunakan keyword extends. Class Vendor sebagai superclass menyimpan atribut umum, sedangkan kedua subclass menambahkan atribut khusus sesuai dengan jenis vendor. Keyword super() juga digunakan untuk untuk menginisialisasi atribut yang diwarisi dari Vendor. Pada jenis vendor catering, terdapat atribut tambahan seperti jenisMasakan, sistemPenyajian, dan hargaPerPax. Sementara pada jenis vendor dekorasi, terdpat atribut tambahan seperti temaDekorasi, jenisDekorasi, dan hargaPaketDekorasi. Pada constructor digunakan super() untuk menginisialisasi atribut yang diwarisi dari Vendor.

---

## Penerapan Polymorphism, sebagai Nilai Tambah

Pada program ini saya menerapkan polymorphism melalui overriding, yaitu subclass memberikan implementasi yang berbeda pada method yang sudah dimiliki oleh superclass Vendor. Overriding digunakan karena setiap jenis vendor memiliki kebutuhan dan perilaku yang berbeda, meskipun menggunakan method yang sama.

Implementasi polymorphism pada kode dapat dilihat pada gambar berikut:

<img width="857" height="643" alt="image" src="https://github.com/user-attachments/assets/b914ab33-15d9-459b-8d9d-ea94396ec014" />


<img width="970" height="623" alt="image" src="https://github.com/user-attachments/assets/9bdbcf59-5a0e-4969-9340-2811c8a004a3" />

Pada method getJenisVendor(), overriding diperlukan karena setiap subclass memiliki jenis vendor yang berbeda. VendorCatering mengembalikan Catering, sedangkan VendorDekorasi mengembalikan Dekorasi.

Pada method getHarga() dan setHarga(), overriding digunakan karena setiap jenis vendor memiliki atribut harga yang berbeda. VendorCatering menggunakan hargaPerPax, sedangkan VendorDekorasi menggunakan hargaPaketDekorasi. Dengan begitu, method yang sama dapat mengambil dan mengubah harga sesuai dengan jenis vendor.

Pada method tampilkanInfo(), overriding digunakan karena informasi yang perlu ditampilkan pada setiap jenis vendor berbeda. VendorCatering menampilkan informasi seperti jenis masakan dan sistem penyajian, sedangkan VendorDekorasi menampilkan tema dan jenis dekorasi. Method super.tampilkanInfo() tetap digunakan untuk menampilkan informasi umum yang berasal dari superclass Vendor.

---

## Dokumentasi dan Alur Program

Secara umum, alur program dimulai ketika pengguna menjalankan program selanjutnya dan akan diarahkan ke menu utama yang terdiri dari menu Tambah, Tampilkan, Update, Hapus, dan Keluar. Pengguna dapat memilih menu sesuai kebutuhan, kemudian memilih data yang ingin dikelola, yaitu data pelanggan, paket wedding, pemesanan wedding, maupun vendor. 

Apabila pengguna telah menyelesaikan proses CRUD yang dipilih dan memilih menu “Kembali ke Menu Utama”, program akan kembali ke menu utama sehingga pengguna dapat melakukan proses lainnya. Program akan terus berjalan selama pengguna belum memilih menu Keluar.

---

### Menu Utama

<img width="469" height="343" alt="image" src="https://github.com/user-attachments/assets/f6555eb4-c5d0-4b76-98fc-6c57ecea81c4" />

Pada gambar di atas, ditampilkan menu utama dari program Sistem Manajemen Wedding Organizer. Terdapat 5 menu utama yang dapat dipilih, yaitu menu untuk menambahkan data, menampilkan data, menghapus data, mengupdate data, serta menu untuk keluar dari program. Pengguna akan diminta untuk memilih salah satu dari kelima menu tersebut.

---

### 1. Menu Tambah

<img width="476" height="248" alt="image" src="https://github.com/user-attachments/assets/9cc63606-3804-4402-bb8e-315ea4b4f1a3" />

Ketika pengguna memilih “1” pada menu utama, pengguna akan masuk ke dalam Menu Tambah, di mana menu ini memungkinkan pengguna untuk memasukkan data baru pada data pelanggan, paket wedding, maupun pemesanan wedding. Pengguna dapat memilih salah satu jenis data yang ingin ditambahkan sesuai dengan kebutuhan. Pada tampilan tersebut, saya memilih menu “1", "yaitu Tambah Pelanggan”, sehingga program akan melanjutkan ke proses untuk memasukkan data pelanggan.

---

* **Tambah Pelanggan**

<img width="652" height="490" alt="image" src="https://github.com/user-attachments/assets/13fe427f-c92f-4c1d-9636-2b30e41cdf68" />

Selanjutnya, program akan menampilkan tempat untuk memasukkan data pelanggan. Pengguna diminta memasukkan ID Pelanggan, Nama Pelanggan, dan No HP. Setelah seluruh data berhasil dimasukkan, program menampilkan pesan bahwa data pelanggan berhasil ditambahkan, kemudian kembali menampilkan Menu Tambah agar pengguna dapat melanjutkan proses penambahan data lainnya.

Berikut merupakan proses penambahan data lainnya:

* **Tambah Paket Wedding**

<img width="648" height="232" alt="image" src="https://github.com/user-attachments/assets/82385aae-f5c2-4f6f-b81d-499c1bf0b9b4" />

* **Tambah Pemesanan Wedding**

<img width="472" height="574" alt="image" src="https://github.com/user-attachments/assets/03bda7f1-3ce7-4006-b3f8-0ce4747e2179" />

<img width="797" height="871" alt="image" src="https://github.com/user-attachments/assets/0989a8b0-11ab-4780-8a1e-71882967112e" />

* **Tambah Vendor**

<img width="471" height="220" alt="image" src="https://github.com/user-attachments/assets/9e231808-40c2-46a5-9fb7-c2a6f44c5fe6" />

Pada menu Tambah Vendor, pengguna terlebih dahulu memilih jenis vendor yang ingin ditambahkan.

<img width="674" height="227" alt="image" src="https://github.com/user-attachments/assets/94ded310-d2b0-4295-a632-f67653933790" />

Jika memilih vendor catering, pengguna memasukkan data umum vendor serta data khusus catering seperti jenis masakan, sistem penyajian, dan harga per pax.

<img width="668" height="221" alt="image" src="https://github.com/user-attachments/assets/1db7c2b2-4e77-41c1-a017-c2aa20f9d827" />

Jika memilih vendor dekorasi, pengguna memasukkan data umum vendor serta data khusus dekorasi seperti tema dekorasi, jenis dekorasi, dan harga paket dekorasi.

* **Kembali ke Menu Utama**

<img width="474" height="630" alt="image" src="https://github.com/user-attachments/assets/771162d4-f782-4354-a346-5e72c7cef961" />

Apabila telah menyelesaikan proses _create_, pengguna dapat memilih menu "5" untuk keluar dari Menu Tambah dan kembali ke Menu Utama.

---

### 2. Menu Tampilkan

<img width="468" height="248" alt="image" src="https://github.com/user-attachments/assets/9e9402ab-23ce-4d10-abc9-e8e0e652b806" />


Ketika pengguna memilih “2” pada menu utama, pengguna akan masuk ke dalam Menu Tampilkan, di mana menu ini memungkinkan pengguna untuk melihat data yang sudah ada pada data pelanggan, paket wedding, maupun pemesanan wedding. 

---

Berikut merupakan tampilan untuk Menu Tampilkan di setiap data:

* **Tampilkan Pelanggan**

<img width="470" height="338" alt="image" src="https://github.com/user-attachments/assets/6801f89b-bbc0-46aa-b1d8-58b1c8379c7c" />


* **Tampilkan Paket Wedding**

<img width="492" height="670" alt="image" src="https://github.com/user-attachments/assets/567103d8-74d2-4e78-9546-d17188a7679f" />


* **Tampilkan Pemesanan Wedding**

<img width="473" height="306" alt="image" src="https://github.com/user-attachments/assets/6b40f314-e123-4a53-bc8c-96804ce09528" />


* **Tampilkan Vendor**

<img width="473" height="224" alt="image" src="https://github.com/user-attachments/assets/53f50f51-081b-4b12-9963-76cd62d7b0b5" />

Pada menu Tampilkan Vendor, pengguna diminta untuk memilih vendor apa yang ingin dilihat. Pada gambar di atas, diketahui bahwa pengguna dapat melihat semua vendor, vendor catering saja, dan vendor dekorasi saja. Output dari masing masing menu tampilkan adalah sebagai berikut:

1. Tampilkan Semua Vendor

<img width="474" height="907" alt="image" src="https://github.com/user-attachments/assets/655b5659-f397-4eef-a4b5-a854d6bbd7bc" />

3. Tampilkan Vendor Catering

<img width="461" height="469" alt="image" src="https://github.com/user-attachments/assets/a204b304-7029-4d04-9002-9e115b5e8762" />

4. Tampilkan Vendor Dekorasi

<img width="477" height="692" alt="image" src="https://github.com/user-attachments/assets/0e7334eb-97cc-497f-9f87-10db3eca7fec" />


* **Kembali ke Menu Utama**

<img width="470" height="628" alt="image" src="https://github.com/user-attachments/assets/92d959b4-05c8-4713-b8ec-6f5515fffb3c" />

Apabila telah menyelesaikan proses _read_, pengguna dapat memilih menu "5" untuk keluar dari Menu Tampilkan dan kembali ke Menu Utama.

---

### 3. Menu Update

Ketika pengguna memilih “3” pada menu utama, pengguna akan masuk ke dalam Menu Update. Menu ini digunakan untuk mengubah data yang sudah tersimpan pada program. Pengguna dapat memilih data yang ingin diperbarui, yaitu data pelanggan, paket wedding, maupun pemesanan wedding.

<img width="474" height="272" alt="image" src="https://github.com/user-attachments/assets/e5ee7df4-c3f9-4954-bc1b-7c54b1cf398f" />

Pada Menu Update, pengguna dapat memilih salah satu dari 4 jenis data yang tersedia untuk diperbarui. Setelah memilih jenis data, pengguna akan diminta memasukkan ID dari data yang ingin diubah. Program kemudian akan mencari data berdasarkan ID tersebut. Apabila data ditemukan, pengguna dapat memasukkan informasi baru sesuai dengan atribut yang dapat diperbarui.

---

Berikut merupakan proses update pada setiap data:

* **Update Pelanggan**

<img width="531" height="225" alt="image" src="https://github.com/user-attachments/assets/a087e433-8374-4fee-a40a-12dba07a002d" />


Pada proses Update Pelanggan, pengguna diminta memasukkan ID pelanggan yang ingin diperbarui. Setelah ID ditemukan, pengguna dapat mengubah nama pelanggan dan No HP. Setelah data berhasil diperbarui, program akan menampilkan pesan bahwa data pelanggan berhasil diupdate.

* **Update Paket Wedding**

<img width="593" height="191" alt="image" src="https://github.com/user-attachments/assets/5a60d5e8-793e-40dc-ae32-ab8738bb404d" />


Pada proses Update Paket Wedding, pengguna diminta memasukkan ID paket yang ingin diperbarui. Setelah paket ditemukan, pengguna dapat mengubah harga paket wedding. Setelah proses berhasil dilakukan, program akan menampilkan pesan bahwa data paket berhasil diupdate.

* **Update Pemesanan Wedding**

<img width="577" height="248" alt="image" src="https://github.com/user-attachments/assets/77a7562b-80d5-499a-942d-aed56aaf90b0" />

Pada proses Update Pemesanan Wedding, pengguna diminta memasukkan ID booking yang ingin diperbarui. Setelah data ditemukan, pengguna dapat mengubah venue, tanggal acara, dan jumlah pax sesuai dengan kebutuhan. Setelah data berhasil diperbarui, program akan menampilkan pesan bahwa data pemesanan berhasil diupdate.

* **Update Vendor**

<img width="629" height="283" alt="image" src="https://github.com/user-attachments/assets/c1047330-b90b-40ab-b684-e5d6ca2ffecb" />

<img width="627" height="278" alt="image" src="https://github.com/user-attachments/assets/afdb6063-5a9e-44c3-bbc7-e7f87b14cc67" />

Pada proses Update Vendor, pengguna diminta untuk memilih jenis vendor yang ingin diperbarui. Apabila pengguna memilih "1", maka pengguna akan diminta untuk memasukkan ID vendor catering untuk mengubah harga per pax dari vendor tersebut. Apabila pengguna memilih "2" maka pengguna akan diminta untuk memasukkan ID dari vendor dekorasi untuk mengubah harga paket dekorasi dari vendor tersebut.

* **Kembali ke Menu Utama**

<img width="480" height="601" alt="image" src="https://github.com/user-attachments/assets/84058989-ffa6-41b6-8bbc-634d4b5874d8" />

---

### 4. Menu Hapus

Ketika pengguna memilih “4” pada menu utama, pengguna akan masuk ke dalam Menu Hapus. Menu ini digunakan untuk menghapus data yang sudah tersimpan pada sistem. Pengguna dapat memilih data yang ingin dihapus, yaitu data pelanggan, paket wedding, maupun pemesanan wedding.

<img width="479" height="278" alt="image" src="https://github.com/user-attachments/assets/3b7a9ff2-d03d-4d41-aeb3-0e3cf2794b50" />

Pada Menu Hapus, pengguna dapat memilih salah satu jenis data yang tersedia. Setelah memilih jenis data, pengguna akan diminta memasukkan ID dari data yang ingin dihapus. Program kemudian akan mencari data berdasarkan ID tersebut. Apabila data ditemukan, data akan dihapus dari daftar penyimpanan.

---

Berikut merupakan proses penghapusan pada setiap data:

* **Hapus Pelanggan**

<img width="471" height="166" alt="image" src="https://github.com/user-attachments/assets/e26bbf15-903a-440f-a0cd-6b9de18b74b5" />

Pada proses Hapus Pelanggan, pengguna diminta memasukkan ID pelanggan yang ingin dihapus. Program akan mencari ID tersebut pada daftar pelanggan. Apabila ID ditemukan, data pelanggan akan dihapus dan program akan menampilkan pesan bahwa data pelanggan berhasil dihapus.

* **Hapus Paket Wedding**

<img width="462" height="163" alt="image" src="https://github.com/user-attachments/assets/91557b55-d901-4f1a-8ca6-695caf75f9f7" />

Pada proses Hapus Paket Wedding, pengguna diminta memasukkan ID paket yang ingin dihapus. Program akan mencari ID tersebut pada daftar paket wedding. Apabila ID ditemukan, data paket akan dihapus dari sistem dan program akan menampilkan pesan bahwa data paket berhasil dihapus.

* **Hapus Pemesanan Wedding**

<img width="492" height="163" alt="image" src="https://github.com/user-attachments/assets/bed7fbb2-88cc-4f17-a6ce-390c9803bc08" />

Pada proses Hapus Pemesanan Wedding, pengguna diminta memasukkan ID booking yang ingin dihapus. Program akan mencari ID booking tersebut pada daftar pemesanan. Apabila ditemukan, data pemesanan akan dihapus dan program akan menampilkan pesan bahwa data pemesanan berhasil dihapus.

* **Hapus Vendor**

<img width="504" height="248" alt="image" src="https://github.com/user-attachments/assets/4cee8013-e17a-44a0-bab4-4d1260d4dc13" />

Pada proses Hapus Vendor, pengguna diminta untuk memilih jenis vendor yang ingin dihapus. Apabila pengguna memilih "1", maka pengguna akan diminta untuk memasukkan ID vendor catering yang ingin dihapus. Apabila pengguna memilih "2" maka pengguna akan diminta untuk memasukkan ID dari vendor dekorasi yang ingin dihapus. Apabila ditemukan, data vendor akan dihapus dan program akan menampilkan pesan bahwa data pemesanan berhasil dihapus.


* **Kembali ke Menu Utama**

<img width="522" height="599" alt="image" src="https://github.com/user-attachments/assets/b039d9a6-bf83-4a40-8707-48032fc2040a" />

Apabila telah menyelesaikan proses _delete_, pengguna dapat memilih menu "5" untuk keluar dari Menu Update dan kembali ke Menu Utama.

---

### 5. Keluar >>>

<img width="545" height="516" alt="image" src="https://github.com/user-attachments/assets/b9ca1bc7-6617-4d37-bc53-8842b47c691d" />


Apabila pengguna telah selesai melakukan pengelolaan data Wedding Organizer, pengguna dapat memilih menu “5” pada menu utama untuk mengakhiri program. Setelah pengguna memilih menu tersebut, program akan menampilkan pesan “BYEEEE!!” sebagai tanda bahwa program telah selesai dijalankan.

---

# 💍 Sistem Manajemen Wedding Organizer

## Houry Do Wedds

#### Alya Hauranisa Nugroho | 2509116005 | Sistem Informasi A 2025

#### Mata Kuliah: Pemrograman Berorientasi Objek

---

## 📌 Deskripsi Program

Sistem Manajemen Wedding Organizer merupakan program berbasis bahasa pemrograman Java yang digunakan untuk mengelola data pada usaha Wedding Organizer "Houry Do Wedds" secara sederhana.

Program ini dibuat dengan menerapkan konsep Object Oriented Programming atau OOP, serta fitur fitur sederhana yang mendukung CRUD yang meliputi _Create, Read, Update, Delete_. Program ini memungkinkan pengguna untuk mengelola dan mencatat informasi seperti pada data pelanggan, paket wedding, pemesanan wedding, serta vendor.

---

## 📂 Struktur MVC dan Class

Program Sistem Manajemen Wedding Organizer, setiap class disusun dalam beberapa package yang menerapkan struktur MVC, yaitu _Model_, _Controller_, dan _View_. Setiap package memiliki fungsi dan class masing masing, diantaranya: terdiri dari beberapa class dengan fungsi yang berbeda, yaitu:

---

### 📦 Package `com.mycompany.weddingorganizerminpro2` sebagai Main
Package ini merupakan package utama yang berisi class WeddingOrganizerMinpro2.java sebagai titik awal program melalui method main().

#### 1. `WeddingOrganizerMinpro2.java`

Class ini merupakan class utama yang menjadi *entry point* program. Class ini digunakan untuk menjalankan program dan menampilkan menu utama.

Menu utama pada program ini terdiri dari:

1. Tambah
2. Tampilkan
3. Update
4. Hapus
5. Keluar >>>

---

### 📦 Package `model` sebagai Model
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

### 📦 Package `controller` sebagai Controller

Package ini merupakan bagian Controller dalam penerapan struktur MVC. Controller berfungsi untuk mengatur alur program dan menghubungkan antara Model dengan View. Package ini berisi class yang menangani operasi CRUD serta validasi input dari pengguna sebelum data diproses.

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

### 📦 Package `view` View

Package ini merupakan bagian Controller dalam penerapan struktur MVC. Controller berfungsi untuk mengatur alur program dan menghubungkan antara Model dengan View. Package ini berisi class yang menangani operasi CRUD serta validasi input dari pengguna sebelum data diproses.

---

## ⭐ Penerapan Encapsulation

Pada program ini, saya menerapkan konsep encapsulation dengan menyembunyikan atribut menggunakan access modifier private dan menyediakan getter serta setter untuk mengakses atau mengubah data tertentu.

Sebagai contoh, pada class Pelanggan terdapat penerapan method getter dan setter:

<img width="453" height="517" alt="image" src="https://github.com/user-attachments/assets/273dd8bf-606c-4172-ba3c-2a3f09745a7a" />


Getter digunakan untuk mengambil nilai dari atribut, sedangkan setter digunakan untuk mengubah nilai atribut. Sehingga akses terhadap data dalam object dilakukan melalui method yang telah disediakan oleh class, sehingga data tidak diakses secara langsung dari luar class.

---

## ⭐ Penerapan Inheritance

Konsep inheritance diterapkan dengan menjadikan `Vendor` sebagai superclass dari `VendorCatering` dan `VendorDekorasi`.

Atribut yang bersifat umum seperti ID vendor, nama vendor, dan nomor telepon ditempatkan pada superclass `Vendor`. Kemudian kedua subclass mewarisi atribut dan method tersebut serta menambahkan atribut yang sesuai dengan kebutuhan masing-masing jenis vendor.

Secara konsep:

```text
Vendor
├── idVendor
├── namaVendor
└── noTelepon
        │
        ├── VendorCatering
        │   ├── jenisMasakan
        │   ├── sistemPenyajian
        │   └── hargaPerPax
        │
        └── VendorDekorasi
            ├── temaDekorasi
            ├── jenisDekorasi
            └── hargaPaketDekorasi
```

Penerapan ini membuat informasi yang sama pada setiap vendor tidak perlu dibuat kembali pada masing-masing subclass.

Pada `WeddingCRUD`, kedua subclass kemudian digunakan untuk menyimpan data vendor sesuai dengan jenisnya. Program menyediakan pilihan vendor catering atau vendor dekorasi ketika pengguna ingin mengelola data vendor.

Implementasi inheritance pada kode saya adalah sebagai berikut:

<img width="1231" height="338" alt="image" src="https://github.com/user-attachments/assets/78efd2d3-e143-46fd-a96e-6b600977e5c9" />

<img width="1241" height="341" alt="image" src="https://github.com/user-attachments/assets/671d9545-d431-4a7e-8fc5-c69937696114" />

Inheritance diterapkan pada `VendorCatering` dan `VendorDekorasi` yang merupakan subclass dari `Vendor` menggunakan keyword `extends`. Class `Vendor` sebagai superclass menyimpan atribut umum seperti `idVendor`, `namaVendor`, dan `noTelepon`, sedangkan kedua subclass menambahkan atribut khusus sesuai jenis vendornya. Pada constructor digunakan `super()` untuk menginisialisasi atribut yang diwarisi dari `Vendor`. Dengan inheritance, kode menjadi lebih sederhana karena atribut dan method yang sama tidak perlu ditulis ulang pada setiap subclass.

---

## ⭐ Penerapan Polymorphism, sebagai nilai tambah

---

## 📸 Dokumentasi dan Alur Program

Secara umum, alur program dimulai ketika pengguna menjalankan program selanjutnya dan akan diarahkan ke menu utama yang terdiri dari menu Tambah, Tampilkan, Update, Hapus, dan Keluar. Pengguna dapat memilih menu sesuai kebutuhan, kemudian memilih data yang ingin dikelola, yaitu data pelanggan, paket wedding, atau pemesanan wedding. 

Apabila pengguna telah menyelesaikan proses CRUD yang dipilih dan memilih menu “Kembali ke Menu Utama”, program akan kembali ke menu utama sehingga pengguna dapat melakukan proses lainnya. Program akan terus berjalan selama pengguna belum memilih menu Keluar.

---

### **Menu Utama**
<img width="472" height="341" alt="image" src="https://github.com/user-attachments/assets/e2ec58d7-0361-4558-8b5e-46fbd85224e4" />

<img width="470" height="326" alt="image" src="https://github.com/user-attachments/assets/4e3910f0-7e09-477f-a1a5-c9cb82d8c35a" />

Pada gambar di atas, saya menampilkan menu utama dari program yang telah dirancang. Terdapat 5 menu utama yang dapat dipilih, yaitu menu untuk menambahkan data, menampilkan data, menghapus data, mengupdate data, serta menu untuk keluar dari program. Pengguna akan diminta untuk memilih salah satu dari kelima menu tersebut.

---

### **1. Menu Tambah**

<img width="480" height="276" alt="image" src="https://github.com/user-attachments/assets/e853f97f-933b-4c7f-8ce2-3ea249087249" />

Ketika pengguna memilih “1” pada menu utama, pengguna akan masuk ke dalam Menu Tambah, di mana menu ini memungkinkan pengguna untuk memasukkan data baru pada data pelanggan, paket wedding, maupun pemesanan wedding. Pengguna dapat memilih salah satu jenis data yang ingin ditambahkan sesuai dengan kebutuhan. Pada tampilan tersebut, saya memilih menu “1", "yaitu Tambah Pelanggan”, sehingga program akan melanjutkan ke proses untuk memasukkan data pelanggan.

---

* **Tambah Pelanggan**

<img width="564" height="432" alt="image" src="https://github.com/user-attachments/assets/9373d943-2d1f-46c4-ac4e-0d91518e7241" />


Selanjutnya, program akan menampilkan tempat untuk memasukkan data pelanggan. Pengguna diminta memasukkan ID Pelanggan, Nama Pelanggan, dan No HP. Setelah seluruh data berhasil dimasukkan, program menampilkan pesan bahwa data pelanggan berhasil ditambahkan, kemudian kembali menampilkan Menu Tambah agar pengguna dapat melanjutkan proses penambahan data lainnya.

Berikut merupakan proses penambahan data lainnya:

* **Tambah Paket Wedding**

<img width="542" height="224" alt="image" src="https://github.com/user-attachments/assets/147a4c5b-e140-4a0b-9fff-0c76b142049d" />

* **Tambah Pemesanan Wedding**

<img width="463" height="362" alt="image" src="https://github.com/user-attachments/assets/2cc31b67-7149-4bb5-a765-a501251e9c0d" />

<img width="706" height="876" alt="image" src="https://github.com/user-attachments/assets/65cdc62c-9d67-49fe-b4c7-614ca256c260" />

* **Tambah Vendor**

<img width="499" height="225" alt="image" src="https://github.com/user-attachments/assets/57d63793-853a-4266-85d7-6c20d8071518" />


Pada menu Tambah Vendor, pengguna terlebih dahulu memilih jenis vendor yang ingin ditambahkan.

<img width="577" height="223" alt="image" src="https://github.com/user-attachments/assets/7798d385-ad96-4c9e-a16e-5cbaa495dfa5" />

Jika memilih vendor catering, pengguna memasukkan data umum vendor serta data khusus catering seperti jenis masakan, sistem penyajian, dan harga per pax.

<img width="584" height="226" alt="image" src="https://github.com/user-attachments/assets/5740952d-53fc-4553-a5f4-80f2eea02f78" />


Jika memilih vendor dekorasi, pengguna memasukkan data umum vendor serta data khusus dekorasi seperti tema dekorasi, jenis dekorasi, dan harga paket dekorasi.

---

Berdasarkan gambar di atas, diketahui bahwa pengguna dapat menambahkan:

* **Pelanggan**, dengan memasukkan ID, nama, dan nomor HP.
* **Paket Wedding**, dengan memasukkan ID, nama paket, dan harga.
* **Pemesanan Wedding**, dengan memilih pelanggan dan paket wedding yang sudah tersedia, kemudian memasukkan venue, tanggal acara, dan jumlah pax.
* **Vendor**, dengan memilih jenis vendornya terlebih dahulu, yaitu vendor catering atau vendor dekorasi, kemudian mengisi data vedor yang dibutuhkan sesuai jenisnya.


* **Kembali ke Menu Utama**

<img width="489" height="599" alt="image" src="https://github.com/user-attachments/assets/f27b7b1f-a20a-4f94-8b22-d1bfe9b17b4f" />


Apabila telah menyelesaikan proses tambah, pengguna dapat memilih menu "5" untuk keluar dari menu tambah dan kembali ke menu utama.

---

### **2. Menu Tampilkan**

<img width="494" height="277" alt="image" src="https://github.com/user-attachments/assets/8465ea91-3a02-4785-b3bc-7a4d0b4752a2" />

Ketika pengguna memilih “2” pada menu utama, pengguna akan masuk ke dalam Menu Tampilkan, di mana menu ini memungkinkan pengguna untuk melihat data yang sudah ada pada data pelanggan, paket wedding, maupun pemesanan wedding. 

---

Berikut merupakan tampilan untuk Menu Tampilkan di setiap data:

* **Tampilkan Pelanggan**

<img width="466" height="213" alt="image" src="https://github.com/user-attachments/assets/6a5c670e-ce87-42a5-818e-132a04b48806" />

* **Tampilkan Paket Wedding**

<img width="480" height="756" alt="image" src="https://github.com/user-attachments/assets/b9631b23-686c-4740-ac43-4ce9df8fe1f5" />

* **Tampilkan Pemesanan Wedding**

<img width="469" height="293" alt="image" src="https://github.com/user-attachments/assets/84801c1a-3880-4d73-8a4c-4f80163d660b" />

* **Tampilkan Vendor**

<img width="484" height="673" alt="image" src="https://github.com/user-attachments/assets/0d1cd904-85e5-44c5-94ca-e15704dd7eaf" />

<img width="496" height="675" alt="image" src="https://github.com/user-attachments/assets/f424a544-0dff-488d-b3a5-ed13d9fe5283" />


* **Kembali ke Menu Utama**

<img width="496" height="601" alt="image" src="https://github.com/user-attachments/assets/23cc5658-367b-465a-8c3b-f3eecff24ff5" />

Pengguna dapat memilih menu "5" untuk keluar dari menu tampilkan dan kembali ke menu utama.

---

### **3. Menu Update**

Ketika pengguna memilih “3” pada menu utama, pengguna akan masuk ke dalam Menu Update. Menu ini digunakan untuk mengubah data yang sudah tersimpan pada program. Pengguna dapat memilih data yang ingin diperbarui, yaitu data pelanggan, paket wedding, maupun pemesanan wedding.

<img width="474" height="272" alt="image" src="https://github.com/user-attachments/assets/e5ee7df4-c3f9-4954-bc1b-7c54b1cf398f" />

Pada Menu Update, pengguna dapat memilih salah satu dari tiga jenis data yang tersedia untuk diperbarui. Setelah memilih jenis data, pengguna akan diminta memasukkan ID dari data yang ingin diubah. Program kemudian akan mencari data berdasarkan ID tersebut. Apabila data ditemukan, pengguna dapat memasukkan informasi baru sesuai dengan atribut yang dapat diperbarui.

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

Apabila telah menyelesaikan proses update, pengguna dapat memilih menu “5” untuk keluar dari Menu Update dan kembali ke menu utama.

---

### **4. Menu Hapus**

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

Apabila telah menyelesaikan proses hapus, pengguna dapat memilih menu **“4”** untuk keluar dari Menu Hapus dan kembali ke menu utama.

---

5. **Keluar >>>**

<img width="545" height="516" alt="image" src="https://github.com/user-attachments/assets/b9ca1bc7-6617-4d37-bc53-8842b47c691d" />


Apabila pengguna telah selesai melakukan pengelolaan data, pengguna dapat memilih menu “5” pada menu utama untuk mengakhiri program. Setelah pengguna memilih menu tersebut, program akan menampilkan pesan “BYEEEE!!” sebagai tanda bahwa program telah selesai dijalankan.

---

## Penerapan Nilai Tambah pada Program

Program ini memiliki penerapan nilai tambah, yaitu sebagai berikut:

### **1. Access Modifier**
Pada program ini, saya menerapkan access modifier private pada atribut yang terdapat di dalam class data, seperti Pelanggan, PaketWedding, dan PemesananWedding. Penggunaan private membuat atribut tersebut hanya dapat diakses secara langsung dari dalam class tempat atribut tersebut didefinisikan.

Contohnya terdapat pada baris kode di class Pelanggan, yaitu:

<img width="361" height="118" alt="image" src="https://github.com/user-attachments/assets/752974b1-c388-4f47-bed3-eb56448a9b13" />

Penggunaan access modifier pada gambar di atas menunjukkan bahwa data pada setiap object tidak dapat diakses atau diubah secara langsung dari luar class.

### **2. Access Modifier**
Pada program ini, saya menerapkan konsep encapsulation dengan menyembunyikan atribut menggunakan access modifier private dan menyediakan getter serta setter untuk mengakses atau mengubah data tertentu.

Sebagai contoh, pada class Pelanggan terdapat penerapan method getter dan setter:

<img width="453" height="517" alt="image" src="https://github.com/user-attachments/assets/273dd8bf-606c-4172-ba3c-2a3f09745a7a" />


Getter digunakan untuk mengambil nilai dari atribut, sedangkan setter digunakan untuk mengubah nilai atribut. Sehingga akses terhadap data dalam object dilakukan melalui method yang telah disediakan oleh class, sehingga data tidak diakses secara langsung dari luar class.

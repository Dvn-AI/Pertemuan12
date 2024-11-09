                                   LANGKAH-LANGKAH MEMBUAT JAVA GUI CRUD MENGGUNAKAN PERSISTENCE

1.	Pertama-tama, hapus dulu semua kodingan di setiap button nya serta method untuk menampilkan datanya. Kemudian buat Entity Class dengan cara seperti berikut:
   ![image](https://github.com/user-attachments/assets/b3062769-7f0f-4828-8478-74a98daaf98b)

  	Klik kanan pada package > New > Entity Classes from Database. Setelah itu pilih koneksi database > pilih tabel yang diinginkan lalu klik add. 
    ![image](https://github.com/user-attachments/assets/0759b024-aa50-48ff-b6cc-bc9a6efe2f82)

2.	Next, akan mucul pop up seperti dibawah ini:
   ![image](https://github.com/user-attachments/assets/cdac38ce-560d-4c42-a203-9723c9779b94)

    Pada tahap ini,  pastikan Database dan Tabel nya sudah benar. Jika sudah langsung Next saja.
  	
3.  Setelah itu, akan muncul pop up lagi langsung saja klik finish
     ![image](https://github.com/user-attachments/assets/5f843c49-49fe-49b4-bcdc-dc60e0133095)

4.  Setelah finish, akan muncul package baru bernama META-INF dan ada file persistence.xml didalamnya. Pada tahap ini langsung saja untuk mulai mengkoding tiap button CRUD nya.
     ![image](https://github.com/user-attachments/assets/6a9a5d36-cae0-4947-a9ea-8c7f71258484)

5.  Mulai pada button Insert, berikut adalah kodingannya.
     ![image](https://github.com/user-attachments/assets/50cf2721-f8cf-40df-abb1-aa722503c5c5)

    Pada baris pertama, ganti nama persistence unit sesuai dengan nama persistence unit anda. Anda bias menemukannya di file persistence.xml pada langkah ke-4. Kemudian buat instance baru dari class terkait(pada contoh diatas class saya adalah MataKuliah) lalu ubah tiap nama tiap kolom sesuai dengan nama kolom di tabel anda.
     
6.  Beralih pada button Update, berikut adalah kodingannya.
     ![image](https://github.com/user-attachments/assets/e3740114-eb04-4d62-89f6-7b146f21ca67)

    Pada kodingan diatas, saya menggunakan em.find untuk mencari Primary Key dari tabel saya yaitu Kodemk. Lalu pengguna akan dapat mengganti atau update data jika data tersebut ada, dan jika data yang dipilih kosong atau tidak ada, maka akan menampilkan pesan seperti diatas. 

7.  Lanjut pada button Delete, berikut adalah kodingannya.
     ![image](https://github.com/user-attachments/assets/e087177a-c0f5-40af-8349-fae2ea09dcb9)

    Sama seperti kodingan Update, saya menggunakan em.find untuk mencari Kodemk sebagai acuan. Kemudian pengguna dapat menghapus data jika data tersebut ada, jika data tersebut tidak ada atau kosong, maka akan menampilkan pesan seperti diatas.
    
8.  Kemudian pada method untuk menampilkan data nya, berikut adalah kodingannya.
     ![image](https://github.com/user-attachments/assets/e694fb19-2b21-4632-b893-7e8627900a3e)

    Simpelnya, method ini saya menggunakan EntityManager untuk mengambil data dari database lalu memanipulasi tampilan tabel menggunakan DefaultTableModel.
    
9.  Terakhir, run program dan seperti inilah hasilnya. Selamat Mencoba! 😉
    ![image](https://github.com/user-attachments/assets/116323d9-1e66-48bf-9420-c879c8bb6834)
  

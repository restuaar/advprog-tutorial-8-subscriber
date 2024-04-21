# Tutorial for Advance Programming Course 2023/2024

**Nama** : **Restu Ahmad Ar Ridho** <br/>
**NPM** : **2206028951** <br/>
**Kelas** : **Advance Programming - A**

## Module 8 - Software Architectures
1. What is _ampq_?  
AMQP adalah singkatan dari Advanced Message Queuing Protocol. Ini adalah _open standard application layer protocol_ untuk middleware berorientasi pesan. Fitur-fitur yang menentukan AMQP adalah orientasi pesan, _queuing, routing_ (termasuk _point-to-point_ dan _publisher-and-subscriber_), keandalan dan keamanan.
2. What it means? `guest:guest@localhost:5672`, what is the first quest, and what is the second guest, and what is `localhost:5672` is for?  
`guest:guest@localhost:5672` adalah string koneksi untuk perantara pesan (seperti RabbitMQ) yang menggunakan protokol AMQP.
    - `guest` pertama adalah nama pengguna untuk autentikasi.
    - `guest` kedua setelah tanda titik dua (:) adalah kata sandi untuk autentikasi.
    - `localhost` adalah nama host atau alamat IP dari mesin di mana perantara pesan berjalan. Dalam kasus ini, ia berjalan pada mesin yang sama dengan klien.
    - `5672` adalah nomor port di mana message broker mendengarkan. Ini adalah port default untuk RabbitMQ, sebuah message broker populer yang menggunakan AMQP.


#### Simulating Slow Subscriber
![Queue RabbitMQ](src\images\slowrabbit.png)
> Jumlah total pesan yang mengantri dapat dikaitkan dengan kombinasi beberapa faktor. Salah satunya adalah ketika publisher dengan cepat mengirim pesan ke RabbitMQ, setiap proses menambah antrian, sementara subscriber mengkonsumsi pesan pada kecepatan yang lebih lambat karena penundaan yang disengaja selama 1 detik per pemrosesan pesan. Pemrosesan yang lebih lambat ini memungkinkan pesan menumpuk dalam antrian.


#### Multiple Slow Subscriber 
![Console Mult Subs](src\images\consolemultsubs.png)
![Monitoring RabbitMQ](src\images\multiplesubs.png)
> Ketika beberapa subscriber memproses pesan secara bersamaan, kenaikan antrean pesan akan berkurang lebih cepat karena terdapat pemrosesan paralel dan peningkatan throughput. Dengan setiap subscriber menangani pesan secara independen, beban kerja didistribusikan secara lebih merata di seluruh sistem, mencegah antrean panjang dan memungkinkan lebih banyak pesan untuk diproses secara bersamaan.
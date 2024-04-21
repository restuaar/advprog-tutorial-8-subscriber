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


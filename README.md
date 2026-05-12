## Modul-9-Publisher

### Question 1
1. Dalam satu kali dijalankan, publisher akan mengirim 5 data atau 5 event ke message broker. Setiap event berisi user_id dan user_name, yaitu data untuk Amir, Budi, Cica, Dira, dan Emir.

2. amqp://guest:guest@localhost:5672 adalah alamat koneksi ke message broker. amqp:// menunjukkan protokol yang dipakai, guest pertama adalah username, guest kedua adalah password, localhost berarti RabbitMQ berjalan di komputer lokal, dan 5672 adalah port default untuk koneksi AMQP. Jadi program publisher terhubung ke RabbitMQ lokal dengan akun guest melalui port 5672.
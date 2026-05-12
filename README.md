## Modul-9-Publisher

### Question 1
1. Dalam satu kali dijalankan, publisher akan mengirim 5 data atau 5 event ke message broker. Setiap event berisi user_id dan user_name, yaitu data untuk Amir, Budi, Cica, Dira, dan Emir.

2. amqp://guest:guest@localhost:5672 adalah alamat koneksi ke message broker. amqp:// menunjukkan protokol yang dipakai, guest pertama adalah username, guest kedua adalah password, localhost berarti RabbitMQ berjalan di komputer lokal, dan 5672 adalah port default untuk koneksi AMQP. Jadi program publisher terhubung ke RabbitMQ lokal dengan akun guest melalui port 5672.

### Runnning RabbitMQ Screenshot
![running-rabbitmq](tutorial8/publisher/images/running-rabbitmq.png)

### Sending and Processing Event
![event-processing-terminal](tutorial8/publisher/images/event-processing-terminal.png)

Ketika publisher dijalankan, program mengirim 5 event ke RabbitMQ. Event tersebut kemudian diterima dan diproses oleh subscriber, yang terlihat dari terminal subscriber yang menampilkan message untuk Amir, Budi, Cica, Dira, dan Emir.

### Monitoring Chart Based on Publisher
![publisher-message-rate-spike](tutorial8/publisher/images/publisher-message-rate-spike.png)

Spike pada chart RabbitMQ muncul saat publisher dijalankan berulang. Setiap kali publisher mengirim event ke message broker, grafik message rates naik sesaat kemudian turun lagi setelah event diterima dan diproses oleh subscriber.
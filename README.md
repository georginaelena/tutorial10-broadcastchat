# Tutorial 10

_Nama    : Georgina Elena Shinta Dewi Achti<br>
NPM     : 2206810995<br>
Kelas   : AdvProg - B_

## 2.1. Original code of broadcast chat

![](https://i.imgur.com/dXRqNYh.png)

Ketika server dijalankan, setiap client yang juga dijalankan akan terhubung ke server menggunakan WebSocket. Dari gambar di atas, terlihat bahwa ketika pengguna mengirim pesan dari salah satu client, pesan tersebut akan dikirim ke server dan disebarkan ke semua client yang terhubung ke server.

Dengan demikian, setiap pesan yang dikirim oleh client akan terlihat oleh client lain secara real-time. Ini mirip dengan sebuah ruang obrolan di mana pesan yang dikirim oleh satu client dapat dilihat oleh client lainnya secara langsung. Komunikasi real-time ini dimungkinkan oleh WebSocket yang memfasilitasi komunikasi instan antara server dan client tanpa perlu menunggu respons dari server.

## 2.2. Modifying the websocket port

![](https://i.imgur.com/H60vFoK.png)

![](https://i.imgur.com/RIIn1zj.png)

Seperti yang dijelaskan dalam tutorial, sebuah koneksi melibatkan dua sisi, yaitu client dan server. Jika terjadi modifikasi, perubahan tersebut harus dilakukan di kedua sisi. Dalam kasus ini, modifikasi dilakukan dengan mengubah port menjadi `8080` di bagian server.rs, yaitu `TcpListener::bind("127.0.0.1:8080").await?`, dan di client.rs, yaitu `ws://127.0.0.1:2000`. Dengan melakukan perubahan port di kedua sisi, koneksi antara client dan server dijamin dapat berjalan dengan lancar tanpa masalah.

Server dan client menggunakan protokol yang sama, yaitu WebSocket, yang diimplementasikan menggunakan library `tokio_websockets` untuk mendukung komunikasi real-time. Pada server.rs, WebSocket dijelaskan menggunakan `WebSocketStream` dan `ServerBuilder`, sedangkan pada client.rs, menggunakan `ClientBuilder` dan `WebSocketStream`.


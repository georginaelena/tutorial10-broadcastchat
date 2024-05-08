# Tutorial 10

_Nama    : Georgina Elena Shinta Dewi Achti<br>
NPM     : 2206810995<br>
Kelas   : AdvProg - B_

## 2.1. Original code of broadcast chat

![](https://i.imgur.com/dXRqNYh.png)

Ketika server dijalankan, setiap client yang juga dijalankan akan terhubung ke server menggunakan WebSocket. Dari gambar di atas, terlihat bahwa ketika pengguna mengirim pesan dari salah satu client, pesan tersebut akan dikirim ke server dan disebarkan ke semua client yang terhubung ke server.

Dengan demikian, setiap pesan yang dikirim oleh client akan terlihat oleh client lain secara real-time. Ini mirip dengan sebuah ruang obrolan di mana pesan yang dikirim oleh satu client dapat dilihat oleh client lainnya secara langsung. Komunikasi real-time ini dimungkinkan oleh WebSocket yang memfasilitasi komunikasi instan antara server dan client tanpa perlu menunggu respons dari server.


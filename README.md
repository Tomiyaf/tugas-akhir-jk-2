## Dokumentasi Tugas Akhir Praktikum Jaringan Komputer Judul 2

Link Youtube:

https://youtu.be/6izgbZqipsQ

Capture Saat Gagal PING

<img width="856" height="426" alt="image" src="https://github.com/user-attachments/assets/5f8a5b03-454b-409b-8c34-9c7d129aa342" />

Ping gagal karena router sebagai default gateway belum dikonfigurasi sehingga belum ada proses routing untuk traffic L3 antar subnet. Karena PC-A dan PC-B keduanya beda network. Switch hanya bekerja pada layer 2 (ethernet) dan tidak mampu melakukan routing antar subnet. Ketika PC-A ingin ping PC-B, packet harus lewat router, namun karena interface router belum diberi IP (belum aktif sebagai gateway), maka router tidak dapat meneruskan packet tersebut, sehingga ping dari PC-A ke PC-B otomatis gagal.


Capute Saat Berhasil PING

<img width="865" height="669" alt="image" src="https://github.com/user-attachments/assets/9809f23c-4234-4fd8-96ef-464ba221d138" />

Ping berhasil karena router sudah dikonfigurasi interface-nya (IP gateway tiap subnet) sehingga router sekarang sudah bisa melakukan routing antar subnet. Setelah PC-A mengirim packet ke alamat di luar subnet, packet tersebut bisa diarahkan ke default gateway dan diteruskan oleh router menuju subnet PC-B. Dengan demikian trafik ICMP tidak lagi berhenti di layer 2, melainkan diteruskan di layer 3 melalui router, sehingga akhirnya reply dari PC-B bisa kembali ke PC-A dengan sukses.

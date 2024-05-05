# Advanced Programming - Tutorial


------------
## Overview

This repository contains the code and reflections for Tutorial 10 in Advanced Programming course by Vinka Alrezky As (NPM: 2206820200)❄️

- [Tutorial 10 - Timer](https://github.com/vinkakniv/tutorial10-timer)
- [Tutorial 10 - Broadcast Chat](https://github.com/vinkakniv/tutorial10-broadcastchat)
- [Tutorial 10 - WebChat using yew](https://github.com/vinkakniv/tutorial10-webchatyew)

------------
# Tutorial 10 - Timer

### _Reflection_

![](https://imgur.com/L9AiCUP.png)

Setelah tugas asinkron dijadwalkan menggunakan `spawner.spawn(async { ... });`, pernyataan `println!("Vinka's Komputer: hey hey");` langsung dieksekusi. Ini berarti, pesan `Vinka's Komputer: hey hey` akan muncul terlebih dahulu sebelum tugas asinkron tersebut selesai.

Dalam tugas asinkron yang dibuat dengan `async { ... }`, terdapat perintah `TimerFuture::new(Duration::new(2, 0)).await;`. Ini membuat sebuah _timer_ yang menunggu selama 2 detik sebelum menyelesaikan tugasnya. Meskipun pesan pertama telah dicetak, program akan berhenti selama 2 detik karena _timer_ belum melanjutkan eksekusi ke pesan-pesan berikutnya.

Setelah _delay_ 2 detik, tugas asinkron selesai dan pesan `Vinka's Komputer: howdy!` tercetak. Selanjutnya, program mencetak pesan `Vinka's Komputer: done!` karena tugas asinkron telah selesai menjalankan _timer_ selama 2 detik.



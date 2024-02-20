# Tutorial 2 Game Development 2023 / 2024

## Naufal Zhafari Zahran - 2106752104

### Pertanyaan
- Scene BlueShip dan StonePlatform sama-sama memiliki sebuah child node bertipe Sprite. Apa fungsi dari node bertipe Sprite? 
    - Node bertipe sprite befungsi sebagai node yang menampilkan 2D texture. 
    - Sprite juga dapat digunakan untuk pembuatan animasi. 
    - Sprite dapat digunakan untuk mendeteksi interaksi dengan elemen dalam permainan.
- Root node dari scene BlueShip dan StonePlatform menggunakan tipe yang berbeda. BlueShip menggunakan tipe RigidBody2D sedangkan StonePlatform menggunakan tipe StaticBody2D. Apa perbedaan dari masing-masing tipe node?
    - RigidBody2D : biasanya digunakan untuk mewakili objek yang akan bereaksi terhadap aksi, gravitasi dan tindakan lainnya oleh objek. Node ini biasanya digunakan pada objek - objek seperti karakter pemain, musuh, atau objek lainnya yang dapat bergerak
    - StaticBody2D :  biasanya digunakan untuk mewakili benda yang statis atau tidak bereaksi jika dikenakan aksi. Objek yang diwakili oleh node biasa dapat berupa platform, dinding, atau objek dekoratif pada game.
- Ubah nilai atribut Mass dan Weight pada tipe RigidBody2D secara bebas di scene BlueShip, lalu coba jalankan scene MainLevel. Apa yang terjadi?
    - Ketika mass dan weight pada BlueShip ditingkatkan pergerakan dari BlueShip menjadi lebih sulit digerakkan. Sedangkan jika mass dan weight dikurangi, pergerakan dari BlueShip menjadi lebih ringan dan mudah digerakkan.
- Ubah nilai atribut Disabled pada tipe CollisionShape2D di scene StonePlatform, lalu coba jalankan scene MainLevel. Apa yang terjadi?
    - Ketika disabled CollisionShape2D diaktifkan, maka yang terjadi adalah tidak adanya lagi _collision_ antara objek StonePlatform dengan objek lainnya. Pada kasus ini, BlueShip saat akan jatuh bebas melewati StonePlatform yang dimana sebelumnya BlueShip akan mendarat di atas platform.
- Pada scene MainLevel, coba manipulasi atribut Position, Rotation, dan Scale milik node BlueShip secara bebas. Apa yang terjadi pada visualisasi BlueShip di Viewport?
    - Visualisasi BlueShip akan bergantung pada atrbitut yang diubah. Jika position yang diubah maka posisi dari BlueShip akan berubah dan visualisasinya akan mengikuti koordinat dari position yang diubah. Jika atribut rotation diubah, maka ini akan memutar BlueShip mengikuti perubahasan rotasi yang dibuat. Sedangkan untuk scale akan mengubah visualisasi BlueShip menjadi diperbesar atau diperkecil sesuai dengan skala yang diubah.
- Pada scene MainLevel, perhatikan nilai atribut Position node PlatformBlue, StonePlatform, dan StonePlatform2. Mengapa nilai Position node StonePlatform dan StonePlatform2 tidak sesuai dengan posisinya di dalam scene (menurut Inspector) namun visualisasinya berada di posisi yang tepat?
    - Nilai atribut position di inspector menunjukkan posisi relatif terhadap parent node. Maka posisi StonePlatform StonePlatform2 memiliki nilai atribut yang sesuai dengan parent node nya yaitu BluePlatform. Sementara itu, visualisasi objek akan dihitung berdasarkan posisi absolut dalam koordinat global scene. Ini mengapa nilai atribut position mungkin tidak terlihat sesuai dengan posisi sebenarnyta dalam scene, tetapi visualisasinya berada di posisi yang tepat.
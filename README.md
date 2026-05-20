# Laporan Hasil Praktikum: Final Project Aplikasi Berbasis Container

## Identitas Mahasiswa

- **Nama:** I Made Dwika Ariana
- **NIM:** 2415354001
- **Kelas/Rombel:** TRPL A
- **Tanggal Praktikum:** 20 Mei 2026

---

## Teknologi & Tools yang Digunakan

- **Sistem Operasi:** Windows
- **Containerization:** Docker & Docker Hub
- **Bahasa Pemrograman / Framework:** Node.js
- **Tools Lain:** VS Code, Git, Hopscotch

---

1.⁠ ⁠Pengujian Docker Compose, Volume, Network, Container

## Langkah-Langkah Praktikum & Dokumentasi

1. jalankan perintah

```bash
docker compose up -d
```

2. cek service yang

```bash
docker compose ps
```

3. proses compose berhasil
   (img/serviceList.png)

4. cek volume jalankan

```bash
docker volume ls
```

5. dengan hasil
   (img/volumeCheck.png)

6. cek volume jalankan

```bash
docker network ls
```

7. dengan hasil
   (img/checkNetwork.png)

8. cek container jalankan

```bash
docker container ls
```

9. dengan hasil
   (img/containerCheck.png)



2.⁠ ⁠⁠Pengujian Endpoint -> Request dan Response (Browser, Hoppscotch)

1. buka page https://hoppscotch.io/ dan install extension Hoppscotch browser extension dan ganti interceptor dengan browser extension

2. jalankan

```bash
docker compose up --build -d
```

3. di Hoppscotch isi dengan http://localhost:3000/
4. response yang dihasilkan
   (img/hasilResponse.png)

5. ⁠ ⁠⁠Pengujian upload ke Docker Hub
6. login dulu ke docker hub

```bash
docker login
```

    setelah muncul Login Succeeded

2. cek image yang mau di push dengan

```bash
docker images
```

    yang menghasilkan
    (img/imageList.png)

3. kemudian jalankan

```bash
docker tag backend-crud williman11/backend-crud
```

4. kemudian jalankan

```bash
docker push williman11/backend-crud
```

    dengan hasil (img/hasilPush.png)
    kemudian cek di docker hub dengan akun yang sama


## Kesimpulan

Praktikum Docker berhasil dijalankan menggunakan Docker Compose, termasuk pengujian container, volume, network, dan endpoint aplikasi. Kendala yang dihadapi adalah aplikasi sempat gagal terhubung ke database MySQL dan terjadi error dependency. Solusinya adalah memperbaiki konfigurasi Docker Compose, memastikan package terinstall, dan menambahkan retry connection pada aplikasi.


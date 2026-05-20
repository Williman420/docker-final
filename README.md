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

Tuliskan kesimpulan singkat atau kendala yang Anda hadapi beserta solusinya selama melakukan praktikum ini di sini.











```bash
# Contoh perintah terminal yang dijalankan
docker build -t app-good .
```

**Dokumentasi/Screenshot:**
![Proses Build Sukses](img/screenshot-langkah1.png)

---

### Langkah 2: [Tulis Nama Langkah 2, Contoh: Tag dan Push ke Docker Hub]

Jelaskan proses penamaan ulang _image_ dan proses unggah ke Docker Hub milik Anda.

```bash
docker tag app-good madedianpp/app-good:v1.0
docker push madedianpp/app-good:v1.0
```

**Dokumentasi/Screenshot:**
![Proses Push Berhasil](dokumentasi/push-docker-hub.png)

---

### Langkah 3: [Tulis Nama Langkah 3, Contoh: Pengujian Pull dan Run Container]

Jelaskan bagaimana cara melakukan verifikasi atau pengujian bahwa praktikum Anda berhasil berjalan.

```bash
docker run -d -p 8080:8080 madedianpp/app-good:v1.0
```

**Dokumentasi/Screenshot:**
<img src="img/screenshot-hasil-browser.png" alt="Aplikasi Berjalan di Browser" width="500">

---
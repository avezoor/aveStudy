# Cara Mengupdate GitHub dan Repository Lokal

Dokumentasi ini menjelaskan langkah-langkah untuk memperbarui repository lokal dari GitHub dan sebaliknya, memperbarui GitHub dengan perubahan dari repository lokal.

## Daftar Isi

- [Menambahkan Remote Repository](#menambahkan-remote-repository)
- [Menghapus Remote Repository](#menghapus-remote-repository)
- [Mengupdate Repository Lokal dari GitHub](#mengupdate-repository-lokal-dari-github)
- [Mengupdate GitHub dari Repository Lokal](#mengupdate-github-dari-repository-lokal)
- [Menangani Konflik](#menangani-konflik)

---

## Menambahkan Remote Repository

Untuk menambahkan remote repository ke proyek lokal:

1. **Buka terminal** di dalam direktori proyek lokal.
2. **Tambahkan remote repository**:
   ```bash
   git remote add <nama-remote> <url-repository>
   ```
   Contoh:
   ```bash
   git remote add origin https://github.com/username/repository.git
   ```

---

## Menghapus Remote Repository

Untuk menghapus remote repository yang sudah ada:

1. **Buka terminal** di dalam direktori proyek lokal.
2. **Hapus remote repository**:
   ```bash
   git remote remove <nama-remote>
   ```
   Contoh:
   ```bash
   git remote remove origin
   ```

---

## Mengupdate Repository Lokal dari GitHub

Untuk menarik perubahan terbaru dari GitHub ke repository lokal:

1. **Buka terminal** di dalam direktori proyek lokal.
2. **Pastikan kamu berada di branch yang ingin di-update**:
   ```bash
   git checkout <nama-branch>
   ```
   Ganti `<nama-branch>` dengan nama branch yang ingin di-update (misalnya, `main`).
3. **Tarik perubahan terbaru dari GitHub**:
   ```bash
   git pull origin <nama-branch>
   ```
   Contoh jika kamu berada di branch `main`:
   ```bash
   git pull origin main
   ```

Ini akan mengunduh dan menggabungkan perubahan terbaru dari GitHub ke repository lokal.

---

## Mengupdate GitHub dari Repository Lokal

Untuk mengirim perubahan dari repository lokal ke GitHub:

1. **Periksa status repository** untuk melihat perubahan yang belum di-commit:
   ```bash
   git status
   ```
2. **Tambahkan file yang ingin di-commit**:
   - Untuk menambahkan file tertentu:
     ```bash
     git add <nama-file>
     ```
   - Untuk menambahkan semua file yang berubah:
     ```bash
     git add .
     ```
3. **Lakukan commit terhadap perubahan**:
   ```bash
   git commit -m "Deskripsi singkat tentang perubahan"
   ```
4. **Dorong (push) perubahan ke GitHub**:
   ```bash
   git push origin <nama-branch>
   ```
   Contoh jika kamu bekerja di branch `main`:
   ```bash
   git push origin main
   ```

---

## Menangani Konflik

Jika ada konflik saat melakukan `git pull` atau `git push`, langkah-langkah berikut bisa membantu:

1. **Lakukan pull** untuk menarik perubahan terbaru sebelum melakukan push:
   ```bash
   git pull origin <nama-branch>
   ```
2. **Selesaikan konflik** secara manual. Git akan menunjukkan file mana saja yang memiliki konflik.
3. **Edit file yang mengalami konflik**, lalu tandai perubahan yang telah diselesaikan:
   ```bash
   git add <nama-file>
   ```
4. **Lakukan commit untuk menyimpan perubahan setelah konflik diselesaikan**:
   ```bash
   git commit
   ```
5. **Dorong kembali perubahan ke GitHub**:
   ```bash
   git push origin <nama-branch>
   ```

---

## Catatan

- Pastikan kamu selalu bekerja di branch yang sesuai (`main`, `development`, atau branch lain yang relevan).
- Sebelum melakukan `git push`, lakukan `git pull` terlebih dahulu untuk memastikan kamu memiliki perubahan terbaru dari GitHub.
- Dalam kasus konflik, baca pesan yang diberikan oleh Git untuk membantu menyelesaikan masalah secara manual.
```

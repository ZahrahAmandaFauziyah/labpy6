# labpy6

tugas praktikum 06

Buat program sederhana dengan mengaplikasikan penggunaan fungsi
yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan:
1. Fungsi tambah() untuk menambah data
2. Fungsi tapilkan() untuk menampilkan data
3. Fungsi hapus(nama) untuk menghapus data berdasarkan nama
4. Fungsi ubah(nama) untuk mengubah data berdasarkan nama

KODE PYTHON

        # Daftar untuk menyimpan data mahasiswa
        data_mahasiswa = []

        # Fungsi untuk menambah data mahasiswa
        def tambah():
        nama = input("Masukkan nama mahasiswa: ")
        nim = input("Masukkan NIM: ")
        nilai = float(input("Masukkan nilai: "))
        data_mahasiswa.append({"nama": nama, "nim": nim, "nilai": nilai})
        print("Data berhasil ditambahkan.")

        # Fungsi untuk menampilkan data mahasiswa
        def tampilkan():
        if not data_mahasiswa:
        print("Tidak ada data mahasiswa.")
        else:
        print("Daftar Data Mahasiswa:")
        for i, mahasiswa in enumerate(data_mahasiswa, start=1):
            print(f"{i}. Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")

        # Fungsi untuk menghapus data mahasiswa berdasarkan nama
        def hapus(nama):
        for mahasiswa in data_mahasiswa:
        if mahasiswa['nama'].lower() == nama.lower():
            data_mahasiswa.remove(mahasiswa)
            print(f"Data mahasiswa dengan nama {nama} berhasil dihapus.")
            return
        print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

        # Fungsi untuk mengubah data mahasiswa berdasarkan nama
        def ubah(nama):
        for mahasiswa in data_mahasiswa:
        if mahasiswa['nama'].lower() == nama.lower():
            print(f"Data lama: Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")
            mahasiswa['nama'] = input("Masukkan nama baru: ")
            mahasiswa['nim'] = input("Masukkan NIM baru: ")
            mahasiswa['nilai'] = float(input("Masukkan nilai baru: "))
            print("Data berhasil diubah.")
            return
        print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

        # Menu utama
        def menu():
        while True:
              print("\nMenu:")
              print("1. Tambah Data")
              print("2. Tampilkan Data")
              print("3. Hapus Data")
              print("4. Ubah Data")
              print("5. Keluar")
        pilihan = input("Pilih menu (1-5): ")

        if pilihan == "1":
            tambah()
        elif pilihan == "2":
            tampilkan()
        elif pilihan == "3":
            nama = input("Masukkan nama mahasiswa yang akan dihapus: ")
            hapus(nama)
        elif pilihan == "4":
            nama = input("Masukkan nama mahasiswa yang akan diubah: ")
            ubah(nama)
        elif pilihan == "5":
            print("Keluar dari program.")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

        # Menjalankan menu utama
        menu() 
        
PENJELASAN:
1. Data Mahasiswa: Data mahasiswa disimpan dalam list data_mahasiswa, yang berisi dictionary dengan kunci 'nama', 'nim', dan 'nilai'.
2. Fungsi tambah(): Meminta input nama, NIM, dan nilai mahasiswa, lalu menambahkannya ke dalam daftar.
3. Fungsi tampilkan(): Menampilkan semua data mahasiswa yang ada dalam daftar.
4. Fungsi hapus(nama): Menghapus data mahasiswa berdasarkan nama yang diberikan.
5. Fungsi ubah(nama): Mengubah data mahasiswa berdasarkan nama yang diberikan, termasuk nama, NIM, dan nilai.
6. Menu Utama: Menyediakan antarmuka pengguna untuk memilih operasi yang diinginkan.

INPUT
![Cuplikan layar 2024-11-28 123954](https://github.com/user-attachments/assets/690e8884-346f-418e-8d63-e4179e544d2d)
![Cuplikan layar 2024-11-28 124018](https://github.com/user-attachments/assets/e387ed62-fd2f-4b95-a3af-76e79333a453)
![Cuplikan layar 2024-11-28 124311](https://github.com/user-attachments/assets/47745cd6-7eb8-447c-8755-de744695b5f1)

OUTPUT

![Cuplikan layar 2024-11-28 125413](https://github.com/user-attachments/assets/03b8978c-c3fe-49c7-bacb-44223f59b4c6)
![Cuplikan layar 2024-11-28 125429](https://github.com/user-attachments/assets/eb1a7924-3851-47eb-94d3-e9f67a8adff2)
![Cuplikan layar 2024-11-28 125450](https://github.com/user-attachments/assets/cd166faa-8767-4655-8b6d-d1a8345b1c51)
![Cuplikan layar 2024-11-28 125502](https://github.com/user-attachments/assets/5d1913f7-1527-4b6b-8618-4358cb86592c)

FLOWCHART


Latihan 1

        import math

        # Menggunakan lambda untuk mendefinisikan fungsi
        a = lambda x: x**2
        b = lambda x, y: math.sqrt(x*2 + y*2)
        c = lambda *args: sum(args) / len(args)
        d = lambda s: "".join(set(s))

        if __name__ == "__main__":

    print("a(5):", a(5))

    print("b(3, 4):", b(3, 4))

    print("c(1, 2, 3, 4, 5):", c(1, 2, 3, 4, 5))

    print("d('hello world'):", d('hello world'))

INPUT

![Cuplikan layar 2024-11-28 130044](https://github.com/user-attachments/assets/9ae78847-a3d4-4c7a-b084-f3ce3f1d9794)

OUTPUT

![Cuplikan layar 2024-11-28 130052](https://github.com/user-attachments/assets/afbc5184-c3a2-4ee8-9d64-da5cacc113ff)






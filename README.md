# Praktikum7

Repository ini digunakan untuk memenuhi Tugas Bahasa Pemrograman Pertemuan-11

Nama    : Mohamad Irvan Zidni

NIM     : 312210308

Kelas   : TI.22.A.3

## Tugas

Soal Tugas

![Foto](Foto/Soal%20Tugas.png)

### Flowchart

Buatlah alur flowchart terlebih dahulu untuk mempermudah pada saat membuat program

![Foto](Foto/Flowchart%20Tugas.png)

### Code

Penjelasan

1. Buatlah dictionary kosong terlebih dahulu

        mahasiswa = {}

2. Menu program utama

        def menu():
            print("\n")
            print("====================================================")
            print("      \t\t Program input nilai       ")
            print("====================================================\n")

            x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
            print("\n")

            if x == 'L':
                show()
            elif x == 'T':
                add()
            elif x == 'U':
                update()
            elif x == 'H':
                delete()
            elif x == 'C':
                search()
            elif x == 'K':
                print("==========================================================================")
                print('\n')
                print("> You exit the code                        ")
                print("\n")
                print("==========================================================================")

                exit()

            else:
                print("            KODE YANG ANDA MASUKKAN TIDAK VALID !!!!!!!!!!!")

        // Saya menggunakan perulangan while-true agar program terus berjalan hingga berhenti
        while True:
            menu()

3. Menu program tambah data

        def add():
            print("Tambah Data")
            nama = input("Nama\t         : ")
            nim = input("NIM\t         : ")
            uts = int(input("Nilai UTS\t : "))
            uas = int(input("Nilai UAS\t : "))
            tugas = int(input("Nilai Tugas\t : "))
            akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
            mahasiswa[nama] = nim, tugas, uts, uas, akhir

4. Menu program lihat data

        def show():
            if mahasiswa.items():
                print("Daftar Nilai")
                print("=================================================================================")
                print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
                print("=================================================================================")
                i = 0
                for a in mahasiswa.items():
                    i += 1
                    print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
                        .format(a[0][: 14], a[1][0], a[1][1], a[1][2], a[1][3], a[1][4], no=i))
                print("=================================================================================")

            else:
                print("Daftar Nilai")
                print("=================================================================================")
                print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
                print("=================================================================================")
                print("|                                TIDAK ADA DATA                                 |")
                print("=================================================================================")

5. Menu program ubah data

        def update():
            print("Ubah Data")
            nama = input("Masukkan Nama : ")
            if nama in mahasiswa.keys():
                nim = input("NIM\t : ")
                uts = int(input("Nilai UTS\t : "))
                uas = int(input("Nilai UAS\t : "))
                tugas = int(input("Nilai Tugas\t : "))
                akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
                mahasiswa[nama] = nim, tugas, uts, uas, akhir

            else:
                print("Nama tidak ditemukan ")

6. Menu program hapus data

        def delete():
            print("Hapus Data")
            nama = input("Masukkan Nama : ")

            if nama in mahasiswa.keys():
                del mahasiswa[nama]

            else:
                print("Nama tidak ditemukan")

7. Menu program cari data

        def search():
            print("Cari Data")
            a = input("Masukkan Nama : ")
            if a in mahasiswa.keys():
                print("===========================================================================")
                print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
                print("===========================================================================")
                print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
                    .format(a, mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4]))
                print("===========================================================================")

            else:
                print("=================================================================================")
                print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
                print("=================================================================================")
                print("|                          DATA TIDAK DITEMUKAN                                 |")
                print("=================================================================================")

### Output

1. Disini Saya mencoba menambah data awal

![Foto](Foto/Tambah%20data.png)

2. Tampilan data awal

![Foto](Foto/Lihat%20data.png)

3. Lalu Saya menambah data kedua

![Foto](Foto/Tambah%20data1.png)

4. Tampilan data kedua

![Foto](Foto/Lihat%20data1.png)

5. Lalu Saya mencoba ubah nilai pada data 'Zidni'

![Foto](Foto/Ubah%20data.png)

6. Tampilan setelah diubah

![Foto](Foto/Lihat%20data2.png)

7. Saya mencoba cari data 'Irvan'

![Foto](Foto/Cari%20data.png)

8. Lalu Saya mencoba hapus data 'Zidni'

![Foto](Foto/Hapus%20data.png)

9. Tampilan setelah data 'Zidni' terhapus

![Foto](Foto/Lihat%20data3.png)
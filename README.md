# Praktikum4
# Latihan 1

<img width="536" height="286" alt="image" src="https://github.com/user-attachments/assets/d2c59eaf-c510-4310-8434-11bb5bcf8c42" />

Menggunakan program phyton :

    import random
    # meminta input dari pengguna untuk jumlah bilangan
    n = int(input("masukkan jumlah n: "))

    # menggunakan loop while untuk menghasilkan bilangan acak
    # sampai n bilangan yang kurang dari 0.5 ditemukan
    while n > 0:
        # menghasilkan bilangan acak antara 0.0 dan 1.0
        random_number = random.random()

        # memeriksa apakah bilangan acak kurang dari 0.5
        if random_number < 0.5:
            # menampilkan bilangan jika memenuhi syarat
            print(random_number)

            # mengurangi n karena satu bilangan sudah ditemukan
            n -= 1

Penjelasan kode program tersebut adalah sebagai berikut:

•	Impor Modul: Mengimpor modul random untuk fungsi pembangkit bilangan acak.

•	Input Pengguna: Meminta pengguna untuk memasukkan jumlah bilangan yang akan diproses, yang disimpan dalam variabel n.

•	Perulangan: Melakukan perulangan while sebanyak n kali.

•	Pembangkitan Bilangan Acak: Di setiap perulangan, program menghasilkan satu bilangan acak antara 0.0 dan 1.0.

•	Kondisi dan Output: Memeriksa apakah bilangan acak tersebut kurang dari 0.5. Jika ya, bilangan tersebut akan dicetak ke layar.

•	Pembaruan Variabel: Mengurangi nilai n sebesar 1 di setiap iterasi perulangan hingga n mencapai 0.

Dan menghasilkan :

<img width="686" height="168" alt="image" src="https://github.com/user-attachments/assets/272b1bd4-201c-4b5f-a652-da604c5e2ea1" />

# Latihan 2
Seorang pengusaha menginvestasikan uangnya untuk memulai usahanya dengan modal
awal 100 juta, pada bulan pertama dan kedua belum mendapatkan laba. pada bulan ketiga
baru mulai mendapatkan laba sebesar 1% dan pada bulan ke 5, pendapatan meningkat 5%,
selanjutnya pada bulan ke 8 mengalami penurunan keuntungan sebesar 2%, sehingga laba
menjadi 3%. Hitung total keuntungan selama 8 bulan berjalan usahanya.

Menggunakan :

    modal = 100000000
    total_laba = 0

    for bulan in range(1, 9):
            laba_bulan = 0
            if bulan <= 2:
                laba_bulan = 0
            elif bulan == 3 or bulan == 4:
                laba_bulan = modal * 0.01
            elif bulan >= 5 and bulan <= 7:
                laba_bulan = modal * 0.05
            elif bulan == 8:
                laba_bulan = modal * 0.03

            print(f"laba bulan ke- {bulan} sebesar:{laba_bulan}") 
            total_laba += laba_bulan

    print(f"total laba adalah: {total_laba}")

Penjelasan :
•	Inisialisasi Variabel:

1. modal = 100000000: Menetapkan modal awal sebesar 100.000.000.
2. total_laba = 0: Menginisialisasi variabel total_laba dengan nilai nol.
   
•	Looping (Perulangan)

1. for bulan in range(1, 9):: Kode akan melakukan perulangan untuk setiap bulan dari 1 hingga 8 (range(1, 9) berarti angka 1 sampai 8, tidak termasuk 9).
   
•	Logika Perhitungan Laba Bulanan:

1. if bulan <= 2:: Jika bulan adalah 1 atau 2, laba_bulan adalah 0.
2. elif bulan == 3 or bulan == 4:: Jika bulan adalah 3 atau 4, laba_bulan adalah 1% dari modal.
3. elif bulan >= 5 and bulan <= 7:: Jika bulan adalah 5, 6, atau 7, laba_bulan adalah 5% dari modal.
4. elif bulan == 8:: Jika bulan adalah 8, laba_bulan adalah 3% dari modal.
   
•	Pembaruan Laba:

1. print(f"laba bulan ke- {bulan} sebesar:{laba_bulan}"): Mencetak laba yang diperoleh untuk bulan yang sedang diproses.
2. total_laba += laba_bulan: Menambahkan laba_bulan ke total_laba untuk mengakumulasi total keuntungan.
   
•	Hasil Akhir:

1. print(f"total laba adalah: {total_laba}"): Setelah perulangan selesai, kode mencetak total laba yang telah diakumulasi dari bulan 1 sampai 8.

Hasilnya :

<img width="449" height="243" alt="image" src="https://github.com/user-attachments/assets/73ebeee5-6606-4efc-9911-ccb41b359725" />

# Latihan 3

Buat program yang mensimulasikan mesin ATM sederhana. Pengguna memiliki saldo awal
sebesar Rp 1.000.000, dan dapat menarik uang hingga saldo habis atau memilih untuk
keluar.

menggunakan program phyton :

    saldo = 1000000

    while True:
        print(f"Saldo saat ini: Rp {saldo}")
        print("1. Tarik Uang")
        print("2. Keluar")

        pilihan = input("Pilih menu (1/2): ")

        if pilihan == "1":
            try:
                jumlah_penarikan = int(input("Masukkan jumlah penarikan: "))
                if jumlah_penarikan <= saldo:
                    saldo -= jumlah_penarikan
                    print("Penarikan berhasil!")
                else:
                    print("Saldo tidak cukup!")
            except ValueError:
                print("Input tidak valid. Masukkan angka.")
        elif pilihan == "2":
            print("Terima kasih telah menggunakan ATM!")
            break
        else:
            print("Pilihan tidak valid.")


Penjelasan :
•	saldo = 1000000: Baris ini menginisialisasi variabel saldo dengan nilai awal Rp 1.000.000.

•	while True:: Program akan terus berjalan dalam sebuah perulangan tak terbatas, menampilkan menu dan meminta input, sampai pengguna memilih untuk keluar.

•	print(...): Bagian ini menampilkan saldo saat ini dan dua pilihan menu kepada pengguna: "1. Tarik Uang" dan "2. Keluar".

•	pilihan = input(...): Program meminta pengguna untuk memasukkan pilihan menu (1 atau 2).

•	if pilihan == "1":: Jika pengguna memilih "1", program akan masuk ke blok kode ini untuk melakukan penarikan uang.
1. try...except ValueError: Blok ini digunakan untuk menangani kesalahan. Program akan mencoba mengonversi input jumlah penarikan menjadi angka (int). Jika input bukan angka, program akan menampilkan pesan kesalahan "Input tidak valid. Masukkan angka."
2. if jumlah_penarikan <= saldo:: Program memeriksa apakah jumlah penarikan yang diminta kurang dari atau sama dengan saldo yang tersedia.
3. Jika ya, saldo akan dikurangi dengan jumlah_penarikan, dan program akan menampilkan "Penarikan berhasil!"
4. Jika tidak, program akan menampilkan "Saldo tidak cukup!".
   
•	elif pilihan == "2":: Jika pengguna memilih "2", program akan menampilkan "Terima kasih telah menggunakan ATM!" dan kemudian keluar dari perulangan (break), mengakhiri program.

•	else:: Jika pengguna memasukkan pilihan selain "1" atau "2", program akan menampilkan "Pilihan tidak valid." dan kembali ke awal perulangan, menampilkan menu lagi.

Hasilnya :

<img width="470" height="182" alt="image" src="https://github.com/user-attachments/assets/bf10abb8-b0ef-4a02-9942-c21aa8adf07b" />

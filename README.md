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


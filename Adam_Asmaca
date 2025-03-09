import random

def tahmin_et():
    print("\nBir sayı düşünün (1 ile 100 arasında), ve ben tahmin etmeye çalışacağım!")
    input("Hazırsanız ENTER tuşuna basın.")

    alt_sinir = 1
    ust_sinir = 100
    tahmin_sayisi = 0

    while True:
        tahmin = random.randint(alt_sinir, ust_sinir)
        tahmin_sayisi += 1
        print(f"Tahminim: {tahmin}")
        cevap = input("Bu doğru mu? (e = evet, k = daha küçük, b = daha büyük): ").lower()

        if cevap == "e":
            print(f"Tebrikler! Sayınızı {tahmin_sayisi} denemede buldum.")
            break
        elif cevap == "k":
            ust_sinir = tahmin - 1
        elif cevap == "b":
            alt_sinir = tahmin + 1
        else:
            print("Geçersiz giriş. Lütfen 'e', 'k' veya 'b' girin.")

def adam_asmaca():
    print("\nAdam Asmaca oyununa hoş geldiniz!")
    kelimeler = ["yapayzeka", "bilgisayar", "python", "oyun", "programlama"]
    secilen_kelime = random.choice(kelimeler)
    gorunen_kelime = ["_" for _ in secilen_kelime]
    yanlis_tahminler = 0

    while yanlis_tahminler < 6 and "_" in gorunen_kelime:
        print("\nŞu ana kadar kelime:", " ".join(gorunen_kelime))
        print(f"Kalan hakkınız: {6 - yanlis_tahminler}")
        tahmin = input("Bir harf tahmin edin: ").lower()

        if tahmin in secilen_kelime:
            for index, harf in enumerate(secilen_kelime):
                if harf == tahmin:
                    gorunen_kelime[index] = tahmin
            print("Doğru tahmin!")
        else:
            yanlis_tahminler += 1
            print("Yanlış tahmin!")

    if "_" not in gorunen_kelime:
        print("\nTebrikler! Kelimeyi doğru bildiniz:", secilen_kelime)
    else:
        print("\nKaybettiniz! Kelime:", secilen_kelime)

def ana_menu():
    while True:
        print("\nMini Oyunlar:")
        print("1. Tahmin Etme Oyunu")
        print("2. Adam Asmaca")
        print("3. Çıkış")
        secim = input("Bir oyun seçin (1-3): ")

        if secim == "1":
            tahmin_et()
        elif secim == "2":
            adam_asmaca()
        elif secim == "3":
            print("Oyun sona erdi. Görüşmek üzere!")
            break
        else:
            print("Geçersiz seçim, lütfen tekrar deneyin.")

ana_menu()

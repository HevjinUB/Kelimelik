import random

def kelime_sec():
    kelimeler = ["elma", "kalem", "bilgisayar", "yapayzeka", "robot"]
    return random.choice(kelimeler)

def oyunu_baslat():
    kelime = kelime_sec()
    tahmin_edilen = ["_" for _ in kelime]
    tahmin_edilen_harfler = set()
    hak = 6

    print("\n✨ Adam Asmaca Oyununa Hoş Geldiniz! ✨")
    print(" ".join(tahmin_edilen))
    
    while hak > 0 and "_" in tahmin_edilen:
        harf = input("Bir harf tahmin edin: ").lower()
        
        if len(harf) != 1 or not harf.isalpha():
            print("Lütfen sadece tek bir harf girin!")
            continue
        
        if harf in tahmin_edilen_harfler:
            print("⚠️ Bu harfi zaten tahmin ettiniz!")
            continue
        
        tahmin_edilen_harfler.add(harf)
        
        if harf in kelime:
            for i in range(len(kelime)):
                if kelime[i] == harf:
                    tahmin_edilen[i] = harf
            print("✔️ Doğru!", " ".join(tahmin_edilen))
        else:
            hak -= 1
            print(f"❌ Yanlış! Kalan hakkınız: {hak}")
    
    if "_" not in tahmin_edilen:
        print("🎉 Tebrikler! Kelimeyi buldunuz: ", kelime)
    else:
        print("💀 Oyunu kaybettiniz! Kelime şuydu:", kelime)

if __name__ == "__main__":
    oyunu_baslat()

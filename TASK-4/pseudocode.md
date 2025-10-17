Başla

Değişkenler:
    ogrenciAdi ← ""
    ogrenciNo ← ""
    mevcutDersler ← ["Matematik", "Fizik", "Algoritmalar", "Tarih"]
    secilenDersler ← boş liste

Ekrana yaz "Ad Soyad giriniz:"
ogrenciAdi ← kullanıcıdan giriş al

Ekrana yaz "Öğrenci Numaranızı giriniz:"
ogrenciNo ← kullanıcıdan giriş al

Ekrana yaz "Alabileceğiniz dersler:"
mevcutDersleri listele

Ders ekleme döngüsü:
Tekrarla
    Ekrana yaz "Bir ders seçin (bitirmek için 'q' yazın):"
    ders ← kullanıcıdan giriş al

    Eğer ders = 'q' ise
        döngüden çık
    Eğer ders mevcutDersler içinde değilse
        Ekrana yaz "Geçersiz ders!"
    Aksi halde
        Eğer ders zaten secilenDersler içinde ise
            Ekrana yaz "Bu dersi zaten seçtiniz."
        Aksi halde
            secilenDersler listesine dersi ekle
            Ekrana yaz "Ders eklendi."

Döngü sonu

Eğer secilenDersler boşsa
    Ekrana yaz "Hiç ders seçmediniz."
Aksi halde
    Ekrana yaz "Ders kaydınız başarıyla tamamlandı:"
    Seçilen dersleri listele

Bitir

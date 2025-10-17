Başla

Değişkenler:
    adSoyad ← ""
    TC ← ""
    bolum ← ""
    tarih ← ""
    saat ← ""

Ekrana yaz "Ad Soyad giriniz:"
adSoyad ← kullanıcıdan giriş al

Ekrana yaz "TC Kimlik Numarası giriniz:"
TC ← kullanıcıdan giriş al

Ekrana yaz "Randevu alınacak bölümü seçiniz (Örn: Kardiyoloji, Dahiliye, vb.):"
bolum ← kullanıcıdan giriş al

Ekrana yaz "Randevu tarihi giriniz (GG/AA/YYYY):"
tarih ← kullanıcıdan giriş al

Ekrana yaz "Randevu saati giriniz (Örn: 10:30):"
saat ← kullanıcıdan giriş al

Eğer girilen bilgiler eksikse
    Ekrana yaz "Lütfen tüm bilgileri eksiksiz giriniz."
Aksi halde
    Randevuyu kaydet
    Ekrana yaz "Randevunuz başarıyla oluşturuldu!"
    Ekrana yaz "Ad: " & adSoyad
    Ekrana yaz "Bölüm: " & bolum
    Ekrana yaz "Tarih: " & tarih & " Saat: " & saat

Bitir

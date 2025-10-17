Başla

Sepet ← boş liste
toplamTutar ← 0

Tekrarla
    Ekrana yaz "Ürün adı giriniz (çıkmak için 'q' yazın):"
    urun ← kullanıcıdan giriş al

    Eğer urun = 'q' ise
        Döngüden çık
    Aksi halde
        Ekrana yaz urun & " ürününün fiyatını giriniz:"
        fiyat ← kullanıcıdan fiyat al

        Sepete urun ve fiyatı ekle
        toplamTutar ← toplamTutar + fiyat

Döngü sonu

Eğer Sepet boş ise
    Ekrana yaz "Sepetiniz boş. Alışveriş yapmadınız."
Aksi halde
    Ekrana yaz "Sepetinizdeki ürünler:"
    Her ürün için:
        Ürün adını ve fiyatını yazdır
    Ekrana yaz "Toplam Tutar: " & toplamTutar & " TL"
    Ekrana yaz "Satın almak istiyor musunuz? (evet/hayır)"
    cevap ← kullanıcıdan giriş al

    Eğer cevap = "evet" ise
        Ekrana yaz "Satın alma işlemi başarılı!"
    Aksi halde
        Ekrana yaz "Satın alma iptal edildi."

Bitir

Başla

Değişkenler:
    bakiye ← 5000  // Başlangıç bakiyesi
    cekilecekTutar ← 0

Ekrana yaz "Lütfen çekmek istediğiniz tutarı giriniz:"
cekilecekTutar ← kullanıcıdan giriş al

Eğer cekilecekTutar ≤ 0 ise
    Ekrana yaz "Geçersiz tutar girdiniz. Lütfen pozitif bir tutar girin."
Aksi halde eğer cekilecekTutar > bakiye ise
    Ekrana yaz "Yetersiz bakiye."
Aksi halde
    bakiye ← bakiye - cekilecekTutar
    Ekrana yaz cekilecekTutar & " TL başarıyla çekildi."
    Ekrana yaz "Kalan bakiye: " & bakiye
Son

Bitir

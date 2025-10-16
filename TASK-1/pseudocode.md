

Kaan Mert Keklik 
Öğr No:250541053
ATMDEN PARA ÇEKME ALGORİTMASI SÖZDE KODLAR

Başla

Kart takıldı mı?
    Evetse devam et
    Hayırsa bekle

PIN_kodu_gir
PIN_dogrulama_hakki = 3

PIN doğru mu?
    Evetse devam et
    Hayırsa
        PIN_dogrulama_hakki -= 1
        PIN_dogrulama_hakki > 0 ise tekrar PIN iste
        Aksi halde
            "Kart bloke edildi" mesajı göster
            Kartı iade et
            Bitir

Çekilecek_miktarı_gir

Eğer Çekilecek_miktar > Bakiye ise
    "Yetersiz bakiye" mesajı göster
    Kartı iade et
    Bitir

Aksi halde
    Bakiyeden Çekilecek_miktar düş
    Nakit ver
    "İşlem başarılı" mesajı göster
    Kartı iade et

Bitir


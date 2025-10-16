BAŞLA

// 1. Kullanıcıdan giriş bilgileri alınır
KartıTak()
PIN = PIN_kodu_gir()

EĞER PIN geçerliyse
    GirişBaşarılı = TRUE
DEĞİLSE
    GirişBaşarılı = FALSE
    HATA_MESAJI("Geçersiz PIN. Lütfen tekrar deneyin.")
    DUR

// 2. Para çekme işlemi başlatılır
EĞER GirişBaşarılı ise
    Bakiye = HesapBakiyesiniGetir()
    ParaÇekmeTutarı = TutarGir("Çekmek istediğiniz tutarı girin: ")

    // 3. Tutar geçerli mi?
    EĞER ParaÇekmeTutarı <= 0
        HATA_MESAJI("Geçersiz tutar.")
        DUR
    SON

    // 4. Yeterli bakiye kontrolü
    EĞER ParaÇekmeTutarı <= Bakiye
        // 5. ATM'nin para durumu kontrol edilir
        EĞER ATMParaStokuYeterliMi(ParaÇekmeTutarı) == TRUE
            Bakiye = Bakiye - ParaÇekmeTutarı
            GüncelBakiyeyiKaydet(Bakiye)
            ParayıVer(ParaÇekmeTutarı)
            MesajGöster("Lütfen paranızı alınız.")
        DEĞİLSE
            HATA_MESAJI("ATM’de yeterli miktarda nakit yok.")
        SON
    DEĞİLSE
        HATA_MESAJI("Yetersiz bakiye.")
    SON
SON

KartıÇıkar()
MesajGöster("İyi günler!")
DUR

BİTİR





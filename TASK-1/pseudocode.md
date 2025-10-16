BAŞLA

  KARTI_TAK()

  PIN = PIN_GİR()

  EĞER PIN_DOĞRU(PIN) DEĞİLSE
    HATA_MESAJI_GÖSTER("Hatalı PIN. Lütfen tekrar deneyin.")
    PIN = PIN_GİR()
    
    EĞER PIN_DOĞRU(PIN) DEĞİLSE
      HATA_MESAJI_GÖSTER("Hatalı PIN. Kart iade ediliyor.")
      KART_IADESI()
      BİTİR
    SON
  SON

  İŞLEM_SEÇ = MENÜ_GÖSTER(["Para Çekme", "Bakiye Sorgulama", "Çıkış"])

  EĞER İŞLEM_SEÇ == "Para Çekme" İSE
    TUTAR = TUTAR_GİR()
    
    EĞER BAKİYE_YETERLİ(TUTAR) DEĞİLSE
      HATA_MESAJI_GÖSTER("Yetersiz bakiye.")
      KART_IADESI()
      BİTİR
    SON

    PARA_VER(TUTAR)
    BAKİYE_GÜNCELLE(TUTAR)

  DEĞİLSE EĞER İŞLEM_SEÇ == "Bakiye Sorgulama" İSE
    BAKİYE = BAKİYE_GÖRÜNTÜLE()
    BAKİYE_GÖSTER(BAKİYE)

  DEĞİLSE
    MESAJ_GÖSTER("İşlem iptal edildi.")
  SON

  KART_IADESI()

BİTİR

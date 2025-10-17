Başla

Durumlar:
    sistemAktif ← false
    hareketAlgilandi ← false
    alarmCalıyor ← false

Ekrana yaz "Güvenlik sistemini başlatmak istiyor musunuz? (evet/hayır)"
cevap ← kullanıcıdan giriş al

Eğer cevap = "evet" ise
    sistemAktif ← true
    Ekrana yaz "Güvenlik sistemi aktif."

Eğer sistemAktif = true ise
    Sürekli:
        hareketAlgilandi ← sensörden veri al

        Eğer hareketAlgilandi = true ise
            alarmCalıyor ← true
            Ekrana yaz "Hareket algılandı! Alarm çalışıyor!"
            Kullanıcıya bildirim gönder
            Kamera kaydını başlat
            Kullanıcıdan alarmı durdurmak için şifre al

            Eğer şifre doğruysa
                alarmCalıyor ← false
                Ekrana yaz "Alarm durduruldu."
            Aksi halde
                Ekrana yaz "Yanlış şifre! Alarm çalmaya devam ediyor."
        Aksi halde
            Ekrana yaz "Her şey normal. Sistem izliyor..."
        Kısa süre bekle (örn. 5 saniye)

Aksi halde
    Ekrana yaz "Sistem pasif. Güvenlik devrede değil."

Bitir

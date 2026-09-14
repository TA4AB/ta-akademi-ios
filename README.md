# TA Akademi - Amatör Telsizcilik Eğitim Uygulaması

<div align="center">
  <img src="https://img.shields.io/badge/Platform-iOS%2016.0%2B-blue.svg" alt="Platform">
  <img src="https://img.shields.io/badge/Swift-5.9-orange.svg" alt="Swift">
  <img src="https://img.shields.io/badge/License-Proprietary-red.svg" alt="License">
</div>

## 📡 Genel Bakış

**TA Akademi**, Türkiye'deki amatör telsizcilik sınavına hazırlanan adaylar için tasarlanmış kapsamlı bir iOS eğitim uygulamasıdır. Uygulama, KEGM ve MEB sınav müfredatını kapsayan 56 eğitim konusu, interaktif Mors kodu antrenmanı ve pratik araçlar sunmaktadır.

### ✨ Özellikler

#### 📚 Eğitim Modülü
- **56 Kapsamlı Konu**: Yönetmelik, Elektronik, Yayılım, Anten, Operatörlük kategorileri
- **Filtreleme ve Arama**: Kategoriye göre filtreleme, anahtar kelime araması
- **Okuma Süresi Göstergesi**: Her konu için tahmini okuma süresi
- **Çevrimdışı Erişim**: Tüm içerik cihazda saklanır, internet bağlantısı gerektirmez

#### 📝 Sınav Sistemi
- **3 Kategori**: Kolay, Orta, Zor
- **Her Kategoride 56 Soru**: Toplam 168 soru bankası
- **Gerçek Sınav Formatı**: 50 soruluk sınav simülasyonu
- **Detaylı İstatistikler**: Başarı oranı, doğru/yanlış sayısı, kategori bazlı performans
- **Anında Geri Bildirim**: Her sorunun doğru cevabı ve açıklaması

#### 🔊 Mors Kodu Eğitimi
- **Tam Alfabe**: A-Z, 0-9 karakterleri
- **3 Seviye Antrenman**: Yavaş, Normal, Hızlı
- **Ses Tonu Ayarı**: 600 Hz profesyonel ses tonu
- **İki Yönlü Çevirici**: Metin → Mors ve Mors → Metin
- **İnteraktif Pratik**: Sesli Mors dinleme ve tanıma

#### 🛠️ Pratik Araçlar
1. **ISS Uydu Takibi**: Uluslararası Uzay İstasyonu geçiş tahminleri
2. **QTH Locator**: Maidenhead grid hesaplayıcı
3. **Çağrı İşareti Sorgulama**: TRAC veritabanı entegrasyonu
4. **Propagasyon Haritası**: HF yayılım koşulları
5. **APRS Mesajlaşma**: Konumsal mesaj göndericisi
6. **Anten Hesaplayıcı**: Dipol, Yagi, Ground Plane
7. **Sınav Rehberi**: KEGM ve MEB sınav bilgileri
8. **Daha Fazlası**: 12 farklı araç

#### 🎨 Kullanıcı Deneyimi
- **Modern SwiftUI Tasarım**: Fluid animasyonlar ve gradient efektler
- **Karanlık/Aydınlık Tema**: Sistem temasıyla uyumlu
- **iPad Optimizasyonu**: Responsive tasarım, büyük ekranlar için optimize edilmiş
- **Erişilebilirlik**: VoiceOver desteği, dinamik font boyutları
- **Hızlı Erişim Kartları**: Ana sayfadan tek dokunuşla erişim

## 📋 Sistem Gereksinimleri

- **iOS**: 16.0 veya üzeri
- **Cihazlar**: iPhone, iPad
- **Depolama**: ~50 MB
- **İnternet**: Yalnızca ilk indirme için gerekli (bazı araçlar için opsiyonel)

## 🏗️ Teknik Yapı

### Kullanılan Teknolojiler
- **Framework**: SwiftUI
- **Minimum Deployment**: iOS 16.0
- **Architecture**: MVVM Pattern
- **Data Persistence**: UserDefaults, Local JSON
- **In-App Purchases**: StoreKit 2
- **Ads**: Google AdMob
- **Audio**: AVFoundation (Mors ses sentezi)
- **Location**: CoreLocation (ISS tracking, QTH locator)

### Proje Yapısı
```
TAAkademi/
├── TAAkademiApp.swift          # Ana uygulama giriş noktası
├── ContentView.swift            # Tab bar controller
├── Managers/
│   ├── IAPManager.swift         # In-App Purchase yönetimi
│   └── AdMobManager.swift       # Reklam yönetimi
├── Models/
│   ├── TopicData.swift          # Eğitim içeriği
│   ├── ExamData.swift           # Sınav soruları
│   ├── QuestionBankData.swift   # Soru bankası
│   └── MorseData.swift          # Mors alfabesi
├── Views/
│   ├── Home/                    # Ana sayfa
│   ├── Education/               # Eğitim modülü
│   ├── Exam/                    # Sınav modülü
│   ├── Morse/                   # Mors antrenör
│   ├── Tools/                   # Araçlar
│   └── About/                   # Hakkında & Ayarlar
├── Utilities/
│   ├── PrefsManager.swift       # Kullanıcı tercihleri
│   ├── MorseAudioPlayer.swift   # Mors ses motoru
│   └── ThemeColors.swift        # Tema renkleri
└── Info.plist
```

## 📱 Kurulum

### Xcode ile Çalıştırma
1. Xcode 15.0 veya üzeri gereklidir
2. Projeyi klonlayın:
```bash
git clone https://github.com/TA4AB/ta-akademi.git
cd ta-akademi/TAAkademi
```
3. `TAAkademi.xcodeproj` dosyasını açın
4. Bundle Identifier'ı değiştirin (gerekirse)
5. Signing & Capabilities'i yapılandırın
6. Simulator veya gerçek cihazda çalıştırın

### App Store'dan İndirme
Uygulama Apple App Store'da yayında:
- **Bundle ID**: `com.arsesoft.TAAkademi`
- **Version**: 1.0.2

## 🎯 Kullanım

### İlk Başlangıç
1. Uygulamayı açın
2. Ana sayfada hızlı erişim kartlarını kullanarak modüllere erişin
3. Eğitim → Konuları okumaya başlayın
4. Sınav → Bilginizi test edin
5. Mors → Mors kodunu öğrenin

### Sınav Hazırlığı
1. **Eğitim Modülü**: 56 konuyu sırayla okuyun
2. **Soru Bankası**: Her kategorideki soruları çözün
3. **Deneme Sınavları**: 50 soruluk gerçek sınav simülasyonu
4. **Mors Antrenmanı**: En az 12 WPM hıza ulaşın (sınav gereksinimi)
5. **Araçlar**: Pratik bilgilerinizi pekiştirin

## 🔐 Gizlilik & Güvenlik

- **Veri Toplama**: Minimal veri toplama (yalnızca IAP ve reklam için)
- **Çevrimdışı Çalışma**: Tüm eğitim içeriği yerel
- **AdMob**: Google AdMob reklamları gösterilir
- **IAP**: Reklamları kaldırma seçeneği (opsiyonel)
- **Konum**: Yalnızca ISS tracking ve QTH locator için (izinle)

Detaylı bilgi: [Gizlilik Politikası](https://www.arsesoft.com/privacy-policy)

## 📞 Destek & İletişim

### Geliştirici
**Arif Onur Bütün (TA4AB)**  
Bireysel Uygulama Geliştirici

### İletişim Kanalları
- **E-posta**: info@arsesoft.com
- **Web**: [www.arsesoft.com](https://www.arsesoft.com)
- **Destek**: [www.arsesoft.com/support](https://www.arsesoft.com/support)
- **Instagram**: [@arifbutuns](https://www.instagram.com/arifbutuns)
- **Instagram**: [@arse.soft.technology](https://www.instagram.com/arse.soft.technology)

### Hata Bildirimi
Hata veya öneri bildirmek için:
1. E-posta: info@arsesoft.com
2. Konu: "TA Akademi - [Hata/Öneri]"
3. Açıklama: Detaylı açıklama, ekran görüntüsü, cihaz bilgisi

## 🙏 Teşekkürler

### Katkıda Bulunanlar
- **Aren SADE (TA4PWB)** - İçerik danışmanlığı
- **Anıl ÖZER (TA4JEO)** - Teknik danışmanlık
- **Amazon Web Services (AWS)** - Hosting desteği
- **Tekser Elektronik Sistemler** - Sponsorluk

### Kaynaklar
- **KEGM** - Kıyı Emniyeti Genel Müdürlüğü
- **MEB** - Milli Eğitim Bakanlığı
- **TRAC** - Türkiye Radyo Amatörleri Cemiyeti
- **BTK** - Bilgi Teknolojileri ve İletişim Kurumu

## 📄 Lisans

Bu yazılım telif hakkı koruması altındadır.  
© 2026 Arif Onur Bütün (TA4AB) - Arsesoft. Tüm hakları saklıdır.

**Bireysel Geliştirici Uygulaması** - Ticari kullanım için izin gereklidir.

## 🔄 Sürüm Geçmişi

### v1.0.2 (2026-09-14)
- 🎨 iPad arayüz optimizasyonu
- 🛠️ IAP hata yönetimi iyileştirmeleri
- 🔗 Destek URL'si güncellendi
- 📱 Responsive tasarım geliştirmeleri

### v1.0.1 (2026-09-05)
- 🐛 Mors ses motoru hata düzeltmeleri
- ⚡ Performans iyileştirmeleri
- 🎨 UI/UX iyileştirmeleri

### v1.0.0 (2026-09-01)
- 🎉 İlk yayın
- 📚 56 eğitim konusu
- 📝 168 sınav sorusu
- 🔊 Mors kodu eğitimi
- 🛠️ 12 pratik araç

---

**73 de TA Akademi** 📡

*"Amatör Telsizcilik bilgini test et, sınavına hazırlan!"*

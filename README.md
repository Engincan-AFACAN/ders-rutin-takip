# Ders & Rutin — GitHub Pages PWA

Ders, çalışma süresi, alışkanlık, günlük not, görev, haftalık program ve istatistik takip uygulamasıdır. Ücretsiz ve üyelik gerektirmez.

## 1. GitHub Pages ile yayımlama

1. https://github.com/ adresinden oturum aç.
2. Sağ üstteki **+** > **New repository** yolunu aç.
3. `ders-rutin-takip` gibi bir depo adı seç ve **Public** olarak oluştur.
4. Dosyaları ZIP'ten çıkar. `index.html`, `styles.css`, `app.js`, `sw.js`, `manifest.webmanifest`, `README.md` ve `icons` klasörünü birlikte deponun kök dizinine yükle. **ZIP'i tek dosya olarak yükleme.**
5. Depoda **Settings > Pages > Build and deployment > Deploy from a branch** seç.
6. **Branch: main**, **Folder: /(root)** seçip kaydet.
7. Birkaç dakika sonra adres `https://KULLANICIADI.github.io/ders-rutin-takip/` biçiminde açılır. Depo adın farklıysa son kısım da farklı olur.

## 2. Telefona ekleme

- **Android Chrome:** Siteyi aç > sağ üst üç nokta > **Uygulamayı yükle** veya **Ana ekrana ekle**.
- **iPhone Safari:** Siteyi aç > **Paylaş** > **Ana Ekrana Ekle**.
- PWA kurulumu ve çevrimdışı önbellekleme için site HTTPS üzerinden (GitHub Pages gibi) açılmalıdır.

## 3. Ders saatleri

Başlangıç haftalık bireysel çalışma hedefi **15 saattir**:
- Termodinamik: **4 saat**
- Makina Elemanları: **2,5 saat**
- Lineer Cebir: **2 saat**
- Diğer dersler (özelleştir): **6,5 saat**

Son satır, adı ve süreleri doğrulanamayan diğer dersler için geçici alandır. **Ayarlar** sayfasından bu alanı silebilir, dersleri ayrı ayrı tanımlayabilir ve her birinin haftalık hedefini değiştirebilirsin.

Okul/sınıf ders saatleri, **Planım** bölümüne eklenir ve çalışma süresine otomatik eklenmez.

## 4. Kayıt ve yedek

- Bütün veriler cihazın tarayıcısının `localStorage` alanındadır.
- Yeni cihazda veriler **kendiliğinden görünmez**; **Ayarlar > Yedek indir** ile JSON dosyası alıp diğer cihazda **Yedek geri yükle** seç.
- Tarayıcının site verilerini silmek mevcut kayıtları da silebilir; düzenli yedek al.
- Odak sayacı açıkken sekmeyi arka plana almak veya sayfayı yenilemek geçen süreyi kaybettirmez.
- Odak sayacının kaydedildiği an haftalık ilerlemeye katkı yapar. Görevleri işaretlemek süre eklemez.

## 5. Yerel test

`index.html` çift tıklamayla temel takip için açılabilir. PWA'yı tam test etmek için bu dizinde bir yerel sunucu çalıştır:

```bash
python -m http.server 8000
```

Ardından `http://localhost:8000/` adresini aç. Service worker localhost'ta çalışır. GitHub Pages'de HTTPS otomatik sağlanır.

## Not

Bu uygulama Google arama sonuçlarında otomatik olarak görünmeyi garanti etmez. Adres herkesle paylaşılabilir; arama dizinine eklenme Google'ın taramasına bağlıdır. Ayrıca kod dosyalarını herkese açık depoya yüklemek **kullanıcının yerel görevlerini ve notlarını yayımlamaz**.

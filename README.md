# Odak Planlayıcı

Pomodoro tekniğiyle çalışan görev planlayıcı ve odak sayacı. Görevleri önem rengine göre toplar, günün planını yapar ve planı odak ile mola süreleri arasında kendiliğinden ilerleyen bir sayaçla çalıştırır.

## Özellikler

- **Görevler:** Görevin adı, önem rengi (kırmızı: mutlaka yapılacak, turuncu: orta önemde, yeşil: daha az önemli), tahmini süresi ve giriş tarihi girilir. Görevler her renk grubunun içinde sıralanabilir.
- **Planla:** Bir gün için görev havuzundan seçim yapılır, sıra ve süreler ayarlanır. "Önceliğe göre doldur", seçilen hedef süreye (örneğin 2 saat) kırmızıdan başlayarak sığan görevleri ekler. Planın kaç pomodoro ve mola sürdüğü, saat saat akışı ve tahmini bitiş saati gösterilir.
- **Pomodoro sayacı:** Odak süresi bitince mola, mola bitince odak kendiliğinden başlar ve her geçişte ses çalar. Odak süresi, kısa mola, uzun mola ve uzun molanın kaç pomodoroda bir verileceği seçilebilir.
- **Hafta:** Günlere göre planlar yan yana görünür.
- **Arşiv:** Görevler giriş tarihine göre listelenir. Ada göre arama yapılabilir; renge ve duruma göre süzülebilir. Tamamlanma zamanı ve çalışılan süre de görünür.
- **Yedek:** Arşiv sekmesinden tüm veriler bir JSON dosyası olarak indirilip geri yüklenebilir.

## Dosyalar

| Dosya | Görevi |
|---|---|
| `index.html` | Uygulamanın tamamı (HTML, CSS, JavaScript) |
| `manifest.webmanifest` | Ana ekrana eklenince uygulama adı, simgesi ve görünümü |
| `sw.js` | Uygulamanın bir kez açıldıktan sonra internetsiz de çalışmasını sağlar |
| `apple-touch-icon.png` | iPhone ana ekran simgesi |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Tarayıcı ve Android simgeleri |

## GitHub Pages ile yayınlama

1. GitHub'da yeni bir depo oluştur, örneğin `odak-planlayici`.
2. Tüm dosyaları deponun ana dizinine yükle. Klasör gerekmez; hepsi `index.html` ile yan yana durur.
3. Depoda **Settings → Pages** bölümüne gir. **Source** olarak "Deploy from a branch", dal olarak `main` ve klasör olarak `/ (root)` seç, sonra kaydet.
4. Bir iki dakika içinde uygulama `https://KULLANICI-ADIN.github.io/odak-planlayici/` adresinde açılır.

## iPhone'a kurulum

1. Adresi **Safari**'de aç.
2. Paylaş düğmesine dokun ve **Ana Ekrana Ekle**'yi seç.
3. Uygulama, ana ekranda "Odak" adıyla kendi simgesiyle görünür ve tam ekran açılır.

iPhone simgeyi yalnızca ana ekrana eklerken bir kez alır. Simge dosyalarını sonradan yüklediysen ana ekrandaki eski kısayolu sil ve yeniden ekle.

## Bilinmesi gerekenler

- **Veriler cihazda saklanır.** Veriler tarayıcının yerel deposunda tutulur ve cihazlar arasında eşitlenmez. Ana ekrana eklenen uygulamanın deposu, Safari'deki sayfanınkinden ayrıdır. Düzenli olarak Arşiv'den yedek al.
- **Ekran açık kalmalı.** Sayaç ve sesler yalnızca uygulama açıkken çalışır. Uygulama program sürerken ekranın kapanmasını engellemeye çalışır. Ekran kilitlenirse sayaç kaldığı yerden doğru süreyle devam eder, ama arada ses çalmaz.
- **Ses için dokunma gerekir.** iOS, sesin çalabilmesi için sayfaya en az bir kez dokunulmasını ister. Programı başlatma düğmesi bunu sağlar.
- **Güncelleme:** Dosyaları değiştirip yeniden yüklediğinde uygulama, internete bağlıyken bir sonraki açılışta yeni sürümü alır. Değişiklik görünmezse uygulamayı tamamen kapatıp yeniden aç.

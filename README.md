# DiyetDegisim

Diyetisyen listesini değişim (porsiyon eşdeğeri) mantığıyla gösteren tek sayfalık bir site.

## Neler yapar

- Öğün kalemleri aynı gruptaki başka besinlerle değiştirilebilir ya da birkaç besine bölünebilir; miktarlar otomatik hesaplanır. Bir kalem doluyken bir besine **+** basınca en çok seçili diğer besin otomatik azalır, toplam değişmez.
- Her profil kendi **e-posta ve şifresiyle** girer. Herkes yalnızca kendi listesini görür ve değiştirir; liste hesaba kaydedilir, aynı hesapla girilen her cihazda görünür.
- **Diyetisyen listesini fotoğraftan ekleme:** listenin fotoğrafı telefonda okunur (açık kaynak Tesseract yazı tanıma, ücretsiz), öğünler ve değişim sayıları otomatik çıkarılır: "6 yemek kaşığı pilav" → 3 ekmek değişimi. Kaydetmeden önce sonuç gösterilir, yanlış okunan düzeltilir. Metni yapıştırarak da eklenebilir.
- Kaydedilen diyetisyen listesi o hesabın limitidir, hem öğün öğün hem günlük; değiştirirken, kalem eklerken ya da öğünler arasında kaydırırken aşılamaz. * işaretli meyveler her profilde günde en fazla 1 porsiyon.
- Berkay Er'in listesi (Et 9, Süt 2, Sebze 2, Meyve 2, Ekmek 12, Yağ 1) yalnızca onun hesabına yüklenir.
- Değişim tabloları (et, süt, sebze, meyve, ekmek, yağ) ve diyet kuralları giriş yapmadan da görülebilir.

## Kullanım

Siteyi aç: `https://erberkay.github.io/DiyetDegisim/`. "Hesap oluştur" ile e-posta ve şifre belirle, sonra listeni seç.

## Altyapı

- Giriş ve veriler Firebase projesi **diyetdegisim** üzerinde (Authentication: e-posta/şifre, Cloud Firestore).
- Her hesabın listesi `users/{uid}` belgesinde durur. Erişim kuralları `firestore.rules` dosyasında: bir hesap yalnızca kendi belgesini okuyup yazabilir.
- Kural değişikliğini yayınlamak için: `firebase deploy --only firestore,auth --project diyetdegisim`

## GitHub Pages

Site `main` dalının kökünden yayınlanır: **Settings > Pages > Branch: main / root**.

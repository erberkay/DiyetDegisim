# DiyetDegisim

Diyetisyen listesini değişim (porsiyon eşdeğeri) mantığıyla gösteren tek sayfalık bir site.

## Neler yapar

- Öğün kalemleri aynı gruptaki başka besinlerle değiştirilebilir ya da birkaç besine bölünebilir; miktarlar otomatik hesaplanır.
- Berkay Er'in listesindeki günlük değişim sayıları (Et 9, Süt 2, Sebze 2, Meyve 2, Ekmek 12, Yağ 1) üst sınırdır; değiştirirken ya da kalem eklerken aşılamaz. * işaretli meyveler günde en fazla 1 porsiyon.
- 3 profil var: **Berkay Er** (liste yüklü), **Profil 2** ve **Profil 3**.
- Değişim tabloları (et, süt, sebze, meyve, ekmek, yağ) ve diyet kuralları sitenin içinde.

## Kullanım

`index.html` dosyasını tarayıcıda aç. Kurulum gerekmez; harici bağımlılık yok (yalnızca Google Fonts).

Veriler tarayıcıda (localStorage) saklanır. Başka cihaza taşımak için **Profili düzenle > Yedek / başka cihaza taşı** bölümünden yedeği kopyala, diğer cihazda yapıştırıp **İçe aktar**'a bas.

## GitHub Pages

Siteyi yayına almak için: **Settings > Pages > Branch: main / root**. Birkaç dakika sonra site `https://erberkay.github.io/DiyetDegisim/` adresinde açılır.

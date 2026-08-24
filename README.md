# 🎮 Oyun Takip & Kütüphane

Sürükle-bırak ile çalışan, tek dosyalık (bağımlılıksız) oyun takip listesi.
Oyunlar tarayıcının `localStorage`'ında tutulur — sunucu, hesap veya veritabanı yok.

## Özellikler

- **Dört liste:** Şu an oynananlar · Bitirilenler · Yarım kalanlar · Bekleyenler
- **Sürükle & bırak:** kartı başka listeye taşı; etiket kategoriye göre kendiliğinden güncellenir, taşınan oyun listenin en altına eklenir
- **Favoriler:** yalnızca *bitirilen* oyunlar yıldızlanabilir; favoriler listenin en üstünde görünür
- **Hızlı ekleme formu** ve kart üzerinden silme
- Bölüm başlıklarında adet sayacı

## Kullanım

`index.html` tek başına çalışır — tarayıcıda açman yeterli. Kurulum veya derleme adımı yok.

## Veri

Her şey tarayıcıda, `myGameListDragDrop_v2` anahtarında saklanır. Yani:

- Liste **cihaza/tarayıcıya özeldir**, kişiler arasında paylaşılmaz.
- İlk açılışta örnek bir liste yüklenir; kendi listeni kurmak için kartları silip yenilerini ekleyebilirsin.
- Tarayıcı verisini temizlemek listeyi de siler.

Sıfırdan başlamak için tarayıcı konsolunda:

```js
localStorage.removeItem('myGameListDragDrop_v2'); location.reload();
```

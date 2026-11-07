# — nasıl çalışır

## Yeni yazı eklemek
`_posts` klasörüne, dosya adı `YIL-AY-GUN-baslik.md` formatında yeni bir dosya oluştur. Örnek: `2026-08-10-yeni-yazim.md`

İçine şunu yapıştır, kendi bilgilerinle doldur:

```
---
layout: post
title: "Yazının Başlığı"
date: 2026-08-10
category: Pilates
published: true
---
Yazının metni buraya gelir.
```

`published: false` yaparsan yazı taslak olarak kalır, sitede görünmez. `true` yapınca yayına girer.

Yeni bir kategori kullanmak istersen, `category:` alanına istediğin ismi yaz (örn. `category: Marketing`) — Blog sayfasındaki kategori filtreleri otomatik güncellenir, ayrıca bir şey yapman gerekmez.

## Metinleri değiştirmek
`_data/strings.yml` dosyasını aç, tırnak içindeki metni değiştir, kaydet. Ana sayfa, Blog sayfası başlıkları ve buton yazıları buradan yönetiliyor.

Kategori notu eklemek istersen (örn. Bukowski atfı), aynı dosyanın en altındaki `category_notes` bölümüne ekle.

## Görsel eklemek
Görselleri `assets/img/` klasörüne koy, yazının içinde şöyle çağır:
```
![açıklama](/assets/img/gorsel-adi.jpg)
```

## Sayfa metinlerini değiştirmek (Hakkımda, Dersler, Eğitimler)
İlgili dosyayı aç (`hakkimda.md`, `studio/dersler.md`, `studio/egitimler.md`), `---` işaretlerinden sonraki metni değiştir, kaydet.

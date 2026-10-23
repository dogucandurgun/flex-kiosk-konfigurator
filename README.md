# Flex Kiosk Konfigüratörü

Flex konteyner market kiosku için tarayıcıda çalışan 3B konfigüratör. Kapılar, yakıt ödeme penceresi, tente, rampa, iç bölümler, renkler ve panel baskıları sayfa üzerinden değiştirilebilir.

## Çalıştırma

Sayfa statik dosyalardan oluşur, bir web sunucusundan açılması yeterlidir. Dosyaya çift tıklayarak açıldığında model yüklenmez.

```bash
python3 -m http.server 8000
```

Ardından tarayıcıda `http://localhost:8000` adresini aç.

## Bir web sitesine ekleme

Klasörün tamamı sitenin sunucusuna, örneğin `/kiosk/` altına kopyalanır. Mevcut bir sayfaya gömmek için:

```html
<iframe src="/kiosk/" title="Flex Kiosk Konfigüratörü" style="width:100%;height:720px;border:0" allow="fullscreen"></iframe>
```

## İçerik

- `index.html`: Uygulamanın tamamı.
- `assets/kiosk/`: Tasarım modelinden dönüştürülen kiosk modeli ve dokuları.
- `assets/tex/`, `assets/hdri/`: Zemin dokuları ve gökyüzü (Poly Haven, CC0).
- `.nojekyll`: GitHub Pages'in alt çizgiyle başlayan doku dosyalarını yayınlaması için gerekli.

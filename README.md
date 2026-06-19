# Trend-gsm.v1
telefoncu web sayfası

## Fiyat veritabanını güncelleme

Fiyatlar `data/prices.csv` dosyasından okunur. Excel, Google Sheets veya Numbers ile açıp düzenleyebilirsin.

Sütunlar:
- `Marka` — örn. iPhone, Samsung
- `Model` — örn. iPhone 13
- `Islem` — sabit kodlardan biri: `ekran`, `batarya`, `sarj`, `arkaCam`, `kamera`, `hoparlor`
- `ParcaFiyatiUSD` — parça maliyeti (dolar)
- `IscilikUSD` — işçilik (dolar)
- `KargoUSD` — kargo maliyeti (dolar)

Web sayfası bu üç dolar değerini toplar, güncel USD/TRY kurunu otomatik çeker (kur servisine ulaşılamazsa yaklaşık sabit kur kullanılır) ve sonucu en yakın 100 TL'ye yukarı yuvarlayarak gösterir. Toplam fiyat sütunu eklemene gerek yok, otomatik hesaplanır.

Yeni marka/model eklemek için tabloya yeni satırlar eklemen yeterli — site dosyayı her açılışta okur, kod değiştirmen gerekmez.

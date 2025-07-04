ARA ÇIKTI RAPORU
Fog Önleme Sensör Sistemi (ESP32 tabanlı)
Tarih : 4 Temmuz 2025

1 | Proje Amacı
Soğuk oda içinde oluşan fog (yoğuşma) riskini ortadan kaldırmak için 

sıcaklık & nem değerlerini gerçek‑zamanlı izleyen,

seçilecek haberleşme altyapısıyla (Wi‑Fi/MQTT/Node‑RED) uzaktan raporlayan,

ileri aşamada ısıtıcı / soğutucu aktüatörleri otomatik yönetecek
bir gömülü sistem prototipi geliştirmek.

2 | Zaman Çizelgesi ve Ara Çıktılar
(Başlangıç: 7 Temmuz 2025, haftalar pazartesi – pazar olarak planlandı.)

No	İş Paketi	Süre	Takvim	Ara Çıktı / Başarı Kriteri
1	ESP32 + Isı Sensörü Denemeleri	1 hafta	7 → 13 Tem 2025	- DS18B20 ölçüm kodu
- Seri ekranda sıcaklık akışı
- Ölçüm doğruluk tablosu (±0.5 °C)
2	ESP32 + Nem Sensörü Denemeleri	1 hafta	14 → 20 Tem 2025	- SHT31 / DHT22 okuma kodu
- RH verisi kaydı
- Sensör kararlılık raporu
3	Isı + Nem Sensörlerini Birlikte Çalıştırma	1 hafta	21 → 27 Tem 2025	- Ortak I²C/OneWire çalışması
- Çiğ noktası (Td) hesap fonksiyonu
- CSV veri dosyası
4	MQTT · Wi‑Fi · Node‑RED Karşılaştırması	2 gün	28 → 29 Tem 2025	- Kısa döküman: mimari farklar
- Demo: MQTT Explorer & Node‑RED dashboard ekran görüntüsü
5	Haberleşme Yöntemine Karar	1 hafta	30 Tem → 5 Ağu 2025	- Seçilen yöntem (örn. Wi‑Fi + MQTT)
- Bağlantı güvenliği taslağı
- Broker bağlantı testi
6	Sistemin Son Hali & Saha Denemeleri	1 hafta	6 → 12 Ağu 2025	- Prototip kutu montajı
- 48 saatlik veri log’u
- İlk fog‑önleme algoritması taslağı
- Sunum slaydı (gelecek faz için öneriler)

3 | Kritik Noktalar & Riskler
Başlık	Açık / Risk	Önlem
Sensör kalibrasyonu	±1 °C / ±3 %RH üzerinde sapma oluşabilir	Referans termometre‑higrometre ile çapraz test
Güç bütçesi	Sonradan eklenecek Peltier + ısıtıcı yüksek akım çeker	12 V / 6 A adaptör + ayri buck dönüştürücü
MQTT güvenliği	Şirket ağına TLS’siz erişim kabul edilmeyebilir	TLS 1.3 + kullanıcı/parola + ağ VLAN’ı
Veri kaybı	Wi‑Fi kesintisi	Yerel SD kart tamponu (paket 6’da)

4 | İleri Aşamada Planlanan Adımlar (Özet)
PID tabanlı sıcaklık‑nem denetimi (heater / Peltier kontrolü)

Fog alarm eşikleri → Node‑RED üzerinden e‑posta / SMS bildirimi

Kutu izolasyonu & anti‑fog kaplama testleri

Uzun süreli (1 hafta) saha testi → enerji tüketimi & performans raporu
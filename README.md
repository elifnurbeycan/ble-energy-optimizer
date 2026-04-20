# Akıllı Enerji Yönetim Sistemleri  
## IoT & Makine Öğrenmesi Entegrasyonu ile BLE Cihazlarında Enerji ve Performans Optimizasyonu

---

## Grup Bilgileri

**Grup:** 1  

**Grup Üyeleri:**
- Fatma Nur Yazıcı    
- Elif Nur Beycan  
- Nermin Baycan 
- Mualla Gülsüm Çapar 

---

## Proje Özeti

Bu projede, **Bluetooth Low Energy (BLE)** tabanlı IoT cihazlarında  
**enerji tüketimi ile bağlantı kalitesi (QoS)** arasındaki dengeyi sağlamak amacıyla  
**veriye dayalı ve dinamik bir enerji yönetim sistemi** geliştirilmiştir.

Klasik **statik güç seviyesi** yaklaşımlarının aksine, sistem ortam koşullarını analiz ederek  
**cihazın ihtiyacı olan kadar enerji harcamasını** hedeflemektedir.

---

## Problem Tanımı

Statik BLE sistemlerinde enerji yönetimi aşağıdaki temel ikilemle karşı karşıyadır:

- 🔋 Düşük enerji tüketimi → Zayıf bağlantı kalitesi  
- 📶 Yüksek bağlantı kalitesi → Artan batarya tüketimi  

Bu proje, söz konusu ikilemi **makine öğrenmesi destekli adaptif bir karar mekanizması** ile çözmeyi amaçlamaktadır.

---

## Sistem Mimarisi

### TX (Verici)

- BLE üzerinden yayın yapan IoT cihazıdır
- Duty Cycle seviyeleri (**L0, L1, L2**) arasında dinamik geçiş yapar
- Yayın gücü, RX tarafından verilen karara göre ayarlanır

### RX (Alıcı)

- BLE sinyallerini dinler
- RSSI ve Advertising Rate verilerini toplar
- Makine öğrenmesi modeli ile **optimal güç seviyesini** belirler

### İletişim Yapısı

- Bluetooth Low Energy (BLE)
- TX ve RX arasında HTTP tabanlı kontrol mekanizması

---

## Metodoloji

### Duty Cycle (L-Level) Yaklaşımı

Batarya tüketimini simüle etmek için cihazın aktif kalma süresi (duty cycle) kontrollü olarak değiştirilmiştir.  
10 saniyelik zaman pencereleri içerisinde **iletişim (on)** ve **uyku (off)** süreleri düzenlenmiştir.

| Seviye | Enerji Tüketimi | Amaç |
|------|----------------|------|
| L0 | Düşük | Maksimum enerji tasarrufu |
| L1 | Orta | Dengeli performans |
| L2 | Yüksek | Maksimum bağlantı kalitesi |

---

## Toplanan Veri Parametreleri

Çalışma kapsamında aşağıdaki parametreler toplanmış ve analiz edilmiştir:

- RSSI (Received Signal Strength Indicator)
- Advertising Rate
- Mesafe
- TX güç seviyesi
- Zaman bilgisi

Veriler CSV formatında kaydedilmiştir.

---

## Makine Öğrenmesi Modeli

**Kullanılan Model:** Decision Tree  

### Model Girdileri
- Mesafe
- RSSI
- Advertising Rate

### Model Çıktısı
- Optimal güç seviyesi (**L0 / L1 / L2**)

### Model Tercih Nedeni
- Hafif ve hızlı çalışması
- Mikrodenetleyici tabanlı sistemler için uygun olması
- Karar mekanizmasının kolay yorumlanabilir olması

---

## Elde Edilen Kazanımlar

- Statik BLE sistemlerine kıyasla **daha verimli enerji kullanımı** sağlanmıştır
- Ortam koşullarına uyum sağlayabilen **adaptif BLE iletişimi** elde edilmiştir
- IoT ve makine öğrenmesi entegrasyonunun **gerçek zamanlı bir uygulaması** gerçekleştirilmiştir
- Akademik çalışmalar ve endüstriyel uygulamalar için **ölçeklenebilir bir sistem** geliştirilmiştir

---

## Sonuç

Bu çalışma, BLE tabanlı IoT sistemlerinde  
**enerji ve performans optimizasyonunun**,  
**makine öğrenmesi destekli karar mekanizmaları** ile  
başarılı bir şekilde gerçekleştirilebileceğini ortaya koymaktadır.

---

## Teşekkürler

Projeye katkı sağlayan tüm ekip üyelerine teşekkür ederiz.

**Grup 1 – Akıllı Enerji Yönetim Sistemleri**

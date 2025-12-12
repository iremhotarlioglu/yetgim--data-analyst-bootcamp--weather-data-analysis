# yetgim--data-analyst-bootcamp--weather-data-analysis
Pandas ve NumPy kullanarak Türkiye'deki illere ait hava durumu verilerinin temel analizi ve manipülasyonu.

# ⛈️ YETGİM Data Analyst Bootcamp - Hava Durumu Veri Analizi

Bu proje, Yetgim Power Bi & Tableau bootcamp ödevi kapsamında hazırlanmıştır. Amacı, sunulan 'weather_data.csv' dosyasını kullanarak Pandas ve NumPy kütüphaneleriyle temel veri manipülasyonu, filtreleme, analiz ve raporlama becerilerini göstermektir.

## 🛠️ Kullanılan Teknolojiler ve Kütüphaneler

* **Python**
* **Jupyter Notebook / Colab**
* **Pandas** (Veri Analizi ve Manipülasyonu)
* **NumPy** (Sayısal İşlemler için)

## 📊 Gerçekleştirilen Analiz Adımları

### 1. Kütüphane ve Veri Yükleme
Pandas ve NumPy kütüphaneleri projeye dahil edilmiş ve 'weather_data.csv' dosyası bir DataFrame (df) içine okunmuştur.

### 2. Veri Keşfi
Veri setinin yapısını anlamak için ilk 5 ve son 5 satırı görüntülenmiş, ayrıca sayısal sütunların istatistiksel özeti (`describe()`) incelenmiştir.

### 3. Sütun Seçimi
Analiz için gerekli olan 'Date', 'City', 'Temperature' ve 'City', 'Temperature' sütunları ayrı ayrı seçilerek listelenmiştir.

### 4. Basit Filtreleme
* Sıcaklığın 30 derecenin üzerinde olduğu kayıtlar filtrelenmiştir.
* Şehrin sadece "Bursa" olduğu kayıtlar filtrelenmiştir.

### 5. Mantıksal Operatörler ile Filtreleme
* Şehri "İstanbul" olan **VE** Nem oranı %60'tan büyük olan kayıtlar.
* Şehri "Ankara" olan **VEYA** Sıcaklığı 5 dereceden küçük olan kayıtlar.
* Sıcaklığı 10°C altında **VEYA** Nem oranı %70 üzerinde olan veriler.

### 6. Sıralama (Sorting)
* Sıcaklık değerine göre büyükten küçüğe sıralanmış (ilk 10 kayıt gösterilmiştir).
* Neme göre azalan şekilde sıralama yapılmıştır.
* Şehir adına göre artan şekilde sıralama yapılmıştır.

### 7. Yeni Sütun Ekleme
Sıcaklık verileri kullanılarak iki yeni sütun oluşturulmuştur:
* **Temperature_F** (Fahrenheit cinsinden sıcaklık)
    	Formül: (Temperature * 9/5) + 32
* **FeelsLike** (Hissedilen sıcaklık)
    	FeelsLike = Temperature - (Humidity / 100)

### 8. Gruplama ve İstatistiksel Analiz
* Her şehirdeki toplam veri kaydı sayısı (`count`) bulunmuştur.
* **Şehirlere göre ortalama sıcaklık** (`mean`) hesaplanmıştır.

### 9. En Yüksek/Düşük Değer Analizi
* Veri setindeki en yüksek sıcaklığa sahip kayıt (tüm satır bilgisi) bulunmuştur.
* Veri setindeki en düşük nem oranına sahip kayıt (tüm satır bilgisi) bulunmuştur.

### 10. Dışa Aktarma (Export)
Hesaplanan "Şehirlere göre ortalama sıcaklık" tablosu, `sehir_sicakliklari.xlsx` ve `sehir_sicakliklari.csv` dosyaları olarak dışa aktarılmıştır.

# Makine Öğrenmesi Yol Haritası (7 Adım)

Derste işlediğimiz ML sürecini adım adım şöyle özetleyebiliriz:

### 1. Veri Toplama
Hocanın notlarında da geçtiği gibi; makine ona ne verirsen onu öğrenir.
**Önemli:** Yanlış veya eksik veri toplarsan, modelin tahminleri de saçmalar (Garbage In, Garbage Out mantığı).

### 2. Veri Hazırlama & Temizleme
Burası işin "amelelik" ama en gerekli kısmı.
* Veriyi karıştır (Randomize et) ki sıraya göre ezberlemesin.
* Eksik yerleri doldur, hatalıları sil.
* **Train/Test Split:** Veriyi ikiye bölüyoruz (Eğitim ve Test). Hepsini eğitimde kullanırsak sınav sorularını önceden görmüş öğrenci gibi olur, ezber yapar.

### 3. Model Seçimi
Probleme göre seçimi yapıyoruz.
* Resim mi tanıyacağız? Sayısal bir değer mi tahmin edeceğiz? Ona göre algoritma seçiyoruz.

### 4. Modeli Eğitme (Training)
Veriyi modele "yedirdiğimiz" aşama. Model burada verideki gizli kalıpları (pattern) bulmaya çalışıyor.

### 5. Değerlendirme (Evaluation)
Modeli eğittik ama çalışıyor mu?
* Kenara ayırdığımız **Test Verisi** (görülmemiş veri) ile modeli sınıyoruz.
* Eğer eğitim verisinde %100 başarı verip testte çakılıyorsa **Overfitting** (Ezberleme) yapmış demektir!

### 6. Parametre Ayarı (Tuning)
Modelin ince ayarlarını yaptığımız yer. Doğruluğu artırmak için "vida sıkma" işlemi.

### 7. Tahmin (Prediction)
Artık model hazır. Gerçek dünyadan yeni veriler verip sonucu alıyoruz.

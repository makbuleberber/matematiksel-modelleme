# 📚 Bölüm 2: Denetimsiz Öğrenme ve Kümeleme (Clustering)

Büyük veri kümelerindeki ilgili veri noktalarını gruplandırmak için kullanılır. Amaç; küme içi benzerliği artırmak, kümeler arası benzerliği azaltmaktır.

## Kümeleme Yöntemleri

### 1. Bölümleme Yöntemleri (Partitioning)
* Veriyi $k$ adet kümeye böler ($k \le n$).
* Amaç fonksiyonunu optimize eder.
* **Algoritmalar:** K-means, K-Mediods, CLARA.

### 2. Hiyerarşi Tabanlı Yöntemler
* Kümelerin ağaç yapısını (Dendrogram) oluşturur.
    * **Agglomerative (Aşağıdan Yukarı):** Her gözlem kendi kümesinde başlar, birleşerek yukarı çıkar.
    * **Divisive (Yukarıdan Aşağı):** Tüm gözlemler tek kümede başlar, bölünerek aşağı iner.

### 3. Yoğunluk Tabanlı Yöntemler (Density-based)
* Yüksek yoğunluklu bölgeleri kümeler, düşük yoğunluklu bölgeleri ayırır.
* **Algoritmalar:** DBSCAN, OPTICS, DENCLUE.

---

## Mesafe Ölçümleri (Distance Measures)
İki nesne ($N_1, N_2$) arasındaki mesafe $d(N_1, N_2) \ge 0$ olmalıdır.

1. **Öklid (Euclidean):** $\sqrt{\sum (x_{ik} - x_{jk})^2}$.
2. **Minkowski (Manhattan):** $\sum |x_{ik} - x_{jk}|$.
3. **Chebyshev:** $\max(|x_i - y_i|)$.

---

## 🌑 DBSCAN Algoritması
*(Density-based spatial clustering of applications with noise)*

Gürültülü ve rastgele şekilli (küresel olmayan) kümeleri bulmak için kullanılır. K-means'in aksine küme sayısı ($k$) önceden verilmez.

### Temel Parametreler
1.  **Eps ($\epsilon$):** Komşuluk yarıçapı.
2.  **MinPts:** Bir bölgenin yoğun sayılması için gereken minimum nokta sayısı.

### Nokta Türleri
* **Core Point (Çekirdek Nokta):** $\epsilon$ yarıçapında en az *MinPts* kadar komşusu olan nokta.
* **Border Point (Sınır Nokta):** Bir çekirdek noktaya erişebilen ama kendisi çekirdek olmayan nokta.
* **Noisy Point (Gürültü):** Herhangi bir kümeye dahil olmayan (outlier) nokta.

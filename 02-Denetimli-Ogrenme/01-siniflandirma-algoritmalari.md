# 🚦 Sınıflandırma (Classification) Algoritmaları

Derste gördüğümüz temel sınıflandırma algoritmalarının kısa özetleri, avantajları

### Sınıflandırma Türleri
1.  **İkili Sınıflandırma (Binary Classification):** İki sınıf etiketi vardır (Doğru/Yanlış, Evet/Hayır). Genellikle biri "normal" diğeri "anormal" durumdur (Örn: Kanser tespit edildi/edilmedi).
2.  **Çok Sınıflı Sınıflandırma (Multiclass Classification):** İkiden fazla sınıf etiketi vardır. Normal/Anormal ayrımı yoktur, örnekler bir sınıf aralığına girer.
3.  **Çoklu Etiket Sınıflandırması (Multi-label Classification):** Bir örnek aynı anda birden fazla sınıfa ait olabilir. (Örn: Bir haber hem "Teknoloji" hem "Son Haberler" kategorisinde olabilir).

## 1. Naive Bayes (NB)
**Mantığı:** "Saf" (Naive) denmesinin sebebi, verideki her özelliğin birbirinden bağımsız olduğunu varsaymasıdır (ki gerçek hayatta bu zordur).
* **Kullanım:** Spam filtreleme, metin sınıflandırma.
* **Avantajı:** Az veriyle hızlı çalışır, parametre tahmini kolaydır.

#### 2. Linear Discriminant Analysis (LDA)
* **Mantık:** Sınıf koşullu yoğunlukları verilere uydurur ve Bayes kuralını uygular. Doğrusal bir karar sınırı oluşturur.
* **Özellik:** Veriyi daha düşük boyutlu bir uzaya yansıtarak (boyut indirgeme) karmaşıklığı ve hesaplama maliyetini azaltır.
* **Varsayım:** Tüm sınıflar aynı kovaryans matrisini paylaşır ve Gauss yoğunluğuna sahiptir.

## 3. Lojistik Regresyon (Logistic Regression)
**Mantığı:** Adı regresyon olsa da bir sınıflandırma algoritmasıdır. Çıktıyı 0 ile 1 arasında bir olasılık değerine sıkıştırmak için **Sigmoid Fonksiyonu** kullanır.
* **Formül:** $g(z) = \frac{1}{1 + e^{-z}}$.
* **Not:** Veriler doğrusal (linear) ayrılabiliyorsa çok iyi çalışır.

## 4. K-En Yakın Komşu (KNN - K-Nearest Neighbors)
**Mantığı:** "Bana arkadaşını söyle, sana kim olduğunu söyleyeyim." Yeni bir veri geldiğinde, ona en yakın **K** adet komşusuna bakar. Çoğunluk hangi sınıftaysa o sınıfa atar.
* Verileri kullanır ve benzerlik ölçütlerine (örneğin, **Öklid mesafe** fonksiyonu) göre yeni veri noktalarını sınıflandırır
* **Özellik:** Gürültülü eğitim verilerine karşı oldukça dayanıklıdır. Hem sınıflandırma hem de regresyon için kullanılabilir.
* **Kritik Nokta:** `k` sayısını doğru seçmek çok önemlidir.

## 5. Destek Vektör Makineleri (SVM)
**Mantığı:** Sınıfları birbirinden ayıran en geniş yolu (margin) bulmaya çalışır. En uçtaki verilere "Destek Vektörü" denir.
* **Kernel Trick:** Veri doğrusal ayrılmıyorsa, veriyi üst boyutlara taşıyıp orada ayırır (RBF, Polinom vb.).

#### 6. Decision Tree (DT) - Karar Ağacı
* **Mantık:** Ağacı kökten yapraklara doğru sıralayarak sınıflandırma yapar.
* **Algoritmalar:** ID3, C4.5, CART.
* **Bölme Kriterleri:**
    * **Entropi (Bilgi Kazancı):** $H(x) = -\sum p(x) \log_2 p(x)$
    * **Gini Safsızlığı:** $Gini(E) = 1 - \sum p_i^2$.

#### 7. Random Forest (RF)
* **Mantık:** "Topluluk" (Ensemble) tekniğidir. Birden fazla karar ağacını paralel olarak eğitir ve çoğunluk oyunu (sınıflandırma) veya ortalamayı (regresyon) alır.
* **Avantaj:** Tek bir ağaca göre aşırı uyum (overfitting) sorununu azaltır ve doğruluğu artırır. Bootstrap aggregating (bagging) kullanır.

---

## B. Regresyon Analizi (Regression)
Sürekli bir sonuç değişkenini ($Y$) tahmin etmek için kullanılır. Sınıflandırmadan farkı, çıktının kategorik değil sayısal olmasıdır.

### 1. Basit ve Çoklu Doğrusal Regresyon
* En uygun düz çizgiyi (regresyon doğrusu) oluşturur.
* **Formül (Basit):** $y = a + bx + e$ (a: kesim noktası, b: eğim, e: hata).
* **Çoklu:** Birden fazla bağımsız değişken ($x_1, x_2...$) varsa kullanılır.

### 2. Polinom Regresyonu
* İlişki doğrusal değilse kullanılır. $x$'in $n$. dereceden polinomu alınır.
* **Formül:** $y = b_0 + b_1x + b_2x^2 + ... + b_nx^n + e$.

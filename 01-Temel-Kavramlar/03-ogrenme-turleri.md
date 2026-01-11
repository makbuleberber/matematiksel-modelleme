# 🧠 Makine Öğrenmesi Türleri

Algoritmalar öğrenme tarzına göre 4'e ayrılıyor. Ben karıştırmamak için şöyle kodladım:

## 1. Denetimli Öğrenme (Supervised) 👨‍🏫
**Mantığı:** Başında bir öğretmen var gibi düşün.
* Elimizde **etiketli veri** (cevap anahtarı) var.
* Makineye hem soruyu (input) hem cevabı (output) veriyoruz.
* En yaygın denetimli öğrenme görevleri: Verileri ayıran sınıflandırma ve verilere uyan regresyondur. 
* **Örnek:** E-postaları "Spam" veya "Spam Değil" diye etiketleyip sisteme vermek.

> **İkiye ayrılır:**
> * **Sınıflandırma:** Kategori tahmin eder (Kedi/Köpek, Hasta/Sağlıklı).
> * **Regresyon:** Sayı tahmin eder (Evin fiyatı, Yarınki sıcaklık).

## 2. Denetimsiz Öğrenme (Unsupervised) 🕵️‍♂️
**Mantığı:** Öğretmen yok, cevap anahtarı yok.
* Veriler **etiketsiz**. Makineyi veriyle baş başa bırakıyoruz.
* Makine verideki benzerlikleri kendi bulup grupluyor.
* **Amaç:** Gizli yapıları keşfetmek.
* **Örnek:** Müşteri segmentasyonu (Bu müşteriler birbirine benziyor, bunları bir kümeye alalım).

## 3. Yarı Denetimli (Semi-Supervised) 🌓
Az miktarda etiketli veri + Çok miktarda etiketsiz veri.
* Etiketlemek pahalı ve zor olduğu için bu yöntem kullanılıyor (Hibrit yöntem).

## 4. Pekiştirmeli Öğrenme (Reinforcement) 🎮
**Mantığı:** Ödül ve Ceza yöntemi.
* Bir veri seti yok, dinamik bir ortam var. Çevre odaklı bir yaklaşım.
* Ajan (Agent) bir hareket yapar, sonucunda ödül alırsa o hareketi tekrar eder, ceza alırsa yapmaz.
* **Örnek:** Satranç oynayan yapay zeka veya yürümeyi öğrenen robot.

---
**Özet Tablo:**

| Tür | Veri Tipi | Anahtar Kelime |
| :--- | :--- | :--- |
| **Denetimli/Supervised** | Etiketli | Sınıflandırma |
| **Yarı Denetimli/Unsupervised** | Etiketsiz | Kümeleme |
| **Pekiştirmeli/Reinforcement** | Ortam/Environment | Ödül & Ceza, Kontrol |

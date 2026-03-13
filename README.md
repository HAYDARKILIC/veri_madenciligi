# 🔍 Veri Madenciliği — Ders Notları ve Uygulamalı Notebook'lar

**Haydar Kılıç | Mühendislik Fakültesi, Yapay Zeka Mühendisliği**  

---

## 📖 Hakkında

Bu repository, **Veri Madenciliği** dersine ait haftalık Jupyter Notebook'larını içermektedir. Her notebook, o haftanın teorik ders sunumuna eşlik eden uygulamalı Python çalışmasıdır: slayttaki kavramlar ve sayısal örnekler aynen yeniden üretilir, ardından genelleştirilerek pekiştirilir.

---

## 📂 İçindekiler

| Ders | Konu | Notebook |
|------|------|----------|
| Ders 1 | Sınıflandırma: Temel Kavramlar ve Teknikler | [`Ders1/VMD_Ders1_Notebook.ipynb`]|
| Ders 2 | Sınıflandırma: İleri Düzey Teknikler (KNN, NBC, ANN, SVM) | [`Ders2/VMD_Ders2_Notebook.ipynb`]|
| Ders 3 | Sınıflandırma: İleri Düzey Teknikler II (ANN, SVM, Bayes Ağları, Topluluk, Dengesizlik, Metrikler) | [`Ders3/VMD_Ders3_Notebook.ipynb`] |
| Ders 4 | Birliktelik Analizi (Apriori, FP-Growth, GSP, Örüntü Değerlendirme) | [`Ders4/VMD_Ders4_Notebook.ipynb`] |
| Ders 5 | Kümeleme Analizi ve Anomali Tespiti | [`Ders5/VMD_Ders5_Notebook.ipynb`] |

---

## 📚 Ders 1 — Sınıflandırma: Temel Kavramlar ve Teknikler

### Kapsanan Konular

| # | Konu | Öne Çıkan Kavramlar |
|---|------|---------------------|
| 1 | Sınıflandırma Nedir? | `(x, y)` ikilisi, tümevarım (induction), tümdengelim (deduction) |
| 2 | Omurgalı Veri Seti | Gerçek dünya örneği, çok sınıflı → ikili dönüşüm |
| 3 | Confusion Matrix | TP, TN, FP, FN; doğruluk ve hata oranı formülleri |
| 4 | Karar Ağacı Yapısı | Kök / iç / yaprak düğüm; `DecisionTreeClassifier` |
| 5 | Hunt Algoritması | Özyinelemeli ağaç büyütme simülasyonu (sıfırdan) |
| 6 | Öznitelik Türleri | Nominal, sıralı, sürekli; bölme koşulları |
| 7 | Safsızlık Ölçüleri | Entropi, Gini indeksi, sınıflandırma hatası; karşılaştırma grafikleri |
| 8 | Bilgi Kazancı & Kazanç Oranı | `ΔInfo`, bölme bilgisi, CustomerID tuzağı |
| 9 | Overfitting & Underfitting | Derinlik–hata eğrisi, genelleme hatası `errgen(T)` |
| 10 | Model Seçimi & CV | Holdout, k-fold cross-validation, hiperparametre arama |
| 11 | İstatistiksel Model Karşılaştırması | Güven aralığı, örneklem boyutu etkisi |

---

## 📚 Ders 2 — Sınıflandırma: İleri Düzey Teknikler

### Kapsanan Konular

| # | Konu | Öne Çıkan Kavramlar |
|---|------|---------------------|
| 1 | K-En Yakın Komşu (KNN) | Öklid mesafesi, mesafe ağırlıklı oylama, k parametresi etkisi |
| 2 | Naif Bayes Sınıflandırıcı (NBC) | Bayes teoremi, koşullu bağımsızlık, Gaussian NBC, Laplace düzeltmesi |
| 3 | Yapay Sinir Ağları (ANN) | Perseptron, ağırlık güncelleme, XOR problemi, vanishing gradient, ReLU |
| 4 | Destek Vektör Makineleri (SVM) | Maksimum marj hiperdüzlemi, destek vektörler, kernel trick (RBF, Poly, Sigmoid) |
| 5 | Algoritma Karşılaştırması | Breast Cancer & Half-Moon veri setleri üzerinde KNN / NBC / MLP / SVM karşılaştırması |

---

## 📚 Ders 3 — Sınıflandırma: İleri Düzey Teknikler II

### Kapsanan Konular

| # | Konu | Öne Çıkan Kavramlar |
|---|------|---------------------|
| 1 | ANN Derinlemesine | Biyolojik nöron analogisi, ileri yayılım, mini-batch gradyan inişi, geri yayılım |
| 2 | SVM (Derinlemesine) | Dual problem, KKT koşulları, kernel trick, özellik uzayı dönüşümü φ |
| 3 | Bayes Ağları | DAG yapısı, yerel Markov özelliği, CPT, ortak dağılım, çıkarım |
| 4 | Topluluk Öğrenmesi | Binom hata analizi, Bias-Variance trade-off, Bagging, Random Forest, AdaBoost |
| 5 | Sınıf Dengesizliği | Doğruluk paradoksu, undersampling, oversampling, SMOTE (sıfırdan), class weight |
| 6 | Performans Metrikleri | Confusion matrix, Precision/Recall/F1/Fβ, ROC eğrisi, PR eğrisi, optimal karar eşiği, maliyet matrisi |


---

## 📚 Ders 4 — Birliktelik Analizi

### Kapsanan Konular

| # | Konu | Öne Çıkan Kavramlar |
|---|------|---------------------|
| 1 | Temel Kavramlar | Destek sayısı σ(X), destek s(X), güven c(X→Y), birliktelik kuralı |
| 2 | Apriori İlkesi | Anti-monotonluk özelliği, öğe kafesi yapısı, budama stratejisi |
| 3 | Apriori Algoritması | candidate-gen (Fₖ×Fₖ birleştirme), candidate-prune, destek sayımı (sıfırdan) |
| 4 | Kural Üretimi | ap-genrules, güven anti-monotonluğu, Lift hesabı |
| 5 | Kompakt Gösterim | Maksimal sık kümeler, kapalı sık kümeler, hiyerarşi |
| 6 | FP-Growth | FP-ağacı (sıfırdan), header tablosu, koşullu FP-ağacı, aday üretmeden madencilik |
| 7 | Örüntü Değerlendirme | Lift, PS (Piatetsky-Shapiro), φ-korelasyonu, IS (Cosine) ölçütleri |
| 8 | Simpson Paradoksu | Gizli değişkenler, katmanlı vs birleşik analiz, HDTV örneği |
| 9 | Kategorik & Sürekli | İkili forma dönüşüm, ayrıştırma (discretization), aralık genişliği etkisi |
| 10 | Sekans Örüntüleri | GSP algoritması, alt-sekans testi, web ziyaret sırası örneği |
| 11 | Seyrek & Negatif | h-güven (All-Confidence), çapraz-destek örüntüsü, rakip ürün analizi |

---
## 📚 Ders 5 — Kümeleme Analizi ve Anomali Tespiti

### Kapsanan Konular

| # | Konu                      | Öne Çıkan Kavramlar                    |
| - | ------------------------- | -------------------------------------- |
| 1 | Kümeleme Analizine Giriş  | Denetimsiz öğrenme, benzerlik kavramı  |
| 2 | K-Means Algoritması       | SSE, centroid güncelleme, yakınsama    |
| 3 | Başlangıç Seçimi          | Rastgele vs K-Means++                  |
| 4 | Optimal K                 | Elbow yöntemi, Silhouette analizi      |
| 5 | Hiyerarşik Kümeleme       | Agglomerative clustering, dendrogram   |
| 6 | Yoğunluk Tabanlı Kümeleme | DBSCAN, epsilon, minPts                |
| 7 | Anomali Tespiti           | Local Outlier Factor (LOF), Z-score    |
| 8 | Kümeleme Değerlendirme    | Silhouette, intra/inter cluster mesafe |




---

## 🛠️ Kurulum

### 1. Repository'yi klonlayın

```bash
git clone https://github.com/HAYDARKILIC/veri_madenciligi.git
cd veri_madenciligi
```

### 2. Sanal ortam oluşturun (önerilir)

```bash
python -m venv venv
source venv/bin/activate        # Linux / macOS
venv\Scripts\activate           # Windows
```

### 3. Bağımlılıkları yükleyin

```bash
pip install -r requirements.txt
```

### 4. Jupyter'ı başlatın

```bash
jupyter notebook
```

---

## 📦 Gereksinimler

Tam liste için [`requirements.txt`](requirements.txt) dosyasına bakın.

| Paket | Kullanım Amacı |
|-------|---------------|
| `numpy` | Sayısal hesaplama, dizi işlemleri |
| `pandas` | Veri çerçeveleri, tablo işlemleri |
| `matplotlib` | Görselleştirme |
| `scikit-learn` | KNN, NBC, MLP, SVM, Ensemble, metrikler, cross-validation |
| `scipy` | İstatistiksel testler, Gaussian yoğunluk, binom katsayısı |
| `networkx` | Bayes Ağı DAG görselleştirmesi (Ders 3, opsiyonel) |
| `jupyter` | Notebook ortamı |

> **Not:** Ders 4 (Birliktelik Analizi) yalnızca standart kütüphaneleri (`itertools`, `collections`) kullanır; ek bağımlılık gerektirmez.

---

## 📁 Repository Yapısı

```
veri_madenciligi/
│
├── README.md
├── requirements.txt
│
├── Ders1/
│   └── VMD_Ders1_Notebook.ipynb
│
├── Ders2/
│   └── VMD_Ders2_Notebook.ipynb
│
├── Ders3/
│   └── VMD_Ders3_Notebook.ipynb
│
├── Ders4/
│   └── VMD_Ders4_Notebook.ipynb
│
├── Ders5/
│   └── VMD_Ders5_Notebook.ipynb
```

---
---

*Veri Madenciliği — Haydar Kılıç, Yapay Zeka Mühendisliği*

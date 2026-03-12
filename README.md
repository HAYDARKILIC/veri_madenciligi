# 🔍 Veri Madenciliği

**Yapay Zeka Mühendisliği Bölümü — Ders Notları ve Uygulamalı Notebook'lar**  
Haydar Kılıç

---

## 📖 Hakkında

Bu repository, **Veri Madenciliği** dersine ait haftalık Jupyter Notebook'larını içermektedir. Her notebook, o haftanın teorik ders sunumuna eşlik eden uygulamalı Python çalışmasıdır: slayttaki kavramlar ve sayısal örnekler aynen yeniden üretilir, ardından genelleştirilerek pekiştirilir.

Hedef kitle: Yapay Zeka Mühendisliği lisans öğrencileri.

---

## 📂 İçindekiler

| Ders | Konu | Notebook |
|------|------|----------|
| Ders 1 | Sınıflandırma: Temel Kavramlar ve Teknikler | [`Ders1/VMD_Ders1_Notebook.ipynb`](Ders1/VMD_Ders1_Notebook.ipynb) |
| Ders 2 | *(yakında)* | — |
| Ders 3 | *(yakında)* | — |
| Ders 4 | *(yakında)* | — |
| Ders 5 | *(yakında)* | — |

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

## 🛠️ Kurulum

### 1. Repository'yi klonlayın

```bash
git clone https://github.com/<kullanici_adi>/veri_madenciligi.git
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
| `scikit-learn` | Karar ağacı, metrikler, cross-validation |
| `scipy` | İstatistiksel testler (güven aralığı) |
| `jupyter` | Notebook ortamı |

---

## 📁 Repository Yapısı

```
veri_madenciligi/
│
├── README.md                          ← Bu dosya
├── requirements.txt                   ← Bağımlılıklar
│
├── Ders1/
│   └── VMD_Ders1_Notebook.ipynb      ← Sınıflandırma temelleri
│
├── Ders2/                             ← (yakında)
├── Ders3/                             ← (yakında)
├── Ders4/                             ← (yakında)
└── Ders5/                             ← (yakında)
```

---

## 📝 Notebook Hakkında Notlar

- Her notebook **bağımsız çalışabilir**; gerekli tüm veri setleri kod içinde oluşturulmaktadır.
- Hücreler **sırayla** çalıştırılmalıdır; sonraki hücreler önceki hücrelerde tanımlanan değişkenlere bağımlıdır.
- Tüm grafikler `matplotlib` ile üretilmekte, harici dosya gerektirmemektedir.
- Notebook'lar Python **3.10+** ile test edilmiştir.

---

## 📖 Kaynaklar

- Tan, P.-N., Steinbach, M., & Kumar, V. (2018). *Introduction to Data Mining* (2nd ed.). Pearson.
- [scikit-learn Karar Ağacı Dokümantasyonu](https://scikit-learn.org/stable/modules/tree.html)

---

## 📜 Lisans

Bu materyal eğitim amaçlı hazırlanmıştır. Kaynak göstererek serbestçe kullanılabilir.

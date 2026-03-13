# 🤖 Üretken Yapay Zeka — Ders Notları ve Uygulamalı Notebook'lar

**Haydar Kılıç | Mühendislik Fakültesi, Yapay Zeka Mühendisliği**

Bu repo, *Üretken Yapay Zeka* dersinin teorik slayt içeriklerini Python ile pekiştiren Jupyter Notebook'larını barındırmaktadır. Her notebook, derste işlenen formülleri sıfırdan türeterek görselleştirir ve gerçek veri senaryolarına uyarlar.

---

## 📚 İçerik

| Ders | Konu | Notebook |
|------|------|----------|
| Ders 1 | Üretken Modelleme Temelleri | [`UYZ_Ders1_Notebook.ipynb`] |
| Ders 2 | Üretken Modellerin Türetilmesi (MAP · MLE · Beta-Binom · Dirichlet) | [`UYZ_Ders2_Notebook.ipynb`] |
| Ders 3 | Derin Üretken Modeller (VAE · GAN · GMMN · Difüzyon) | [`UYZ_Ders3_Notebook.ipynb`] |
| Ders 4 | Transformer ve Büyük Dil Modelleri (Attention · RoPE · Mini GPT · Ölçekleme) | [`UYZ_Ders4_Notebook.ipynb`] |

> Yeni dersler eklendikçe tablo güncellenecektir.

---

## 🗂 Ders 1 — Üretken Modelleme Temelleri

### Ele Alınan Konular

**Bölüm 1 — Temel Kavramlar**
- El yazısı rakam tanıma: 28×28 piksel vektör temsili, eğitim/test/doğrulama ayrımı
- Polinom regresyon ve eğri uydurma (Vandermonde matrisi, En Küçük Kareler)
- Overfitting / Underfitting ve RMS hata analizi
- Ridge Regularization (L2 cezası, λ hiperparametresi)

**Bölüm 2 — Olasılık Teorisi**
- Bileşik, marjinal ve koşullu olasılık dağılımları
- Bayes teoremi — hasta teşhisi ve *base rate fallacy*
- Gaussian (Normal) dağılım: PDF, CDF, sayısal doğrulama
- Maksimum Olabilirlik Tahmini (MLE) ve yanlılık
- Bayesçi güncelleme: madeni para atışı ile önsel → sonsal

**Bölüm 3 — Karar Teorisi**
- Minimum hata karar sınırları ve sonsal olasılıklar
- Reddetme seçeneği (Reject Option) ve θ eşiği
- Asimetrik kayıp matrisi (tıbbi tanı senaryosu)
- Üretken / Ayrıştırıcı / Diskriminant model karşılaştırması

---

## 🗂 Ders 2 — Üretken Modellerin Türetilmesi

### Ele Alınan Konular

**Bölüm 1 — Pozitif Örneklerden Öğrenme & Number Game**
- Kavram öğrenme = ikili sınıflandırma; sonsal öngörüsel dağılım
- Güçlü örnekleme varsayımı: `p(D|h) = (1/|h|)^N`
- **Boyut Prensibi (Size Principle):** dar hipotez → yüksek olabilirlik
- Önsel, olabilirlik ve sonsal hesabı; Bayesçi güncelleme
- **MAP kestirimi** ve N → ∞ davranışı (Dirac yakınsaması)
- **Bayes Model Ortalaması (BMA)** vs. Tak-Çıkar yaklaşımı
- Karışım önseli (π₀ parametresi): kural tabanlı vs. aralık tabanlı hipotezler

**Bölüm 2 — Beta-Binom Modeli**
- Bernoulli olabilirliği ve yeterli istatistikler (N₁, N₀)
- Beta dağılımı: konjuge önsel, farklı (a, b) parametreleri
- Ardışık Bayesçi güncelleme: Beta(a,b) → Beta(N₁+a, N₀+b)
- MLE, MAP ve sonsal ortalama formülleri; N arttıkça yakınsama
- **Sıfır Sayım Problemi** ve Laplace ardışıklık kuralı
- Sonsal varyans ve güven aralığı: σ ∝ 1/√N
- **Bileşik Beta-Binom dağılımı:** gelecekteki denemelerin tahmini

**Bölüm 3 — Dirichlet-Multinomial**
- Multinomial olabilirlik ve Dirichlet önsel
- K=3 olasılık simpleksinin görselleştirilmesi (barycentric koordinatlar)
- Dirichlet-Multinomial güncelleme ve sonsal tahmin
- **Add-K düzeltmesi (β):** MLE → Laplace → uniform

**Bölüm 4 — Karışım Modeli**
- π₀ parametresinin sonsal öngörüsel dağılıma etkisi

**Bölüm 5 — MLE vs MAP vs Bayes Karşılaştırması**
- Hata analizi, θ tahminlerinin N ile yakınsaması

---

## 🗂 Ders 3 — Derin Üretken Modeller

### Ele Alınan Konular

**Bölüm 1 — Olasılıksal Çerçeve & MLE**
- 2D Gaussian karışımı ile gerçek veri simülasyonu
- Log-Gaussian log-olasılık fonksiyonu
- MLE vs. kötü model karşılaştırması

**Bölüm 2 — KL Iraksaması**
- Kapalı form Gaussian KL hesabı
- KL asimetrisi: KL(p‖q) ≠ KL(q‖p)
- MLE ≡ KL minimizasyonu ilişkisi

**Bölüm 3 — Latent Uzay & Manifold Hipotezi**
- MNIST: 784 piksel → ~10 boyutlu manifold (PCA varyans analizi)
- 2D PCA projeksiyonu ile latent uzay görselleştirme
- Latent uzay aritmetiği: z(7) − z(1) + z(0) ≈ z(6)

**Bölüm 4 — ELBO Türetimi**
- Kapalı form KL hesabı ve ısı haritası
- Rekonstrüksiyon vs. KL terimlerinin dengesi

**Bölüm 5 — Variational Autoencoder (VAE)**
- Encoder–Decoder mimarisi, Reparametrization Trick
- Gradyan akışı gösterimi (backprop neden çalışır?)
- MNIST üzerinde eğitim; 2D latent uzay görselleştirme
- β-VAE: KL düzenlileştirme etkisi; Posterior Collapse sorunu

**Bölüm 6 — Generative Adversarial Networks (GAN)**
- Generator + Discriminator mimarisi (LeakyReLU, BatchNorm)
- Optimal Discriminator formülü ve Nash dengesi görselleştirmesi
- MNIST eğitimi; G/D kayıp eğrileri ve mod çöküşü tartışması

**Bölüm 7 — GMMN & MMD**
- Gaussian (RBF) çekirdeği ve MMD² hesabı (multi-scale)
- MMD sezgisel testi: aynı / yakın / uzak dağılımlar
- Discriminator'sız GMMN eğitimi (sadece MMD kaybı)

**Bölüm 8 — Difüzyon Modelleri (DDPM)**
- İleri süreç: β çizelgesi, kapalı form q(x_t|x_0)
- SimpleUNet: zaman gömüşü + skip bağlantılı gürültü tahmini
- DDPM eğitimi (MSE kaybı) ve ters süreç örnekleme
- Adım adım gürültü temizleme görselleştirmesi

**Bölüm 9 — Model Karşılaştırması & FID**
- Fréchet Inception Distance hesabı (PCA feature uzayı)
- Radar grafik: Kalite / Çeşitlilik / Hız / Kararlılık / Latent Kontrol
- Üretken modeller kronolojisi (1985–2022)
- Kapsamlı karşılaştırma tablosu

---

## 🗂 Ders 4 — Transformer ve Büyük Dil Modelleri

### Ele Alınan Konular

**Bölüm 1 — RNN vs Transformer: Gradyan Kaybolması**
- Basit RNN'de |dL/dh_t| ≈ |W_hh|^(T-t) ile üstel küçülme simülasyonu
- Kaybolma / stabil / patlama rejimleri (|W_hh| = 0.85 / 1.00 / 1.15)
- Transformer'da O(1) bağlantı mesafesi: her token çiftine doğrudan erişim

**Bölüm 2 — Encoder–Decoder ve Bilgi Darboğazı**
- GRU encoder ile farklı dizi uzunluklarında kosinüs benzerliği kaybı
- RNN Enc-Dec tek vektör darboğazı vs. Attention bağlam vektörü karşılaştırması
- c_t = Σ α_{t,i} · h_i formülünün görsel açıklaması

**Bölüm 3 — Bahdanau (Additive) Dikkat Mekanizması**
- Sıfırdan BahdanauAttention: W_s, W_h, v parametreli skorlama
- e_{t,i} = vᵀ tanh(W_s·s_{t-1} + W_h·h_i) → softmax → bağlam vektörü
- İngilizce–Almanca çeviri simülasyonu: 4×4 dikkat ısı haritası

**Bölüm 4 — Scaled Dot-Product Attention (Q, K, V)**
- `Attention(Q,K,V) = softmax(QK^T / √d_k) · V` adım adım implementasyon
- √d_k ölçeklemesinin önemi: entropi analizi (d_k büyüdükçe ölçeksiz softmax çöküyor)
- Boyut analizi: (B, T, d_model) → Q/K/V → (B, T, d_k) → Z

**Bölüm 5 — Multi-Head Attention**
- Tek büyük W_q/W_k/W_v matris yaklaşımı; split_heads ile (B, n_heads, T, d_k) dönüşümü
- 4 başlık dikkat haritası: Pozisyon / Sözdizimi / Anlam / Mesafe
- Parametre analizi: 4 × d_model² ağırlık

**Bölüm 6 — Pozisyonel Kodlama (Sinüzoidal, RoPE, ALiBi)**
- PE_{pos,2i} = sin(pos/10000^{2i/d}), PE_{pos,2i+1} = cos(…): matris görselleştirme
- Dalga frekansları: düşük boyut = yüksek frekans; PE benzerlik matrisi
- RoPE: 2D rotasyon ile göreceli pozisyon kodlaması; q^T_m k_n ∝ f(m-n)
- ALiBi: e_{ij} = q_i^Tk_j − m·|i−j| lineer ceza; eğim m_i = 2^{−8i/n_heads}
- Karşılaştırma tablosu: Sinüzoidal / Öğrenilen / RoPE / ALiBi

**Bölüm 7 — Feed-Forward Network & Aktivasyon Fonksiyonları**
- ReLU → GELU → Swish/SiLU → SwiGLU(x,W,V) = Swish(xW) ⊙ xV
- Gradyan analizi: ReLU'da x<0 bölgesi "ölü nöron" problemi
- d_ff = 4×d_model genişleme kuralı ve FFN parametre büyümesi

**Bölüm 8 — Layer Normalization: LayerNorm vs RMSNorm / Pre-LN vs Post-LN**
- LN(x) = γ·(x−μ)/√(σ²+ε)+β vs. RMSNorm(x) = γ·x/RMS(x) (β yok, ~10% hızlı)
- Farklı girdi ölçeklerinde std/ortalama karşılaştırması
- Pre-LN (modern) vs Post-LN (orijinal): gradyan dağılımı histogramı
- BN vs LN vs RMSNorm: dizi modellerinde tercih analizi

**Bölüm 9 — Dikkat Maskeleme: Full vs Causal**
- make_full_mask (Bidirectional): BERT/RoBERTa — her token her tokena bakabilir
- make_causal_mask (Alt üçgen): GPT — sadece geçmiş görülür, gelecek −∞
- Maskeleme → model ailesi → görev eşleşme tablosu (Encoder / Decoder / Enc-Dec)

**Bölüm 10 — Tam Transformer Bloğu (Sıfırdan Implementasyon)**
- TransformerEncoderBlock: Pre-LN + MHA + FFN + Residual
- TransformerEncoder: N katman, öğrenilen PE, final LayerNorm
- 3 model konfigürasyonu (Küçük / BERT-mini / BERT-base) parametre analizi
- #params ≈ 12 × N × d²_model tahmini formülü

**Bölüm 11 — Mini GPT: Karakter Seviyesi Dil Modeli**
- GPTDecoderBlock: Causal MHA + Pre-LN + FFN
- MiniGPT: tok_emb + pos_emb + 3 decoder bloğu + lm_head (ağırlık bağlama)
- Otoregresif generate(): top-k örnekleme + temperature kontrolü
- Türkçe metin üzerinde 500 adım eğitim: kayıp eğrisi + dikkat haritası
- Farklı temperature (0.5 / 1.0 / 1.5) ile üretim örnekleri

**Bölüm 12 — Hiperparametre Analizi & Ölçekleme Yasası**
- Gerçek LLM tablosu: BERT-base/large, GPT-2, GPT-3, LLaMA-2 7B/70B
- Ölçekleme yasası: L ∝ N^{−0.076} log-log görselleştirme
- d_model vs baş sayısı (d_k = d_model/h ≈ 64–128 kuralı)
- GPT vs BERT karşılaştırma tablosu: mimari, görev, bağlam, kullanım
- Modern LLM bloğu: RMSNorm + Pre-LN + SwiGLU + RoPE

---

## ⚙️ Kurulum

```bash
# Depoyu klonla
git clone https://github.com/HAYDARKILIC/uretken_yapay_zeka.git
cd uretken_yapay_zeka

# Sanal ortam oluştur (önerilir)
python -m venv venv
source venv/bin/activate        # Linux/macOS
# venv\Scripts\activate         # Windows

# Bağımlılıkları yükle
pip install -r requirements.txt

# Jupyter'ı başlat
jupyter notebook
```

---

## 📦 Gereksinimler

```
numpy>=2.0
matplotlib>=3.7
scipy>=1.11
scikit-learn>=1.3
jupyter>=1.0
ipykernel>=6.0
torch>=2.0
torchvision>=0.15
tqdm>=4.65
```

> `requirements.txt` dosyası repoya eklenmiştir.
>
> ⚠️ `torch` ve `torchvision`, Ders 3'ten itibaren zorunludur. GPU desteği için [pytorch.org](https://pytorch.org/get-started/locally/) üzerinden CUDA uyumlu versiyon seçiniz.

---

## 🏗 Proje Yapısı

```
uretken-yapay-zeka/
├── README.md
├── requirements.txt
├── UYZ_Ders1_Notebook.ipynb   # Ders 1 — Üretken Modelleme Temelleri
├── UYZ_Ders2_Notebook.ipynb   # Ders 2 — MAP · MLE · Beta-Binom · Dirichlet
├── UYZ_Ders3_Notebook.ipynb   # Ders 3 — VAE · GAN · GMMN · Difüzyon
├── UYZ_Ders4_Notebook.ipynb   # Ders 4 — Transformer · Attention · Mini GPT · LLM
└── (ilerleyen derslere ait notebook'lar eklenecek)
```

---

*Üretken Yapay Zeka — Haydar Kılıç, Yapay Zeka Mühendisliği*

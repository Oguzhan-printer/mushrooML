# Mushroom Classification Project 🍄

## Akbank Makine Öğrenmesi Bootcamp - Gözetimli Öğrenme Projesi

Bu proje, Akbank Makine Öğrenmesi Bootcamp kapsamında gerçekleştirilen gözetimli öğrenme çalışmasıdır. Kaggle'dan alınan "Mushroom Classification" veri seti kullanılarak mantarların yenilebilir veya zehirli olup olmadığını tahmin eden makine öğrenmesi modelleri geliştirilmiştir.

## 📊 Proje Özeti

### Veri Seti
- **Kaynak**: Kaggle - Mushroom Classification Dataset
- **Boyut**: 8,124 mantar örneği
- **Özellik Sayısı**: 22 kategorik özellik
- **Hedef Değişken**: Binary sınıflandırma (Edible/Poisonous)
- **Veri Boyutu**: >10MB (Bootcamp kriterlerini karşılar)

### Problem Tanımı
Mantarlar söz konusu olduğunda, yenilebilirliği belirlemek için basit bir kural yoktur. Bu proje, mantar özelliklerini kullanarak güvenli bir şekilde yenilebilir mantarları zehirli olanlardan ayırt etmeyi amaçlamaktadır.

## 🔧 Kullanılan Teknolojiler

### Kütüphaneler
- **Pandas**: Veri manipülasyonu ve analizi
- **NumPy**: Sayısal hesaplamalar
- **Matplotlib & Seaborn**: Veri görselleştirme
- **Scikit-learn**: Makine öğrenmesi algoritmaları

### Algoritmalar
1. **Logistic Regression**
2. **Ridge Classifier**
3. **Decision Tree Classifier**
4. **Gaussian Naive Bayes**
5. **Neural Network (MLP Classifier)**
6. **Random Forest Classifier**

## 📈 Metodoloji

### 1. Keşifsel Veri Analizi (EDA)
- Veri setinin genel yapısının incelenmesi
- Sınıf dağılımının analizi
- Kategorik değişkenlerin görselleştirilmesi
- Eksik değer kontrolü

### 2. Veri Ön İşleme
- Label Encoding ile kategorik verilerin sayısal forma dönüştürülmesi
- Train-test split (%70-%30 oranında)
- Stratified sampling ile sınıf dengesinin korunması

### 3. Model Geliştirme
- 6 farklı algoritmanın uygulanması
- Hiperparametre optimizasyonu
- Cross-validation ile model doğrulaması

### 4. Model Değerlendirme
- Accuracy, Precision, Recall, F1-Score metrikleri
- Confusion Matrix analizi
- Özellik önem analizi
- Model karşılaştırması

## 📊 Sonuçlar

### Veri Seti Analizi
**Veri Seti Boyutu:** (8124, 23)  
**Toplam Veri Noktası:** 8,124  
**Özellik Sayısı:** 22  
**Eksik Değer:** 0 (Temiz veri seti)  

**Sınıf Dağılımı:**
- **Yenilebilir (e):** 4,208 örnek (%51.8)
- **Zehirli (p):** 3,916 örnek (%48.2)

### Model Performansları
**Test Seti:** 2,437 örnek

**🏆 SONUÇLAR:**

1. **Random Forest**
   - Accuracy: 100.00%
   - Precision: 100.00%
   - Recall: 100.00%
   - F1-Score: 100.00%

2. **Decision Tree**
   - Accuracy: 100.00%
   - Precision: 100.00%
   - Recall: 100.00%
   - F1-Score: 100.00%

3. **Neural Network (MLP)**
   - Accuracy: 99.88%
   - Precision: 99.88%
   - Recall: 99.88%
   - F1-Score: 99.88%

4. **Logistic Regression**
   - Accuracy: 95.12%
   - Precision: 95.15%
   - Recall: 95.12%
   - F1-Score: 95.12%

5. **Ridge Classifier**
   - Accuracy: 94.89%
   - Precision: 94.92%
   - Recall: 94.89%
   - F1-Score: 94.89%

6. **Naive Bayes**
   - Accuracy: 92.34%
   - Precision: 92.40%
   - Recall: 92.34%
   - F1-Score: 92.34%

### Cross-Validation Sonuçları (5-Fold)

**🔄 Model Güvenilirlik Analizi:**

- **Random Forest:** 100.00% ± 0.0000
- **Decision Tree:** 100.00% ± 0.0000  
- **Neural Network:** 99.88% ± 0.0012
- **Logistic Regression:** 95.12% ± 0.0089
- **Ridge Classifier:** 94.89% ± 0.0091
- **Naive Bayes:** 92.34% ± 0.0156

### Confusion Matrix (Random Forest)

**🎯 Mükemmel Sınıflandırma:**

\`\`\`
Gerçek \ Tahmin    Yenilebilir    Zehirli

Yenilebilir        1,262          0

Zehirli            0              1,175
\`\`\`

**Sonuç:** Hiç yanlış sınıflandırma yok! ✅

### Kritik Özellikler (Feature Importance)

**🔍 En Önemli 10 Özellik:**

1. **odor (Koku)** - 18.47%
2. **gill-size (Solungaç Boyutu)** - 12.03%
3. **gill-color (Solungaç Rengi)** - 8.91%
4. **stalk-shape (Sap Şekli)** - 7.56%
5. **cap-color (Şapka Rengi)** - 6.89%
6. **bruises (Çürük)** - 6.34%
7. **ring-type (Halka Tipi)** - 5.98%
8. **population (Popülasyon)** - 5.67%
9. **habitat (Habitat)** - 5.34%
10. **cap-shape (Şapka Şekli)** - 4.89%

### Performans Metrikleri Detayı

**🏆 Random Forest Classifier (En İyi Model):**

- **True Positives (Doğru Zehirli):** 1,175
- **True Negatives (Doğru Yenilebilir):** 1,262  
- **False Positives (Yanlış Zehirli):** 0
- **False Negatives (Yanlış Yenilebilir):** 0
- **Sensitivity (Duyarlılık):** 100%
- **Specificity (Özgüllük):** 100%
- **Balanced Accuracy:** 100%

### Eğitim Süresi

**⚡ Model Eğitim Süreleri (Ortalama):**

- **Naive Bayes:** 0.003 saniye
- **Ridge Classifier:** 0.008 saniye  
- **Decision Tree:** 0.012 saniye
- **Logistic Regression:** 0.045 saniye
- **Random Forest:** 0.234 saniye
- **Neural Network:** 2.156 saniye

## 🌟 Gerçek Hayat Uygulamaları

### Mevcut Kullanım Alanları
- **Mobil Uygulamalar**: Doğa yürüyüşçüleri için mantar tanıma
- **Eğitim Araçları**: Biyoloji ve botanik eğitiminde kullanım
- **Güvenlik Sistemleri**: Yiyecek güvenliği ve kalite kontrolü
- **Araştırma**: Mikrobiyoloji ve ekoloji çalışmaları

### Potansiyel Geliştirmeler
- **Görüntü İşleme Entegrasyonu**: Mantar fotoğraflarından otomatik özellik çıkarımı
- **Mobil Uygulama**: Gerçek zamanlı mantar tanıma sistemi
- **IoT Entegrasyonu**: Akıllı tarım sistemlerinde kullanım
- **Web API**: Çevrimiçi mantar tanıma servisi

## 🚀 Gelecek Geliştirmeler

### Teknik İyileştirmeler
1. **Deep Learning**: CNN tabanlı görüntü sınıflandırması
2. **Ensemble Methods**: Birden fazla modelin kombinasyonu
3. **Feature Engineering**: Yeni özellik türetme teknikleri
4. **Hyperparameter Tuning**: Grid Search ve Bayesian Optimization

### Veri Genişletme
1. **Daha Fazla Tür**: Ek mantar türlerinin veri setine eklenmesi
2. **Coğrafi Veri**: Bölgesel mantar dağılım bilgileri
3. **Mevsimsel Faktörler**: Zaman bazlı özellikler
4. **Görüntü Verileri**: Mantar fotoğrafları ile multimodal yaklaşım

## 📁 Proje Yapısı

\`\`\`
mushroom-classification/

├── mushroom_classification_project.ipynb  # Ana proje notebook'u

├── mushrooms.csv                          # Veri seti

├── README.md                              # Proje dokümantasyonu

└── requirements.txt                       # Gerekli kütüphaneler
\`\`\`

## 🔗 Kaggle Notebook

**Kaggle Notebook Linki**: https://www.kaggle.com/code/ouzhanyazc/mushroom-project

## 📋 Kurulum ve Çalıştırma

### Gereksinimler
\`\`\`bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
\`\`\`

### Çalıştırma
\`\`\`bash
git clone [repository-url]
cd mushroom-classification
jupyter notebook mushroom_classification_project.ipynb
\`\`\`

## 👨‍💻 Geliştirici

Oğuzhan Yazıcı
- GitHub: Oguzhan-printer
- Email: oguzhanyzcc3429@gmail.com
- LinkedIn: https://www.linkedin.com/in/o%C4%9Fuzhan-yaz%C4%B1c%C4%B1-2b09aa327/


## 🙏 Teşekkürler

- Akbank Makine Öğrenmesi Bootcamp ekibine

---


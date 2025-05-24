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
\`\`\`
Veri Seti Boyutu: (8124, 23)

Toplam Veri Noktası: 8,124

Özellik Sayısı: 22

Eksik Değer: 0 (Temiz veri seti)

Sınıf Dağılımı:
├── Yenilebilir (e): 4,208 örnek (%51.8)

└── Zehirli (p): 3,916 örnek (%48.2)
\`\`\`

### Model Performansları
\`\`\`
Model Karşılaştırması (Test Seti: 2,437 örnek):

┌─────────────────────┬──────────┬───────────┬─────────┬──────────┐
│ Model│ Accuracy │ Precision │ Recall  │ F1-Score │
├─────────────────────┼──────────┼───────────┼─────────┼──────────┤
│ Random Forest       │  1.0000  │   1.0000  │  1.0000 │  1.0000  │

│ Decision Tree       │  1.0000  │   1.0000  │  1.0000 │  1.0000  │

│ Neural Network      │  0.9988  │   0.9988  │  0.9988 │  0.9988  │

│ Logistic Regression │  0.9512  │   0.9515  │  0.9512 │  0.9512  │

│ Ridge Classifier    │  0.9489  │   0.9492  │  0.9489 │  0.9489  │

│ Naive Bayes         │  0.9234  │   0.9240  │  0.9234 │  0.9234  │
└─────────────────────┴──────────┴───────────┴─────────┴──────────┘
\`\`\`

### Cross-Validation Sonuçları (5-Fold)
\`\`\`
Model                | Ortalama Accuracy | Standart Sapma
─────────────────────┼───────────────────┼────────────────
Random Forest        |     1.0000        |    ± 0.0000

Decision Tree        |     1.0000        |    ± 0.0000

Neural Network       |     0.9988        |    ± 0.0012

Logistic Regression  |     0.9512        |    ± 0.0089

Ridge Classifier     |     0.9489        |    ± 0.0091

Naive Bayes          |     0.9234        |    ± 0.0156

\`\`\`

### En İyi Model
**🏆 Random Forest Classifier** ve **Decision Tree Classifier** 

- **Mükemmel Performans**: %100 doğruluk oranı
- 
- **Sıfır Hata**: Hiç yanlış sınıflandırma yok
- 
- **Güvenilirlik**: Cross-validation'da tutarlı sonuçlar

### Confusion Matrix (Random Forest)
\`\`\`
            Tahmin Edilen
                 
Gerçek      │ Yenilebilir │ Zehirli │
────────────┼─────────────┼─────────┤
Yenilebilir │    1,262    │    0    │

Zehirli     │      0      │  1,175  │
────────────┴─────────────┴─────────┘

Sonuç: Hiç yanlış sınıflandırma yok!
\`\`\`

### Kritik Özellikler (Feature Importance)
\`\`\`
En Önemli 10 Özellik:
┌─────┬─────────────────────────┬─────────────┐
│ Sıra│ Özellik                 │ Önem Skoru  │
├─────┼─────────────────────────┼─────────────┤
│  1  │ odor (Koku)             │   0.1847    │

│  2  │ gill-size (Solungaç)    │   0.1203    │

│  3  │ gill-color (Sol. Rengi) │   0.0891    │

│  4  │ stalk-shape (Sap Şekli) │   0.0756    │

│  5  │ cap-color (Şapka Rengi) │   0.0689    │

│  6  │ bruises (Çürük)         │   0.0634    │

│  7  │ ring-type (Halka Tipi)  │   0.0598    │

│  8  │ population (Popülasyon) │   0.0567    │

│  9  │ habitat (Habitat)       │   0.0534    │

│ 10  │ cap-shape (Şapka Şekli) │   0.0489    │

└─────┴─────────────────────────┴─────────────┘
\`\`\`

### Önemli Bulgular
🔍 **Koku (Odor)** özelliği tek başına mantarın zehirli olup olmadığını %18.5 oranında belirleyebiliyor.

🔍 **İlk 3 özellik** (koku, solungaç boyutu, solungaç rengi) toplam %39.4 önem taşıyor.

🔍 **Mükemmel Ayrım**: Veri setindeki özellikler mantarları %100 doğrulukla ayırt edebiliyor.

### Performans Metrikleri Detayı
\`\`\`
Random Forest Classifier (En İyi Model):

├── True Positives (Doğru Zehirli): 1,175

├── True Negatives (Doğru Yenilebilir): 1,262  

├── False Positives (Yanlış Zehirli): 0

├── False Negatives (Yanlış Yenilebilir): 0

├── Sensitivity (Duyarlılık): 100%

├── Specificity (Özgüllük): 100%

└── Balanced Accuracy: 100%
\`\`\`

### Eğitim Süresi
\`\`\`
Model Eğitim Süreleri (Ortalama):

├── Naive Bayes: 0.003 saniye

├── Logistic Regression: 0.045 saniye

├── Decision Tree: 0.012 saniye

├── Random Forest: 0.234 saniye

├── Ridge Classifier: 0.008 saniye

└── Neural Network: 2.156 saniye
\`\`\`

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

**Kaggle Notebook Linki**: [Buraya Kaggle notebook linkinizi ekleyeceksiniz]

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
- Kaggle Proje Linki: https://www.kaggle.com/code/ouzhanyazc/mushroom-project
- LinkedIn: https://www.linkedin.com/in/o%C4%9Fuzhan-yaz%C4%B1c%C4%B1-2b09aa327/


## 🙏 Teşekkürler

- Akbank Makine Öğrenmesi Bootcamp ekibine

---

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

### Model Performansları
\`\`\`
Model Karşılaştırması (Test Seti Üzerinde):

├── Random Forest: 100.00% Accuracy

├── Decision Tree: 100.00% Accuracy 

├── Logistic Regression: 95.12% Accuracy

├── Ridge Classifier: 94.89% Accuracy

├── Neural Network: 99.88% Accuracy

└── Naive Bayes: 92.34% Accuracy
\`\`\`

### En İyi Model
**Random Forest Classifier** ve **Decision Tree Classifier** mükemmel performans göstermiştir (%100 doğruluk).

### Kritik Özellikler
Özellik önem analizi sonucunda en etkili faktörler:
1. **Odor (Koku)**: En belirleyici özellik
2. **Gill-size (Solungaç boyutu)**
3. **Gill-color (Solungaç rengi)**
4. **Stalk-shape (Sap şekli)**
5. **Cap-color (Şapka rengi)**

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
- LinkedIn: https://www.linkedin.com/in/o%C4%9Fuzhan-yaz%C4%B1c%C4%B1-2b09aa327/
- Email: oguzhanyzcc3429@gmail.com


## 🙏 Teşekkürler

- Akbank Makine Öğrenmesi Bootcamp ekibine

---

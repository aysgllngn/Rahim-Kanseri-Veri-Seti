Rahim Ağzı Kanseri Risk Tahmini
Rahim ağzı ameliyatı,rahimin vajinaya sağlanan alt kısmı olan rahim ağzında kullanılabilir bir kanser türü.Bu proje, uterus (rahim) hastalarına ait klinik ve veriler, tümör hastalıkları ve sağkalım durumlarını tahmin etmeyi amaçlayan bir makine öğrenmesi çalışmasıdır.Veri seti üzerinde veri temizleme,keşifsel veri analizi(EDA) kesme veri tamamlama (imputation), kullanarak sınıf yönetimi (SMOTE) ve fonksiyonu çalıştırma. Model olarak, mesafe tabanlı bir sistem olan K-En Yakın Komşular (KNN) tercih edildi.

Kullanılan Teknolojiler ve Kütüphaneler:Veri Analizi: Pandas, NumPy, Görselleştirme: Matplotlib, Seaborn, Missingno (Eksik veri analizi için), Makine Öğrenmesi: Scikit-Learn, Veri Önişleme: IterativeImputer, MinMaxScaler, LabelEncoder, Dengesiz Veri (Imbalanced Data): Imbalanced-learn (SMOTE, NearMiss)

Veri Seti ve Önişleme: Projede odaklanılan temel özellikler: Klinik Veriler: Teşhis Yaşı, Sağkalım Durumu, Hastalıksız Sağkalım. Moleküler Veriler: MSI MANTIS Skoru, MSIsensor Skoru, Mutasyon Sayısı, Genom Değişim Oranı. Sınıflandırma: Histopatolojik ve Moleküler tümör oluşumları.

Modelin genelleme yeteneği adına veri seti %70 eğitim ve %30 test şekilde değişebilecek. Rastgelelik süresi sabitlemek için random_state=100 kullanıldı.

Veri Dağıtım Analizi: Sayısal özelliklerin güncel durumu. Özellikle Mutasyon Sayısı ve MSI Skoru gibi değişkenlerdeki yoğunlaşmalar, modelin bu özelliklerinin nasıl işleneceği konusunda kritik ipuçları sunuyor. Dağılımların farklı ölçeklerde olması nedeniyle modele giriş öncesinde MinMaxScaler geliştirildi.

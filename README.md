# 📑 **Spotify ve YouTube Veri Seti ile Keşifsel Veri Analizi (EDA)** 

<img src="https://github.com/hamzaugursumer/CapstoneProjectKodlasam/assets/127680099/b1a96964-2cce-4c6e-8171-fc5d32511e87" width="1200" height="500" />

## 📌 **Keşifsel Veri Analizi nedir ?** 

<img src="https://github.com/hamzaugursumer/CapstoneProjectKodlasam/assets/127680099/cec9fc0e-0341-491b-9af3-2a5aff811be6" width="1200" height="500" />

* Keşifsel Veri Analizi (EDA), veri setlerini analiz etmek ve araştırmak için kullanılan bir yöntemdir. Veri bilimciler ve Veri analistleri, EDA’yı veri setlerinin temel özelliklerini belirlemek ve görselleştirmek için kullanır. EDA, veri kalıplarını keşfetmeye, anormallikleri tespit etmeye, hipotez testi yapmaya, veri içerisindeki örüntüleri anlamaya ve varsayımlarda bulunmaya yardımcı olur.

* EDA’nın yapılmasının nedenleri arasında, veri setine derinlemesine bakmayı sağlamak, bariz hataları tespit etmek, veri setindeki kalıpları daha iyi anlamak, aykırı değerleri ve/veya anormal olayları bulmak ve değişkenler arasındaki ilişkileri ortaya çıkarmak yer alır.

* EDA’nın alt başlıkları genellikle istatistiksel grafikler ve diğer veri görselleştirme yöntemlerini içerir. Ancak öncelikle EDA , verilerin bize resmi modelleme veya hipotez testi görevinin ötesinde neler söyleyebileceğini görmek için vardır. Bunların dışında veri setinde bu aşamayı yapmak ve sonrasında bir çalışmaya başlamak daha doğru sonuçların elde edilmesine katkı sağlar.

* **John Tukey'in EDA Tanımı :**
   - "Verileri analiz etme prosedürleri, bu tür prosedürlerin sonuçlarını yorumlama teknikleri, analizini daha kolay, daha kesin veya daha doğru hale getirmek için veri toplamayı planlama yolları ve verilerin analizi için geçerli olan (matematiksel) istatistiklerin tüm makineleri ve sonuçları." (Tukey, John W. (1 Mayıs 1991). "Data Analysis". Fort Belvoir, VA.)

## 📌 **Veri Seti Hakkında**

* [Veri Seti](https://www.kaggle.com/datasets/salvatorerastelli/spotify-and-youtube)

Dünyadaki çeşitli sanatçıların şarkılarından oluşan bir veri kümesidir ve her şarkı için aşağıdakiler mevcuttur:
* Spotify'daki müzik versiyonunun akış sayısı da dahil olmak üzere çeşitli istatistikleri;
* Şarkının resmi müzik videosunun youtube'daki izlenme sayısı.

| **Sütun İsimleri** | **Sütun Açıklamaları** |
|-------------------------|-----------------------------|
| **Şarkı Adı (Track)**       | Şarkının adı, Spotify platformunda görünen şekliyle. |
| **Sanatçı (Artist)**        | Şarkıyı seslendiren sanatçının adı. |
| **Spotify URL'si (Url_spotify)**  | Şarkıyı seslendiren sanatçının Spotify profilinin URL'si. |
| **Albüm (Album)**           | Şarkının yer aldığı albümün adı Spotify'da. |
| **Albüm Türü (Album_type)** | Şarkının Spotify'da tekil bir şarkı mı yoksa bir albümün parçası olarak mı yayınlandığını belirten gösterge. |
| **Spotify Bağlantısı (Uri)** | Şarkının Spotify API üzerinden erişilebilmesi için kullanılan Spotify bağlantısı. |
| **Dans Edilebilirlik (Danceability)** | Bir şarkının dans etmek için ne kadar uygun olduğunu temsil eden bir değer. |
| **Enerji (Energy)**         | Şarkının algısal yoğunluğunu ve aktivite düzeyini temsil eden bir ölçek. |
| **Anahtar (Key)**           | Şarkının müziğinin hangi anahtarla bestelendiğini ifade eden bir sayısal değer. |
| **Ses Şiddeti (Loudness)** | Şarkının genel ses şiddeti, desibel (dB) cinsinden ölçülmüş. |
| **Konuşma Benzerliği (Speechiness)** | Bir şarkıdaki konuşma benzeri seslerin varlığını belirleyen bir ölçek. |
| **Akustiklik (Acousticness)** | Bir şarkının akustik olma olasılığını ifade eden bir güven ölçüsü. |
| **Enstrümantal (Instrumentalness)** | Bir şarkının vokal içerip içermediğini tahmin eden bir ölçek. |
| **Canlılık (Liveness)**    | Kayıtta bir izleyici kitlesinin varlığını tespit etmeye yarayan bir ölçek. |
| **Duygu Durumu (Valence)** | Bir şarkının ilettiği müzikal olumlu veya olumsuz his durumunu belirleyen bir ölçek. |
| **Tempo (Tempo)**           | Bir şarkının genel tahmini tempo hızı, vuruş per dakika (BPM) cinsinden ifade edilir. |
| **Süre (Duration_ms)**     | Şarkının süresi, milisaniye cinsinden ifade edilir. |
| **Spotify'da Akış Sayısı (Stream)** | Şarkının Spotify'da ne kadar kez dinlendiğini gösteren bir sayı. |
| **YouTube URL'si (Url_youtube)** | Şarkıya bağlı olan YouTube videosunun URL'si, mevcut ise. |
| **Video Başlığı (Title)**  | Şarkının YouTube videoklibinin başlığı. |
| **Kanal (Channel)**         | YouTube'da videoyu yayınlayan kanalın adı. |
| **Görüntülenme Sayısı (Views)** | YouTube videoklibinin kaç defa görüntülendiğini gösteren bir sayı. |
| **Beğeni Sayısı (Likes)**  | YouTube videoklibine yapılan beğeni sayısı. |
| **Yorum Sayısı (Comments)** | YouTube videoklibine yapılan yorum sayısı. |
| **Açıklama (Description)** | YouTube videoklibinin içeriği hakkında açıklama. | 
| **Lisanslı (Licensed)**    | Videonun lisanslı içerik olup olmadığını gösteren bir işarettir. |
| **Resmi Video (official_video)** | Şarkının resmi müzik videosu olup olmadığını belirleyen boolean bir değer. |

## 📌 **Yapılan Çalışmanın İçeriği ve Alt Başlıkları**

* [Jupyter Çalışma Dosyası](https://github.com/hamzaugursumer/CapstoneProjectKodlasam/blob/main/Capsone%20Project%20EDA1.ipynb)

1. Giriş
2. Veri Kümesi Hakkında
3. Sütunlar Hakkında
4. Kütüphanelerin İçe Aktarılması
5. DataFrame'in oluşturulması
6. Veri Setinin incelenmesi (EDA ve Data Preprocessing)
7. Aykırı Değerler
8. İçgörüler (Analizler) :
   - YouTube Metrikleri arasındaki Korelasyon
   - Top 10 Sanatçı YouTube İzlenme, Beğeni ve Spotify Stream Sayıları
   - Albüm Türüne göre Dağılım
   - Spotify Metriklerinin Korelasyonu
   - Spotify Metriklerinin Veri seti içerisinde Dağılımı
   - En çok dinlenen Spotify ve YouTube şarkılarının Karşılaştırılması
   - Sanatçı ve Şarkı bazlı Platform Karşılaştırması
   - Kanal İstatistikleri
   - Top 5 şarkının Metrikleri
   - Enerji, Dans Edilebilirlik ve Duygu durumlarına göre Top 1 Sanatçıların Yüzde Değerleri

   
**NOT :** 
* Yaptığım çalışmada plotly kütüphanesi ile görselleştirdiğim analizler dosyada görüntülenmemektedir Github'dan dolayı. Ancak kodlar çalıştırıldığında görselleştirmeler oluşmaktadır.
* Bu çalışma boyunca, Spotify ve YouTube hakkında kapsamlı bir keşifsel veri analizi gerçekleştirdim ve veri setinin içindeki bilgilere ulaşmak için çeşitli analitik yöntemleri uyguladım. Verilerin temizlenmesi, görselleştirilmesi ve anlaşılması süreci, projemin temelini oluşturdu ve bu aşamada edindiğim bilgiler, Veri analisti olma sürecime ışık tuttu.
* Bu projeyi başarıyla tamamlamamda yardımcı olan herkese teşekkür etmek isterim. Ayrıca, herhangi bir geri bildiriminiz veya öneriniz varsa, lütfen çekinmeden paylaşın. Bu, gelecekteki çalışmalarımızı daha da iyileştirmemize yardımcı olacaktır.
* Son olarak ⭐ vermeyi unutmayın, Teşekkürler.

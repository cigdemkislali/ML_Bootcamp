## FUTBOL TAKIMI DEĞERLEMELERİNİ MAKİNE ÖĞRENMESİ MODELLERİYLE TAHMİN ETME
- **PROJENİN AMACI:**
Bu projede futbol takımlarının fiyatlarını tahmin etmek için bir veri seti kullanılır.Veri seti, büyük Avrupa liglerindeki futbol takımı fiyatlarının analizi ve modellemesine yardımcı olmak için tasarlanmış titizlikle düzenlenmiş bir veri noktaları koleksiyonudur. Bu veri seti, futbol takımlarının finansal değerlemesini etkileyen faktörlere dair kapsamlı bir görünüm sağlayan çeşitli sayısal ve kategorik özellikleri kapsar.
- **VERİ SETİ:**
Kullanılan veri seti, 50000 satır içerir. Sütun isimleri ise sırasıyla şu şekildedir:
-AveragePlayerAge(OrtalamaOyuncuYaşı): Takım oyuncularının yaş ortalaması.
-TotalGoalsLastSeason(GeçenSezonToplamGoller):Takımın geçen sezon attığı toplam gol sayısı.
-MatchesWonLastSeason(Son Sezonda Kazanılan Maçlar):Takımın son sezonda kazandığı maç sayısı
-MatchesDrawnLastSeason(Geçen SezonÇekilen Maçlar): Takımın son sezonda berabere kaldığı maç sayısı.
-MatchesLostLastSeason(Geçen Sezon Kaybedilen Maçlar): Takımın son sezonda kaybettiği maç sayısı.
-TotalGoalsConcededLastSeason(ToplamGeçen Sezon Yenilen Goller):
-TotalRevenueLastSeason(Geçen Sezon Toplam Gelir)
-StadiumCapacity(Stadyum Kapasitesi)
-AverageAttendance(Ortalama Katılım)
-TransferSpendingLastSeason(TransferHarcamalarıGeçenSezon)
-TransferIncomeLastSeason(TransferGeliriGeçenSezon)
-NumberOfTrophies(Kupa Sayısı) 
-MarketValueOfSquad(Takımın Piyasa Değeri)
-AveragePlayerMarketValue(ortalamaOyuncuPiyasaDeğeri)
-YouthAcademyRating(gençlikAkademiDeğerlendirme)
-League(Lig)
-Country(Ülke)
-Manager(müdür)
-TeamFormation(TakımOluşumu)
-PlayingStyle(Oyun Tarzı)
-HomeCity(Ana SayfaŞehir)
-StadiumType(Stadyum Türü)
-MainSponsor(AnaSponsor)
-KitManufacturer(KitÜreticisi)
-OwnershipType(Sahiplik Türü)
-Price(Fiyat): Takım oyuncularının fiyatlarını gösteren sütun.
- **PROJENİN KAPSAMI:**
Projede denetimli öğrenme ve denetimsiz öğrenme algoritmalarıyla çalışıldı. Denetimli öğrenme algortimaları olan LGBM ve Catboost algoritmalarıyla çalışıldı. Bağımlı değişken olarak(Price) sütunu ele alınarak futbol takımlarının finansal değerlemesini etkileyen faktörlere dair kapsamlı bir görünüm sağlayan çeşitli sayısal ve kategorik özelliklerle tahmin edildi. Denetimsiz Öğrenme algoritmalarından ise Kümeleme algoritmasıyla çalışıldı. Bu öğrenme türünde aynı veri seti kullanılarak sadece veri setinde bulunan bağımlı(Price) değişken çıkarılarak bağımsız değişkenler arasındaki ilişki incelendi.
- **SONUÇLAR:**
Aynı veri seti, her iki öğrenme türü modeliyle analiz edilerek bu öğrenme türleri kapsamında en iyi performansı gösteren modelin kümeleme algoritması(K-Means) olduğu sonucuna ulaşılmıştır. Denetimli öğrenme kapsamında kullanılan LGBM ve Catboost algoritmalarında değerlendirme metriği olarak RMSE(hata kareler ortalamasının karekökü) kullanılmış olup denetimsiz öğrenme algoritması olan K-means 'ta ise adjusted_rand_score, homogeneity_score, v_measure_score ve completeness_score metrikleri kullanılmıştır.

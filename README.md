# BOYUT AZALTMA NEDİR?

Gerçek hayattaki veriler çok fazla boyuta (özniteliğe) sahip oluyor ve boyut büyüdükçe veri 
temizlemeden model kurmaya bütün süreçlerde harcamamız gereken zaman ve kaynaklar artıyor. 
Boyut azatma bu sorunun önüne geçmek için kullanılan yöntemlerden biridir. Hemen her veri 
setinde bazı öznitelikler arasında yüksek korelasyon oluyor ve bu bizim gereksiz bilgiye sahip 
olmamıza ve modelimizde overfitting problemine sebep olabiliyor.

![3d-boyutsal-küçültmenin-etkisi-2dye-etkisi](https://user-images.githubusercontent.com/72496488/207951049-df1d3e7c-ec76-4e1e-a265-c3707cfa1214.jpg)

# Nasıl Uygulanır ?

Boyut küçültmenin en kolay yolu verimizi en iyi tanımlayan öznitelikleri bulup diğerlerini atmaktır 
(öznitelik seçimi — feature selection). Dikkat edilmesi gereken nokta en az bilgi kaybıyla bu işi 
yapmaktır ve aslında önemli olan öznitelikleri silmemektir. Bunu yapmak için verideki dağılımın 
maksimum varyansını-bilgisini tutan minimum sayıda değişken oluşturuyoruz. Eğer bir değişken her 
örnek için aynı değere sahip ise gereksiz bir değişkendir. Biz en yüksek varyansa sahip olan 
değişkenleri bulmalıyız.

![Ekran Alıntısı](https://user-images.githubusercontent.com/72496488/207951177-5e34ab8b-9ea4-4af7-b797-ed3f21803e72.PNG)


# HDI(İnsani Kalkınma Endeksi)

 Buna en güzel örneklerden biri HDI(İnsani Kalkınma Endeksi) hesaplaması 
olabilir.Ülkelerin sahip olduğu değişkenlerden bazıları (wiki): resmi dil, yüz ölçümü 
(toplam), su oranı, nüfus, nüfus yoğunluğu, GSYH, para birimi, trafik akışı, hukuk, dış 
ilişkiler, din, eğitim, sağlık, sanayi, tarım, turizm… Bunlara ek olarak ülkeden ülkeye 
değişen yüzlerce değişken sıralayabiliriz.

# HDI(İnsani Kalkınma Endeksi)

• PCA metodu sanayi, tarım, turizm vs. ekonomiyle ilgili yüzlerce değişkeni ve nüfusu kullanıp kişi 
başına düşen gayri safi milli gelir diye tek bir değişken oluşturuyor. Yani yüzlerce boyutluk bilgi en az 
bilgi kaybıyla tek boyutta tutulmuş oluyor.
•HDI hesaplamalarında sadece 5 özniteliğe bakılarak pek de itiraz edilmeyecek bir tablo karşımıza 
çıkıyor.
• Kişi başına düşen gayri safi milli gelir
• İnsan gelişmişlik endeksi — HDI sıralaması
• Beklenen ortalama yaşam süresi
• Beklenen eğitim yılı
• Ortalama eğitim yılı

![sadsa](https://user-images.githubusercontent.com/72496488/207951519-3445d2a1-c1d8-420d-ae83-23527831d664.PNG)

# PCA Metodu

Boyut azaltma işlemlerinde sıklıkla kullanılan PCA verideki gerekli bilgileri ortaya çıkarmada oldukça 
etkili bir yöntemdir. PCA’nın arkasında yatan temel mantık çok boyutlu bir veriyi, verideki temel 
özellikleri yakalayarak daha az sayıda değişkenle göstermektir. En iyi sonucu elde etmek için genelde 
öncelikle standardizasyon yapılır.
 x = StandardScaler().fit_transform(x)

![asdads](https://user-images.githubusercontent.com/72496488/207951693-fd6f0c85-6a3c-42be-ae3e-d9e7406fbbd1.PNG)

# PCA Metodu
• Sonrasında PCA uygulanılır.
• from sklearn.decomposition import PCA
• pca = PCA(n_components=2)
• principalComponents = pca.fit_transform(x)
• principalDf = pd.DataFrame(data = principalComponents, columns = ['principal component 1', 'principal component 2'])

![sad](https://user-images.githubusercontent.com/72496488/207951825-34be4de2-a7ad-4b88-b161-6c5ae83f837c.PNG)

#KAYNAKÇA

https://medium.com/data-science-tr/makine-%C3%B6%C4%9Frenmesi-dersleri-boyut-azaltma-pca-5ae9e902ef92
https://medium.com/@gulcanogundur/pca-principal-component-analysis-temel-bile%C5%9Fenler-analizi-bf9098751c62#:~:text=T%C3%BCrk%C3%A7esi%20%E2%80%9CTemel%20Bile%C5%9Fenler%20Analizi%E2%80%9D%20olan,indirgemeyi%20sa%C4%9Flamak%20olan%20bir%20tekniktir.








# BOYUT AZALTMA NEDİR?

Gerçek hayattaki veriler çok fazla boyuta (özniteliğe) sahip oluyor ve boyut büyüdükçe veri 
temizlemeden model kurmaya bütün süreçlerde harcamamız gereken zaman ve kaynaklar artıyor. 
Boyut azatma bu sorunun önüne geçmek için kullanılan yöntemlerden biridir. Hemen her veri 
setinde bazı öznitelikler arasında yüksek korelasyon oluyor ve bu bizim gereksiz bilgiye sahip 
olmamıza ve modelimizde overfitting problemine sebep olabiliyor.

![cubukgrafik](https://user-images.githubusercontent.com/72496488/207949307-a88f6551-b911-48f8-be92-dea782d9a75e.png)


# Nasıl Uygulanır ?

Boyut küçültmenin en kolay yolu verimizi en iyi tanımlayan öznitelikleri bulup diğerlerini atmaktır 
(öznitelik seçimi — feature selection). Dikkat edilmesi gereken nokta en az bilgi kaybıyla bu işi 
yapmaktır ve aslında önemli olan öznitelikleri silmemektir. Bunu yapmak için verideki dağılımın 
maksimum varyansını-bilgisini tutan minimum sayıda değişken oluşturuyoruz. Eğer bir değişken her 
örnek için aynı değere sahip ise gereksiz bir değişkendir. Biz en yüksek varyansa sahip olan 
değişkenleri bulmalıyız.

# HDI(İnsani Kalkınma Endeksi)

Buna en güzel örneklerden biri HDI(İnsani Kalkınma Endeksi) hesaplaması 
olabilir.Ülkelerin sahip olduğu değişkenlerden bazıları (wiki): resmi dil, yüz ölçümü 
(toplam), su oranı, nüfus, nüfus yoğunluğu, GSYH, para birimi, trafik akışı, hukuk, dış 
ilişkiler, din, eğitim, sağlık, sanayi, tarım, turizm… Bunlara ek olarak ülkeden ülkeye 
değişen yüzlerce değişken sıralayabiliriz.

![thumbs_b_c_e36b48579f43bc734835288303fd38f6](https://user-images.githubusercontent.com/72496488/207949761-c6be79bf-6373-49c9-bc9a-d38d10aefa90.jpg)

# PCA Metodu

Boyut azaltma işlemlerinde sıklıkla kullanılan PCA verideki gerekli bilgileri ortaya çıkarmada oldukça 
etkili bir yöntemdir. PCA’nın arkasında yatan temel mantık çok boyutlu bir veriyi, verideki temel 
özellikleri yakalayarak daha az sayıda değişkenle göstermektir. En iyi sonucu elde etmek için genelde 
öncelikle standardizasyon yapılır.













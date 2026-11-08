# Rapor

**Ad Soyad:Ali Deniz Tüfekci**
**Numara:722**

## 1. Problem Analizi
<-- Bir deneme sınavı sonuç hesaplama mekanizması , kullanıcıdan doğru sayısı ve yanlış sayısı verilerini ayrı ayrı alıp bunlardan hareketle boş sayısı, net sayısı ve başarı durumu değerlerini hesaplar. Bunları sırasıyla ekrana yansıtır. Ancak değerlerden birinin veya her ikisinin yanlış girilip girilmediğini de ölçer ve eğer bir yanlışlık yakalarsa uyarı verir.   -->


## 2. Girdi - İşlem - Çıktı

**Girdiler:**
-TEST:girdi int ds:13 , girdi int ys:5 

**İşlemler:**
-TEST:ilk önce ds ve ys girdilerini alır ve uygunluklarını (0'dan küçük ya da 20'den büyük olup olmama durumlarını) ölçer. Uygunlarsa (ki öyleler) önce boş sayısını (int boss değişkenini) , sonra net sayısını (double nets değişkenini) hesaplar ve nets değişkeninin ne olduğunu göz önünde bulundurarak if , else if ve else kodlarına göre başarı durumunu ve bununla birlikte boş ve net sayılarını çıktı verir(TEST:çıktı kısmında görüleceği üzere).

**Çıktılar:**
-TEST: çıktı "Basari durumunuz IYI olarak olculmustur.Ayrica net sayiniz 11.75'dir ve bos sayiniz de 2'dir"     (çünkü 13-5/4=11.75'tir ve programdaki koşul karar yapıları 11.75 neti IYI kategorisine almaktadır,yani çıktı buna uygun."

## 3. Matematiksel Formüller

-1)girilen doğru ve yanlış sayılarının uygunluğunu ölçerken kullandığımız :else if (ys+ds<0 || ys + ds >20)   ifadesi
-2)int boss =20- (ys+ds) ifadesi
-3)double nets = ds - (double)ys /4 ifadesi

not:herhangi bir +/-/*// işareti olmadan sadece matematiksel operatör kullandığım ifadeleri dahil etmedim.
## 4. Sözde Kod (Pseudocode)

```
1.output : "MERHABA!Sizden deneme sinav sonuclarini girmenizi istiyorum.Ilk önce dogru cevap sayinizi giriniz."
2.input: tam sayı ds (değişken tanımlama +girdi)
3.if (ds<0 ya da ds>20) ise 4'den devam et , else 5'den devam et.
4.output "GECERSİZ DOGRU SAYISI!!!!!",BİTTİ.
5.output "Simdi de yanlis sayinizi giriniz."
6.input: tam sayı ys (değişken tanımlama +girdi) 
7.if (ys>20 ya da ys<0) ise 8'den , else  9'dan devam et.
8.output "GECERSİZ YANLIS SAYISI!!!!!",BİTTİ.
9.else if  (ys+ds>20 ya da ys + ds <0) ise 10'dan , else 11'den devam et.
10.output "Bu iki sayinin en az biri yanlis girilmistir cunku sayilarin toplami 20'den coktur. "
11.int boss = 20 - (ys +ds)
12.double nets =ds - (double)ys/4
13.if (nets<=5) ise 14'den,else 15'den devam et.
14.output: "Basari durumunuz ,GELISTIRILMELI olarak olculmustur."+ "Ayrica net sayiniz " + nets + "'dir ve bos sayiniz de "+ boss + "'dir"
15.else if (nets >5 ve nets<=10) ise 16'dan ,else 17'den devam et.
16.output:"Basari durumunuz ORTA olarak olculmustur."+ "Ayrica net sayiniz " + nets + "'dir ve bos sayiniz de "+ boss + "'dir"
17.else if (nets >10 and nets <=15) ise 18'den , else 19'dan devam et.
18.output:"Basari durumunuz IYI olarak olculmustur."+ "Ayrica net sayiniz " + nets + "'dir ve bos sayiniz de "+ boss + "'dir"
19.else output:"Basari durumunuz COK IYI olarak olculmustur."+ "Ayrica net sayiniz " + nets + "'dir ve bos sayiniz de "+ boss + "'dir"BİTİR.






















```

## 5. Akış Şeması

![Akış Şeması](docs/akis-semasi.png)

## 6. Başarı Durumu Koşulları
<!-- Koşulları hangi sırayla ve hangi operatörlerle yazdığınızı, nedenini açıklayın. -->


## 7. Test Sonuçları

| Doğru | Yanlış | Beklenen | Programın sonucu | Doğru mu? |
|---|---|---|---|---|
| 20 | 0 | Net 20, Çok iyi | | |
| 15 | 4 | Net 14, İyi | | |
| 10 | 8 | Net 8, Orta | | |
| 5 | 0 | Net 5, Geliştirilmeli | | |
| 0 | 20 | Net -5, Geliştirilmeli | | |
| 10 | 10 | Net 7,5, Orta | | |
| 15 | 10 | Geçersiz giriş | | |
| 12 | 9 | Geçersiz giriş | | |
| -1 | 5 | Geçersiz giriş | | |

---
layout: post
title: Makine Öğrenmesi Nedir?
---

<h3> Makine Öğrenmesi nedir? </h3>

Makine öğrenimi şu sorudan doğar: Bir bilgisayar, belirli bir görevi nasıl gerçekleştireceğini kendi başına öğrenebilir mi? Veri işleme kurallarını kodlayan programcılar olmaksizin, bir bilgisayar bu kuralları verilere bakarak otomatik olarak öğrenebilir mi?

Bu soru yeni bir programlama paradigmasının kapısını açıyor. Klasik programlamada, sembolik yapay zeka paradigması, insan girdi kuralları (bir program) ve bu kurallara göre işlenecek veriler ve cevaplar ortaya çıkar. Makine öğrenimiyle, insanlar verinin yanı sıra verilerden beklenen yanıtları da girer ve kurallar ortaya çıkar. Bu kurallar daha sonra orijinal cevaplar üretmek için yeni verilere uygulanabilir.

Makine öğreniminin ilk tanımı, Amerikan yapay zeka öncüsü Arthur Samuel'e (1959) kadar uzanıyor: "Makine öğrenimi, bilgisayarlara açıkça programlanmadan öğrenme yeteneği veren çalışma alanıdır". Buradaki temel unsurlar, açıkça programlanmadan öğrenmedir. 

Bir bilgisayarı açıkça programlamak, belirli bir görevi gerçekleştirmek için uyması gereken kuralları ve talimatları tanımlamak anlamına gelir. Bu, yazılım mühendislerinin geliştirdiği öğrenme yeteneği olmayan her türlü uygulamayı yazarken yaptığı şeydir. Fakat her zaman kuralları tanımlamak ilk bakışta mümkün değildir. Bazı önemsiz eylemleri gerçekleştirirken verdiğiniz çeşitli kararlar hakkında düşünelim: Arkadaşlarınızı gördüğünüzde tanımak için izlediğiniz süreci açıklayabilir misiniz? Araba sürerken verdiğiniz tüm anlık kararlar? Konuşurken uyguladığın tüm İngilizce gramer kurallarını listeleyebilir misin? Bir şeyi nasıl yaptığınızı tam olarak açıklayamıyorsanız, bir bilgisayara onu yapması için talimat verme şansınız yoktur. 

Artur Samuel, "talimat verilen bilgisayarları" "onlara öğrenme yeteneği vermek" ile değiştirmeyi önerdi. Aslında talimatlara uymak yerine öğrenmek, İnsanların her zaman yaptığı şeydir. Annelerimiz ve babalarımız, henüz bir yaşında bize gramer kitapları vererek ana dillerini öğretmiyorlar. Bizimle sadece doğal bir şekilde konuşuyorlar ve biz onların örneklerinden öğreniyoruz, binlerce gramer kuralını bilmeden uyguluyoruz. Aslında beynimiz, okulda dilbilgisini rasyonel bir şekilde anlayabilmeden çok önce kuralları otomatik olarak çıkarma yeteneğine sahip. Biz insanlar için bile, örneklerden kuralları öğrenmek, hem doğal hem de daha kolay olabilir gibi görünüyor. Aşağıdaki şekil geleneksel programlama ve makine öğrenimi arasındaki farkı göstermektedir.

![](/images2/ClassicProgrammingVSmachineLearning.png)
<br>[Image source: “Zero to AI”, Gianluca Mauro & Nicolo Valigi](https://www.manning.com/books/zero-to-ai#:~:text=About%20the%20book,AI%20to%20shape%20their%20industries)

Bir makine öğrenimi sistemi, açıkça programlanmak yerine eğitilir. Bir görevle ilgili birçok örnek sunulur ve bu örneklerde, görevi otomatikleştirmek için kurallar oluşturmaya izin veren kalıplar, istatistiksel metodlar uygulanarak bulunur. İnsanların deneyimlerden öğrendiği gibi, makine öğrenimi teknikleri de bilgisayarların verilerden öğrenmesini sağlar. Mesela, bir bilgisayara kediler ve köpekleri resimlerle ayırt etmeyi öğretmek. Verilen resimdeki canlının kedi mi yoksa köpek mi olduğu sorusuna yönelik bir makine öğrenmesi çözümü, çocukluk öğrenme deneyimlerimize benzer. Bilgisayarı binlerce kedinin resmiyle besliyoruz ve ona "bunlar kedi" diyoruz ve sonra binlerce köpek resmi ve "bunlar köpek" diyoruz. Son olarak, iki evcil hayvan arasındaki farkı otomatik olarak bulmasına izin veriyoruz. Köpekleri kedilerden ayıran temel unsurları açıklamamıza gerek yok. İyi bir makine öğrenimi uygulaması bunu aldığı örneklerden anlamayı öğrenir. 

![](/images2/catVSdog.gif)
<br>[Image source: https://github.com/ReiCHU31/Cat-Dog-Classification-Flask-App](https://github.com/ReiCHU31/Cat-Dog-Classification-Flask-App)

<h3>Makine öğrenmesi uygulama alanları</h3>

2000'li yıllarla beraber büyük veri ve bilgi işlem gücü teknolojilerinin gelişmesi, makine öğrenimi algoritmaları için mükemmel ortamı yarattı. Gerçekten de, bugün AI dediğimiz şeyin tüketiciye yönelik en havalı uygulamalarının çoğu büyük ölçüde makine öğrenimine güveniyor: Siri sesli sanal asistanı, Google Translate, kendi kendine giden arabalar ve daha fazlası:
1. **Voice Assistants** - Sesli asistanlar her yerde karşımıza çıkabiliyor. En bilinenleri "Apple’s Siri", "Amazon's Alexa" ve "Google Assistant" olarak sıralayabiliriz.
2. **Smartphone Cameras** - Akıllı telefonların kameralarının her geçen gün gelişen fotoğraf kalitelerinin arkasında makine öğrenmesi teknikleri var. Nesneleri algılamak, arka planı bulanıklaştırmak ve filtreleme işlemleri için görüntüdeki her piksel analiz ediliyor.

<p>
  <kbd>
    <img src="/images/ML_sampleUseCase1.png" width="600">
  </kbd>
  <br/>
  <a href="https://www.infoq.com/presentations/ml-dl-visual-intro/?utm_source=presentations&utm_medium=london&utm_campaign=qcon">Image source: Jay Alammar, QCON 2020 London speech</a>
</p>

3. **Smartphone Face Unlock** - Akıllı telefonumuzu alıyoruz ve yüzümüzü algılayarak kendi kendine açılıyor. Akıllı, verimli, zaman kazandıran bir özellik. 
4. **Netflix Recommendations** - Netflix'te gördüğünüz her önerilen video bir algoritma tarafından seçilmektedir. Şirket, algoritmaların sağladığı kişiselleştirilmiş servislerin müşteriyi elde tutma konusunda, yılda 1 milyar dolar değer ürettiğini tahmin ediyor.
5. **Dynamic Pricing** - Müşterilerin artık saniyeler içinde birden çok tedarikçi arasında fiyatları kolayca karşılaştırabildiği e-ticaret çağında, fiyat artık satın alma kararındaki en büyük faktör olarak kabul ediliyor. Uçak ve otel rezervasyonları, online alış-veriş siteleri başta olmak üzere pek çok alanda kullanılmaktadır.
6. **Google Maps** - Google Maps uygulaması en efektif rotayı ve alternatiflerini hesaplarken yada tahmini varış süresi ve trafik yoğunluğu bilgileri için makine öğrenmesi tekniklerinden yararlanır.
7. **Email Filtering** - Örnek olarak Gmail gelen mailin spam olup olmadığına makine öğrenmesi ile karar verir. Ayrıca mailleri konu başlıklarını inceleyerek otomatik olarak 3 sınıfa ayırabilir: Birincil (Primary), sosyal (social) ve promotion (promosyon).
8. **Google Translate** - Belki de en yaygın kullanılan makine öğrenmesi uygulaması, teşekkürler Google!..
9. **Customer Support Queries/Chatbots** - Bugünlerde neredeyse her müşteri destek uygulamasında makine öğrenmesi teknikleri karşımıza çıkıyor. Sesli uygulamalarda makine öğrenimi gelen mesajı yada soruyu uygun destek elemanına yönlendirmek için kullanılır. Metin tabanlı sorgular ise, artık neredeyse yalnızca sohbet robotları (chatbots) tarafından ele alınmaktadır. Neredeyse tüm işletmeler artık sitelerinde bu sohbet robotlarından yararlanıyor.
10. **Video Surveillence** - Küresel olarak devletler ve kuruluşlar, davetsiz misafirleri ve olası tehditleri tespit etmek, suçluları yakalamak gibi çeşitli görevler için makine öğrenmesi tabanlı video gözetimini kullanıyor.
11. **Catching Fraud in Banking** - Hiç kredi kartı dolandırıcılığının kurbanı oldunuz mu?.. Makine öğrenimi algoritmaları, dolandırıcılık tespitinden dolandırıcılığı önlemeye kadar, bankaların müşteri deneyimini iyileştirmek için çalışma şeklini değiştiriyor.
12. **Self Driving Cars** - Donanım ve makine öğrenimi açısından teknolojinin ortaya koyduğu belki de en inanılmaz ve en hayranlık verici uygulama alanıdır.
13. **Identifying Diseases and Diagnosis** - Sağlık hizmetlerinde başlıca ML uygulamalarından biri, başka türlü teşhis edilmesi zor kabul edilen hastalıkların ve rahatsızlıkların tanımlanması ve teşhisidir. Bu, ilk aşamalarda yakalanması zor olan kanser ve diğer genetik hastalıklara kadar her şeyi içerebilir. IBM Watson Genomics, makine öğreniminin genom tabanlı tümör dizilimi ile bütünleştirilmesinin hızlı tanı koymaya nasıl yardımcı olabileceğinin en iyi örneğidir

<br>ve çok daha fazlası........


Kaynakça:
1. [“Zero to AI”, Gianluca Mauro & Nicolo Valigi](https://www.manning.com/books/zero-to-ai#:~:text=About%20the%20book,AI%20to%20shape%20their%20industries)
2. ["Deep Learning with Python", François Chollet](https://www.manning.com/books/deep-learning-with-python)
3. [Machine learning - Wikipedia](https://en.wikipedia.org/wiki/Machine_learning)
4. ["Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow", Aurellion Geron](https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1492032646)

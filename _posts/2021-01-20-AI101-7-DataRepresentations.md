---
layout: post
title: Verilere farklı şekillerde bakmak
---

<p>
  <kbd>
    <img src="/images2/ML_vs_DL.png" width="800">
  </kbd>
</p>

<br>[Image source: HBR, How to win with ML](https://bluehexagon.ai/blog/what-is-deep-learning-and-how-is-it-different-from-machine-learning/)

<h3> Verilerden temsilleri öğrenmek </h3>
"Deep Learning with python" kitabında **François Chollet** bu konuyu mükemmel anlatmış:

Makine öğrenimi yapmak için üç şeye ihtiyacımız var:
1. Giriş veri noktaları — Örneğin, görev konuşma tanıma ise, bu veri noktaları konuşan insanların ses dosyaları olabilir. Görev resim etiketleme ise, bunlar resim olabilir.
2. Beklenen çıktı örnekleri - Bir konuşma tanıma görevinde bunlar, ses dosyalarının insan tarafından oluşturulmuş transkriptleri olabilir. Bir görüntü görevinde, beklenen çıktılar "köpek", "kedi" vb. Etiketler olabilir.
3. Algoritmanın iyi bir iş yapıp yapmadığını ölçmenin bir yolu — Bu, algoritmanın mevcut çıktısı ile beklenen çıktı arasındaki mesafeyi belirlemek için gereklidir. Ölçüm, algoritmanın çalışma şeklini ayarlamak için bir geri bildirim sinyali olarak kullanılır. Bu ayarlama adımı (optimizasyon), öğrenme dediğimiz şeydir.

Bir makine öğrenimi modeli, girdi verilerini anlamlı çıktılara dönüştürmek için kullanılır. Bu nedenle, makine öğrenimi ve derin öğrenmedeki temel sorun, verileri anlamlı bir şekilde dönüştürmektir: başka bir deyişle, eldeki girdi verilerinin yararlı temsillerini - bizi beklenen çıktıya yaklaştıran temsilleri - öğrenmek. 

Peki temsil nedir? Özünde, verilere bakmanın farklı bir yoludur — verileri temsil etmek veya kodlamak. Örneğin, renkli bir görüntü RGB formatında (kırmızı-yeşil-mavi) veya HSV formatında (ton-doygunluk-değeri) kodlanabilir: bunlar aynı verinin iki farklı temsilidir. Bir temsilde zor olabilecek bazı görevler, diğeriyle kolay hale gelebilir. Örneğin, "görüntüdeki tüm kırmızı pikselleri seçme" görevi RG formatında daha basitken "görüntüyü daha az doygun hale getir" daha basittir
HSV formatında. Makine öğrenimi modellerinin tümü, girdi verileri için uygun temsilleri bulmakla ilgilidir - verilerin, sınıflandırma görevi gibi, eldeki göreve daha uygun hale getiren dönüştürmeleri.
<h3>Makine Öğrenimi Yöntemleri</h3>
Makine öğrenimi yöntemleri 3 ana kategoriye ayrılır: 
<p>
  <kbd>
    <img src="/images2/ML_types_summary.jpeg" width="600">
  </kbd>
</p>

<iframe src="https://www.youtube.com/embed/TmPfTpjtdgg" width="600" height="400"  frameborder="0" allow="allowfullscreen">
</iframe>
[Source: https://towardsdatascience.com/tutorial-double-deep-q-learning-with-dueling-network-architectures-4c1b3fb7f756](https://towardsdatascience.com/tutorial-double-deep-q-learning-with-dueling-network-architectures-4c1b3fb7f756)

Kaynakça:
1. [“Zero to AI”, Gianluca Mauro & Nicolo Valigi](https://www.manning.com/books/zero-to-ai#:~:text=About%20the%20book,AI%20to%20shape%20their%20industries)
2. ["Deep Learning with Python", François Chollet](https://www.manning.com/books/deep-learning-with-python)
3. [Machine learning - Wikipedia](https://en.wikipedia.org/wiki/Machine_learning)

---
layout: post
title: Verilere farklı şekillerde bakmak
---

<p>
  <kbd>
    <img src="/images2/ML_vs_DL.png" width="800">
  </kbd>
</p>

<h3> Verilerden temsilleri öğrenmek </h3>
"Deep Learning with python" kitabında **François Chollet** bu konuyu mükemmel anlatmış:

Makine öğrenimi yapmak için üç şeye ihtiyacımız var:
1. Giriş veri noktaları — Örneğin, görev konuşma tanıma ise, bu veri noktaları konuşan insanların ses dosyaları olabilir. Görev resim etiketleme ise, bunlar resim olabilir.
2. Beklenen çıktı örnekleri - Bir konuşma tanıma görevinde bunlar, ses dosyalarının insan tarafından oluşturulmuş transkriptleri olabilir. Bir görüntü görevinde, beklenen çıktılar "köpek", "kedi" vb. Etiketler olabilir.
3. Algoritmanın iyi bir iş yapıp yapmadığını ölçmenin bir yolu — Bu, algoritmanın mevcut çıktısı ile beklenen çıktı arasındaki mesafeyi belirlemek için gereklidir. Ölçüm, algoritmanın çalışma şeklini ayarlamak için bir geri bildirim sinyali olarak kullanılır. Bu ayarlama adımı (optimizasyon), öğrenme dediğimiz şeydir.

Bir makine öğrenimi modeli, girdi verilerini anlamlı çıktılara dönüştürmek için kullanılır. Bu nedenle, makine öğrenimi ve derin öğrenmedeki temel sorun, verileri anlamlı bir şekilde dönüştürmektir: başka bir deyişle, eldeki girdi verilerinin yararlı temsillerini - bizi beklenen çıktıya yaklaştıran temsilleri - öğrenmek. 

Peki temsil nedir? Özünde, verilere bakmanın farklı bir yoludur: verileri temsil etmek veya kodlamak. Örneğin, renkli bir görüntü RGB formatında (kırmızı-yeşil-mavi) veya HSV formatında (ton-doygunluk-değeri) kodlanabilir: bunlar aynı verinin iki farklı temsilidir. Bir temsilde zor olabilecek bazı görevler, diğeriyle kolay hale gelebilir. Örneğin, "görüntüdeki tüm kırmızı pikselleri seçme" görevi RGB formatında daha basitken, "görüntüyü daha az doygun hale getir" görevi HSV ile daha basittir.

Makine öğrenimi modellerinin tümü, girdi verileri için uygun temsilleri bulmakla ilgilidir. Buna bir örnek ile bakalım:

Aşağıdaki resimde görüldüğü gibi, birkaç beyaz noktamız ve birkaç siyah noktamız var. Diyelim ki, bir noktanın koordinatlarını (x, y) alabilen ve bu noktanın siyah veya beyaz olma durumunu tahmin edebilen bir algoritma geliştirmek istediğimizi varsayalım. Bu durumda,
1. Giriş verisi, noktalarımızın koordinatlarıdır.
2. Beklenen çıktılar, noktalarımızın renkleridir.
3. Algoritmamızın iyi bir iş yapıp yapmadığını ölçmenin bir yolu, doğru şekilde sınıflandırılan noktaların yüzdesi olabilir.

Burada ihtiyacımız olan şey, beyaz noktaları siyah noktalardan temiz bir şekilde ayıran verilerimizin yeni bir temsilidir. Diğer birçok olasılığın yanı sıra kullanabileceğimiz bir dönüşüm, alttaki şeklin sağ tarafında olduğu gibi bir koordinat değişikliği olabilir.

<p>
  <kbd>
    <img src="/images2/BetterRepresentation.png" width="600">
  </kbd>
</p>

Bu yeni koordinat sisteminde, noktalarımızın koordinatlarının verilerimizin yeni bir temsili olduğu söylenebilir. Bu gösterimle, siyah / beyaz sınıflandırma sorunu basit bir kural olarak ifade edilebilir: "Siyah noktalar öyle ki: x > 0" veya "Beyaz noktalar: x <0" olacak şekildedir. Bu yeni temsil, temelde sınıflandırma problemini çözer.
Bu durumda koordinat değişikliğini elle tanımladık. Ancak bunun yerine, sistematik olarak farklı olası koordinat değişikliklerini aramayı deneseydik ve doğru şekilde sınıflandırılan noktaların yüzdesini geri bildirim olarak kullanırsak, o zaman makine öğrenimi yapıyor olurduk. Makine öğrenimi bağlamında öğrenme, daha iyi temsiller için otomatik bir arama sürecini tanımlar.

Tüm makine öğrenimi algoritmaları, verileri belirli bir görev için daha yararlı temsillere dönüştüren bu tür dönüşümleri otomatik olarak bulmaktan oluşur. Makine öğrenimi algoritmaları bu dönüşümleri bulmada genellikle yaratıcı değildir; onlar yalnızca hipotez alanı adı verilen önceden tanımlanmış bir dizi işlemde arama yapıyorlar.
Teknik olarak makine öğrenimi budur: önceden tanımlanmış bir olasılık alanı içinde bazı girdi verilerinin faydalı temsillerini bir geri bildirim sinyalinden rehberlik kullanarak aramak. Bu basit fikir, oldukça geniş bir yelpazeyi çözmeye olanak tanır.

Derin öğrenme, makine öğreniminin belirli bir alt alanıdır: giderek anlamlı hale gelen temsillerin birbirini izleyen katmanlarından oluşur. Derin öğrenmedeki derinlik, yaklaşımla elde edilen daha derin herhangi bir anlayışa referans değildir; daha ziyade, bu ardışık temsil katmanları fikrini temsil eder. Bir veri modeline kaç katman katkıda bulunursa, bu modelin derinliği olarak adlandırılır. Modern derin öğrenme genellikle onlarca hatta yüzlerce ardışık temsil katmanını içerir ve bunların tümü, otomatik olarak öğrenir. 

<p>
  <kbd>
    <img src="/images2/DL_Layers.png" width="600">
  </kbd>
</p>

Derin öğrenmede, bu katmanlı temsiller birbirinin üzerine yığılmış gerçek katmanlarda yapılandırılmış sinir ağları adı verilen modelleri oluşturur. Sinir ağı terimi, nörobiyolojiye bir göndermedir, ancak derin öğrenmedeki bazı temel kavramlar kısmen beyin anlayışımızdan ilham alınarak geliştirilmiş olsa da, derin öğrenme modelleri beynin modelleri değildir. Beynin, modern derin öğrenme modellerinde kullanılan öğrenme mekanizmalarına benzer herhangi bir şeyi uyguladığına dair hiçbir kanıt yoktur. Derin öğrenmenin beyin gibi çalıştığını veya beyinden sonra modellendiğini iddia eden popüler bilim makalelerine rastlayabilirsiniz, ancak durum bu değil. Alana yeni başlayanlar için derin öğrenmenin herhangi bir şekilde nörobiyoloji ile ilgili olduğunu düşünmek kafa karıştırıcı ve ters etki yaratabilir; "tıpkı zihnimiz gibi" mistik ve gizem örtüsüne ihtiyacımız yok ve derin öğrenme ile biyoloji arasındaki varsayımsal bağlantılar hakkında okuduğumuz her şeyi sorgulamalıyız. Amaçlarımız doğrultusunda, derin öğrenme, verilerden temsilleri öğrenmek için matematiksel bir çerçevedir.

Karmaşık konuları görselleştirek açıklamak konusunda belki de en başarılı Youtube kanalı **3Blue1Brown**, sinir ağları ve derin öğrenme konusunda da harika bir iş çıkarmış: 

<iframe width="640" height="360" src="https://www.youtube.com/embed/aircAruvnKk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Kaynakça:
1. ["Deep Learning with Python", François Chollet](https://www.manning.com/books/deep-learning-with-python)

<div align="center">
  <img src="https://img.shields.io/github/languages/count/keyvanarasteh/Project?style=flat-square&color=blueviolet" alt="Language Count">
  <img src="https://img.shields.io/github/languages/top/keyvanarasteh/Project?style=flat-square&color=1e90ff" alt="Top Language">
  <img src="https://img.shields.io/github/last-commit/keyvanarasteh/Project?style=flat-square&color=ff69b4" alt="Last Commit">
  <img src="https://img.shields.io/github/license/keyvanarasteh/Project?style=flat-square&color=yellow" alt="License">
  <img src="https://img.shields.io/badge/Status-Active-green?style=flat-square" alt="Status">
  <img src="https://img.shields.io/badge/Contributions-Welcome-brightgreen?style=flat-square" alt="Contributions">
</div>

# *DRFM   📡*


 DRFM (Sayısal Radyo Frekans Belleği), hedef radar sinyallerini anlık olarak sayısallaştıran, dijital hafızasında işleyen ve üzerinde yaptığı manipülasyonlarla yeniden yayınlayarak karıştırma ve aldatma (jamming and deception) işlevi gören temel bir elektronik harp (EH) teknolojisidir.

---

## *Elektronik Harp  Nedir ?*

Elektronik harp (EH), elektromanyetik spektrumun askerî amaçlarla etkin biçimde kullanılması, kontrol altına alınması ve düşman tarafından kullanılmasının engellenmesi amacıyla geliştirilen savunma disiplinidir. EH, modern muharebe ortamlarında fiziksel kuvvet kullanılmadan hedef sistemlerin işlevselliğini bozmak, aldatmak veya bu sistemlerden istihbarat elde etmek için kritik rol oynamaktadır.
Genellikle üç temel unsurdan oluşur:

- **Elektronik Destek (ED):** Düşman veya tarafsız kaynaklardan yayılan elektromanyetik sinyallerin tespiti, tanımlanması, yerinin belirlenmesi ve analizini kapsar. Bu aşama, tehdidin karakterizasyonu için gereklidir.
  
- **Elektronik Taarruz (ET):** Düşman elektronik sistemlerini baskı altına almak, bozmak veya aldatmak amacıyla uygulanan aktif müdahaleleri içerir. Karıştırma (jamming) ve aldatma (deception) teknikleri bu kapsamda değerlendirilir.

- **Elektronik Koruma (EK):** Kendi elektromanyetik sistemlerinin düşman müdahalelerine karşı güvenliğini ve sürekliliğini sağlamak amacıyla alınan önlemleri içerir.


---

## *DRFM Çalışma Prensibi*
 


DRFM sistemlerinin işleyişi, aşağıda ana hatları belirtilen sıralı ve yüksek hızlı adımlardan oluşan bir süreci takip eder.



### 1. Sinyal Alımı (Signal Acquisition)
Sistem, hedef radar tarafından yayınlanan `RF` (Radyo Frekans) sinyalini yüksek hassasiyetli bir alıcı ile tespit eder.


### 2. Dijitalleştirme (Digitization)
Alınan analog `RF` sinyali, yüksek hızlı bir **Analog-Dijital Çevirici** (`ADC`) kullanılarak anlık olarak dijital veri akışına dönüştürülür.



### 3. Depolama ve Manipülasyon (Storage & Manipulation)
Oluşturulan dijital veri, sistemin belleğine kaydedilir. Bu aşama, `DRFM`'in temel aldatma kabiliyetlerinin uygulandığı kritik adımdır. Kaydedilen sinyal üzerinde, aşağıdaki teknikler başta olmak üzere çeşitli manipülasyonlar gerçekleştirilir:



* **Geciktirme - *Range Deception*:** Sinyalin geri yayınlanması kasıtlı olarak geciktirilir. Bu, radar ekranında hedefin gerçekte olduğundan daha uzakta görünmesine (menzil kaydırma) neden olur.



* **Doppler Kaydırması - *Velocity Deception*:** Sinyalin frekansı değiştirilerek yayınlanır. Bu, hedefin hızının (örneğin yaklaşan bir hedefin yavaşlıyor veya uzaklaşıyor gibi gösterilmesi) yanlış algılanmasını sağlar.


* **Çoklu Sahte Hedef Üretimi - *Multiple False Target Generation*:** Tek bir sinyal kopyalanarak ve aralarında küçük farklar oluşturularak birden çok kez yayınlanır. Bu, radar ekranında tek bir gerçek hedef yerine çok sayıda sahte hedef (hayalet hedef) yanılsaması oluşturur.



* **Gürültü Modülasyonu ve Karıştırma - *Noise Modulation & Jamming*:** Orijinal sinyalin üzerine gürültü bindirilir veya sinyalin yapısı bozularak radarın hedefi net bir şekilde tespit etmesi veya hedefe kilitlenmesi engellenir.



### 4. Geri Yayınlama (Re-transmission)
Manipüle edilen dijital sinyal, bir **Dijital-Analog Çevirici** (`DAC`) aracılığıyla tekrar analog `RF` formatına dönüştürülür ve yüksek güçlü bir verici ile hedef radara doğru yönlendirilir.

---

### Sonuç
Bu işlemler o kadar yüksek hızda ve sinyal sadakatiyle gerçekleştirilir ki, hedef radar sisteminin geri dönen sinyalin gerçek bir yansıma mı yoksa `DRFM` tarafından üretilmiş bir aldatmaca mı olduğunu ayırt etmesi genellikle mümkün olmaz.



---


### *🧪 Test Betikleri*


⏱️ Zamanlama Testi

python src/drfm_timing_test.py

Bu betik, radar darbesi üretiminin ve DRFM yankı işleminin ne kadar sürdüğünü raporlar.



🧠 Bellek Kullanımı Testi

python src/drfm_memory_test.py

Bu betik, sinyal üretimi ve yankı süreci sırasında kullanılan RAM miktarını ölçer.



📦 Çıktı Boyutu Testi

python src/drfm_output_size_test.py


Bu betik, oluşturulan sinyallerin bayt cinsinden bellek boyutlarını karşılaştırır.

---






## ⚙️ Kullanılan Temel Teknolojiler

DRFM sistemleri aşağıdaki temel teknolojiler üzerine kuruludur:

| 🧩 **Teknoloji**             | 📘 **Açıklama**                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| **RF Alıcı & Verici**        | Geniş bant radar sinyallerini alır, işledikten sonra manipüle edilmiş olarak tekrar yayınlar. |
| **ADC / DAC**                | Analog sinyalleri dijital forma dönüştürür (ADC), ardından işlenmiş sinyali tekrar analog hale getirir (DAC). |
| **Bellek (RAM, FIFO)**       | Alınan radar sinyalleri geçici olarak yüksek hızlı belleklerde saklanır.      |
| **DSP / FPGA**               | Dijital sinyal işleme birimleri; zaman geciktirme, frekans kaydırma, faz manipülasyonu gibi işlemleri gerçek zamanlı olarak yapar. |
| **Gömülü Yazılım**           | Sistem üzerinde çalışan yazılımlar, tehdit algılama ve sinyal üretme süreçlerini yönetir. |
| **Karşı Tedbir Yazılımları** | Düşman radarlarını yanıltmaya yönelik senaryolar üretir (örneğin: sahte hedef oluşturma, Doppler aldatma). |





## 🚀 Kullanım Senaryoları

**DRFM (Digital Radio Frequency Memory)** sistemleri, elektronik harp sahasında çeşitli taktik avantajlar sağlamak amacıyla aşağıdaki alanlarda kullanılır:

### 🎯 Sahte Hedef Oluşturma (False Target Generation)
Gerçek hedefin konumuna benzer birden fazla sahte hedef sinyali gönderilerek düşman radarının yanıltılması sağlanır.

### 🎯 Radar Karıştırma ve Yanıltma
Düşman radarına gönderilen bozulmuş veya değiştirilmiş sinyallerle hedefin algılanması engellenir.

### 🎯 Doppler Aldatması (Velocity Gate Pull-Off)
Sinyalin Doppler kayması değiştirilerek hedefin hızının yanlış algılanması sağlanır.

### 🎯 Menzil Aldatması (Range Gate Pull-Off)
Sinyalin zamanlama parametreleriyle oynanarak hedefin farklı bir uzaklıkta algılanması sağlanır.

### 🎯 Anti-Radyasyon Füzelerinden Kaçınma
Radar sinyallerini taklit ederek yönlendirilen füzelerin hedefi şaşırması sağlanır.

---


## *Katkıda Bulunma*

We welcome contributions! To help:  
1. Fork the repository.  
2. Clone your fork (`git clone git@github.com:YOUR_USERNAME/YOUR_REPO.git`).  
3. Create a branch (`git checkout -b feature/your-feature`).  
4. Commit changes with clear messages.  
5. Push to your fork (`git push origin feature/your-feature`).  
6. Open a Pull Request.  

Follow our coding standards (see [CONTRIBUTING.md](CONTRIBUTING.md)).  

*Topluluk katkilerini memnuniyetle karşılıyoruz! Katkıda bulunmak için yukarıdaki adımları izleyin ve kodlama standartlarımıza uyun.*

---

## *Lisans*

Licensed under the [MIT License](LICENSE.md).  
*MIT Lisansı altında lisanslanmıştır.*


---

## *İletişim* 


*Proje Sorumlusu: Sude Nur Komut - [2320191034@stu.istinye.edu.tr]. Hata bulursanız bir sorun bildirin.*

---



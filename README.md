# trex_research

## 1. Modern Yazılım Geliştirme Pratikleri

<details>

<summary>Git nedir? GitHub nedir?</summary>

### Git nedir?

* Git, versiyon kontrol sistemidir.

* Yazılım projelerinde yapılan değişiklikleri kaydetmek, takip etmek ve gerektiğinde eski sürümlere dönebilmek için kullanılır.

* Tek kişi de kullanabilir ama özellikle ekip çalışmalarında çok faydalıdır.

* Bir nevi “projenin zaman makinesi” gibidir. Kodun hangi aşamalardan geçtiğini, kim ne değiştirdiğini görebilirsin.

#### Örneğin:
Bir dosyada değişiklik yaptığında Git bu değişiklikleri kaydeder. Daha sonra bu değişiklikleri “commit” adı verilen paketler halinde saklarsın. İstediğinde eski commitlere geri dönebilirsin.

### GitHub nedir?

* GitHub, Git ile yönetilen projeleri internette barındırmaya yarayan bir platformdur.

* Git’i kendi bilgisayarında kullanabilirsin, ama projeni başkalarıyla paylaşmak ya da ortak geliştirmek istediğinde GitHub devreye girer.

* GitHub sayesinde kodunu uzaktan yedekleyebilir, ekip arkadaşlarınla paylaşabilir, açık kaynak projelere katkı yapabilirsin.

* Ayrıca GitHub, Git’e ek olarak hata takip sistemi, proje yönetim araçları, wiki gibi ek özellikler sunar.

#### Özet:

* Git: Kodunun versiyonlarını yönetmeni sağlayan araç.

* GitHub: Git ile oluşturduğun projeleri paylaşabileceğin, işbirliği yapabileceğin çevrim içi platform. 

</details>


<details>

<summary>Temel Git komutları: init, clone, add, commit, push, pull, branch, merge</summary>


### Git İnit Nedir:

* Git komutlarından biridir klasörleri Git deposuna dönüştürmek için kullanılır

#### Örneğin:
Bir uygulama klasörü oluşturdun.Bu klasör şuan normal bir klasör.Bu klasörü Git ile takip etmek için GİT İNİT komutu çalıştırdın.Bu klasör artık GİT Deposu haline geldi


### Git Clone Nedir:

* Git Clone bir projeye sıfırdan başlamak yerine var olan bir projeyi geçmişiyle birlikte elinde olmasını sağlar.

#### Örneğin:
Arkadaşının GitHub´daki projesi ´´LogIn Ekranı Sistemi´´ olsun. Sen Git Clone kullandığında bu proje tamamen senin bilgisayarına kopyalanır. Dosyalar,projenin geçmişi de sana gelir. Bu proje artık senin bilgisayarında da bir GİT deposudur. Sende değişiklik yapıp GitHub´a geri gönderebilirsin.


### Git Add Nedir:

* Git’te bir değişikliği “staging area”ya eklemek için kullanılan komuttur. Git, dosyalardaki değişiklikleri doğrudan kaydetmez. Önce hangi değişiklikleri commit yapacağını belirtmek gerekir.

#### Örneğin:
Projene ´´notlar.txt´´ adında bir proje ekledin bu dosya üzerine birkaç satır yazı yazdın Git Add komutunu kullanarak Git’e “Bu dosyayı takip et ve sonraki commit’e ekle” demiş oluyorsun.


### Git Commit Nedir:

* Git Commit, proje gelişimini adım adım kaydeden,geçmişi kaydeden bir komuttur.

#### Örneğin:
Bir proje dosyası içinde ´´anasayfa.html´´ dosyasını oluşturdun ve içine bazı bilgilerde ekledin önce Git Add komutu ile bu projeyi takip listesine ekledin, ardından Git Commit komuuutunu kullandığında, bu değişiklik artık Git deposuna kalıcı olarak kaydedilmiş olur 

  
### Git Push Nedir:

* Git push, kendi bilgisayarında yaptığın Commitleri başkalarının da görebileceği merkezi bir depoya aktarma işlemidir. Genellikle bu merkezi depo GitHub, GitLab veya Bitbucket gibi platformlarda bulunur.

#### Örneğin:
Bilgisayarda Main, Develop, Admin-Panel gibi dallar var hepsini Git İnit deposuna göndermeni ve herkesin görmesini sağlıyor


### Git Pull Nedir:

*Başka bir depodaki Git Hub çalışmalarını kendi çalışma alanına çeken bir komuttur.

#### Örneğin:
Aynı projeyi yapan iki kullanıcı den biri projede bir değişiklik yaptı ve başka bir depoya gönderdi diğer kullanıcının şuan bu projesi güncel değil Git Pull yapıp diğer depodaki güncel kodları kendi kodlarıyla birleştirerek Git Pull yapmış oldu.


### Git Branch Nedir:

* Bir projenin ana hattından ayrılarak bağımsız bir geliştirme alanı açmanı sağlar.Böylece yeni özellikler ekleyebilir, hata düzeltebilir veya denemeler yapabilirsin.

#### Örneğin:
İki kullanıcıdan biri Admin-Panel de diğeri Kullanıcı-Profili dalında çalışıyor ikiside çalışmayı bitirince Main dalında birleştirerek Git Branch yaptılar.


### Git Merge Nedir:
Bir branch de yapılan değişikleri alıp başka branch´le birleştiren komuttur.

#### Örneğin:
Bir kullanıcı e-ticaret projesinde çalışıyor kullanıcı Arama-Fonksiyonu dalında bir arama özelliği geliştirdi önce kendi dalında tüm testleri yaptı, her şeyin düzgün çalıştığını emin oldu artık bu özelliğin tüm projeye eklenmesi gerekiyor Git Merge ile Arama-Fonksiyonu dalını main ile birleştirdi.: Artık ana dalda kullanıcılar ürün araması yapabilir, kullanıcının geliştirdiğin değişiklikler tüm ekip için kullanılabilir hale gelir.

</details>

<details>

<summary>Merge conflict nedir, nasıl çözülür?</summary>


Merge conflict, Git üzerinde çalışırken iki farklı dalda yapılan değişikliklerin aynı dosya veya aynı satır üzerinde çakışması durumunda ortaya çıkan bir durumdur. Git, hangi değişikliğin geçerli olduğunu otomatik olarak belirleyemediği için kullanıcı müdahalesi gerekir.
Bu çatışmayı çözmek için öncelikle Git’in işaretlediği çatışan dosyalar belirlenir ve açılarak hangi değişikliğin korunacağına karar verilir. Kullanıcı, gerekli düzenlemeleri yapar ve dosyaları kaydeder. Böylece çatışma giderilmiş olur ve dallar sorunsuz bir şekilde birleştirilebilir.
Özetle, merge conflict bir “karar gerektiren çakışma”dır ve çözümü, hangi değişikliğin geçerli olacağına manuel olarak karar verip düzenleme yapmaktır.

</details>

<details>

<summary>CI/CD nedir? Azure DevOps, GitHub Actions ile pipeline örnekleri</summary>


### CI/CD NEDİR:


CI/CD, yazılımın geliştirilmesinden test edilmesine, dağıtılmasına ve izlenmesine kadar tüm süreci otomatikleştirerek hızlı, güvenli ve sürekli güncel bir geliştirme ortamı sağlar. Unit test, otomatik build, deployment ve monitoring gibi kavramlarla birlikte modern yazılım geliştirme süreçlerinin temelini oluşturur.

CI (Continuous Integration – Sürekli Entegrasyon): Geliştiriciler kodlarını sık sık ortak bir depoya gönderir. Her değişiklik otomatik olarak derlenir ve test edilir. Böylece hatalar erken fark edilir, kod tabanı tutarlı kalır ve ekip içinde entegrasyon sorunları minimize edilir.

CD (Continuous Delivery / Continuous Deployment – Sürekli Teslim / Dağıtım): Kodun testlerden geçtikten sonra üretim veya test ortamına otomatik olarak taşınmasıdır. Continuous Delivery’de canlıya geçiş genellikle manuel onay gerektirirken, Continuous Deployment tamamen otomatik olarak kodu canlıya çıkarır.


### Azure DevOps Pipeline Örneği

#### Trigger (Tetikleme):

* Geliştirici main veya develop dalına kod gönderir.

* Azure DevOps pipeline otomatik olarak tetiklenir.

#### Build (Derleme):

* Web uygulaması derlenir, gerekli paketler yüklenir.

* Backend servisleri derlenir ve bağımlılıklar kontrol edilir.

* Derleme sırasında oluşan hatalar hemen ekibe bildirilir.

#### Test (Otomatik Testler):

* Unit testler çalıştırılır: Her bir fonksiyon ve modülün beklenen şekilde çalıştığı kontrol edilir.

* Integration testler çalıştırılır: Web uygulaması ile backend servisleri arasında veri akışı ve API çağrıları test edilir.

* Testlerde bir hata bulunursa pipeline durur ve hata detayları ekibe bildirilir.

#### Deploy (Dağıtım):

* Testler başarılı ise uygulama staging ortamına deploy edilir.

* Staging ortamında manuel test veya kullanıcı kabul testleri yapılabilir.

* Gerektiğinde pipeline, production ortamına deploy için onay adımı ekler.

#### Feedback ve Monitoring:

* Pipeline tamamlandığında ekibe bildirim gönderilir (e-posta veya Slack).

* Uygulamanın logları ve performans verileri izlenir.

* Olası hatalar veya performans sorunları bir sonraki geliştirme döngüsüne aktarılır.

Bu sayede ekibin kodu her zaman güncel, hatasız ve güvenli bir ortamda çalışır durumda olur.


GitHub Actions Pipeline Örneği

 Pipeline Açıklaması

- **Trigger:** Pipeline, `main` branch’ine yapılan her push veya pull request’te çalışır.  
- **Ortam:** GitHub, pipeline’ı `ubuntu-latest` üzerinde çalıştırır.  
- **Adımlar:**  
  1 . Kod repository’den çekilir.  
  2. Node.js ortamı kurulur.  
  3. Bağımlılıklar yüklenir.  
  4. Testler çalıştırılır.  
  5. Build işlemi yapılır.
  
# GitHub Actions Pipeline Örneği

Bu doküman, basit bir Node.js projesi için GitHub Actions pipeline (workflow) örneğini anlatır.  


```yaml
jobs:
  build-and-test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test
```

 Ortak Özellikleri:
* Her iki pipeline da kodun otomatik olarak test edilmesini ve dağıtılmasını sağlar.

* Hatalar erken tespit edilir, düzeltmek kolaylaşır.

* Kod her zaman güncel, ekip hızlı ve güvenli bir şekilde çalışabilir.

* Build, test ve deploy adımları ardışık veya paralel olarak çalıştırılabilir.

* CI/CD süreçleri sayesinde manuel müdahale minimuma iner, hata olasılığı düşer.

</details>

<details>

<summary>Ek Bilgiler</summary>

Software Development Life Cycle (SDLC)

##### 1. Planlama (Planning):

* Proje amaçlarının belirlenmesi

##### 2. Analiz (Requirement Analysis):

* Kullanıcı ihtiyaçlarının toplanması

##### 3. Tasarım (Design):

* Sistem mimarisi oluşturulur

##### 4. Geliştirme (Implementation / Development):

* Kodlama süreci başlar

##### 5. Test (Testing):

* Yazılım hatalarının bulunması ve düzeltilmesi

##### 6. Dağıtım (Deployment):

* Yazılım canlı ortama aktarılır

##### 7. Bakım (Maintenance):

* Yazılımın güncellenmesi

### SDLC Avantajları

* Geliştirme sürecine düzen getirir.

* Kaynak ve zaman yönetimini kolaylaştırır.

* Hataları erken aşamada yakalamayı sağlar.

* Yazılımın kalitesini artırır.

* Kullanıcı ihtiyaçlarına uygun yazılım geliştirilmesine yardımcı olur.































































</details>
















































































































































































































































































































































































































































































































# trex_research

  *Yazılım Temel Kavramları*


## 1. Modern Yazılım Geliştirme Pratikleri

<details>

<summary>Git nedir? GitHub nedir?</summary>

> Git nedir?

* Git, versiyon kontrol sistemidir.

* Yazılım projelerinde yapılan değişiklikleri kaydetmek, takip etmek ve gerektiğinde eski sürümlere dönebilmek için kullanılır.

* Tek kişi de kullanabilir ama özellikle ekip çalışmalarında çok faydalıdır.

* Bir nevi “projenin zaman makinesi” gibidir. Kodun hangi aşamalardan geçtiğini, kim ne değiştirdiğini görebilirsin.

#### Örneğin:
Bir dosyada değişiklik yaptığında Git bu değişiklikleri kaydeder. Daha sonra bu değişiklikleri “commit” adı verilen paketler halinde saklarsın. İstediğinde eski commitlere geri dönebilirsin.

> GitHub nedir?

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


> Git İnit Nedir:

* Git komutlarından biridir klasörleri Git deposuna dönüştürmek için kullanılır

#### Örneğin:
Bir uygulama klasörü oluşturdun.Bu klasör şuan normal bir klasör.Bu klasörü Git ile takip etmek için GİT İNİT komutu çalıştırdın.Bu klasör artık GİT Deposu haline geldi


> Git Clone Nedir:

* Git Clone bir projeye sıfırdan başlamak yerine var olan bir projeyi geçmişiyle birlikte elinde olmasını sağlar.

#### Örneğin:
Arkadaşının GitHub´daki projesi ´´LogIn Ekranı Sistemi´´ olsun. Sen Git Clone kullandığında bu proje tamamen senin bilgisayarına kopyalanır. Dosyalar,projenin geçmişi de sana gelir. Bu proje artık senin bilgisayarında da bir GİT deposudur. Sende değişiklik yapıp GitHub´a geri gönderebilirsin.


> Git Add Nedir:

* Git’te bir değişikliği “staging area”ya eklemek için kullanılan komuttur. Git, dosyalardaki değişiklikleri doğrudan kaydetmez. Önce hangi değişiklikleri commit yapacağını belirtmek gerekir.

#### Örneğin:
Projene ´´notlar.txt´´ adında bir proje ekledin bu dosya üzerine birkaç satır yazı yazdın Git Add komutunu kullanarak Git’e “Bu dosyayı takip et ve sonraki commit’e ekle” demiş oluyorsun.


> Git Commit Nedir:

* Git Commit, proje gelişimini adım adım kaydeden,geçmişi kaydeden bir komuttur.

#### Örneğin:
Bir proje dosyası içinde ´´anasayfa.html´´ dosyasını oluşturdun ve içine bazı bilgilerde ekledin önce Git Add komutu ile bu projeyi takip listesine ekledin, ardından Git Commit komuuutunu kullandığında, bu değişiklik artık Git deposuna kalıcı olarak kaydedilmiş olur 

  
> Git Push Nedir:

* Git push, kendi bilgisayarında yaptığın Commitleri başkalarının da görebileceği merkezi bir depoya aktarma işlemidir. Genellikle bu merkezi depo GitHub, GitLab veya Bitbucket gibi platformlarda bulunur.

#### Örneğin:
Bilgisayarda Main, Develop, Admin-Panel gibi dallar var hepsini Git İnit deposuna göndermeni ve herkesin görmesini sağlıyor


> Git Pull Nedir:

*Başka bir depodaki Git Hub çalışmalarını kendi çalışma alanına çeken bir komuttur.

#### Örneğin:
Aynı projeyi yapan iki kullanıcı den biri projede bir değişiklik yaptı ve başka bir depoya gönderdi diğer kullanıcının şuan bu projesi güncel değil Git Pull yapıp diğer depodaki güncel kodları kendi kodlarıyla birleştirerek Git Pull yapmış oldu.


> Git Branch Nedir:

* Bir projenin ana hattından ayrılarak bağımsız bir geliştirme alanı açmanı sağlar.Böylece yeni özellikler ekleyebilir, hata düzeltebilir veya denemeler yapabilirsin.

#### Örneğin:
İki kullanıcıdan biri Admin-Panel de diğeri Kullanıcı-Profili dalında çalışıyor ikiside çalışmayı bitirince Main dalında birleştirerek Git Branch yaptılar.


> Git Merge Nedir:
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


> CI/CD NEDİR:


CI/CD, yazılımın geliştirilmesinden test edilmesine, dağıtılmasına ve izlenmesine kadar tüm süreci otomatikleştirerek hızlı, güvenli ve sürekli güncel bir geliştirme ortamı sağlar. Unit test, otomatik build, deployment ve monitoring gibi kavramlarla birlikte modern yazılım geliştirme süreçlerinin temelini oluşturur.

CI (Continuous Integration – Sürekli Entegrasyon): Geliştiriciler kodlarını sık sık ortak bir depoya gönderir. Her değişiklik otomatik olarak derlenir ve test edilir. Böylece hatalar erken fark edilir, kod tabanı tutarlı kalır ve ekip içinde entegrasyon sorunları minimize edilir.

CD (Continuous Delivery / Continuous Deployment – Sürekli Teslim / Dağıtım): Kodun testlerden geçtikten sonra üretim veya test ortamına otomatik olarak taşınmasıdır. Continuous Delivery’de canlıya geçiş genellikle manuel onay gerektirirken, Continuous Deployment tamamen otomatik olarak kodu canlıya çıkarır.


> Azure DevOps Pipeline Örneği

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


> GitHub Actions Pipeline Örneği

 Pipeline Açıklaması

- **Trigger:** Pipeline, `main` branch’ine yapılan her push veya pull request’te çalışır.  
- **Ortam:** GitHub, pipeline’ı `ubuntu-latest` üzerinde çalıştırır.  
- **Adımlar:**  
  1 . Kod repository’den çekilir.  
  2. Node.js ortamı kurulur.  
  3. Bağımlılıklar yüklenir.  
  4. Testler çalıştırılır.  
  5. Build işlemi yapılır.
  
> GitHub Actions Pipeline Örneği

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

> Software Development Life Cycle (SDLC)

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

> SDLC Avantajları

* Geliştirme sürecine düzen getirir.

* Kaynak ve zaman yönetimini kolaylaştırır.

* Hataları erken aşamada yakalamayı sağlar.

* Yazılımın kalitesini artırır.

* Kullanıcı ihtiyaçlarına uygun yazılım geliştirilmesine yardımcı olur.


> Yazılım geliştirme sürecinin aşamaları (Planlama, analiz, geliştirme, test, dağıtım, bakım)

#### Yazılım geliştirme sürecinin aşamaları:

Planlama:
* Projenin kapsamı ve hedefleri belirlenir.
 ↓
 
Analiz:
* Kullanıcı ihtiyaçları ve gereksinimler toplanır.
 ↓

Geliştirme:
* Belirlenen tasarıma uygun şekilde kodlama yapılır.
 ↓

Test:
* Belirlenen tasarıma uygun şekilde kodlama yapılır.
 ↓

 Bakım:
* Yazılım canlı ortama aktarılır.
 ↓

 Dağıtım:  
* Hatalar düzeltilir ve iyileştirmeler yapılır.


> Agile/Scrum/Kanban metodolojileri

* Agile → Felsefe (çevik yaklaşım)

* Scrum → Agile’ın çerçevesi (Sprint’lerle yönetim)

* Kanban → Görselleştirme ve sürekli akış yöntem

</details>

## 2.Net Ekosistemi

<details>

<summary>.NET nedir? Tarihçesi, amacı, neden kullanılır?</summary>



> .Net Nedir:
.NET, program çalıştırmak için bir çalışma zamanı ortamıdır.

Normal derlenmiş programlama dillerinde, kod yazarsın ve derleyici kodunu CPU'nun çalıştırdığı makine koduna çevirir. Makine kodu, bellekte veri taşıma ve aritmetik işlemler yapma gibi bir dizi talimat listesidir.

Yani bir sürü özel donanım makinesi için kod derlemek yerine, sanal bir makineye (VM) kod derleyebilirsiniz. Sanal makine bir CPU gibi davranır, ama her yerde aynı olan bir CPU. VM, farklı donanımlar ve işletim sistemleri arasındaki farkları gizler, böylece derleyicinizin sadece tek bir program oluşturması gerekir.

Bu "bir kere derle, her yerde çalıştır" davranışına ek olarak, .NET gibi sanal makineler başka bir sürü özellik de sunar: otomatik bellek yönetimi, güvenlik, sınır kontrolü, vb. Yani tek bir derlemeyle daha fazla platformu desteklemekle kalmazsınız, aynı zamanda bazı problemler VM tarafından zaten "çözüldüğü" için geliştirme de daha kolay olabilir ve bu çözümleri elde etmek için özel bir şey yapmanız gerekmez.

Derleyicisi .NET IL'ye derlenen bir dilde yazılım yazarak .NET'i kullanabilirsiniz: C#, VB.NET, F# ve bir avuç küçük dil ve dil portu bunu yapar.

> .Net Tarihçesi:

.NET framework'ün ilk beta sürümleri 2000'lerin sonlarında yayınlandı ve 13 Şubat 2002'de ilk sürüm olan . NET 1.0 yayınlandı. Temel özelliği CLR'ydi ve web uygulamalarının nesne yönelimli geliştirilmesini destekliyordu.

> .Net Amacı:

.NET, birçok uygulama türü oluşturmaya yönelik ücretsiz, platformlar arası bir açık kaynak geliştirici platformu. Birden çok dilde yazılmış programları çalıştırabilir, en popüler olan C#. birçokyüksek ölçekli uygulama tarafından üretimde kullanılan yüksek performanslı çalışma zamanına dayanır.

> .Net Neden Kullanılır:

.NET yazılım geliştirmede daha kararlı, etkin ve performansı yüksek sistemlerin oluşturulmasında kullanılmaktadır.
</details>


<details>

<summary>.NET Framework, .NET Core ve .NET 7/8+ farkları</summary>


| **Kriter**              | **.NET Framework**                                                    | **.NET Core**                                                            | **.NET 5/6/7/8+ (Güncel .NET)**                                                               |
| ----------------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| **Çıkış Yılı**          | 2002 – Microsoft’un ilk geliştirme platformu                          | 2016 – Daha modern ve açık kaynak olarak çıktı                           | 2020’den itibaren, Framework ve Core birleşerek tek çatı altında toplandı                     |
| **Platform Desteği**    | Sadece **Windows** üzerinde çalışır                                   | **Cross-platform**: Windows, Linux, macOS                                | **Tam cross-platform**: Windows, Linux, macOS + Mobil (Android/iOS), Bulut, IoT               |
| **Kaynak Yapısı**       | Kapalı kaynak (bazı kısımlar sonradan açıldı)                         | Tamamen **açık kaynak**                                                  | **Açık kaynak** ve topluluk katkısına açık                                                    |
| **Performans**          | Orta seviyede, eski teknolojiye dayalı                                | Yüksek performanslı, özellikle web ve bulut uygulamalarında              | En yüksek performans – sürekli iyileştirmeler (ör. .NET 7/8 ile %30-40 performans artışı)     |
| **Destek Durumu**       | Yeni geliştirme yok, sadece güvenlik yamaları                         | 3.1 sürümü ile birlikte desteği sona erdi                                | Aktif olarak geliştiriliyor; LTS (uzun süreli) ve STS (kısa süreli) sürümlerle düzenli destek |
| **Kullanım Alanı**      | Eski kurumsal Windows uygulamaları (WinForms, WPF, ASP.NET Web Forms) | Web, bulut, konsol uygulamaları, sınırlı mobil desteği (Xamarin ayrıydı) | Web, mobil (.NET MAUI), masaüstü, oyun (Unity), IoT, bulut – çok yönlü ekosistem              |
| **Mobil Desteği**       | Yok                                                                   | Xamarin ile ayrı bir çözüm kullanılır                                    | Doğrudan **.NET MAUI** ile destek (tek kod tabanı → Android, iOS, Windows, macOS)             |
| **Gelecek Perspektifi** | Yavaş yavaş terk ediliyor; yeni projeler için önerilmiyor             | Geçiş teknolojisi olarak görevini tamamladı                              | Microsoft’un gelecekteki ana geliştirme platformu                                             |


* .NET Framework → Eski, Windows’a bağlı, artık sadece bakımda.

* .NET Core → Modernleşme adımı, açık kaynak, cross-platform, ama artık geliştirilmiyor.

* .NET 5/6/7/8+ → Geleceğin yolu, tek çatı, cross-platform, açık kaynak, mobil + bulut + IoT desteğiyle en güçlü sürüm.

</details>

<details>

<summary>Platformlar arası çalışabilir mi? (Windows, Linux, macOS)</summary>

* .NET Framework yalnızca Windows üzerinde çalışır.

* .NET Core ve .NET 5/6/7/8+ ise platformlar arası çalışabilir ve modern uygulama geliştirme için uygundur.
</details>

<details>

<summary>Dotnet --info çıktısı örneği ve yorumlama</summary>

> Dotnet --info Yorumlaması
#### SDK (Software Development Kit)

* Version: 8.0.100 → Kurulu SDK sürümü, yani bu sürümle projeler geliştirebilirsiniz.

* Commit → SDK’nın derleme kodu, genellikle hata ayıklama ve destek için önemlidir.

#### Runtime Environment (Çalışma Ortamı)

* OS Name ve OS Version → İşletim sistemi bilgisi.

* RID (Runtime Identifier) → Hedef platform bilgisi (win10-x64 → 64 bit Windows 10).

* Base Path → SDK’nın kurulu olduğu dizin.

#### Host

* .NET çalıştırıcısının sürümü, genellikle destek ve uyumluluk kontrolü için kullanılır.

#### .NET SDKs installed

* Bilgisayarda yüklü olan tüm SDK sürümlerini gösterir.

* Örnekte hem 6.0 hem de 8.0 SDK’sı yüklü.

#### .NET runtimes installed

* Çalıştırılabilir .NET sürümlerini listeler.

* Örnekte hem 6.0 hem 8.0 runtime var, yani bu sürümlerde geliştirilmiş uygulamalar çalıştırılabilir.

#### .NET workloads installed

* Ek yüklemeler veya özel çalışma setleri (örn. MAUI, Blazor) yüklüyse burada listelenir.

> Dotnet --info Örneği
```yaml
.NET SDK (reflecting any global.json):
 Version:   8.0.100
 Commit:    abcdef1234

Runtime Environment:
 OS Name:     Windows
 OS Version:  10.0.22621
 OS Platform: Windows
 RID:         win10-x64
 Base Path:   C:\Program Files\dotnet\sdk\8.0.100\

Host (useful for support):
  Version: 8.0.0
  Commit:  12345abcde

.NET SDKs installed:
  6.0.414 [C:\Program Files\dotnet\sdk]
  8.0.100 [C:\Program Files\dotnet\sdk]

.NET runtimes installed:
  Microsoft.NETCore.App 6.0.21 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.NETCore.App 8.0.0 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]

.NET workloads installed:
  maui
```
</details>

<details>

<summary>Senkron/Asenkron Örnek Senaryo Açıklamaları</summary>

>Senkron Nasıl Programlanır
* Senkron programlama, işlemlerin ardışık ve sırayla gerçekleştiği bir yöntemdir. Yani bir işlem tamamlanmadan bir sonraki işleme geçilemez. Bu yaklaşım, kodun okunmasını ve anlaşılmasını kolaylaştırır. Ancak uzun süren işlemler, programın diğer bölümlerinin çalışmasını engeller ve kullanıcı beklemek zorunda kalır.
> Senkron Nedir
* Senkron, yazılım ve bilgisayar bilimlerinde, işlemlerin ardışık ve sırayla gerçekleştiği bir çalışma şeklidir. Yani bir işlem tamamlanmadan bir sonraki işleme geçilmez. Her adım bir öncekinin bitmesini bekler. Bu yaklaşım, özellikle basit ve küçük ölçekli işlemlerde anlaşılması ve uygulanması kolaydır.

> Senkron Örneği

```yaml
// Senkron örnek
string rapor = RaporOlustur();  // Bu işlem tamamlanana kadar beklenir
Console.WriteLine(rapor);       // Rapor hazır olduğunda ekrana yazdırılır
```
> Asenkron Nasıl Programlanır
Asenkron programlama ise işlemlerin arka planda yürütülebildiği ve programın diğer işlemleri beklemeden devam edebildiği bir yöntemdir. Bu sayede uzun süren işlemler ana akışı bloke etmez ve kullanıcı başka işler yapabilir. Modern web, mobil ve bulut uygulamalarında performans ve kullanıcı deneyimi açısından çok önemlidir.
> Asenkron Nedir
* Asenkron işlem, bir işlemin tamamlanmasını beklemeden başka işlemlere devam edilebildiği çalışma şeklidir. Yani bir işlem arka planda yürürken program veya kullanıcı başka işlerle meşgul olabilir. Modern yazılım geliştirmede, özellikle web, mobil ve bulut uygulamalarında performans ve kullanıcı deneyimi açısından sık kullanılır.

> Asenkron Örneği
```yaml
// Asenkron örnek
async Task<string> RaporOlusturAsync()
{
    await Task.Delay(5000); // 5 saniye süren rapor oluşturma simülasyonu
    return "Rapor hazır!";
}

async Task MainAsync()
{
    Task<string> raporTask = RaporOlusturAsync();
    Console.WriteLine("Kullanıcı başka işlemler yapabilir...");
    string rapor = await raporTask;
    Console.WriteLine(rapor); // Rapor tamamlandığında yazdırılır
}

```
Senkron/Asenkron Örnek Senaryo Tablosu
| **Kriter**             | **Senkron Programlama**                                   | **Asenkron Programlama**                                                  |
| ---------------------- | --------------------------------------------------------- | ------------------------------------------------------------------------- |
| **İşlem Sırası**       | İşlemler ardışık yürütülür, her adım bir öncekini bekler. | İşlemler arka planda yürüyebilir, bekleme zorunlu değildir.               |
| **Bekleme Durumu**     | Uzun süren işlemler programı bloke eder.                  | Uzun süren işlemler arka planda devam eder, program çalışmaya devam eder. |
| **Kod Yapısı**         | Daha basit ve anlaşılırdır.                               | Daha karmaşıktır; async/await, Task vb. yapılar gerekir.                  |
| **Performans**         | Uzun işlemlerde düşük performans gösterebilir.            | Kaynaklar daha verimli kullanılır, performans yüksektir.                  |
| **Kullanıcı Deneyimi** | Kullanıcı beklemek zorundadır.                            | Kullanıcı beklemeden uygulamayı kullanmaya devam edebilir.                |
| **Kullanım Alanı**     | Küçük ve basit uygulamalar için uygundur.                 | Modern web, mobil ve bulut tabanlı uygulamalar için idealdir.             |


</details>

<details>

<summary>Ek Bilgiler</summary>

> arrow function (=>) ifadesinin C#’taki yeri

C# dilinde => ifadesi, yani lambda operatörü, hem lambda ifadeleri hem de expression-bodied üyeler için kullanılan modern bir sözdizimidir. Lambda ifadelerinde parametrelerle gövdeyi ayırır ve anonim fonksiyonların kısa bir şekilde yazılmasını sağlar; bu yapı özellikle LINQ sorgularında ve koleksiyon işlemlerinde yaygın olarak tercih edilir. Expression-bodied üyelerde ise metotlar veya property’ler tek satırda tanımlanabilir, böylece kod daha okunabilir ve sade hale gelir. Bu özellikler sayesinde =>, C#’ta fonksiyonel programlama yaklaşımını destekleyen ve geliştiricilere daha temiz bir yazım tarzı sunan önemli bir araçtır.
### Async, Await, Task, ConfigureAwait gibi anahtar kavramlar

* async → Bir metodu asenkron hale getirir, içinde await kullanılabilir.

* await → Asenkron işlemi bekler, akışı bloke etmeden devam eder.

* Task → Asenkron işlemleri temsil eder (Task değer döndürmez, Task<T> döndürür).

* ConfigureAwait → İşlem sonrası hangi bağlamda (UI thread, başka thread) devam edileceğini belirler.
</details>

## 3. Backend Geliştirme Temelleri
<details>
<summary>Backend nedir? Frontend ile farkları Nelerdir?</summary>
  
> Backend Nedir
Backend, bir yazılım veya uygulamanın arka planda çalışan kısmıdır. Kullanıcıların doğrudan görmediği, ancak uygulamanın çalışması için gerekli olan iş mantığı, veri işleme ve veri tabanı iletişimi gibi süreçleri yönetir.

* Kullanıcıdan gelen talepleri alır, işler ve gerekli sonuçları döndürür.

* Veritabanı, sunucu, API ve iş kuralları genellikle backend tarafında bulunur.

* Java, C#, Python, PHP, Node.js gibi teknolojilerle geliştirilir.

* Güvenlik, performans, verilerin doğru işlenmesi ve saklanması backend’in sorumluluğundadır.
> Fronted İle Farkları

Frontend, kullanıcıya görünen ve etkileşim sağlanan kısmı; backend ise arka planda veriyi işleyen ve uygulamanın mantığını yöneten kısmıdır.

* Frontend, uygulamanın “görünür yüzüdür” ve kullanıcı ile etkileşim sağlar.

* Backend, uygulamanın “motorudur”, veriyi işler ve iş kurallarını uygular.
 
 </details>
 
<details>

<summary>Web sunucusu nedir? API nedir? API türleri</summary>   

 

> Web sunucusu nedir?

#### Web sunucusu, internet üzerinden gelen istekleri (request) alan ve yanıt (response) döndüren bir yazılım veya sistemdir.

* Kullanıcı tarayıcısı bir web sitesine erişmek istediğinde, bu istek web sunucusuna gider.

* Web sunucusu, ilgili dosyaları veya verileri işleyip tarayıcıya gönderir.

* HTML, CSS, JavaScript dosyaları veya API yanıtları sunucudan gönderilebilir.

* Popüler web sunucuları: Apache, Nginx, Microsoft IIS.


> API Nedir?
#### API (Application Programming Interface), farklı yazılım uygulamalarının birbirleriyle iletişim kurmasını sağlayan arayüzdür.

* API, bir uygulamanın sunduğu işlevleri veya verileri diğer uygulamaların kullanabilmesini sağlar.

* Web API’leri genellikle HTTP protokolü üzerinden çalışır ve JSON veya XML formatında veri alışverişi yapar.

* Örnek: Bir hava durumu uygulaması, bir hava durumu servisinin API’si üzerinden güncel verileri alır.

* API, kullanıcıya doğrudan görünmez, ancak uygulamaların arka planda sorunsuz çalışmasını sağlar.


> API Türleri Nelerdir?
#### API (Application Programming Interface), farklı yazılım uygulamalarının birbirleriyle iletişim kurmasını sağlayan arayüzdür.

* API, bir uygulamanın sunduğu işlevleri veya verileri diğer uygulamaların kullanabilmesini sağlar.

* Web API’leri genellikle HTTP protokolü üzerinden çalışır ve JSON veya XML formatında veri alışverişi yapar.

* Örnek: Bir hava durumu uygulaması, bir hava durumu servisinin API’si üzerinden güncel verileri alır.

* API, kullanıcıya doğrudan görünmez, ancak uygulamaların arka planda sorunsuz çalışmasını sağlar.

</details>


<details>

<summary>HTTP nedir? HTTP metodları: GET, POST, PUT, DELETE</summary>

> HTTP Nedir?

#### HTTP (HyperText Transfer Protocol), web üzerinde veri alışverişi için kullanılan bir iletişim protokolüdür.

* Tarayıcı ile web sunucusu arasında istek (request) ve yanıt (response) mekanizmasını sağlar.

* Web sayfaları, API verileri veya dosya transferleri HTTP üzerinden gerçekleşir.

* Örnek: Tarayıcıda bir web sitesine girdiğinizde, tarayıcı HTTP isteği gönderir; sunucu ise sayfanın HTML, CSS ve JavaScript dosyalarını HTTP yanıtı olarak döner.

* Güvenli versiyonu HTTPS (HTTP Secure) olarak adlandırılır ve verileri şifreleyerek iletir.

> HTTP Metodları

#### Get:
* Sunucudan veri istemek için kullanılır.

* Veri üzerinde değişiklik yapmaz, sadece bilgi alır.
#### Örnek:
* Tarayıcıda bir web sitesine girmek → sunucudan HTML sayfası almak.

```yml
GET https://api.example.com/kullanicilar

```

#### Post:
* Sunucuya yeni veri eklemek için kullanılır.

* Genellikle form gönderimlerinde veya veri oluştururken kullanılır.
#### Örnek:

* Yeni kullanıcı eklemek:
```nginx
POST https://api.example.com/kullanicilar
Body: { "isim": "Ahmet", "yas": 25 }
```

#### Put:
* Sunucudaki var olan veriyi güncellemek için kullanılır.

* Genellikle tüm veri kaydı değiştirilir.
#### Örnek:
* Kullanıcının adını güncellemek:

```yml
PUT https://api.example.com/kullanicilar/1
Body: { "isim": "Ahmet", "yas": 25 }
```

#### Delete:
* Sunucudaki bir veriyi silmek için kullanılır.
#### Örnek:
* Kullanıcıyı silmek:
```yml
DELETE https://api.example.com/kullanicilar/1
```
</details>
 
<details>

<summary>RESTful servislerin çalışma mantığı</summary>

* RESTful servislerin çalışma mantığı, kaynaklara (örneğin kullanıcı veya ürün) URL üzerinden ulaşmak ve bu kaynaklar üzerinde işlem yapmak için HTTP metodlarını kullanmaya dayanır.Her istek bağımsızdır (stateless), yani sunucu önceki isteği hatırlamaz. Veriler genellikle JSON formatında gidip gelir. Böylece sistem hem basit hem de farklı uygulamalar tarafından kolayca kullanılabilir.

</details>
<details>

<summary>JSON veri formatı, kullanım amacı ve JSON veri örneği açıklaması </summary>

> JSON Veri Formatı 

JSON, verileri anahtar–değer (key–value) çiftleri halinde saklayan hafif bir veri formatıdır. Veriler süslü parantez { } içinde tutulur, anahtarlar her zaman çift tırnak " " içinde yazılır. Değerler ise sayı, metin, true/false, null, liste veya başka bir nesne olabilir.

> JSON Kullanım Amacı

* Sunucu ile istemci arasında veri alışverişi yapmak (API’lerde veri transferi).

* Yapılandırılmış bilgileri dosya halinde saklamak (konfigürasyon, ayarlar).

* Farklı platformlar ve programlama dilleri arasında uyum sağlamak.

* İnsanlar tarafından okunabilir ve bilgisayarlar tarafından kolay işlenebilir olmak.

* Hafif yapısı sayesinde ağ üzerinden hızlı veri taşımak ve performansı artırmak.

* Gerçek zamanlı uygulamalarda veri iletimini kolaylaştırmak (chat uygulamaları, canlı bildirimler).

* Verilerin organize ve hiyerarşik şekilde saklanmasını sağlamak.

* Web servisleri ve mobil uygulamalar arasında standart bir veri formatı oluşturmak.

* Büyük veri ve bulut uygulamalarında veri paylaşımını basitleştirmek.

> JSON Veri Örneği 

```yml
{
  "id": 003,
  "name": "Adil",
  "email": "adill@example.com",
  "age": 91,
  "isActive": true,
  "roles": ["user", "admin"],
  "address": {
    "street": "  Yenibosna 85",
    "city": "İstanbul",
    "zip": "34000"
  }
}
```
</details>


<details>

<summary>SOAP ve GraphQL Nedir, REST’ten Farkları Temel Karşılaştırması</summary>

> SOAP ve GraphQL Nedir?

SOAP (Simple Object Access Protocol):
XML tabanlı bir web servis protokolüdür. Katı standartları vardır ve özellikle kurumsal, finansal veya güvenlik gerektiren sistemlerde kullanılır. Mesajlar XML ile paketlenir ve HTTP, SMTP gibi protokoller üzerinden iletilir.

GraphQL:
Facebook tarafından geliştirilen bir API sorgulama dilidir. İstemciye sadece ihtiyaç duyduğu veriyi aldırır ve tek bir endpoint üzerinden birden fazla kaynağa erişim sağlar. REST’in “çok endpoint ve fazla veri alma” sorununu çözer.

> REST İle Farkları (Tablo)

| Özellik             | REST                          | SOAP                                  | GraphQL                                   |
| ------------------- | ----------------------------- | ------------------------------------- | ----------------------------------------- |
| **Veri Formatı**    | JSON, XML (çoğunlukla JSON)   | XML                                   | JSON                                      |
| **Endpoint Yapısı** | Her kaynak için ayrı endpoint | Tek veya birden fazla                 | Genellikle tek endpoint                   |
| **Esneklik**        | Orta; sabit veri              | Düşük; katı standartlar               | Yüksek; istemci ihtiyacına göre veri alır |
| **Güvenlik**        | HTTPS                         | WS-Security gibi gelişmiş protokoller | HTTPS veya token tabanlı                  |
| **Kullanım Alanı**  | Web ve mobil uygulamalar      | Kurumsal, finans, büyük sistemler     | Modern API’ler, esnek veri sorgulamaları  |
| **Veri Alma Şekli** | Sabit endpoint veri yapısı    | Katı mesaj yapısı                     | Sorgu ile sadece gerekli veri çekilir     |
| **Veri Güncelleme** | GET, POST, PUT, PATCH, DELETE | Operasyonlar (RPC tarzı)              | Mutation ile yapılır                      |

> REST vs SOAP vs GraphQL temel karşılaştırması

* REST basitliğiyle öne çıkar ama bazen gereksiz veri döndürür.

* SOAP güvenlik ve standart bakımından güçlüdür fakat ağırdır.

* GraphQL esneklik sağlar, istemci tam olarak ihtiyacı kadar veri alır ama öğrenmesi REST’e göre daha zordur.
</details>

## 4. ASP.NET

<details>
<summary>ASP.NET ve ASP.NET Core nedir? Avantajları, Farkları</summary>

> ASP.NET Nedir:

ASP.NET, Microsoft’un geliştirdiği bir web geliştirme platformudur. Amacı, yalnızca statik sayfalar yerine, dinamik, kullanıcıyla etkileşimli ve veritabanı bağlantılı web siteleri oluşturmayı sağlamaktır.
Bu teknoloji .NET çatısı altında çalışır, yani genellikle C# diliyle kodlanır. Kullanıcı bir sayfa istediğinde ASP.NET, sunucu tarafında kodu çalıştırır, veritabanıyla iletişim kurar, gerekli hesaplamaları yapar ve tarayıcıya son haliyle HTML, CSS, JavaScript gönderir. Böylece kullanıcı, kişiye özel ve dinamik içerik görmüş olur.

> ASP.NET Core Nedir:

ASP.NET Core, Microsoft’un geliştirdiği, ASP.NET’in modern ve gelişmiş sürümüdür. Klasik ASP.NET yalnızca Windows üzerinde çalışırken, ASP.NET Core Windows, Linux ve macOS’ta çalışabilir. Ayrıca daha hafif, hızlı ve esnek olacak şekilde tasarlanmıştır.
Bu teknoloji ile hem dinamik web siteleri hem de API servisleri geliştirilebilir. Modüler yapısı sayesinde sadece ihtiyaç duyulan bileşenler projeye eklenir, bu da performansı artırır. Genellikle C# dili ile kullanılır ve bulut tabanlı uygulamalar için de oldukça uygundur.
Kısacası: ASP.NET Core, günümüzde web uygulamaları geliştirmek için kullanılan, platform bağımsız, açık kaynaklı ve yüksek performanslı Microsoft teknolojisidir.

> Avantajları:
* Platform her işletim sisteminde kullanabilir Win, MacOS, Linux

* Yüksek performanslıdır daha az yer kaplayan  ve hızlı bir yapıya sahiptir.

* Modülerdir sadece ihtiyaç duyulan bileşenler eklenir, gereksiz yük yoktur.

* Bulut uyumludur özellikle Azure gibi bulut servisleriyle sorunsuz çalışır.

* Güvenlidir kimlik doğrulama, yetkilendirme ve veri koruma için güçlü araçlar sunar.

* Modern geliştirme desteği vardır RESTful API, gRPC, SignalR gibi teknolojilerle uyumludur.

* Açık kaynaklıdır Topluluk katkısı vardır ve sürekli gelişmektedir.

* Sürekli güncellenir Microsoft tarafından aktif olarak desteklenir.
> Farkları:
* ASP.NET yalnızca Windows üzerinde çalışır, ASP.NET Core ise Windows, Linux ve macOS üzerinde çalışabilir.

* ASP.NET kapalı kaynaklıdır, ASP.NET Core açık kaynaklıdır.

* ASP.NET daha ağır bir yapıya sahiptir, ASP.NET Core daha hafif ve yüksek performanslıdır.

* ASP.NET’te yapı monolitiktir, ASP.NET Core ise modülerdir; sadece gerekli bileşenler eklenebilir.

* ASP.NET bulut için optimize edilmemiştir, ASP.NET Core bulut tabanlı uygulamalara uygundur.

* ASP.NET eski Web Forms ve MVC modellerine dayanır, ASP.NET Core modern yaklaşımları (MVC, Razor Pages, minimal API vb.) destekler.

* ASP.NET geliştirmesi büyük ölçüde durmuş durumdadır, ASP.NET Core ise aktif olarak güncellenmeye devam etmektedir.
</details>

<details>

<summary>MVC nedir, ne için kullanılır?</summary>

> MVC Nedir:

MVC, Yazılım Mühendisliği’nde önemli bir yere sahip architectural patterns (yazılım mimari desenleri)’ın bir parçasıdır. Model, View ve Controller kelimelerinin baş harflerinden oluşan MVC (Model-View-Controller), 1979 yılında Tygve Reeskaug tarafından oluşturulmuş ve yazılım gelişmede bir çok projede kullanılmıştır. Son dönemlerde Microsoft’un MVC desenini Asp.Net teknolojisi ile birleştirmesi ile popülaritesi daha da artmıştır.

> MVC Ne İçin Kullanılır

MVC projeleri daha düzenli, esnek ve yönetilebilir yapmak için kullanılır. 

* Kod düzeni sağlar uygulamayı 3 katmana ayırır (Model, View, Controller).

* Bakımı kolaylaştırır görünüm, iş mantığı ve veri birbirinden bağımsızdır.

* Takım çalışmasını kolaylaştırır frontend ve backend geliştiriciler ayrı katmanlarda çalışabilir.

* Yeniden kullanılabilirlik sağlar aynı Model veya iş mantığı başka projelerde de kullanılabilir.

* Test edilebilirliği artırır katmanlar ayrı olduğu için daha kolay test yapılır.

* Sürdürülebilirlik sağlar büyük ve uzun vadeli projelerde düzeni korur.
 
 </details>
 
<details>
 
<summary>Middleware nedir, nasıl çalışır?</summary>

> Middleware Nedir:

Middleware, yazılım dünyasında özellikle web uygulamaları ve frameworkler (ör. ASP.NET, Django, Express.js) içinde sıkça kullanılan bir kavramdır.

#### Örneğin:
```yml
// Basit bir middleware
function logger(req, res, next) {
  console.log(`İstek: ${req.method} ${req.url}`);
  next(); // bir sonraki middleware'e veya route'a geç
}

app.use(logger);
```

> Middleware Nasıl Çalışır:

* Kullanıcı istek gönderir bir URL çağrılır.

* İstek sunucuya ulaşmadan önce middleware zincirine girer.

* Her middleware:

  * Gelen isteği inceleyebilir.

  * İsteği değiştirebilir.

  * Yanıtı durdurabilir.

  * Veya bir sonrakine iletebilir (next() fonksiyonu ile).

* Sonunda istek asıl hedefe (controller/route) ulaşır.

* Yanıt oluşturulduktan sonra middleware zincirinden geri dönebilir.

#### Örneğin:
```yml
// 1. Middleware
function logger(req, res, next) {
  console.log("İstek alındı:", req.method, req.url);
  next(); // devam et
}

// 2. Middleware
function auth(req, res, next) {
  if (!req.headers.authorization) {
    return res.status(401).send("Yetkisiz!");
  }
  next(); // devam et
}

app.use(logger);
app.use(auth);

app.get("/", (req, res) => {
  res.send("Hoş geldin!");
});


  ```

> Startup.cs, Program.cs içindeki middleware sıralamasının açıklaması

ASP.NET Core’da middleware sıralaması, uygulamaya gelen isteğin hangi sırada işleneceğini belirler. İstek önce tanımlanan ilk middleware’den geçer ve sırasıyla diğerlerine aktarılır. Yanıt da ters yönde geri döner. Bu yüzden sıralama çok önemlidir.
Örneğin UseExceptionHandler en başta olmalıdır çünkü daha sonra çalışan herhangi bir middleware hata üretirse bu hatayı yakalayabilsin. UseHttpsRedirection erken çalışır çünkü gelen tüm isteklerin güvenli bağlantıya yönlendirilmesi gerekir. UseStaticFiles, routing’den önce çalışır çünkü aksi takdirde CSS, JS gibi dosyalar route gibi algılanabilir. UseRouting ile istek hangi controller ve action’a gidecekse belirlenir. Daha sonra UseAuthentication devreye girerek kullanıcının kimliği doğrulanır. Ardından UseAuthorization çalışarak doğrulanmış kullanıcının yetkili olup olmadığı kontrol edilir. En sonda ise UseEndpoints veya MapControllerRoute bulunur; bu da isteği gerçek endpoint’e yönlendirir ve yanıt üretir.

> Middleware sıralaması:

 ```yml

Request  → Middleware1 → Middleware2 → Middleware3 → Endpoint
Response ← Middleware1 ← Middleware2 ← Middleware3 ← Endpoint
 ```
</details>

<details>

<summary>Dependency Injection (DI) nedir, neden önemlidir?</summary>

> Dependency Injection DI Nedir:

Dependency Injection DI, yazılım geliştirmede bir sınıfın ihtiyaç duyduğu başka nesneleri veya hizmetleri kendisi yaratmak veya yönetmek yerine, bu bağımlılıkların dışarıdan sağlanması prensibine dayanan bir tasarım yöntemidir.


> Dependency Injection Neden Önemlidir:

Yazılım geliştirmede sınıfların birbirine sıkı sıkıya bağlı olması işleri zorlaştırır. DI sayesinde bu bağımlılıklar gevşetilir ve kod daha esnek hale gelir.

Önemli olmasının sebepleri:

Sınıflar birbirine bağımlı olmaz, daha kolay değiştirilip genişletilebilir.

Test edilebilirliği artırır gerçek nesne yerine sahte/mock nesneler kullanılabilir, birim testler kolaylaşır.

Bakımı kolaylaştırır bir bağımlılık değişirse diğer sınıflara dokunmadan güncelleme yapılabilir.

Yeniden kullanılabilirlik sağlar aynı sınıf farklı senaryolarda farklı bağımlılıklarla çalışabilir.

Sürdürülebilirlik sağlar büyük projelerde karmaşıklığı azaltır ve ekiplerin daha verimli çalışmasına yardımcı olur.

> Dependency Injection DI Kullanımı Örneneği:
 ```yml
// 1. Önce bir arayüz tanımlıyoruz
public interface INotificationService
{
    void Send(string message);
}

// 2. Email servisi
public class EmailNotification : INotificationService
{
    public void Send(string message)
    {
        Console.WriteLine("Email gönderildi: " + message);
    }
}

// 3. SMS servisi
public class SmsNotification : INotificationService
{
    public void Send(string message)
    {
        Console.WriteLine("SMS gönderildi: " + message);
    }
}

// 4. Bildirim yöneticisi (Dependency Injection burada devreye giriyor)
public class NotificationManager
{
    private readonly INotificationService _notificationService;

    // Bağımlılık dışarıdan enjekte ediliyor
    public NotificationManager(INotificationService notificationService)
    {
        _notificationService = notificationService;
    }

    public void Notify(string message)
    {
        _notificationService.Send(message);
    }
}

// 5. Kullanım
class Program
{
    static void Main(string[] args)
    {
        // Email servisini kullanmak istersek:
        var emailManager = new NotificationManager(new EmailNotification());
        emailManager.Notify("Hoş geldiniz!");

        // SMS servisini kullanmak istersek:
        var smsManager = new NotificationManager(new SmsNotification());
        smsManager.Notify("Şifreniz: 1234");
    }
}

```
</details>

<details>
<summary>Katmanlı Mimari (Layered Architecture)</summary>

> Presentation, Business, Data Access katmanları:

#### Presentation Layer (Sunum Katmanı)

  * Kullanıcıyla etkileşim kurmak
    
  * Kullanıcıdan veri alır ekrana çıktı verir.

  * İş kurallarını içermez sadece görselleştirme ve yönlendirme yapar.

#### Business Layer (İş Katmanı)

  * Uygulamanın iş mantığını bulundurması
   
  * İş kuralları ve algoritmalar burada uygulanır.

  * Sunum katmanından gelen talepleri işler.

  * Veri erişim katmanıyla iletişim kurar ama veritabanına doğrudan bağlanmaz.
    
#### Data Access Layer (Veri Erişim Katmanı)

  * Veritabanı ile uygulama arasında iletişim kurmak

  * Veritabanı sorgularını SQL, ORM, Repository içerir.

  * CRUD (Create, Read, Update, Delete) işlemlerini yapar.

  * Business Layer’a sadece işlenmiş veri nesneleri döner.

#### Repository Pattern:

 * Veritabanına erişimi soyutlar.

 * CRUD ekle, oku, güncelle, sil işlemlerini yapar.

 * İş katmanı veritabanı detaylarını bilmez sadece repository’den veri ister.


#### Service Pattern:

 * İş kurallarını içerir.

 * Doğrulama, hesaplama, kurallar burada uygulanır.

 * Sunum katmanı sadece service ile konuşur, repository ile doğrudan iletişime geçmez.

   
![1_vNZs7q1OgPc2yDaiGJpCwg](https://miro.medium.com/v2/resize:fit:786/format:webp/1*yRlhn__kn1enuvb6rja0gw.png)
</details>

<details>

<summary>Clean Architecture</summary>

> Domain, Application, Infrastructure, API katmanları:


#### Domain Layer (Alan Katmanı)

* Temel iş kurallarını ve mantığını içerir.

* Entity ve Value Object’ler burada bulunur.

* Domain servisleri iş akışlarını yönetir.

#### Application Layer (Uygulama Katmanı)

* İş kurallarını kullanarak uygulama mantığını yönetir.

* Use-case ve servisler burada yer alır.

* Domain katmanına bağımlıdır, iş akışını koordine eder.

#### Infrastructure Layer (Alt Yapı Katmanı)

* İş kurallarını kullanarak uygulama mantığını yönetir.

* Use-case ve servisler burada yer alır.

* Domain katmanına bağımlıdır, iş akışını koordine eder.

#### API Layer (Arayüz Katmanı)

* Kullanıcı ve diğer sistemlerle iletişim sağlar.

* Gelen istekleri Application katmanına yönlendirir.

* Yanıtları kullanıcıya veya dış sistemlere döndürür.

> Bağımlılıkların dışa akması ilkesi:

İç katmanlar (Domain, Application) dış katmanlara bağımlı olamaz.
Yani iş kuralları (Domain) veritabanını, API’yi veya dış servisleri bilmemelidir.
Tam tersi, dış katmanlar iç katmanlara bağımlıdır.


![1_vNZs7q1OgPc2yDaiGJpCwg](https://i.sstatic.net/DJm5T.png)
  
</details>

##  5. Veritabanı ve ORM


> SQL nedir?

SQL (Structured Query Language), ilişkisel veritabanlarını yönetmek için kullanılan standart bir sorgu dilidir.
Verilerin tanımlanması, saklanması ve düzenlenmesi için geliştirilmiş olup, günümüzde birçok veritabanı sisteminde temel iletişim dili olarak kullanılır.




















































































































































































































































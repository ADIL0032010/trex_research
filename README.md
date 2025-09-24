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



















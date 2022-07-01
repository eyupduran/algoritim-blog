---
title: "Container ve Sanal Makine"
date: 2022-06-30T12:12:26+03:00
draft: false
tags: ["container","docker","virtual makine"]
categories: ["yazılım"]
ShowToc: true
---
### Virtual Makine-Container Nedir ve Arasındaki Farklar Nelerdir?

Hem VM'ler hem de containerlar, mevcut bilgisayar donanım ve yazılım kaynaklarını en üst düzeye çıkarmanıza yardımcı olmak için sanallaştırmayı kullanır. Konteynerler bir süredir piyasada ancak son birkaç yılda geniş çapta benimsenmeleri, BT uygulamalarını temelden değiştirdi. VM'ler ise bir süredir çok popüler ve her boyuttaki veri merkezinde yer almaya devam ediyor. Bulutta hizmet ve uygulama çalıştırma dahil mimari kararlara yaklaşırken, bu sanallaştırma teknolojilerini anlamanız gerekir.

---
### İlk olarak Bazı Temel Bilgiler
### Sanallaştırma Nedir?
Sanallaştırma, fiziksel bilgi işlem donanımından (esas olarak bilgisayar tarafından oluşturulan bir bilgisayar) soyutlanmış simüle edilmiş bir bilgi işlem ortamı yaratma sürecidir. Sanallaştırma, tek bir makinenin donanım ve yazılım bileşenlerinden birden çok sanal bilgi işlem örneği oluşturmanıza olanak tanır. Bu örnekler, geleneksel anlamda bir bilgisayar veya bir depolama havuzu, uygulama, sunucu veya ağ yapılandırması olabilir

### Hypervisor nedir?
Sanallaştırmayı sağlayan yazılıma hiper yönetici denir. Fiziksel donanım ile sanallaştırılmış ortamlar arasında yer alan ve birden çok işletim sisteminin aynı donanım üzerinde birlikte çalışmasına izin veren hafif bir yazılım katmanıdır. Hiper yönetici, altyapınızın ham maddelerinden kaynakları çeken ve bunları çeşitli bilgi işlem örneklerine yönlendiren aracıdır.

### Virtual Makine ve Containerler

### Virtual Makineler Nelerdir?
Sanallaştırmanın mümkün kıldığı bilgisayar tarafından oluşturulan bilgisayarlar, sanal makineler (VM'ler) olarak bilinir.Gerçekte tek bir fiziksel bilgisayarda bulunan donanım üzerinde çalışan ayrı bilgisayarlardır. Her VM kendi işletim sistemine ihtiyaç duyar. İşletim sistemi ve bağımsız bir VM üzerinde çalışan tüm uygulamalar, tek bir ana bilgisayar sunucusundan veya bir ana bilgisayar sunucuları havuzundan donanım kaynaklarını paylaşır.Hypervisor sayesinde donanım kaynakları sanallaştırılır ve her VM komşularından izole edilir. Uygun fiyatlı sanallaştırma teknolojisi ve bulut bilişim hizmetlerinin ortaya çıkmasından bu yana, büyük ve küçük BT departmanları, maliyetleri düşürmenin ve verimliliği artırmanın bir yolu olarak VM'leri tercih ettiler.

![](https://www.backblaze.com/blog/wp-content/uploads/2018/06/VM-Transparent-Fill-01-1024x1024.png)

Ancak VM'ler çok fazla sistem kaynağını alabilir. Her VM, yalnızca bir işletim sisteminin tam bir kopyasını değil, işletim sisteminin çalıştırması gereken tüm donanımın sanal bir kopyasını da çalıştırır. VM'lerin bazen "monolitik" terimiyle ilişkilendirilmesinin nedeni budur; bunlar tek, büyük dosyalar olarak oluşturulmuş uygulamaları çalıştırmak için yaygın olarak kullanılan tek, hepsi bir arada birimlerdir. Bu, hızla çok fazla RAM ve CPU'ya ihtiyaç duyar. Ayrı gerçek bilgisayarları çalıştırmaya kıyasla hala ekonomiktirler, ancak bazı kullanım durumları aşırıya kaçabilir.


### Virual Makine'nin Faydaları
- Tüm işletim sistemi kaynakları uygulamalar tarafından kullanılabilmesi

- İyi kurulmuş işlevsellik

- Güçlü yönetim araçlarına sahip oluşu

- Bilinen güvenlik araçları ve kontrolleri

- Farklı işletim sistemlerini tek bir fiziksel makinede çalıştırma yeteneği

- Ayrı, fiziksel makineler çalıştırmaya kıyasla maliyet tasarrufu sağlaması


### Popüler Virtual Makine Sağlayıcıları
> VMware Workstation Player.

> VirtualBox..

> Xen Project.

> Microsoft Hyper-V.

### Container Nedir?
Container'larla, temeldeki bilgisayarı bir VM gibi sanallaştırmak yerine, yalnızca işletim sistemi sanallaştırılır. Containerlar, fiziksel bir sunucunun ve ana bilgisayar işletim sisteminin (genellikle Linux veya Windows) üzerine oturur. Her container, ana bilgisayar işletim sistemi çekirdeğini ve genellikle ikili dosyaları ve kitaplıkları da paylaşır. Paylaşılan bileşenler salt okunurdur. Kitaplıklar gibi işletim sistemi kaynaklarının paylaşılması, işletim sistemi kodunu yeniden oluşturma ihtiyacını önemli ölçüde azaltır; bir sunucu, tek bir işletim sistemi kurulumuyla birden çok iş yükünü çalıştırabilir.

Conteinerlar bu nedenle son derece hafiftir; boyutları yalnızca megabayttır ve başlamaları yalnızca birkaç saniye sürer. Bunun pratikte anlamı, containerlı tek bir sunucuya bir VM ile yapabileceğinizden iki ila üç kat daha fazla uygulama koyabilirsiniz. Conteinerlarla karşılaştırıldığında, VM'lerin çalışması dakikalar alır ve gigabayt ile megabayt olarak ölçülen eşdeğer bir conteinerdan çok daha büyüktür. Conteiner teknolojisi uzun süredir varlığını sürdürüyor, ancak 2013'te Docker'ın piyasaya sürülmesi, conteinerlari uygulama ve yazılım geliştirme için esasen endüstri standardı haline getirdi. Çevre tutarsızlığı sorununu çözerler.

Geliştiriciler genellikle yerel olarak, örneğin dizüstü bilgisayarlarında kod yazarlar ve ardından bu kodu bir sunucuya dağıtırlar. Bu ortamlar (yazılım sürümleri, izinler, veritabanı erişimi vb.) arasındaki herhangi bir farklılık, hatalara yol açar. Conteinerlar sayesinde geliştiriciler, yerel, geliştirme, test veya üretim olsun, bu birimin herhangi bir ortamda çalışması için gereken tüm bağımlılıkları içeren taşınabilir, paketlenmiş bir birim oluşturabilir. Uygulama geliştirme için mikro hizmet mimarileri, bu conteinerların patlamasından doğdu.

Conteinerlarla uygulamalar, tek bir amaca hizmet eden en küçük bileşen parçalarına veya “hizmetlerine” bölünebilir ve bu hizmetler tek bir tek parça birim yerine birbirinden bağımsız olarak geliştirilebilir ve dağıtılabilir. Örneğin, müşterilerin dünyadaki her şeyi satın almasına olanak tanıyan bir uygulamanız olduğunu varsayalım. Bir arama çubuğunuz, bir alışveriş sepetiniz, bir satın alma düğmesi vb. olabilir. Bu "hizmetlerin" her biri kendi conteinerlarında bulunabilir, böylece, örneğin, arama çubuğu yüksek yük nedeniyle başarısız olursa, bu "hizmetlerin" her şey aşağı. Ve bugün Prime Day fırsatlarınızı bu şekilde alırsınız.


![Second](https://www.backblaze.com/blog/wp-content/uploads/2018/06/Containers-Transparent-Fill-01-1024x1024.png)

### Container Araçları
> Linux Containers (LXC)

> Docker

> Kubernetes

### Container'ın Faydaları
- Azaltılmış BT yönetim kaynakları.

- Daha küçük kaynak tahsisi, bir fiziksel makinenin birçok containeri barındırabileceği anlamına gelir.

- Azaltılmış ve basitleştirilmiş güvenlik güncellemeleri.

- İş yüklerini aktarmak, taşımak ve yüklemek için daha az kod yazımı


### Virtual Makine Ve Container Arasındaki Fark Nedir?
Sanal makine ve container tartışması, geleneksel BT mimarisi ile çağdaş DevOps uygulamaları arasındaki tartışmanın merkezinde yer alır. VM'ler son derece popüler ve kullanışlı oldu ve olmaya devam ediyor, ancak ne yazık ki onlar için artık 25 tonluk bir Stonehenge gibi gittikleri her yerde "monolitik" terimini yanlarında taşıyorlar. Bu arada containerlar“mikro hizmetler” örtüsüne büründü.

Başka bir ilginç teknoloji metaforu sunmak için, VM'ler, ultra hafif sırt çantasıyla seyahat için glamping ne ise, containerlar için de o anlama gelir. Her ikisi de sizi sanallaştırmanın vahşi ortamında hayatta kalmak için ihtiyacınız olan her şeyle donatıyor. Her ikisi de taşınabilir, ancak hedefiniz buysa, containerlar sizi daha uzağa, daha hızlı götürecektir. VM'ler her şeyi ve mutfak lavabosunu getirirken, kaplar ağırlığı azaltmak için diş fırçasını evde bırakır. Daha doğrudan farklılıkları karşılaştırmak için tabloya bakabilirsiniz.

|**Virtual Makine** | **Container** |
|--- |--- |
|Depolama olarak çok yer kaplar.|Az yer kaplar.|
|Sınırlı performans|Yerel performans.|
|Her VM kendi işletim sisteminde çalışır.|Tüm containerlar,ana bilgisayar işletim sistemini paylaşır|
|Donanım düzeyinde sanallaştırma.|işletim sistemi sanallaştırma.|
|Dakika cinsinden başlatma süresi.|Milisaniye cinsinden başlatma süresi.|
|Uygulamayı çalıştırmak için gerekli belleği ayırır.|Daha az bellek alanı gerektirir.|
|Tamamen izole ve dolayısıyla daha güvenli.|Süreç düzeyinde izolasyon, muhtemelen daha az güvenli.|


### VM'ler için Kullanımlar ve Konteynerler için Kullanımlar
Hem containerlar hem de VM'lerin avantajları ve dezavantajları vardır ve nihai karar, özel ihtiyaçlarınıza bağlı olacaktır. Sunucularda birden çok uygulama çalıştırmanız gerektiğinde veya yönetilmesi gereken çok çeşitli işletim sistemleriniz olduğunda, işletim sisteminin tüm kaynaklarını ve işlevselliğini gerektiren uygulamaları çalıştırmak için VM'ler daha iyi bir seçimdir. Mikro hizmetlere yeniden düzenlemeyi planlamadığınız veya ihtiyaç duymadığınız mevcut bir monolitik uygulamanız varsa, VM'ler kullanım durumunuza iyi hizmet etmeye devam edecektir.

En büyük önceliğiniz minimum sayıda sunucuda çalışan uygulama veya hizmet sayısını en üst düzeye çıkarmak olduğunda ve maksimum taşınabilirliğe ihtiyacınız olduğunda containerlar daha iyi bir seçimdir. Yeni bir uygulama geliştiriyorsanız ve ölçeklenebilirlik ve taşınabilirlik için bir mikro hizmet mimarisi kullanmak istiyorsanız, containerlar gitmeniz gereken yoldur. Bir mikro hizmet mimarisine dayalı bulutta yerel uygulama geliştirme söz konusu olduğunda containerlar parlıyor.

Ayrıca, containerları sanal bir makinede çalıştırabilir , bu da soruyu, iş yükleriniz için hangi teknolojinin en anlamlı olduğunu anlamak için bir/veya daha fazla alıştırmadan daha az hale getirir.

Kısaca: VM'ler,sınırlı sayıda donanım ve yazılımdan çıkarabileceğiniz makine sayısını artırarak şirketlerin altyapı kaynaklarından en iyi şekilde yararlanmalarına yardımcı olur. Containerlar,mikro hizmetleri ve DevOps uygulamalarını etkinleştirerek şirketlerin geliştirme kaynaklarından en iyi şekilde yararlanmasına yardımcı olur .









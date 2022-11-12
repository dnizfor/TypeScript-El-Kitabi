---
description: İlk adımlar
---

# Hakkında



Programlama topluluğuna tanıtılmasından 20 yılı aşkın bir süre sonra JavaScript, şu ana kadar oluşturulmuş en yaygın platformlar arası dillerden biridir. Web sayfalarına önemsiz etkileşimler eklemek için küçük bir dil olarak başlayan JavaScript, her boyuttaki hem ön uç hem de arka uç uygulamaları için tercih edilen bir dil haline geldi.JavaScript ile yazılan programların boyutu, kapsamı ve karmaşıklığı katlanarak artarken, JavaScript dilinin farklı kod birimleri arasındaki ilişkileri ifade etme yeteneği bu ddeğişimlere ayak uyduramamıştır. Bütün bunlar JavaScript'in kendine özgü çalışma zamanı semantiği ile birleştiğinde; dil ve program karmaşıklığı arasındaki bu uyumsuzluk , JavaScript geliştirmeyi büyük ölçekte yönetilmesi zor bir iş haline getirmiştir.

Kod yazılırken en yaygın yapılan hatalardan biri tip hatalarıdır. Örneğin önceden belirlenmiş bir tipte beklenen veri yerine başka tipte bir veri girildiğinde bu hata oluşur (basit bir hesap makinesi uygulamasına _integer_ göndermek yerine _string_ veri göndermek). Bunun sebebi basit bir dikkat dağınıklığı , dökümantasyonu iyi anlamamak veya herhangi bir sebep olabilir. İşte TypeScript'in amacı da , bu tür durumlardan kaçınmak için ; JavaScript programı için statik bir tip denetleyicisi olmaktır.Başka bir değişle programınız çalışmadan önce çalışan (statik) ve programınızda tiplerden kaynaklı bir hata olmadığını kontrol eden bir araç olmaktır.

Eğer TypeScript'e JavaScript geçmişiniz olmadan, TypeScript'in ilk diliniz olması niyetiyle geliyorsanız, öncelikle [Microsoft Learn JavaScript](https://docs.microsoft.com/javascript/) eğitimindeki belgeleri okumaya başlamanızı veya [Mozilla Web Docs'ta JavaScript'i](https://developer.mozilla.org/docs/Web/JavaScript/Guide) okumanızı öneririz. Eğer diğer dillerde deneyiminiz varsa, el kitabını okuyarak JavaScript sözdizimini hızlıca öğrenebilirsiniz.

[Dil Temellerini ](temeller.md)öğrenmeye başlamadan önce, aşağıdaki giriş sayfalarından birini okumanızı öneririz. Bu tanıtımlar, TypeScript ile favori programlama diliniz arasındaki temel benzerlikleri ve farklılıkları vurgulamayı ve bu dillere özgü yaygın yanlış anlaşılmaları gidermeyi amaçlamaktadır.



### El Kitabının Yapısı

Kitap iki ana bölümden oluşmaktadır.

* **The Handbook**

TypeScript El Kitabı, TypeScript'i herhangi bir programcıya açıklayan kapsamlı bir belge olmayı amaçlamaktadır. El kitabını sol taraftaki navigasyonda yukarıdan aşağıya doğru ilerleyerek okuyabilirsiniz.

Her bölüm size verilen kavramları güçlü bir şekilde anlamanızı sağlamak için tasarlandı . TypeScript El Kitabı orjinal dökümantasyon kadar ayrıntılı olmasa dahi dilin tüm özellikleri ve davranışları için kapsamlı bir kılavuz olması amaçlanmıştır.



Bu kitabı okuyan bir okuyucu şunları yapabilmelidir:

* Yaygın olarak kullanılan TypeScript sözdizimini ve kalıplarını okuma ve anlamaş
* Derleyici davranışlarını anlamak
* Bir çok durumda doğru tip sistemini kullanmak

Kısa ve net olmak açısından, El Kitabının ana içeriği; açıklanan özelliklerin her ayrıntısını incelemeyecektir. Belirli kavramlar hakkında daha fazla ayrıntıyı referans makalelerinde bulabilirsiniz.



* **Referans Makaleleri**

Bu kısım konseptlerin daha ayrıntılı olarak açıklanması amacıyla kitabın sonuna eklenmiştir. Aşağıdan yukarıya doğru okuyabilseniz de her başlık ayrı bir konsepti açıkladığı için akıcılık kaygısı güdülmemiştir.

#### Kitabın Yazılış Amacı Bu Değil

El Kitabının birkaç saat içinde rahatça okunabilecek, kısa ve öz bir belge olması amaçlanmıştır. Kısa tutmak amacıyla bazı konular ele alınmayacaktır.

Bu el kitabı ;fonksiyonlar, sınıflar gibi JavaScript temellerini tam olarak açıklamaz. Gerekli gördüğümüz yerlerde okuyabilmeniz için gerekli kaynakları bıraktık.

Bu el kitabı , orjinal dökümantasyon yerine geçmeyi amaçlamaz. Özellikle bazı durumlarda , okumayı kolaylaştırmak için ileri seviye kavramlardan kısaca bahsettik ve ayrıntıları referans makaleleri kısmında verdik.

Referans makaleleri TypeScript'e aşina olmayan okuyucular için tasarlanmamıştır, bu nedenle bu sayfalarda ileri düzey terminoloji kullanabilir veya henüz okumadığınız konulara referans verebilirler.

Son olarak bu kitap TypeScript'in diğer araçlarla (webpack,npm,react...) nasıl etkileşime girdiğini açıklamaz. Bunları zaten internette bulabilirsiniz




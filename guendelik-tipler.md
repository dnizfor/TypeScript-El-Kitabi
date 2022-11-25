---
description: Temel değişken türlerini öğrenelim
---

# Gündelik Tipler

Bu bölümde, JavaScript kodunda bulacağınız en yaygın değişken türlerinden bazılarını ele alacağız ve bu türleri TypeScript'te tanımlamanın yollarını açıklayacağız. Bu ayrıntılı bir liste değildir ve gelecek bölümlerde diğer türleri adlandırmak ve kullanmak için daha fazla yol açıklanacaktır.



Hadi JavaScript veya TypeScript kodu yazarken karşılaşabileceğiniz en temel ve yaygın tipleri gözden geçirerek başlayalım. Bu öğreneceklerimiz ileriki bölümlerde anlatacağımız daha karmaşık tiplerin temel yapı taşlarını oluşturacaktır.

### Temel değişken türleri : string , number ve boolean

JavaScript'in çok sık kullanılan 3 [değişken türü](https://developer.mozilla.org/en-US/docs/Glossary/Primitive) vardır: **string , number ve boolean.** Bu değişken türlerinin her birinin TypeScript'te dengi bir tip tanımlaması vardır. Tahmin edebileceğiniz üzere bu tip tanımlamarı da bu değişkenleri JavaScript'teki **typeof** operatörüyle kullandığımızda dönen değerlerle aynıdır:

* **string** veri tipi "hello word" gibi **string** değerler içindir
* **boolean** veri tipi **true** ve **false** değerleri içindir
* **number** veri tipi 42 gibi sayısal değerler içindir. JavaScript'te **int** ve **float** değerler için özel bir ayrım yoktur. Onun için her ikisi de **number'**dır**.**&#x20;

> Bu veri tiplerini String, Number , Boolean şeklinde kullanabilirsiniz fakat bazı özel durumlarda sorunlara sebebiyet verebilir. Bu sebeple tip tanımlamalarınızı her zaman küçük harflerle yapmaya çalışın.

### Diziler

**\[1,2,3]** gibi diziler için de **number\[]** söz dizimini kullanabilirsiniz. Bu söz dizimi herhangi bir tip ile çalışabilir. ( Örneğin **\["a","b","c"]** için **string\[]** ). Ayrıca **Array\<number>** söz dizimini de kullanabilirsiniz. Jenerikler kısmına geldiğimizde **`T<U>`**şeklindeki bu söz dizilimini daha ayrıntılı bir şekilde işleyeceğiz.

> \[string] bir dizi için değil bir [demet ](obje-tipleri.md#demet-veri-tipi)için yapılan bir tanımlamadır.&#x20;

### any

TypeScript, belirli bir değerin herhangi bir tip kontrolü hatasına neden olmasını istemediğinizde kullanabileceğimiz özel bir tip'e sahiptir. Bu tip **any** veri tipidir.

**any** veri tipini kullandığınız verinin her hangi bir özelliğine erişebilir ( o da **any** tipinde olacaktır), onu bir fonksiyon gibi çağırabilir, herhangi bir türdeki bir değere atayabilir veya söz dizimsel olarak hemen hemen her şeyi yapabilirsiniz.

```ts
let obj: any = { x: 0 };
// Aşağıdaki kodlar normalde yanlış kullanım olmasına rağmen hiçbiri derleyici
// hatası vermez.
// any kullandığınızda tip kontrolünü devre dışı bırakıyorsunuz gibi düşünebiliriz
// TypeScript programcının en iyisini bildiğini varsayar
obj.foo();
obj();
obj.bar = 100;
obj = "hello";
const n: number = obj;
```

> **`any`tipi**, yalnızca TypeScript'i belirli bir kod satırının uygun olduğuna ikna etmek için uzun bir kod yazmak istemediğinizde kullanışlıdır.

### noImplicitAny

Eğer bir değişkene spesifik bir tip tanımlamazsanız ve TypeScript değişkenin tipini tahmin edemediğinde değerini otomatik olarak **any** olarak tanımlar.

Genellikle böyle durumlardan sakınmak isteriz çünkü doğrudan tanımlanmamış **any** tipleri kodumuzda hatalara sebep olabilir. Bu durumlar için **noImplicitAny** seçeneğini kullanın. Bu seçenek kodunuzda doğrudan tanımlanmamış **any** tip bir veri olduğunda hata verecektir.

### Değişkenlerde Tip Atamaları

**const , let** veya **var** kullanarak bir değişken tanımladığınız zaman , isteğe bağlı olarak, değişkeninize bir tip atayabilirsiniz.

```ts
let myName: string = "Alice";
//          ^^^^^^ tip ataması
```

> TypeScript , tiplerin solda yazıldığı `int x = 0; gibi` tip tanımlama sistemlerini kullanmaz. Tip tanımlamaları her zaman değerden sonra yapılır.

Lakin çoğu zaman değişkeninize tip atamaya gerek yoktur. TypeScript değişkenin değerinden türü tahmin edebilir.

```ts
// tip atamasına gerek yok -- TypeScript 'myName' değişkeninin 
//'string' veri tipinde olduğunu anlar.
let myName = "Alice";
```

### Fonksiyonlar

Fonksiyonlar JavaScript'te veri işlemenin en temel yoludur. TypeScript fonksiyonunuzun hem girdisine hem çıktısına tip ataması yapabilmenizi sağlar.

#### Tip Fonksiyonu Parametreleri

Fonksiyonunuzu tanımlarken fonksiyonunun alacağı her parametre için tip ataması yapabilirsiniz. Tip atamaları parametre isminden sonra yapılır.

```ts
// Parametreye tip ataması
function greet(name: string) {
  //                 ^^^^^^^^
  console.log("Hello, " + name.toUpperCase() + "!!");
}
```

Fonksiyona bir parametre girildiğinde artık bu parametrenin tipi kontrol edilecektir.

<figure><img src=".gitbook/assets/aaa.png" alt=""><figcaption></figcaption></figure>

> Parametrelerinize tip atamaları yapmasanız dahi TypeScript doğru sayıda argüman gönderilip gönderilmediğini kontrol eder.

### Fonksiyonun Döndürdüğü Değere Tip Ataması Yapmak

Ayrıca TypeScript'te fonksiyonun döndürdüğü değere de tip ataması yapabilirsiniz.

```ts
function getFavoriteNumber(): number {
  //                        ^^^^^^^^
  return 26;
}
```




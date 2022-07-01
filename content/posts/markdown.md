---
title: "Markdown"
date: 2022-06-28T11:30:04+03:00
draft: false
categories: ["yazılım"]
tags: ["markdown"]
ShowToc: true
#TocOpen: true
---

Markdown, John Gruber ve Aaron Swartz tarafından geliştirilen ve 2004 yılından bu yana kullanılan metinden HTML'e (text-to-HTML) dönüşüm için kullanılan hafif bir işaretleme dilidir.

GitHub gibi platformları kullananların aşina olduğu Markdown formatı, yaygın kanının aksine sadece README dosyaları oluşturmak kullanılmaz. Temel amaç okunabilirliği ve kullanılabilirliği arttırmaktır. Basitliği ve sadeliği sayesinde forumlarda ileti yazmaktan, kitap yazmaya kadar pek çok yerde kullanılabilir. Asıl güçlü olduğu kısım klavyeden elinizi kaldırmadan tablolardan, matematiksel ifadelere kadar ihtiyaç duyduğunuz her şeyi oluşturabilmeniz ve sonrasında biçimlendirebilmenizdir.

Sözü fazla uzatmadan dilerseniz örnekler üzerinden ilerleyelim. Başta da dediğim gibi zaten oldukça basit bir yapısı var, çok seveceğinizi düşünüyorum.

#### MARKDOWN TEMEL SYNTAX(SÖZDİZİMİ)

***
<!-- Başlık -->
#### Başlık
Syntaxı aşağıdaki gibidir.
> *ilgili etiket* ***başlık***(Araya bir tane boşluk bırakılır)

***Etiketler***


***#***    -----> Html'de h1' e karşılık gelmektedir.

***##***    -----> Html'de h2 'e karşılık gelmektedir

***###***    -----> Html'de h3' e karşılık gelmektedir

***####***   -----> Html'de h4' e karşılık gelmektedir

***#####***   -----> Html'de h5 'e karşılık gelmektedir

***######***   -----> Html'de h6 'e karşılık gelmektedir

***

<!-- Paragraf  -->
#### Paragraf
> Paragraf oluşturmak için herhangi birşey yapmaya gerek yok :) Yazımızı istediğimiz satırdan başlayarak direk yazabiliriz.

***Örnek paragraf***

Markdown öğrenmek ve uygulamak için çok basit bir işaretleme dilidir.Markdown, düz-metin-biçimlendirme sözdizimine sahip hafif bir işaretleme dili. Tasarımı, birçok çıktı biçimine dönüştürülmesine izin verir, ancak aynı ada sahip orijinal araç yalnızca HTML'yi destekler
***
<!-- Yeni bir satıra geçme -->
#### Yeni bir satıra geçme
Bu ilk satır yazısı

Bu da ikinci satır yazısı

Bu şekilde alt alta geçerek yazılarımızı yazabiliriz.
***
<!-- Bold(kalın) yazı -->
####  Bold(kalın) yazı

Yazıyı bold yapmanın syntaxı sekildeki gibidir.
> ** Text ** ve ya __Text __
Kelimenin başı ve sonuna iki tane ** veya iki tane __ kullanarak oluşturabiliriz.

**örnek bold(kalın) yazı**

***
<!-- İtalik yazı -->
####  İtalik yazı
Yazıyı italik yapmanın syntaxı sekildeki gibidir.
> * Text * 
Kelimenin başı ve sonuna bir tane * koyarak yazımızı italik yapabiliriz.


*örnek italik yazı*
***

<!-- Hem italik hem de bold -->
####  Hem italik hem de bold
Yazıyı hem italik hem de bold yapmanın syntaxı sekildeki gibidir.
> *** Text *** 
Yazımızın hem italik hem de bold olması için kelimemizi üç tane * arasında yazarak oluştururuz.

***örnek italik ve bold yazısı***


***
<!-- Blog alıntı -->
####  Blog alıntı
Blog yazısına almasını istediğimiz paragrafın başına bir tane ***>*** işareti konulur.

> Örnek blog yazısı
<!-- İç içe blog yazısı -->
####   İç içe blog yazısı
İçe girecek olan satır için iki tane *>* işareti kullanılır.
>Örnek blog yazısı
>
>> İç blog satırı
***
<!-- Listeleme -->
####  Liste yapısı

List yapısı oluşturmak için her satırın başına ***-*** konulur.
- birinci 
- ikinci 
- üçüncü

Satırların başına rakamlar yazarak da liste oluşturabiliriz.
1. birinci
2. ikinci
3. üçüncü 
    - bu alt bir list itemdir
    - ilgili list itemın altında bir tab boşluk bırakarak oluştururuz.
***
<!-- Kod satırları  -->
#### Kod satırları
Kod blokları oluşturmak için bloğun her satırına en az dört boşluk veya bir tab girilir.

    float sayi1 = 1.5f;
    float sayi2 = 2.0f;
    float carpim = sayi1 * sayi2;
    System.out.println("Sayıların Çarpımı: " + carpim);

Bunun yerine ilgili kod satırını  ***üç tane backtick(`)*** arasına alarak da kod satırı ekleyebiliriz.

```
function calculate(){
 
var k1=document.getElementById("kenar1").value;
var k2=document.getElementById("kenar2").value;
 
k1=Number(k1);
k2=Number(k2);
var alan=k1*k2;
alert("İki kenarı girilen dikdörtgenin alanı:"+alan);

```
***
<!-- Yatay çizgi oluşturma -->
####  Satırda yatay çizgi oluşturma
 
Düz çizgi istediğimiz satırda *** |---|___ işaretlerden herhangi bir tanesini kullanarak  oluşturabiliriz.
***
<!-- link oluşturma -->
#### Link oluşturma
Link oluşturmanın syntaxı sekildeki gibidir.
> [Sayfada gözükecek text](linkini de buraya yazıyoruz)

[Youtube](https://www.youtube.com/?hl=TR)a
[Github](https://github.com/)

***
<!-- Url ve Email bırakma -->
#### Url ve Email bırakma
Url ve email oluşturmanın syntaxı şekildeki gibidir
> <Url veya email adresi bu araya yazılır>

<https://github.com/eyupduran>
<eyupduran19@gmail.com>
***
<!-- Resim ekleme -->
#### Resim ekleme
Sayfaya resim ekleme syntaxı şekildeki gibidir
> ![Text](resim urlsi)

![Resim](https://images.pexels.com/photos/11789773/pexels-photo-11789773.jpeg?cs=srgb&dl=pexels-yuliia-tretynychenko-11789773.jpg&fm=jpg)

---
<!-- Tablo oluşturma -->
####  Tablo oluşturma
Sayfaya tablo ekleme syntaxı şekildeki gibidir

> |Sütun Adı | Sütun Adı |

> |--- |--- |

> |Sütunun değeri|Sütunun değeri|

Bu şekilde istediğimiz sütun ve satırdan oluşan tablolar oluşturabiliriz.

|Ad | Soyad |Okuduğu üniversite|Okuduğu bölüm|
|--- |--- |---|---|
|Eyüp|Duran|Pamukkale Üniversitesi|Bilgisayar Mühendisliği|



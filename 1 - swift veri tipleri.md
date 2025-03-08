# swift veri tipleri
<br/>
selamlar, bu yazida veri tiplerinden bahsedecegim.

<br/><br/><br/>


![data types](https://github.com/user-attachments/assets/451c1413-0785-455d-b95f-81a9fb1bc43f)

<br/><br/><br/><br/>


## 1. sayisal veri tipleri

- Int -> tam sayilar icin kullanilir

```
var age: Int = 25
```

- UInt -> negatif olmayan tam sayilar icin kullanilir

```
var count: UInt = 100
```

- Double -> ondalikli sayilar icin kullanilir (64 bit)

```
var precisePi: Double = 3.1415926535
```

- Float -> ondalikli sayilar icin kullanilir (32 bit)

```
var pi: Float = 3.14
```

<br/>

## 2. metin ve karakter veri tipleri

- String -> metinleri saklamak icin kullanilir

```
var name: String = "John"
```
- Character -> tek bir karakteri saklamak icin kullanilir

```
var letter: Character = "A"
```

<br/>

## 3. boolean (mantiksal) veri tipi

- Bool -> true ya da false degerini tutar

```
var isSwiftFun: Bool = true
```

<br/>

## 4. collection veri tipleri

- Array -> aynı turde birden fazla ögeyi iceren collection veri tipi

```
var numbers: [Int] = [1, 2, 3, 4, 5]
// ya da
var numbers = [1, 2, 3, 4, 5]
```

- Set -> benzersiz ögeleri tutan ve sirasiz olan collection veri tipi

```
var uniqueNumbers: Set<Int> = [1, 2, 3, 4, 5]
```

- Dictionary -> anahtar-deger ciftlerini saklayan collection veri tipi

```
var user: [String: String] = ["name": "John", "age": "25"]
```

<br/>

## 5. optional (opsiyonel) veri tipi

- Optional(?) -> bir degiskenin nil (bos) olabilecegini gosterir

```
var optionalNumber: Int? = nil
optionalNumber = 42
```

<br/>

## 6. tuples (demetler)

- birden fazla farkli veri turunu bir arada tutar


```
var person: (name: String, age: Int) = ("Alice", 30)
print(person.name) // Alice
```

<br/>

## 7. Any, AnyObject ve Nil

- Any -> her turden veri icerebilir

```
var anything: Any = "Swift"
anything = 42
```

- AnyObject -> sadece ssnif turleri (class) icin kullanilir
- nil -> bir degiskenin bos oldugunu belirtir (sadece optional lar için gecerlidir)

<br/><br/>
---
<br/><br/>

- bazı programlama dillerinde bir degisken tanimladigimizda tipini belirtmek zorunda oluruz. yani String bir degisken tanimladigimizda basina String yazariz. biz yukaridaki orneklerde bu tipleri belirttik ama aslında swiffte bu zorunlu degildir. hatta tavsiye edilmez. swift te tip kontrolü runtime da yapilir.

```
var greeting = "hello, mobile developers!"
```
bu sekilde degisken tanimliyoruz.

<br/>

- degiskenleri `var` ile sabitleri de `let` ile tanımlıyoruz. 

<br/>

- örnegin bir degisken olusturacagiz ve ici bos kalsin istiyoruz icine herhangi bir deger atamayacagiz boyle bir durumda sadece tipini belirtmemiz yeterli. su sekilde:

```
var blank: String
// ya da bos sabit olusturmak istersek:
let blank : Int
```

<br/><br/>

## collection veri tipine kısa bir bakis 

<br/>

şimdi sırasıyla boş array, set ve dictionary tanimlamanın nasıl yapildigina bakalim. 

<br/>

- boş bir array tanimlamanin 5 farkli yolu vardir:

```
var numbers: [Int] = []        // tür belirterek boş array tanimlama (boş ama nil degil)
var numbers = Array<Int>()     // Array() initializer ile boş array tanimlama (boş ama nil degil)
var numbers = [Int]()          // [] kullanarak kisa tanimlama (en yaygin) (boş ama nil degil)
var array: [Int]? = []         // optional boş array tanimlama (başlangicta boş ama ileride nil olabilir)
var array: [Int]? = nil        // optional boş array tanimlama (bu, ilk başta nil olan ama daha sonra deger atanabilen bir array olusturur)

```
<br/>

![bos array](https://github.com/user-attachments/assets/74c0fdf5-b002-4ad4-9731-b8206ea1808b)

<br/>

- boş bir set tanimlamanin 5 farkli yolu vardir:

```
var numbers: Set<Int> = []             // tür belirterek boş set tanimlama (boş ama nil degil)
var numbers = Set<Int>()               // Set() initializer ile boş set tanimlama (boş ama nil degil) (en yaygin)
var numbers: Set<Int>? = []            // optional boş set tanimlama (başlangicta boş ama ileride nil olabilir)
var numbers: Set<Int>? = nil           // optional boş set tanimlama (bu, ilk başta nil olan ama daha sonra deger atanabilen bir set olusturur)

```
<br/>

![bos set](https://github.com/user-attachments/assets/1485a21d-0c52-4d3d-acd2-4ea6fa97f9c8)

![bos set 2](https://github.com/user-attachments/assets/f374d316-6bf3-4270-8e1d-58660c3c105e)


<br/>

tablodan da anlasildigi uzere bir set in baslangicta ya da daha sonradan nil olabilmesi icin kesinlikle optional kullanmaliyiz.

<br/>

- boş bir dictionary tanimlamanin 4 farkli yolu vardir:

```
var userInfo: [String: Int] = [:]              // tür belirterek boş dictionary tanimlama
var userInfo = Dictionary<String, Int>()       // Dictionary() initializer ile boş dictionary tanimlama
var userInfo = [String: Int]()                 // [:] kullanarak kisa tanimlama (en yaygin)
var userInfo: [String: Int]? = nil             // optional boş dictionay tanimlama (bu, ilk başta nil olan ama daha sonra deger atanabilen bir dictionary olusturur)

```

<br/>

![bos dictionary](https://github.com/user-attachments/assets/1767c48b-d8fb-413e-84ed-7ac334d3793b)

<br/>


<br/><br/><br/><br/><br/><br/><br/><br/><br/>

- collection bir veri tipi olusturmak istiyorsak köseli parantezleri kullaniyoruz. dizi icinde tutulacak deger tipini koseli parantezler arasina yazmamiz tanimlama icin yeterli. eger dizi tanimlamasi sirasinda deger atamasi da yapiyorsak tip atamamiza gerek yoktur. dictionary icin ise anahtar-deger tiplerini koseli parantez icinde yaziyoruz. anahtar ve degerler iki nokta ust uste ile birbirinden ayriliyor. 

```
var shoppingList: [String] = []
var shoppingList = ["water", "bread", "tomato"]

var constantNumbers: [String: Int] = [:]
var constantNumbers = ["pi": 3.14, "gForce": 9.8]
```


<br/>


var helloWorld = Set<String>()
var emptyDictionary: [String: Float] = [:]



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

- Array -> aynı turde birden fazla ögeyi iceren diziler

```
var numbers: [Int] = [1, 2, 3, 4, 5]
```

- Set -> benzersiz ögeleri tutan ve sirasiz olan koleksiyon

```
var uniqueNumbers: Set<Int> = [1, 2, 3, 4, 5]
```

- Dictionary -> anahtar-deger ciftlerini saklayan veri tipi

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

bazı programlama dillerinde tip vardır yani String bir degisken tanimladigimizda basina String yazariz ama swiftte bu zorunlu degildir. swiftte tip kontrolü runtime da yapilir.

```
var greeting = "hello, mobile developers!"
```
bu sekilde tipini belirtmeden degisken tanımlayabiliriz. tipini belirtebiliriz de ama tavsiye edilmez.

<br/>

degiskenleri `var` ile sabitleri de `let` ile tanımlıyoruz. 

<br/>



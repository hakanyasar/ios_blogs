
# collection

<br/>

şimdi sırasıyla boş array, set ve dictionary tanimlamanın nasıl yapildigina bakalim. 

<br/>

- boş bir array tanimlamanin 5 farkli yolu vardir:

```
var numbers: [Int] = []        // tür belirterek boş array tanimlama (boş ama nil degil)
var numbers = Array<Int>()     // Array() initializer ile boş array tanimlama (boş ama nil degil)
var numbers = [Int]()          // [] kullanarak kisa tanimlama (en yaygin) (boş ama nil degil)
var array: [Int]? = []         // optional boş array tanimlama (başlangicta boş yani nil degil ama ileride nil olabilir)
var array: [Int]? = nil        // optional boş array tanimlama (bu, ilk başta nil olan ama daha sonra deger atanabilen bir array olusturur)

```
<br/>

![bos array](https://github.com/user-attachments/assets/74c0fdf5-b002-4ad4-9731-b8206ea1808b)

<br/>

- boş bir set tanimlamanin 4 farkli yolu vardir:

```
var numbers: Set<Int> = []             // tür belirterek boş set tanimlama (boş ama nil degil)
var numbers = Set<Int>()               // Set() initializer ile boş set tanimlama (boş ama nil degil) (en yaygin)
var numbers: Set<Int>? = []            // optional boş set tanimlama (başlangicta boş yani nil degil ama ileride nil olabilir)
var numbers: Set<Int>? = nil           // optional boş set tanimlama (bu, ilk başta nil olan ama daha sonra deger atanabilen bir set olusturur)

```
<br/>

![bos set](https://github.com/user-attachments/assets/1485a21d-0c52-4d3d-acd2-4ea6fa97f9c8)

<br/>

tablodan da anlasildigi uzere bir set in baslangicta ya da daha sonradan nil olabilmesi icin kesinlikle optional kullanmaliyiz. tabloda 2. satirda : yerine = olması lazım. chatgpt hatali yazmis orada.

<br/>

- boş bir dictionary tanimlamanin 5 farkli yolu vardir:

```
var userInfo: [String: Int] = [:]              // tür belirterek boş dictionary tanimlama
var userInfo = Dictionary<String, Int>()       // Dictionary() initializer ile boş dictionary tanimlama
var userInfo = [String: Int]()                 // [:] kullanarak kisa tanimlama (en yaygin)
var userInfo: [String: Int]? = nil             // optional boş dictionay tanimlama (bu, ilk başta nil olan ama daha sonra deger atanabilen bir dictionary olusturur)
var userInfo: [String: Int]? = [:]             // optional boş dictionay tanimlama (başlangicta boş yani nil degil ama ileride nil olabilir)

```

<br/>

![bos dictionary](https://github.com/user-attachments/assets/1767c48b-d8fb-413e-84ed-7ac334d3793b)

<br/>


<br/>

---

<br/>

- goruldugu gibi collection bir veri tipi olusturmak istiyorsak köseli parantezleri kullaniyoruz. dizi icinde tutulacak deger tipini koseli parantezler arasina yazmamiz tanimlama icin yeterli. eger dizi tanimlamasi sirasinda deger atamasi da yapiyorsak tip atamamiza gerek yoktur. dictionary icin ise anahtar-deger tiplerini koseli parantez icinde yaziyoruz. anahtar ve degerler iki nokta ust uste ile birbirinden ayriliyor. 

```
var shoppingList: [String] = []
var shoppingList = ["water", "bread", "tomato"]

var constantNumbers: [String: Int] = [:]
var constantNumbers = ["pi": 3.14, "gForce": 9.8]
```

<br/><br/><br/>


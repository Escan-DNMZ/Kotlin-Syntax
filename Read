# Kotlin Temelleri

## Veri tiplerini değiştirme

```kotlin
//İnt dan String
int myNumber = 5
myNumber.toString()
				.toInt()
				.toLong()
//Gibi kullanımları bulunmakta
				
```

## Null değer verme

```kotlin
var myAge: Int? = null
println(myAge)
//Artık int bir null
//peki ben null bir değer ile 10 sayısını çarpabilirmiyim
println(myAge!! * 10) 
/*Artık dedikki myAge kesin bir değer alıcak şuan null ama bir yerden
değer çekicek dedik*/
```

## Güvenli Kodlar

> Güvenli kodlar programımızın çökmesini engeller ve kullanıcıya bir bildiride bulunur buyüzden çok önemlidir
> 

```kotlin
// 1.metot Null Safety
var myAge: Int? = null
println(myAge)
if(myAge != null){ //Eğer myAge doluysa
 println(myAge * 10) //10 ile çarp
}
else{ //Değil ise myAge null yazdır
	println("myAge null")
}
//2.metot elvis
val myResult = myAge.compareTo(2) //myResult u myAge eşitler fakat
// myAge null ise hata verir bunu şöyle engelleyebilirsin
println(myResult)

val myResult = myAge.compareTo(2) ?: -100 //Eğer myAge null ise değeri
// -100 ile eşitler
```

---

## Collections

### Array

```kotlin
val myArray = arrayOf("James","Kirk","Rob") //Tanımladığımız elemanın türünü belirler
println(myArray[0])//James bize getirir 1.Yol
println(myArray.get(0)) //2.Yol

val intArray = intArrayOf(0) //Maksimum 10 adet eleman alabilir
println(intArray[0])//0 bize çağır 1.Yol
println(intArray.get(0))// 2. Yol

val stringArray = arrayOf("")//Maksimum 10 adet eleman gelebilir
println(stringArray[0])//  bize getirir 1.Yol
println(stringArray.get(0))//2.Yol

val doubleArray = doubleArrayOf(1.0)//Makismum 10 eleman gelebilir
println(doubleArray[0])//1.0 ı bize getirir 1.Yol
println(doubleArray.get(0))// 2.Yol

//Eğer elemanları değiştirmek istersek
myArray[0] = "James Hartfield"
myArray.set(0) = "Escan"

//Array eleman ekleme
var myArray = arrayof(0)//int değer oluşturabiiyoruz ilk eleman 0
myArray.set(1,8)//ikinci değeri atadık
myArray.set(2,34)// 3. değeri atadık
myArray.set(3,19)// 4. değeri atadık
myArray.set(4,26)// 5. değeri atadık
myArray.set(5,31)// 6. değeri atadık
myArray.set(6,-5)// 7. değeri atadık
myArray.set(7,78)// 8. değeri atadık

```

### Listeler

```kotlin
val myMusician = ArrayList<string>() //String bir liste oluşturduk
myMusician.add("Escan") //Listemize Escan elemanını ekler
println(myMusician[0])

val myMixedArrayList = ArrayList<Any>() //Herhangi bir türden veri atabilirsiniz
myMixedArrayList.add("Escan")
myMixedArrayList.add(250)
myMixedArrayList.add(true)

println(myMixedArrayList[0])
println(myMixedArrayList[1])
println(myMixedArrayList[2])
```

### Setleme

> Setler içerisinde 1 eleman birden fazla kez kullanılamaz
> 

```kotlin
val mySet = setOf<int>(2,3,4,1)

mySet.foEach{println(it)} // Tek tek değerleri it değişkenine atar ve yazdırır
```

### HashSet

> HashSet de parantez içine eleman yazdırılmak yerine add komutuyla eklenir. Aynı elemanlardan 1 defa ekler
> 

```kotlin
val hSet = HashSet<String>()
        hSet.add("Yunus")
        hSet.add("Yunus")
        hSet.add("Yunus")
        hSet.add("Yavuz")
        hSet.forEach() {
             println(it)
					} 
println(hSet) 
// out put: Yunus
//Yavuz

//Tek bir set çekmek istersek

 var put = hSet.elementAt(2) // bu şekilde 3. indexi seçeriz
println("3. index in değeri ${put}")//bu şekilde de yazdırırız
```

### HashMap

> Bize dizileri yada verileri birbiriyle eşleştirme imkanı sunuyor bunun anlamı ise Key - Value dur
> 

```kotlin
val fruitCaloriMap = hashMapOf<String,int>()
fruitCaloriMap.put("Apple",150) //Elma elemanı eklenir ve buna 150 sayısı value olarak tanır
println(fruitCaloriMap["Apple"]) //Elmayı yazdırır
```

---

# When

> Eğer çok fazla else ifiniz var ise kullanılır
> 

```kotlin
var day = 3
var dayString = ""

if(day == 1){
	dayString = "Monday"
}
else if(day == 2){
	 dayString="Tuesday"
}
else if(day == 3){
	 dayString="Wednessday"
}
println(dayString)

//When ile kullanımı
var day = 3
var dayString = ""

when(day){ //değer ... olduğu zaman
1-> dayString = "Monday" //day 1 olduğu zaman
2-> dayString = "Tuesday"
3-> dayString = "Wednessday"
else -> daystring ="" //Değer yok ise
}
println(dayString)
```

---

# Döngüler

## For

> For Kotlinde c# daki Foreach görevini görüyor
> 

```kotlin

var myArrayOfNumbers = arrayOf("12","23","32","65")
for(number in myArrayOfNumbers){
		val z = number / 3*5
		println(z)
}

//Bir diğer kullanım

for(z in 0..3){ //0 dan 3 e kadar sıralar
		println(z)
}

//Tabiki bunun yerine bunu da kullanabilirsiniz
myArrayOfNumbers.forEach{
 println(it)
}
```

## While

> Kotlinde While C# daki for ile eşdeğer
> 

```kotlin
var i = 0
while(i<10){
	i++
	println(i)
}
```

---

# Fonksiyonlar

> Fonksiyonlar c# daki metotlar ile eşdeğer dir Not: c# daki Void kotlindeki Unit e eşdeğerdir
> 

```kotlin
fun mySum(a: Int,b: Int){ //Burda int değerde bir parametre istiyoruz
	println(a+b)
}
//Sonrasında bunları onCreate da kullanıyoruz
mySum(a:20,b:10) //burda parametreyi giriyoruz

```

### Peki bunu emulatör de gösterebilirmiyiz ?

> Öncelikle Layout umuzda bir TextView oluşturuyor ve onun id sini alıyoruz.
> 

```kotlin
fun mySum(a:Int,b:Int){
 textView.text = "${a+b}" //text içerisinde yanlızca string değer atanabilir
//biz burda int değeri stringe çevirdik
}
//Sonrasında bunları onCreate da kullanıyoruz
mySum(a:20,b:10)

//Artık emülatör açıldığında 30 sayımızı textView de göstericek

//NOT: daha herhangi bir şey döndürmediği için bize Unit vericekdir
//void - Unit
```

### Return (Fonksiyon döndürme)

> Eğer ben bir fonksiyonu başka bir değişkene atamak istiyorsam zorunlu olarak o fonksiyonu geriye döndürülebilir kılmalıyım
> 

```kotlin
//Burda yaptığımız : Int anlamı Int bir değer döndürceğiz demek
fun myMultiply(x:Int,y:Int): Int {
	return x * y
}

//onCreate
val result = myMultiply(a:10,b:5)
textView.text = result.toString()
```

### Görünümler ve Fonksiyonlar

```kotlin
/*view: View anlamı bir görünüm tarafından kullanılacak bir fonksiyon
Fonksiyonu farklı bir fonksiyonda kullanmamıza gerek yok çünkü zaten Layout 
da kullanıyoruz */
fun clicked(view: View){ //clicked button un onClick id si
    button.setOnClickListener{
        println("bana tıkladın"),
				}
    }
```

---

# OOP

## **Sınıf(Class)**

> Sınıflar nesne özelliklerine sahip değişken ve metodların bulunduğu yapılardır. Sınıflar nesne tabanlı programlama kullanan her programlama dilinde kullanılabilir. Sınıf ile nesne aynı yapılar değildir. Sınıf nesne özelliklerini tutan soyut (abstract) ifadelerdir.  Sınıf ve nesne birbirine bağlıdır ama aynı kavramlar değildir. Bunu unutmamak gerekir.
> 

## Constructor

> Sınıf çağırıldıkdan sonra oluşturulacak herhangi bir nesne için constructor çağrılır. Aynı şekilde bir sınıfın isteklerini meslse AgeInput veya NameInput
> 

```kotlin
constructor(ageInput: Int, nameInput: String, jobInput: String){
	this.age = ageInput /*ageInput class objesi oluşturulurken iste
ve bunu age ile eşitle */
this.name = nameInput
this.job = jobInput
//this içinde bulunduğu sınıfa veya bir üst seviyeye referans verir
}

/*Bundan sonra class dan obje çekildiği zaman değerleri parametre
üzerinden vermelisiniz*/

var homer = Simpson(ageInput: 50,nameInput:"Homer Simpson",jobinput"Nuclear")

**//Daha basit bir kullanım ise** 

class Simpson(var name:String,var age:Int,var job:String) {

}

//MainActivity

var sim = Sipmson(name="Escan",age="15",job="student")
//şeklinde de kullanabilirsiniz
```

## Access Modifier

1. **private = sadece tanımlandığı sınıf içerisinde kullanılabilir**
2. **protected = private gibi sadece kalıtım aldığımız sınıfda da kullanılabilir**
3. **internal = bütün projeden ulaşılır sadece bazı modüllerde ulaşılamaz**
4. **public = her yerden ulaşılabilir**

```kotlin
//Örnek classımız üzerrinden gidicem
class Simpson(var name:String,var age:Int,var job:String) {
	private var hairColor = "" 
}

//MainActivity

var homer = Simpson(ageInput: 50,nameInput:"Homer Simpson",jobinput"Nuclear")

homer.hairColor = "yeşil" //Artık bunu kullanamayız bize hata vericekdir
```

Peki biz bunu Private kullanmak isteseydik nasıl kullanırdık

```kotlin
//Örnek classımız üzerrinden gidicem
class Simpson(var name:String,var age:Int,var job:String) {
	private var hairColor = "" 

	fun changeHairColor(){
	this.hairColor = "yellow"
}
}

//MainActivity

var homer = Simpson(ageInput: 50,nameInput:"Homer Simpson",jobinput"Nuclear")
homer.changeHairColor() //fonksionumuz public olduğu için onu kullanabildik
```

### Getter,Setter (Accees Modifier)

```kotlin
class Musician(name: String, instrument: String, age: Int) {

    //encapsulation
//Burda name i değiştiremeyiz fakat çağırabiliriz james.name.ToString() gibi
    var name : String? = name
        private set
        get

    private var instrument : String? = instrument

//Burda age i değiştiremeyiz fakat çağırabiliriz james.age.ToString() gibi
    var age : Int? = age
				get
				// age in değiştirilmesi sadece sınıf içerisinde geçerli olur
				private set
        
}
```

## Inheritence

```kotlin

//Biz bunu bir class a kalıtım olarak eklemek istediğimizde Musician ımıza open belirteci ekler
open class Musician(name:String,age:Int){

		var name:String? = name

		var age:Int? = age
}

class SuperMusician(name: String,  age: Int) : Musician(name, age) {

    fun sing() {
				var lars = SuperMusician("Ahmet",22) // Artık Musician ı Super Musician da kullanabilirim
        printin("nothing else matters")
				}
}
```

## Polymorphism

> Aynı sınıf içerisinde aynı ismi kullanan metotları veya fonksiyonları kullanma
> 

### Static Polymorphism

```kotlin
class Mathematics {

    fun sum() : Int {
        return 0
		}

    fun sum(x : Int, y: Int) : Int {
        return x + y
		}

    fun sum (x: Int, y:Int, z: Int): Int{
				return x+y+z
		}
}

//MainActivity
//Bu şekilde kullanabilirim 
var mathematic = Mathematics()
println(mathematic.sum(10)
println(mathematic.sum(10,20))
println(mathematic.sum(10,20,30))
```

### Dynamic Polymorphism

```kotlin
open class animal{
	open fun sing(){
		println("animal class")
	}
}

class Dog: Animal{
//Sing fonksiyonumuzun üzerine yazdık yani Dog çağrıldığında Dog class gelicek
	override fun sing(){
		println("Dog class")
	}
//super kalıtım aldığımız sınıfa referans verir
	fun test(){
	//Burda çağırdığımız sin animal class ındaki olucak
		super.sing()
	}
	
}

//MainActivity
val animal = Animal()
animal.sing()

val barley = Dog()
//Aslında animal.sing() in aynı çıktısını vericek
barley.test()
//override edilmiş fonskiyonu getiricek
barley.sing()
```

## Abstract

Abstarct bizim bir obje oluşturamayacğımız bir sınıftır genelde kalıtım olarak alınması için kullanılır örnek Animal,People veya Generic gibi kullanılırlar Interface den farkı sadece tek bir class kalıtım alabilir

```kotlin
abstract class People{

		fun information():String {
			return "We are people"
		}
}

class User: People{
		 fun test():String{
				return "Me To"
			}
}

//MainActivty

//Diyerek We are people yazdırabilirsiniz
println(myUser.information());

//Fakat interface veya abstract bir class ı çağıramazsınız
println(People.informatin()); //Hata verir
```

## Interface

> Abstract  ile aynı işe yarar artı olarak istediğiniz kadar kalıtım aldırabilirsiniz
> 

```kotlin
interface HouseDecor{
	var roomName:String
}

interface Insturment{
	fun info(){
		println("instrument info")
	}
}

class Piano: HouseDecor, Insturment{
	var brand: String? = null
	var digital: Boolean? = null

	override var roomName:String
		get() = "Kitchen"
		set(){}
}

//MainActivty
var myPiano = Piano()
myPiano.brand ="Yamaha"
myPiano.digital = false
println(myPiano.roomName)
myPiano.Info()
```

---

# Lambda

Örnek 1:

```kotlin
fun printString(myString:String){
	println(mystring)
}
printString("My Test String")
//Bunu tek satırda yazamazmıyım Lambda ile yazarsın

//Bu şekilde tek satırda yazabilirsin
val testString = {myString: String -> println(myString)}
testString("My Lambda String")
```

Örnek 2:

```kotlin
val multiplyLambda = {a:Int,b:Int -> a * b}
println(multiplyLambda(5,10))

//Bir diğer kullanımı

//Bu şekilde de kullanılabilir
val multiplyLambda2:(Int,Int) -> Int = {a,b -> a*b} 
println(multiplyLambda2(5,10))
```

# İleri Seviye Lambda

## Asynchrnous (Asenkron) (Completion)

Bir işlem yaparken uygulamamızı dondurmaz ve başka bir işlem yapmaya izin verir diyelimki internetten veri çekerken uygulamamızı dondurmaz

```kotlin
//Musician sınıfından Unit döndür
fun Download(url:String, completion: (Musician) -> Unit){
//Yükleme yapıldıktan sonra çağır
val kirkHamet = Musician("Kirk","Guitar",60)
	completion(kirkHamet)
}

Download("escan.com",{musician ->
		println(musician.name)
})
```

---

# Synthetic Binding

> Öncelikle Görseller ile oynama yapmadan önce ufak bir ayarlama yapmalıyız proje ayarlarımızdan Gradle Scripts>Build.gradle 2. sıradakine tıklayın ardından şu kodları yazın
> 

```kotlin
// Bu kodu silip onun yerine
plugins{
	id 'com.android.application'
	id 'kotlin-andorid'
}
//Bu kodu ekleyin
apply plugin: 'com.android.application'
apply plugin: 'kotlin-android'
apply plugin: 'kotlin-android-extensions'
```

```kotlin
fun clicked(){
textView.text = "Merhaba"
}
//Artık bu şekilde çok kolay bir şekilde görseller ile oynayabiliriz
```

- Eğer biz yukarıdaki ayarlamaları yapmasayadık mecburen bir TextView işlemi yaparken bile id yi bulmamız gerekicekdi örnek:

```kotlin
fun clicked(){
val textView = FindViewById<TextView>(R.id.text)
textView.text = "Merhaba"
}
```

<aside>
💡 Sizinde anlıyacağınız gibi yukarıdaki ayarlamaları yapmak sizin için çok daha kolay olucakdır

</aside>

---

# Android View Binding

Kaynak: [https://developer.android.com/topic/libraries/view-binding](https://developer.android.com/topic/libraries/view-binding)

> Öncelikle ViewBinding i aktif etmeliyiz öncelikle aynı işlemleri birdaha yapalım Gradle Scripts>Build.gradle 2. sıradakine tıklayın ardından şu kodları yazın
> 

```kotlin
//Öncelikle burda ufak bir değişiklik yapıcaz
android{
	compileSdkVersion 30
  buildToolsVersin "30.0.2"

	defaultConfig {
    applicationId "com.escan.viewbindingkotlin"
    minsdkversiori 23
    targetSdkversion 30
    versionCode 1
    versionName "1.0"
    testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
		}

	buildTypes {
    release {
        minifyEnabled false
        proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'

compileOptions {
    sourceCompatibility JavaVersion. VERSION_1_8
    targetCompatibility Javaversion. VERSION_1_8

kotlinOptions {
    jvmTarget = '1.8'

//Buraya Android in en altına

buildFeatures {
        viewBinding true
    }
}
```

> Bu işlemleri yaptıktan sonra Build>ReBuild yaparak kotlin in bize hazır class ları kurmasını sağlayabiliriz fakta ekstra olarak birkaç değişken oluşturmalısınız
> 

```kotlin
//lateinit = geç başlatmaya yarıyor sen başlatana kadar bellek yemiyor
private lateinit var binding: ActivityMainBinding 
//ActivityMaingBindin ise proje admızın import kısmından bakabilirsiniz
import com.escan.viewbindingkotlin.databinding.ActivityMainBinding

/*Bundan sonra program projenizi bir kerelik aşağıdaki ayarlar ile 
çalıştırmanızı istiyor*/
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
		//Proje adınızı girmeyi unutmayın
    binding = ActivityMainBinding.inflate(layoutInflater)
    val view = binding.root //Layout ile çalışacağımız belirtiyor
    setContentView(view)
}

//Artık bu şekilde kullanabilirsiniz
fun isimDegis(view:View){
	binding.textView.text = "Merhaba"
}

```

---

# Data Binding

> Gradle Scripts>Build.gradle 2. sıradakine tıklayın ardından şu kodları yazın
> 

```kotlin
android{
	compileSdkVersion 30

	//Buraya Android in en altına

	buildFeatures {
        dataBinding true
    }

  buildToolsVersin "30.0.2"

	defaultConfig {
    applicationId "com.escan.viewbindingkotlin"
    minsdkversiori 23
    targetSdkversion 30
    versionCode 1
    versionName "1.0"
    testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
		}

	buildTypes {
    release {
        minifyEnabled false
        proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'

compileOptions {
    sourceCompatibility JavaVersion. VERSION_1_8
    targetCompatibility Javaversion. VERSION_1_8

kotlinOptions {
    jvmTarget = '1.8'
}
```

> Bu işlemleri yaptıktan sonra Build>ReBuild yaparak kotlin in bize hazır class ları kurmasını sağlayabiliriz sonrasında xml imize gelip Layour umuzun üstüne birdaha Layout oluşturmalıyız
> 

```xml
<Layout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="132dp"
        android:text="TextView"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
</Layout>
```

> Peki Activity mizde buna nasıl ulaşıcaz
> 

```kotlin
private lateinit var binding: ActivityMainBinding 

override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    binding = DataBindingUtil.setContentView(this,R.layout.activity_main)
}

//Artık bu şekilde kullanabilirsiniz
fun isimDegis(view:View){
	binding.textView.text = "Merhaba"
}

```

---

# Scope

> Diyelim ki bir fonksiyonda oluşturduğumuz değişkenlerimiz olsun bunları farklı bir fonksiyonda nasıl kullanırız ?
> 

```kotlin
// Bunun için birkaç fonksiyonda kullanacağınız değişkenleri 
// MainActivity nin bir altına tanımlamanız gerek

fun clicked(view: View){
        val name = binding.Name.text.toString() //Kullanıcının girdiği değerleri aldık
        val age = binding.Age.text.toString().toIntOrNull()
        val job = binding.Job.text.toString()
}
//Eğer bu şekilde çağırmak istersek bize hata verir
fun scopeExample(view:View){
	println(name)
}

//Olması gereken 

class MainActivity : AppCompatActivity() {

//Name,age,job değişkenelerimi burda tanımlıyıcam
		var name = ""
		var job = ""

    private lateinit var binding: ActivityMainBinding

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        binding = ActivityMainBinding.inflate(layoutInflater)
        val view = binding.root
        setContentView(view)
    }

    fun clicked(view: View){
        name = binding.Name.text.toString() //Kullanıcının girdiği değerleri aldık
       var age = binding.Age.text.toString().toIntOrNull()
	       job = binding.Job.text.toString()
    }
		// Artık burda name çağırabilirsiniz clicked butonu yerine scopeExample a basarsak
		// konsola name i yazdıracakdır
		fun scopeExample(view:View){
			println(name)
		}
}
```

---

# Veri Saklamak(Küçük boyutlar)

## Shared Preferences

### Veri Okumak ve Veri Kaydetmek

> Küçük verileri Telefonda saklamak örneğin bir kişi hesap makinesinde bir işlem yapıyor ardından yanlışlıkla sonucu siliyor veya uygulamadan çıkıyor burada bu sonucun kaybolmaması için bir bellekte Telefon hafızasında tutmalıyız
> 

```kotlin
class MainActivity : AppCompatActivity() {

		//uygulama açıldığında saklı olan veriyi getirmek için
// bunu onCreate de de kullanmam lazım buyüzedn sharedPreferences ı burda aoluşturuyorum
    lateinit var sharedPreferences: SharedPreferences
		var ageFromPreferences : Int? = null

   **** override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        //İlk parametrede  verilerin cihazımızda hangi isimle tutulacağını yazıyoruz. 
//Mesela ben com.escan.verisaklamak kullandım. İkinci değer’e ise Context.MODE_PRIVATE yazıyoruz, 
//bunu yazmamızın sebebi dışarıdan erişilmesini engellemek ve güvenli hale getirmek.
        sharedPreferences = this.getSharedPreferences("com.escan.verisaklamak",
            Context.MODE_PRIVATE)
				//birinci parametreye sakladığımız key’in adını,
				// ikinci parametreye ise eğer öyle bir key yoksa geriye döndüreceği 
				//default değeri yazıyoruz.
				//Veri okuma kısmı
        ageFromPreferences = sharedPreferences.getInt("Age",0)
        if (ageFromPreferences == 0){
            textView.text = "YourAge:"
        }
        else{
            textView.text = "YourAge:${ageFromPreferences}"
        }
    }
    //EditText
    fun Save(view: View){
       var dataAge = EditText.text.toString().toInt()
        textView.text = "Your age: ${dataAge}"
        sharedPreferences.edit().putInt("Age",dataAge).apply()
    }

}
```

### Verileri silmek

```kotlin
class MainActivity : AppCompatActivity() {

    lateinit var sharedPreferences: SharedPreferences
		var ageFromPreferences : Int? = null

   **** override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        sharedPreferences = this.getSharedPreferences("com.escan.verisaklamak",
            Context.MODE_PRIVATE)
	
        ageFromPreferences = sharedPreferences.getInt("Age",0)
        if (ageFromPreferences == 0){
            textView.text = "YourAge:"
        }
        else{
            textView.text = "YourAge:${ageFromPreferences}"
        }
    }
    //EditText
    fun Delete(view: View){
       ageFromPreferences = sharedPreferences.getInt("Age",-1)

				if (ageFromPreferences != -1){
						sharedPreferences.edit().remove("Age").apply()
            textView.text="Your age"
			   }

}
```

---

# Intent (Farklı ekranlar ekleme)

> Öncelikle  intent bir Activity dir app>java>com.escan.ProjeAdı>sağ tıklayın>New>Activity>Galery>Görünüm seç ve aktar artık ikinci bir sayfamız oldu isterseniz tekrardan farklı bir tasarım verebilirsiniz veya o sayfaya özel kodlarınızı yazabilirsiniz peki ben bir butona basınca nasıl sayfa değiştiricem ?
> 

```kotlin

//Sayfa1 de yazdığımız kod
fun clicked(view: View){
//Sayfa2 = MainActivity2
        val intent = Intent(applicationContext,MainActivity2::class.java)
        startActivity(intent)
    }
//Buton = clicked
```

## Verileri 2. ekrana aktarma

```kotlin

    fun clicked(view: View){
        val intent = Intent(applicationContext,MainActivity2::class.java)
				//name keyi ile Name id sindde verilen değeri yolladık
        intent.putExtra("name",Name.text.toString())
		    //surname keyi ile Surname id sinde verilen değeri yolladık
        intent.putExtra("surname",Surname.text.toString())
        startActivity(intent)
    }

//Bunu diğer sayfada tutmak için
//Sayfa2

class MainActivity2 : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main2)

        //Sayfa açılırken 1. sayfadan buraya yollanan intentleri tuttuk
        val intent = intent
        val name = intent.getStringExtra("name");
        val surname = intent.getStringExtra("surname");

        textView.text = "${name + surname}"
    }
}
```

---

# Activity Lifecycle

![activity_lifecycle.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dd6a0f66-d158-468d-8fdc-b00cb69fa6a9/activity_lifecycle.png)

> Not: Eğer biz bir Activiteyi kapatmaz isek bu arkada güç harcayacakdır buda uygulamamızın performansını düşürür bunun için finish() ile aktivitelerimizi kapatman bizim için en iyisi olacakdır.
> 

```kotlin
//-----Activity Lifcycle-----//
//Oluşturur
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)
}
//Oluşturulduktan sonra çalışır
override fun onResume() {
        super.onResume()
println("On Resume Called")
}
//Diğer aktiviteye giderken çalışır veya uygulama kapandığında tekrar açıldığında çalışmaz
override fun onPause() {
        super.onPause()
println("On Pause Called")
}
//aktivite çalıştıkdan sonra kendisi çalışır ve  onResume geri dönderir
override fun onStop() {
    super.onStop()
println("On Stop Called")
}
//Activity kapatıldığında verir
override fun onDestroy() {
    super.onDestroy()
println("On Destroy Called")
}
//-----Activity Lifcycle-----//
//Activity başlatıldıkdan sonra kapatılmaz ise uygulama yavaşlar
fun clicked(view: View){
    val intent = Intent(applicationContext,MainActivity2::class.java)
    intent.putExtra("name",Name.text.toString())
    intent.putExtra("surname",Surname.text.toString())
    startActivity(intent)
    //Activity kapatır böylelikle bize performans sağlar
    finish()
}
```

---

# Google Play’e yüklemek

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/946d77a0-6b19-4d50-83ea-dd97934009b1/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4d4edc6f-f9cd-41ae-80e4-50867ae6bb7e/Untitled.png)

> İmzalı apk yükleyin:
> 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/690d321c-c9e2-47ac-960e-9fc920178c89/Untitled.png)

---

# Uyarı Mesajı

```kotlin
class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        Toast.makeText(applicationContext,"Welcome",Toast.LENGTH_LONG).show()
    }
    fun clicked(view:View){
        val alert = AlertDialog.Builder(this)
        alert.setTitle("Save")
        alert.setMessage("Are you sure")
        //Kullanıcı pozitif butona basınca ne yapacak
        alert.setPositiveButton("Yes",){dialog, which ->

            //OnClick listener yes alert ına basıldığı zaman saved yazar
            Toast.makeText(applicationContext,"Saved",Toast.LENGTH_LONG).show()
        }
        alert.setNegativeButton("No"){dialog, which ->

            //OnClick listener yes alert ına basıldığı zaman saved yazar
            Toast.makeText(applicationContext,"Not Saved",Toast.LENGTH_LONG).show()
        }
        alert.show()
    }
}
```

---

# Context Nedir

## Context

## Activity Context → this

> this aktiviteyle ilgili durumlarda kullanılır eğer siz MainActivity e referans vermek isterseniz ve this bunu vermez ise **this@MainActivity** şeklinde kullanabilirsiniz
> 

## App Context  → applicationcontext

> appilcationcontext genel uygulama ile ilgili örnek toast işlemi yaparken applicationcontext kullanabilirsiniz
> 

---

# CountDownTime

```kotlin
class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

    }
    fun clicked(view: View){
        //MyTimer adında bir obje oluştur bu CountDownTimer dan kalıtım alan bir nesne olsun

        object : CountDownTimer(60000,1000){
            //her bir belirtilen periyotda ne olucak
            override fun onTick(p0: Long) {
                textView2.text = "${p0/1000}"

            }
            //işlem bittiğinde ne olucak
            override fun onFinish() {
                textView2.text = "0"

            }

        }.start()

    }
}
```

---

# Kronometre yapımı

```kotlin
class MainActivity : AppCompatActivity() {

    var number = 0
    lateinit var runnable : Runnable
    var handler: Handler = Handler(Looper.getMainLooper())

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
    }
    fun Start(view:View){
        number = 0
        runnable = object:Runnable{
            override fun run() {
                number = number + 1
                textView.text = "$number"

                handler.postDelayed(this,1000)
            }

        }
        handler.post(runnable)
    }

    fun Stop(view:View){
        handler.removeCallbacks(runnable)
        number = 0
        textView.text = "0"
    }
}
```

---

# RecyclerView

> Önce nedir bu recyclerview, ne yapar ondan bahsedelim. Verileri listelemek için kullanılan bir yapıdır. Scroll (kaydırma) işleminin yapılmasını sağlar
> 

## Adapter

> Adapter verileri RecyclerView’e bağlar. Verileri bir ViewHolder içinde görüntülenebilecek şekilde uyarlar. RecyclerView, verilerin ekranda nasıl görüntüleneceğini anlamak için adapter kullanır.
> 

**→ onCreateViewHolder( ):** Adapter oluşturulduğunda ViewHolder’ı başlatıyor.

**→ getItemCount( ):** Listemizin eleman sayısını veriyor.

**→ onBindViewHolder( ) :** onCreateViewHolder’dan dönen verilerin bağlama işlemini gerçekleştiriyor.

## LayoutManager

> Bu nesne RecyclerView’in itemlerini konumlandırır ve ekran dışında geçiş yapan itemlerin ne zaman geri dönüştürüleceğini söyler.
> 

> Default olarak Layout Manager 3 seçenek sunar.
> 

> **→** LinearlayoutManager **:** İtemleri standart ListView şeklinde görünmesini sağlar.
> 

> **→** GridLayoutManager **:** İtemlerin satır ve sütun şeklinde görünmesini sağlar.
> 

> **→** StaggeredGridLayoutManager **:** İtemlerin kademeli satır ve sütun şeklinde görünmesini sağlar.
> 

## ViewHolder (RecyclerView)

> Her itemin içinde bulunan bileşenlerin tanımlama işleminin yapıldığı yerdir.
> 

## Tasarımı oluşturalım (RecyclerView)

1. Öncelikle recycler_row adında bir layout oluşturalım 
2. içerisine CardView imizi veya istediğimiz tasarımı yapalım verilerin bize nasıl gözükmesini istiyorsak ben bir CardView oluşturdum
3. activity_main tasarımımıza recyclerView i atalım ve heigt ve width ine match parent verelim ve contraint ini ekleyelim

## Adapter oluşturma (RecyclerView)

```kotlin
//Ulkeler adında bir data class oluşturulaım
data class Ulkeler(var ulkeNo:String,var ulkeAdi:String){

}

//Adapter adında bir kotlin class oluşturalım

class Adapter(private val context:Context,private val ulkeler:List<Ulkeler>):RecyclerView.Adapter<Adapter.CardViewHolder>{

//inner class iç sınıf anlamına geliyor sınıf içi sınıf oluştururken kullanıyoruz
		inner class CardViewHolder(view:View):RecyclerView.ViewHolder(view){
				var satirCardView: CardView
				var satirYazi:TextView
				var noktaResim:ImageView

				//init yani constructor
				init{
						satirCardView = view.findViewById(R.id.satirCardView)
						satirYazi = view.findViewById(R.id.satirYazi )
						noktaResim = view.findViewById(R.id.noktaResim )
				}
		}

		override fun onCreateViewHolder(parent:ViewGroup,viewType:Int):CardViewHolder{
			var itemView = LayoutInflater.from(context).inflate(R.layout.recycler_row,parent,false)
			return CardViewHolder(itemView)
		}
		override fun onBindViewHolder(holder: CardViewHolder,position:Int){
			val ulke = ulkeler[position]
			holder.satirYazi = ulke.ulkeAdi
			holder.satirCardView.setOnClickListener{
				Toast.makeText(context,"Ülke: ${ulke.ulkeAdi}",Toast.LENGTH_LONG).show(){
			}
		override fun getItemCount():Int{
			return ulkeler.size

		}
}
```

## MainActivity içeriği (RecyclerView)

```kotlin
private lateinit var ulkelerList:ArrayList<Ulkeler>
private lateinit var adapter:Adapter
//onCreate alanı {

	recyclerView.layoutManager = LinearLayoutManager(this)

			val u1 = Ulkeler(1,"Türkiye")
			val u2 = Ulkeler(2,"Almanya")
			val u3 = Ulkeler(3,"ABD")
			val u4 = Ulkeler(4,"Isviçre")

ulkelerList = ArrayList<Ulkeler>()
ulkelerList.add(u1)
ulkelerList.add(u2)
ulkelerList.add(u3)
ulkelerList.add(u4)

		adapter = Adapter(this,ulkelerList)
// }
```

---

# Menu yapımı

> Öncelikle tasarım için Layout dan bir Resource file oluşturalım ardından xml kısmından bu kodlar ile bir menu oluşturlarım xml ile yapmak daha basit olduğundan menu yü xml ile yapmanızı öneririm
> 

```xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">

    <item
        android:id="@+id/add_art"
        android:title="Add Art">

    </item>

</menu>
```

> Bize 3 nokta ya basınca Add Art kutucuğu çıkaran bir menü geldi şimdi bunu nasıl kullanıcaz MainActivity mize gelelim zaten bunlar override edilmesi gereken hazır fonksiyonlar biz burda gelip bunları override ediyoruz
> 

```kotlin
override fun onCreateOptionsMenu(menu: Menu?): Boolean {
        //inflater xml ile activity mizi bağlıcağımız zaman kullanırız
        val menuInflater = menuInflater
        menuInflater.inflate(R.menu.artmenu,menu)
        return super.onCreateOptionsMenu(menu)
    }

override fun onOptionsItemSelected(item: MenuItem): Boolean {
        //item.itemId = Kullanıcının tıkladığı id
        if (item.itemId == R.id.add_art){
            val intent = Intent(MainActivity@this,DetailsActivity::class.java)
            startActivity(intent)
        }
        return super.onOptionsItemSelected(item) //itemi döndür
    }
```

---

# İzin Yönetimi (Permissions)

> Kullanıcıdan erişeceğimiz yelerin iznini almak zorundayız bu uygulamamızın güvenirliğini arttırır bunun için android in kendi sitesinden bunu nasıl yapıcağınıza bakabilirsiniz.
> 

[](https://developer.android.com/reference/android/Manifest.permission)

Bunun için öncelikle protected seviyesi yüksek olan örnek ReadExternalStorage yani kişinin galerisine giriş izni verir bu tarz durumlarda manifests den bunu packages hemen altına eklemeliyiz

```xml
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"></uses-permission>
```

Peki bunu Activity mizde nasıl kullanıcaz işte böyle:

```kotlin
class DetailsActivity : AppCompatActivity() {
    private lateinit var binding: ActivityDetailsBinding
    private lateinit var activityResultLauncher: ActivityResultLauncher<Intent>
    private lateinit var permissionLauncher: ActivityResultLauncher<String>
    var selectedBitmap: Bitmap? = null

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        binding = ActivityDetailsBinding.inflate(layoutInflater)
        val view = binding.root
        setContentView(view)

        registerLauncher()
    }

    fun saved(view: View){

    }
    fun selectImage(view: View){
        //Kullanmamıza izin verdiyse
        if(ContextCompat.checkSelfPermission(this,android.Manifest.permission.READ_EXTERNAL_STORAGE) == PackageManager. PERMISSION_GRANTED){
            //ACTION_PICK ile gidip alıyoruz anlamına geliyor Action larda tüm izinler için farklı kullanımlar var örnek BATTERY_LOW gibi
            // MediaStore.Images.Media.EXTERNAL_CONTENT_URI ise galeri ye gider ve kullanıcının seçtiği fotoğrafı alır
            val intentToGalery = Intent(Intent.ACTION_PICK, MediaStore.Images.Media.EXTERNAL_CONTENT_URI)
            activityResultLauncher.launch(intentToGalery)
        }
        else{
            //Rationale (rasyonel)
                //Kullanıcıya izin alma mantığını göstereyimmi
            if (ActivityCompat.shouldShowRequestPermissionRationale(this,android.Manifest.permission.READ_EXTERNAL_STORAGE)){
                Snackbar.make(view,"Permission needed for gallery",Snackbar.LENGTH_INDEFINITE).setAction("Yes",View.OnClickListener {
                    permissionLauncher.launch(android.Manifest.permission.READ_EXTERNAL_STORAGE)
                }).show()
            }
            else{
                //Request Permission (Kullanıcıdan izin almadan yapar)
                permissionLauncher.launch(android.Manifest.permission.READ_EXTERNAL_STORAGE)
            }
        }
    }
    private fun registerLauncher(){
        activityResultLauncher = registerForActivityResult(ActivityResultContracts.StartActivityForResult()){ result ->

                if (result.resultCode == RESULT_OK){
                    val intentFromResult = result.data
                    if (intentFromResult != null){
                        val imageData = intentFromResult.data

                        if (imageData != null){
                            println("Photos Download")
                            try {
                                if (Build.VERSION.SDK_INT >= 28){
                                    val source = ImageDecoder.createSource(this@DetailsActivity.contentResolver,imageData)
                                    selectedBitmap = ImageDecoder.decodeBitmap(source)
                                    binding.imageView.setImageBitmap(selectedBitmap)
                                }else{
                                    selectedBitmap = MediaStore.Images.Media.getBitmap(contentResolver,imageData)
                                    binding.imageView.setImageBitmap(selectedBitmap)
                                }
                            }catch (e:Exception){
                                e.printStackTrace()
                            }
                        }
                    }
                }
        }
        permissionLauncher = registerForActivityResult(ActivityResultContracts.RequestPermission()){result ->
            if (result){
                //permission Granted
                val intentToGalery = Intent(Intent.ACTION_PICK, MediaStore.Images.Media.EXTERNAL_CONTENT_URI)
                activityResultLauncher.launch(intentToGalery)
            }else{
                //permission Denied
                Toast.makeText(this@DetailsActivity,"Permission Needed",Toast.LENGTH_LONG).show()
            }
        }
    }
}
```

---

# Room Database

> Room aslında Sql Lite ile aynı şey tek fark normal yazdığınız  Sql kodları yerine burda Room kodları yazıyoruz
> 

> Kaynak: [https://developer.android.com/training/data-storage/room](https://developer.android.com/training/data-storage/room)
> 

Öncelikle Gradle ımızda ufak bir ayarlama yapmalıyız Gradle Scripts >2. gradle> ardından Dependecies alanında şu kodları girin

```kotlin
dependencies {
    var roomVersion = "2.4.2"

    implementation("androidx.room:room-runtime:$roomVersion")
    annotationProcessor("androidx.room:room-compiler:$roomVersion")

    // To use Kotlin annotation processing tool (kapt)
    kapt("androidx.room:room-compiler:$roomVersion")
    
		implementation("androidx.room:room-rxjava3:$roomVersion")
		
		implementation "io.reactivex.rxjava3:rxandroid:2.4.2"

    implementation 'androidx.core:core-ktx:1.7.0'
    implementation 'androidx.appcompat:appcompat:1.4.1'
    implementation 'com.google.android.material:material:1.5.0'
    implementation 'com.google.android.gms:play-services-maps:17.0.1'
    implementation 'androidx.constraintlayout:constraintlayout:2.1.3'
    testImplementation 'junit:junit:4.13.2'
    androidTestImplementation 'androidx.test.ext:junit:1.1.3'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.4.0'
}
```

Sonrasında Plugins alanımdan gerekli id yi eklemeliyiz

```kotlin
plugins {
    id 'com.android.application'
    id 'org.jetbrains.kotlin.android'
    id 'kotlin-kapt'
}
```

## Room Arcitecture

![room_architecture.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/20dc6851-0361-4a94-87d3-e733d5824ae6/room_architecture.png)

## Room kullanımı

Öncelikle 4 adet klasör ekliyeceğiz

MainActivitymizi View içerisine atıyoruz

![capture_20220316132653018.bmp](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e0e451ce-33c3-4f92-b7c2-a538ac2d5836/capture_20220316132653018.bmp)

## Entities

> Sonrasında model içerisine Place adında bir class oluşturuyorum
> 

```kotlin
@Entity
class Place(
    //Kolonları ayarladık
    @ColumnInfo(name = "name")
    var name:String,
    @ColumnInfo(name = "latitude")
    var latitude:Double,
    @ColumnInfo(name = "longitude")
    var longitude:Double) {
    
//Otomatik olarak id yi arttırır
    @PrimaryKey(autoGenerate = true)
    var id = 0
}
```

## Data Access Object (DAO)

> roomdb klasörümüzde PlaceDao diye oluşturduk ve içerisine kodlarımızı yazdık
> 

```kotlin
@Dao
interface IPlaceDao {
    @Query("SELECT * FROM Place")
    fun GetList(): List<Place>

    @Insert
    fun insert(place: Place)

    @Delete
    fun delete(place: Place)
}
```

### Database

Burda da database imizi oluşturuyoruz aynı şekilde roomdb ye oluşturuyoruz

```kotlin
@Database(entities = arrayOf(Place::class), version = 1)
abstract class PlaceDatabase:RoomDatabase() {
										//IPlaceDao İçerisindeki insert gibi metotlar bulunuyor
    abstract fun placeDao():IPlaceDao
}
```

## MainActivity de çağırmak

```kotlin
//Öncelikle nesneleri oluşturuk
private lateinit var db : PlaceDatabase
private lateinit var placeDao: IPlaceDao
fun Save(view: View){
        val place = Place(binding.placeText.text.toString(),selectedLatitude!!,selectedLongitude!!)
				//Nesnemizi database e aktardık
        placeDao.insert(place)
    }

//Fakat bize hata vericekdir bunu çözmek için ise RxJava adında bir library eklememiz lazım
```

### RxJava

implement eklemek için:

```kotlin
implementation "io.reactivex.rxjava3:rxjava:2.4.2"
```

```kotlin
val compositeDisposable: CompositeDisposable()

fun Save(view: View){
        val place = Place(binding.placeText.text.toString(),selectedLatitude!!,selectedLongitude!!)
        compositeDisposable.add(
            placeDao.insert(place)
                .subscribeOn(Schedulers.io())
                .observeOn(AndroidSchedulers.mainThread())
                .subscribe(this::handleResponse)
        )

    }
    private fun handleResponse(){
        val intent = Intent(this,MainActivity::class.java)
        intent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP)
        startActivity(intent)
    }
```

PlaceDao sayfamız

```kotlin
//Bize asenkron bir yapı sunar

@Dao
interface IPlaceDao {
    @Query("SELECT * FROM Place")
    fun GetList(): Flowable<Place>

    @Insert
    fun insert(place: Place):Completable

    @Delete
    fun delete(place: Place):Completable
}
```

---

# Navigation Component

Navigation Component Nedir ?

Sayfa geçişlerini daha görsel ve pratik hale getiren bir yapıdır.
• Activity üzerinde istediğimiz şekilde fragment geçişleri yapabiliriz.
• Geçişlerde veri transferi yapabiliriz.
• Geçişlere animasyon ekleyebiliriz.
• Birden fazla activityde kullanılabilir ama her activity için ayrı navigation dosyası oluşturmalıyız


## Kurulum için

> gradle>build.gradle>dependecies{
> 

> implementation "androidx.navigation:navigation-fragment-ktx:2.3.3"
implementation "androidx.navigation:navigation-ui-ktx:2.3.3"
> 

> }
> 

## Navigation Klasörü Oluşturma

> **res** klasörümüze sağ tıklayıp **Android Resource Directory** tıklayın navigation adını verin ResurceType: navigation seçin ardından oluşturun. **Ardından navigation** dosyamıza sağ tıklayıp **Navigation Resource File** diyin file name: main_activity_nav sonrada oluşturun
> 

## Fragment Oluşturma

> MainActivity mizin bulunduğu dosyaya sağ tıklayın new>fragment>fragment(blank)>finish
> 

sonrasında kodda düzenleme yapalım:

```kotlin
override fun onCreateView(inflater: LayoutInflater, container: ViewGroup?, savedInstanceState: Bundle?): View? {
        val tasarim = inflater.inflate(R.layout.fragment_anasayfa, container, false)

        tasarim.buttonBasla.setOnClickListener{

        }

        return tasarim
    }
```

## Navigation Component’e fragment ekleme

> main_activity_nav navigation ımıza geliyoruz tam ortaya basıyoruz ardından teker teker fragment larımızı sürüklüyoruz
> 

Not: Ana fragment eklemek için onunu üzerine ev işaretini eklemelisiniz

## Fragment Arası Geçiş Bağlantısı Oluşturma

> Öncelikle Navigation ımızda  sayfaların sağında çıkan bağlama boloncuklarından bu şekilde bağlıyoruz ve bu bağlamalara birer id veriyorum
> 



> Pekala bağlama işlemini yaptık diyelim bundan sonraki işlem bu butonlara bu sayfa geçiş kodlarını girmeliyiz:
> 

```kotlin
class AnasayfaFragment : Fragment() {

    override fun onCreateView(inflater: LayoutInflater, container: ViewGroup?, savedInstanceState: Bundle?): View? {
        val tasarim = inflater.inflate(R.layout.fragment_anasayfa, container, false)

        tasarim.buttonBasla.setOnClickListener{
            //it butonu temsil ediyor
            Navigation.findNavController(it).navigate(R.id.oyunEkraninaGecis)
        }
        return tasarim
    }
}

//Aynısını OyunFragment içinde yapıyoruz bu sefer gidilcek sayfa olarak sonucFragment seçiyouz
```

## Navigation Component Back Stack

Bu işlemin Active Directory deki karşılığı **finish()** dir.

> Navigation sayfamıza geliyoruz OyunEkranından Sonuç ekranına geçişimizi sağlayan oka tıklıyoruz ve bir popUpTo ekliyoruz burda sonuc ekranına geçilidğinde arkadaki hangi işlemi silelim demiş oluyoruz ve bukadar basit
> 


//Notlar Tamamen Escan Dönmez'e aittir
## Navigation Component Veri Transferi

Not: Eğer yani android sürümünü kullanyorsanız bu linkden yardım alın

[Navigation'da Safe Args ile Ekranlar Arası Veri Paylaşımı (mobiler.dev)](https://www.mobiler.dev/post/navigation-da-safe-args-ile-ekranlar-arasi-veri-paylasimi)

Öncelikle kurlumu yapalım build.gradle(module) gidelim ve bu implementasyonu yapalım

```kotlin
apply plugin: "androidx.navigation.safeargs.kotlin"
```

Ardından build.gradle(project) gidelim ve orayada bu implamanyasyonu yapalım

```kotlin
dependecies{
	classpath "androidx.navigation:navigation-safe-args-gradle-plugin:2.3.3"
}
```

Peki bu işlemi nasıl yapıcaz öncelikle navigation ımıza geliyoruz ve verilerin gönderileceği sayfanın üstüne tıklıyoruz


burdaki gibi gönderilecek verileri seçmemiz lazım
//Notlar Tamamen Escan Dönmez'e aittir


Eklediğimiz implamantasyonlar sonucunda otomatik Directions sınıfı oluştu bunun sayesinde oluşturduğumuz argümanlara veri gönderebiliriz

```kotlin
var gonder = AnasayfaFragmentDirections.oyunEkraniFragment()
gonder.ad = "Escan"
gonder.boy = 177f
gonder.yas = 22
gonder.bekarMi = true
//burda arguments larımıza değer atadık

Navigation.findNavController(it).navigate(gonder)
//bizi gonder değişikenindeki fragment a gönderir ve bununla beraber içerisindeki argümankarları da yollar
```

Sonrasında bu veriyi OyunFragment ımızdan çekiyoruz
//Notlar Tamamen Escan Dönmez'e aittir
```kotlin
//OyunEkraifragmentArgs veriyi alıcak sayfayı temsil eder
val bundle: OyunEkraniFragmentArgs by navArgs()
val gelenAd = bundle.ad
val gelenYas = bundle.yas
val gelenBoy = bundle.boy
val gelenBekarMi = bundle.bekarMi

println(gelenAd,gelenYas,gelenBoy,gelenBekarMi)
```

# Navigation Draw

Sol tarafta sidebar şeklinde ortaya çıkan bir menü türüdür


> Öncelikle Navigation ımızı kurmalıyız bunun için **Navigation Component** Kurulum başlığımıza gidebilirsiniz  ardından iki adet de fragment oluşturun aynı şekilde themes gelip orda şu kodları yazarak menü yü kapatın:
> 

//Notlar Tamamen Escan Dönmez'e aittir

```kotlin
<item name="windowNoTitle">true</item>
<item name="windowActionBar">false</item>
```

1. Öncelikle bir menü dosyası oluşturun
2. menu resource file oluşturun
3. içerisine iki adet menuItem ekleyin

> Evet işte işin asıl püf noktası burda yapacağını şey  Navigation’nınıza dönüp oluşturduğunuz iki fragment ın adlarına bakmanız olucak bu adları menünüzdeki item ların id leri ile aynı olmak ZORUNDA
> 
1. activiy_main.xml e gel
2. Code alanında Constrait i DrawerLayout ile değiştir ve id olarak drawer verelim
3. drawer’ın içerisine bir adet constrait oluşturalım
4. constrait in içine bir adet toolbar koyalım
5. ardından navHostFragment alıp sayfanın üstüne koyalım ve id olarak nav_host_fragment diyelim ki menü değişimlerinde sayfamızda bizimle gelsin 
6. sonrasında constrait layout umuzun altına Not:içine değil altına navigationView ekleyelim ve navigationView adında id verelim ve genişliğini wrap content yapalım
7. navigationView in menu categorysin’e tıklayıp bizim menümüzü ekliyelim
8. Code kısmına girip navigationView’e `android:layout_gravity="start"` bu kodu girerek sidebar şeklini almasını sağlayalım
9. aynı şekilde Code kısmında DrawerLayout un hemen altına bu kodu da girmeliyiz `tools:openDrawer="start"`

//Notlar Tamamen Escan Dönmez'e aittir

## Main Activity kodunu yazalım

öncelikle bağlamaları yapmalıyız fragment ımız ile menümüzü bağlamalıyız

```kotlin
class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

//nav_host_fragment ile navigationView i yani sidebar ı birbirine bağladık artık birinci ikinici diye kategori değiştirebilicez
        var navHostFragment = supportFragmentManager.findFragmentById(R.id.nav_host_fragment) as NavHostFragment
        NavigationUI.setupWithNavController(navigationView,navHostFragment.navController)
//Notlar Tamamen Escan Dönmez'e aittir
//drawer ile toolbarı birbirine bağladık
        toolbar.title = "Başlık"
        val toggle = ActionBarDrawerToggle(this,drawer,toolbar,0,0)
        drawer.addDrawerListener(toggle)
        toggle.syncState()
        //Notlar Tamamen Escan Dönmez'e aittir
    }
}
```
//Notlar Tamamen Escan Dönmez'e aittir
## Geri Tuşu Yapıldığında Drawer(Sidebar) Kapanması

```kotlin
override fun onBackPressed() {
        if(drawer.isDrawerOpen(GravityCompat.START)){
            drawer.closeDrawer(GravityCompat.START)
        }else{
            super.onBackPressed()
        }

    }
```

## Sidebar başlık ekleme

1. Öncelikle Layout dosyamıza sağ tıklayıp Layout Resource File oluştruuyoruz navigation_baslik adında
2. sonrasında constrait Layoutumuzda layout_weight’e 200 dp verelim ardından textView oluşturup üzerinde orantılıyalım ve constraintini ekleyelim
3. bundan sonrası tamamen kodumuza kaldı hadi gelin kodumuzu yazalım

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        var navHostFragment = supportFragmentManager.findFragmentById(R.id.nav_host_fragment) as NavHostFragment
        NavigationUI.setupWithNavController(navigationView,navHostFragment.navController)
//Notlar Tamamen Escan Dönmez'e aittir
        toolbar.title = "Başlık"
        val toggle = ActionBarDrawerToggle(this,drawer,toolbar,0,0)
        drawer.addDrawerListener(toggle)
        toggle.syncState()

			//Başlık navigation tasarımımızla navigation ımızı bağlıyaağcağız
        val baslik = navigationView.inflateHeaderView(R.layout.navigation_baslik)
        baslik.baslik.text = "Başlık"
    }

    override fun onBackPressed() {
        if(drawer.isDrawerOpen(GravityCompat.START)){
            drawer.closeDrawer(GravityCompat.START)
        }else{
            super.onBackPressed()
        }

    }
```

---

# Hazır fotoğraf yükleme thamplate

1. Öncelikle web sitelerinden birine gidelim
2. [Picasso (square.github.io)](https://square.github.io/picasso/)
3. web sitesinde de gördüğünüz implemente etme kodlarını görüyorsunuzdur gelin implemente edelim
4. build gradle da module olanına giriyoruz dependecies alanına bu kodu yapıştırıyoruz
5. `implementation 'com.squareup.picasso:picasso:2.71828'`

```kotlin
Picasso.get().load(postList.get(position).downloadUrl).into(holder.binding.recyclerImageView)
```

---

# Sorgu işlemleri

bir veriyi çekiceğimiz zaman sorgu ile çekebiliriz böylelikle tüm veryii getirmemize gerek kalmaz.

Örnek:

```kotlin
//escandöner@gmail.com getir sadece
.whereEqualTo("userEmail","escandöner@gmail.com")
//Score 200 den büyükse
.whereGreaterThan("Score",200)
//en yakın tarihleri getirir DESCENDİG aşağıdan yukarıya doğru gösterir
.orderBy("date",Query.Direction.Descending)
```

---

# Coroutine ****

> Uzun süreli işlemlerde örnek internetten veri çekerken resim çekerken Async gibi tasarımın donmasını engeller. Not= thread lere göre daha hafif bir yapıdır mesela 100 000 adet println yaptıracaksınız normalde bu tarz bir kod sistemi yavaşlatır fakat bunu coroutine ile sorunsuzca yapabiliriz
> 
//Notlar Tamamen Escan Dönmez'e aittir
## **Global Scope**

```kotlin
// Bütün bir application da kullanmamıza yarar

    GlobalScope.launch {
        repeat(100000){
            launch {
                print("Merhaba")
            }
        }
    }
```

## **runBlocking**

```kotlin
/*
İçerideki Coroutine işlemleri bitene kadar sonrasındaki kodların çalıştırılmasını durdurur
Gördüğünüz gibi ilk önce Coroutine içeriğini çalıştırıyor ondan sonra işlem tamamlandıktan sonra 
Coruitine dışındaki işlemleri gerçekleştiriyor 
*/

    println("run blocking start")
    runBlocking {
        launch {
            delay(5000)
            println("runblocking")
        }
    }
    println("run blocking end")

```

## **Coroutine Scope**

```kotlin
/*
İçerideki bütün Coroutine ler bitene kadar çalışmaya devam eder

CoroutineScopeları sadece bir coroutine veya suspend functionların içerisinde çağırılabilir

Çıktı:
Coroutine start ve end ilk önce görünür ondan 5 sn sonrada coroutine içeriği görünür yani coroutine arka planda çalışır
*/

println("coroutine scope start")
//Dispatchers lar yazının devamında anlatıyorum
CoroutineScope(Dispatchers.Default).launch{
	delay(5000)
	println("coroutine scope")
}
println("coroutine scope end")

**//Coroutine iç içe kullanımda**
runBlocking {
        launch {
            delay(5000)
            println("run blocking")
        }

        coroutineScope {
            launch {
                delay(3000)
                println("Coroutine Scope")
            }
        }
    }

```

## Dispatcher lar

### Dispatchers.Main -> UI

Tasarım ile ilgili durumlarda kullanılır

### Dispatchers.IO -> Input Output, Networking

İnternetten birşey çekerken kullanılır

### Dispatchers.Default -> Cpu Intensive

Uzun  bir diziyi dizerken veya cpu nun yoğun kullanıldığı işlemlerde kullanılır

### Dispatchers.Unconfined -> Inherited disppatcher

İçerisinde çalıştırılan yere göre kalıtım alıyor

```kotlin
//ÖRNEK
//Notlar tamamen Escan Dönmez'e aittir
runBlocking {
    launch(Dispatchers.Main){
        println("Main Thread: ${Thread.currentThread().name}")
    }
    launch(Dispatchers.IO) {
        println("IO Thread:  ${Thread.currentThread().name}")
    }
    launch(Dispatchers.Default) {
        println("Default Thread:  ${Thread.currentThread().name}")
    }
    launch(Dispatchers.Unconfined) {
        println("Unconfined Thread:  ${Thread.currentThread().name}")
    }
}

/*
ÇIKTI:
	Default Thread: DefaultDispatcher-worker-1
	IO Thread: DefaultDispatcher-worker-2
	Unconfined Thread: main
 */
```

## Suspend Coroutine

```kotlin
funmain() {
	runBlocking{
	delay(2000)
	println("run blocking")
  myFunction()
	}
}

suspend fun myFunction(){
    coroutineScope{
			delay(4000)
			println("suspend function")
		}
}
//Notlar tamamen Escan Dönmez'e aittir
/*Çıktı:
	2sn
	run blocking
	4sn sonra
	suspend function
*/
```

## Job Nedir

```kotlin
fun main(){

	runblocking{
		val myJob = launch{
			delay(2000)
			println("job")
			val secondJob = launch{
				println("job2")
			}
		}
//Tüm işler bittikden sonra bunu yap
		myJob.invokeOnCompletion{
			println("Tüm işlemler bitti")
		}
		
	}
}

// Çıktı olarak bize ilk önce job job2 ve Tüm işlemrim bitti çalışır
//Notlar tamamen Escan Dönmez'e aittir
fun main(){

	runblocking{
		val myJob = launch{
			delay(2000)
			println("job")
			val secondJob = launch{
				println("job2")
			}
		}
		myJob.invokeOnCompletion{
			println("Tüm işlemler bitti")
		}
		myJob.cancel()
	}
}
// Çıktı olarak Tüm işler bitti yi verir çünkü burda myJobu tamamen bitirdik 
```

## withContext nedir

```kotlin
fun main(){
	runblocking{
		launch(Dispatchers.Default){
			println("Context: ${coroutineContext}")
			withContext(Dispatchers.IO){
				println("Context: ${coroutineContext}")
			}
		}
	}
}
```

# Work Manager

> Kısaca mantığı uygulama kapatılsa bile çalışmaya devam etmesi
> 

```kotlin
//İmplementasyon
dependencies {
		implementation("androidx.work:work-runtime-ktx:2.7.1")
}
```

## Worker sınıfı

Refresh database adında bir class oluşturularım class a Worker kalıtımı veriyorum ve interface elemanlarını implemente ediyorum

```kotlin
class RefreshDatabase(val context: Context, workerParams: WorkerParameters) :
    Worker(context, workerParams) {
    override fun doWork(): Result {
        val getData = inputData
        val myNumber = getData.getInt("intKey",0)
        refereshDatabase(myNumber)
        return  Result.success()
    }

    private fun refereshDatabase(mysNumber:Int) {

        val sharedPreferences = context.getSharedPreferences("com.escan.workmanager",Context.MODE_PRIVATE)
        var myNumber = sharedPreferences.getInt("myNumber",0)
        myNumber = myNumber + mysNumber
        println(myNumber)
        val editor = sharedPreferences.edit()
        editor.putInt("myNumber",myNumber).apply()

    }
```
//Notlar tamamen Escan Dönmez'e aittir
Sonrasında Main Activity e gelelim

```kotlin
val data = Data.Builder().putInt("intKey",1).build()

        val constraints = Constraints.Builder()
                //İnternet bağlıyken sadece çalışır
            //.setRequiredNetworkType(NetworkType.CONNECTED)
                //sadece şarz da değilken çalışır
            //.setRequiresCharging(false)
            .build()

        //Tek seferde çalışır
        //OneTimeWorkRequestBuilder<>()
        val myWorkRequest :WorkRequest = OneTimeWorkRequestBuilder<RefreshDatabase>()
            .setConstraints(constraints)
            .setInputData(data)
            .build()

        WorkManager.getInstance(this).enqueue(myWorkRequest)

        //periyodik şekilde belli dakikalar la çalışır
        //PeriodicWorkRequestBuilder<>()

        val myWorkRequestPeriodic : PeriodicWorkRequest = PeriodicWorkRequestBuilder<RefreshDatabase>(15,TimeUnit.MINUTES)
            .setConstraints(constraints)
            .setInputData(data)
            .build()

        WorkManager.getInstance(this).enqueue(myWorkRequestPeriodic)
```

## Gözlemleme ve Zincirleme (WorkManager)
//Notlar tamamen Escan Dönmez'e aittir
```kotlin
//Chaining
  val oneTimeRequesta: OneTimeWorkRequest = OneTimeWorkRequestBuilder<RefreshDatabase>()
      .setConstraints(constraints)
      .setInputData(data)
      .build()

  WorkManager.getInstance(this)
          //Bununla başla
      .beginWith(oneTimeRequesta)
          //Ardından bunu yap
      .then(oneTimeRequesta)
           //Ardından bunu yap
      .then(oneTimeRequesta)
      .enqueue()
```

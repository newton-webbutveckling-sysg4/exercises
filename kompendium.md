# Övningar JavaScript + HTML5 + CSS3

Övningar som passar för en första programmeringskurs i JavaScript. Innehåller också HTML och CSS.

1. [Datatyper, variabler, konsolen](#1-datatyper-variabler-konsolen)
2. [Kontrollstrukturer och programflöde](#2-kontrollstrukturer-och-programflöde)
3. [Funktioner](#3-funktioner)
	1. [Rekursion](#1-rekursion)
4. [Listor](#4-listor)
	1. [Läsförståelseövningar på arrayer och funktioner](#1-läsförståelseövningar-på-arrayer-och-funktioner)
	2. [Övningar som bygger på läsövningarna ovan](#2-övningar-som-bygger-på-läsövningarna-ovan)
	3. [Övningar på att skriva kod med arrayer och funktioner](#3-övningar-på-att-skriva-kod-med-arrayer-och-funktioner)
	4. [Sorteringsövningar](#4-sorteringsövningar)
5. [Objekt](#5-objekt)
	1. [JSON](#1-json)
6. [Higher order functions](#6-higher-order-functions)
7. [Git](#7-git)
8. [HTML och CSS](#8-html-och-css)
	1. [Grundläggande HTML och CSS](#1-grundläggande-html-och-css)
	2. [CSS selektorer](#2-css-selektorer)
	3. [Transition och transform](#3-transition-och-transform)
9. [Layout med CSS](#9-layout-med-css)
10. [DOM-manipulation med JavaScript](#10-dom-manipulation-med-javascript)
11. [Events](#11-events)
12. [AJAX](#12-ajax)
13. [Promises](#13-promises)




## 1 Datatyper, variabler, konsolen

Utgå från [detta kodexempel i repl.it](https://repl.it/@david_zocom/UserInput) när du behöver input från användaren. Senare kan du använda vanliga repl.it eller webbläsarens JavaScript-konsol.

0 Ta reda på hur man öppnar JavaScript-konsolen (Console) i din favoritwebbläsare.

1 Vilka datatyper är följande uttryck? Tips: använd `typeof` för att kontrollera ditt svar

Exempelvis kan man svara att första uppgiften är _datatypen Number_ och har _värdet 1,01_. Se till att du förstår _varför_ resultatet blir som det blir.


```
1	1.01	14	true + true + false
2	'false'	15	5 && 8
3	null	16	5 || 8
4	pancake	17	!5
5	1 / 0	18	!!5
6	false || true	19	true && false || false && true
7	"123" - 0	20	typeof (typeof true)
8	"1000" / 10	21	1 + 2 * 3 + 4 * 5 + 6
9	123.4 - ''	22	2 < 3
10	'5' + "0" / '2'	23	'två' < 'tre'
11	'5' + "0" / '5' + 0	24	17 === 17.0
12	'1' + '5' - '4' * '2' - '3'	25	17 === '17'
13	'kalle' - 5	26	17.000000000000000000001 == 17
27	undefined || null || 0 || false || "foo"
```


2 Vilket värde kommer variabeln `z` att ha efter att respektive kodrad har körts? (1 svar per rad) Kör den här kodraden före varje rad när du testar: `let x, y, z;`


```
1	z = 5;
2	z++;
3	--z;
4	z += 15;
5	x = 8;  y = 16;  z = y - x;
6	x = 10;  z = x++;
7	x = 2;  y = 5;  x = x + y;  y = x + y;  z = y;
```


3 Skriv ett program som frågar vad användaren heter och skriver ut <code>"Välkommen <span style="text-decoration:underline;">&lt;NN></span>!"</code> där <code>&lt;NN></code> är användarens namn. Tips: använd <code>console.log</code> för att skriva ut och <code>prompt</code> för att hämta input från användaren. Se till att spara namnet i en variabel. Exempel:  \
<code>let x = prompt("Meddelande");  \
console.log(x);</code>

4 Skriv ett program som frågar användaren efter två tal och sparar dem i variabler. Sedan ska det skriva ut talens summa, differens och produkt.

5 Skriv ett program som frågar användaren efter ett tal. Programmet ska skriva ut talet avrundat till ett heltal. _Extra utmaning_: skriv ut talet avrundat till en decimal i stället.


## 2 Kontrollstrukturer och programflöde

1 Skriv ett program som frågar användaren efter ett lösenord. Hitta på ett hemligt lösenord och spara det i en variabel. När användaren har skrivit in ett ord ska programmet jämföra med det sparade lösenordet och skriva ut om det var rätt eller inte. Använd en if-sats.

2 Skriv ett program som frågar användaren efter ett tal. Det ska skriva ut om talet är mindre än 100, lika med 100 eller större.

3* Skriv ett program som frågar användaren efter ett tal mellan 1 och 100. Programmet ska ha ett hemligt tal lagrat i en variabel. Det ska fortsätta fråga användaren till dess att användaren gissar det hemliga talet. Om man gissade för högt eller för lågt så ska det skrivas ut, så att användaren har en rimlig chans att klara det.

Exempel: programmet har det hemliga talet 27. Användaren gissar på 50. Programmet skriver ut att användaren gissade för högt. Användaren gissar därefter på 20. Programmet skriver ut att det var för lågt. Användaren gissar slutligen på 27. Programmet skriver ut att det var rätt och avslutas.

_Extra utmaning_: slumpa det hemliga talet med hjälp av Math.random och farbror google. Spara antalet gissningar i en variabel och skriv ut det när användaren gissat rätt.

4 Skriv ett program som ber användaren skriva in en månad. Programmet ska göra om månaden till månadens siffervärde. T.ex. ska januari bli 1 och december 12. Använd switch. Jämför din lösning med en klasskamrat när du är klar.

5 Skriv ett program som skriver ut talen 1 till 16 med hjälp av en loop.

6 Skriv ett program som har talet 65536 i en variabel. Så länge som variabeln är större än 2 ska programmet loopa, skriva ut talet och sedan dela variabeln med 2.

7 Skriv ett program som loopar och frågar användaren efter en sträng. Så länge som strängen inte är en tom sträng så ska programmet lägga ihop den med tidigare strängar, med ett mellanrum. Om användaren t.ex. har skrivit `"ord1"` tidigare och skriver `"ord2"` ska den nya strängen bli `"ord1 ord2"`. Fortsätt loopa tills användaren skickar en tom sträng eller en punkt.

7b Skriv ett program som skriver ut de jämna talen 20 till 2 i den ordningen, med hjälp av en loop.

8 Skriv ett program som frågar användaren efter ett tal. Programmet ska loopa så länge som talet är större än 2. Varje loop ska programmet välja: om talet är udda, multiplicera talet med 3 och lägg till 1. Om talet är jämnt, dela det med 2. Skriv ut det nya talet varje varv i loopen.

9a Vad kommer följande kod att skriva ut?

```
let text = '';
for( let i=0; i<6; i++ ) {
	for( let j=0; j<8; j++ ) {
		if( (i + j) % 2 === 0)
			text += '#';
		else
			text += '.';
	}
	text += '\n';
}
console.log(text);
```

Ändra koden så att den skriver ut:

```
9b          9c          9d          9e          9f          9g
#.......	#.......	..###...	..#.....	....##..	#....#..
#.......	.#......	..###...	..#.....	....#...	.#..#...
#.......	..#.....	..###...	########	...##...	..##....
#.......	...#....	..###...	..#.....	..#.#...	..##....
#.......	....#...	..###...	..#.....	.#..#...	.#..#...
#.......	.....#..	..###...	..#.....	#...#...	#....#..
```

```
9h          9i          9j          9k
#.#.#.#.	........	.#O.#O.#	..#..#..
#.#.#.#.	.######.	O.#O.#O.	..#..#..
#.#.#.#.	.#....#.	#O.#O.#O	..#..#..
#.#.#.#.	.#....#.	.#O.#O.#	........
#.#.#.#.	.######.	O.#O.#O.	.#.#.#.#
#.#.#.#.	........	#O.#O.#O	#.#.#.#.
```



## 3 Funktioner

1 Vad skrivs ut av följande koder?


```
1	function foo() {
2		console.log("test");
3	}
4	foo("hej");

1	let a = foo(3);
2	console.log(a);
3	function foo(i) {
4		return i * i;
5	}
```



```
1	console.log( foo(3, 5) );
2	function foo(x, y) {
3		return x * y;
4	}

1	let x = 2;
2	let y = 3
3	let a = foo(foo(x) + foo(y));
4	console.log(a);
5	function foo(i) {
6		return 5 * i;
7	}
```



```
1	let a = 5;
2	function foo(a) {
3		a++;
4	}
5	a += 2;
6	console.log(a);
```



```
1	var foo = function(i) {
2		return 2*i*i;
3	};
4	var goo = function(x, y)
5	{
6		return x(y);
7	};
8	var a = goo(foo, 3);
9	console.log(a);
```


2a Skriv en funktion med namnet `add` som lägger ihop _två _tal och returnerar resultatet.

2b Skriv en funktion med namnet `multi` som multiplicerar _tre _tal och returnerar resultatet. Vad händer om man anropar funktionen med färre än tre parametrar?

2c Skriv en funktion som tar fyra tal som parametrar. Den ska multiplicera de tre första och lägga ihop resultatet med den fjärde. Använd funktionerna `add` och `multi`.

3 Skriv en funktion som tar tre parametrar: name, city och favoriteColor.  Den ska skriva ut informationen till konsolen i en fullständig mening. Exempel <code>"Välkommen <em>Namn</em> från <em>Göteborg</em> med favvofärg <em>blått</em>"</code>.

4 Skriv en funktion som tar en parameter som ska vara en sträng och returnerar ett tal. Om det inte går att göra om parametern till ett tal ska funktionen returnera strängen oförändrad. Tips: minus noll, isNaN(variabel).

5 Skriv en funktion som tar två parametrar och talar om ifall de är samma datatyp. Tips: använd `typeof`.

Exempel:


```
sameDataType('test', 'topp')	→ true
```


`sameDataType(5, '5')		→ false`.

6 Skriv en funktion som avrundar ett tal till två decimaler. Tips: man kan använda Math.round(x) för att avrunda ett tal till närmast heltal.

7 Skriv en funktion med namnet `paragraph`, som tar en parameter. Den ska returnera en sträng enligt det här exemplet: `paragraph('hej') == '&lt;p>hej&lt;/p>'`

8 Skriv en funktion som säger hur många dagar en månad har. Funktionen ska ha en parameter, som är en sträng som motsvarar månadens namn. Strängen ska vara de tre första tecknen i månadens namn, dvs jan, feb, mar, apr osv. Funktionen ska returnera ett tal. Exempelvis så är `daysInMonth("mar") == 31`


```
function daysInMonth(month="jan") { .. }
```


9 Skriv en funktion som returnerar de tre första tecknen i en sträng. Använd funktionen **<code>substring(startindex, endindex)</code></strong>, som plockar ut en del av en sträng. Exempel: <code>'programmering'.substring(3,7)</code> blir <code>'gram'</code>.

10 Skriv en funktion som du kallar `year` som plockar ut året från en sträng i datumformat. Funktionen ska ta en parameter, som ska vara en sträng. Strängen ska alltid ha 10 tecken och följa mönstret `'YYYY-MM-DD'`. Man ska kunna skriva `year('2016-11-02')` och få talet `2016` som resultat.

11 Skriv två funktioner med namnen `month` och `day`, som plockar ut månad respektive dag ur en datumsträng som i uppgift 10. Skriv med hjälp av dem en funktion med namnet `daysBetween` som räknar ut hur många dagar det är mellan två datum. Du kan förenkla funktionen genom att låtsas att alla månader har 30 dagar.

Exempel: `daysBetween('2017-08-30', '2017-09-02') == 4`

12 Skriv en funktion som översätter en temperatur i Fahrenheit till Celsius. Den ska ta en parameter och returnera ett värde. Formeln finns på [den här sidan](http://www.manuelsweb.com/temp.htm).

13 Skriv en funktion som returnerar summan av de 100 första heltalen. Använd en loop. Förbättra sedan funktionen så att den tar en parameter, som är hur många tal som ska läggas ihop.

14 Skriv en funktion som tar en sträng som parameter och returnerar strängen baklänges. Tips: använd funktionen string.charAt.

15* _Extrauppgift_. Skriv en funktion som tar ett tal som parameter och returnerar `true` om det är ett primtal. Ett primtal är ett heltal som bara är delbart med sig självt och 1. De första primtalen är 2, 3, 5, 7. Men 8 är inget primtal eftersom 8 / 2 == 4.

Obs! Det går att hitta färdiga lösningar på internet. Men om du plockar en färdig lösning så lär du dig mindre än om du försöker göra en själv.

Fundera på: vilket är det enklaste sättet att skriva funktionen? Vilket sätt är effektivast? Vad innebär effektivitet för ett datorprogram?


### 1 Rekursion

16 Skriv en funktion `factorial(n)` som räknar ut fakulteten för ett heltal med en loop. Fakulteten tar man genom att multiplicera talet med alla mindre tal ner till 1. Exempel: `1! == 1, 2! == 2*1, 4! == 4*3*2*1` osv.

17 Skriv en ny funktion som beräknar fakulteten rekursivt.

18 Fibonacci-tal är en talserie som börjar med 0, 1. Sedan får man nästa tal i talserien genom att lägga ihop de två föregående. Exempel: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, … Skriv en funktion `fibonacci(n)` som beräknar det n:te Fibonacci-talet rekursivt. _Extrauppgift_: gör en funktion som räknar ut det med en loop.

19 Skriv en rekursiv funktion som tar en sträng som parameter och returnerar en ny sträng, som är den gamla strängen baklänges. Tips: använd string.substring().

20a Skriv en rekursiv funktion som summerar alla tal i en lista. Tips: låt funktionen ta två parametrar, listan och en variabel med namnet _index _som har defaultvärde 0.

20b Skriv en rekursiv funktion som returnerar det minsta talet i en lista.

_Följande uppgifter väntar vi med till efter att vi gått igenom DOM-manipulation._

21 Skriv en rekursiv funktion som ändrar bakgrundsfärgen på alla element som finns inuti ett visst element. Funktionen behöver två parametrar: färgen och ett DOM-element, som du hämtar med getElementById.

22 Skriv en rekursiv funktion som tar ett DOM-element och en sträng som parametrar. Den ska returnera true om strängen finns som text någonstans inuti elementet. Glöm inte att kontrollera eventuella child elements. Om det till exempel handlar om ett _ul_-element så behöver man kontrollera alla _li_-element också.


## 4 Listor


### 1 Läsförståelseövningar på arrayer och funktioner

Dessa övningar läser du och tänker ut svaret på. De handlar om allt vi gått igenom än så länge i kursen. De är inte sorterade efter svårighetsgrad så fastnar du kan du hoppa över och komma tillbaka senare till den du fastnade på. Det kan finnas buggar i koden…



1. Vad skriver programmet ut?

```
function stringEcho(str) {
	console.log(str + str);
}
stringEcho("hej");
```


2. Vad skriver programmet ut?

```
function soundLikeACat(times) {
	for(let i=0; i<times; i++)
		console.log("meow");
}
soundLikeACat(5);
```


3. Vad skriver programmet ut?

```
function soundLikeAnAnimal(sound, times) {
	for(let i=0; i<times; i++)
		console.log("meow");
}
soundLikeAnAnimal("bark", 3);
```


4. Vad skriver programmet ut?

```
let animals = ["dog", "cat", "zebra", "horse", "cow"];
animals.shift();
console.log("My favourite animal is " + animals[0]);
```


5. Vad skriver programmet ut?

```
let animals = ["dog", "cat", "zebra", "horse", "cow"];
animals.unshift("elephant");
if(animals.indexOf("pig")=== -1)
	animals.push("pig");
else
	animals[animals.length-1] = "pig";
console.log("My favourite animal is " + animals[0]);
```


6. Vad skriver programmet ut?

```
let animals = ["dog", "cat", "zebra", "horse", "monkey", "pig", "cow"];
for(let i=0; i<animals.length; i++) {
	if(i>3)
		console.log(animals[i];
}
```


7. Vad skriver programmet ut?

```
const PIG = 0;
const COW = 1;
const DOG = 2;

function makeAnimals(animalId, numberOfAnimals) {
	let animals = [];
	for(let i=0; i<numberOfAnimals; i++) {
		switch(animalId) {
			case PIG:
				animals.push("pig");
				break;
			case COW:
				animals.push("cow");
				break;
			case DOG:
				animals.push("dog");
				break;
			default:
				return ["Error!"];
		}
	}
	return animals;
}
let arr = makeAnimals(DOG, 3);
console.log(arr);
```


8. Vad skriver programmet ut?

```
function stringEcho(str) {
	return str + str;
}
console.log( stringEcho(stringEcho(".a.")+"b.") + stringEcho(".c") );
```


9. Vad skriver programmet ut?

```
function pigSort(unsortedArr) {
	let pigArr = [];
	while(unsortedArr.length > 0) {
		pigArr.push("pig");
		unsortedArr.shift();
	}
	return pigArr;
}

let arr = ["dog", "cat", "zebra", "horse", "cow"];
console.log(pigSort(arr));
```


10. Vad skriver programmet ut?

```
const PIG = 0;
const COW = 1;
const DOG = 2;

const ANIMAL_NAMES = ["pig", "cow", "dog", "animal"];

function makeAnimals(animalId, numberOfAnimals) {
	let animals = [];
	for(let i=0; i<numberOfAnimals; i++) {
		animals.push(ANIMAL_NAMES[animalId]);
	}
	return animals;
}

function animalSort(animals, animalName) {
   if(ANIMAL_NAMES.indexOf(animalName) === -1)
      return makeAnimals(ANIMAL_NAMES.indexOf("animal"), animals.length);
   else
      return makeAnimals(ANIMAL_NAMES.indexOf(animalName), animals.length)
}

let arr = animalSort(["zebra", "monkey", "gorilla", "pig"], "cow");
console.log(arr);
```

Vad skrivs ut om vi ändrar näst sista raden till:


```
let arr = animalSort(["zebra", "monkey", "gorilla", "pig"], "horse");

```



11. Vad skriver programmet ut?

```
const METAL = 0;
const WOOD = 1;
const FIRE = 2;
const DOOM = 3;
const DAGGER = 4;
const SWORD = 5;
const FIRE_SWORD = 6;
const WATER_DAGGER = 7;
const TORCH = 8;

const ITEM_NAME = 0;
const ITEM_COMPONENTS = 1;

let items = [
			["Metal", [] ],
			["Wood", [] ],
			["Fire", [] ],
			["Doom", [] ],
			["Dagger", [METAL, WOOD] ],
			["Sword", [DAGGER, METAL] ],
			["Flaming Sword", [SWORD, FIRE] ],
			["Dagger of Doom", [DAGGER, DOOM] ],
			["Torch", [FIRE, WOOD] ]
];

console.log("The " + items[SWORD][ITEM_NAME] + " is made of " + items[SWORD][ITEM_COMPONENTS]);
```




### 2 Övningar som bygger på läsövningarna ovan

LÖ = läsövning

1. Redigera koden för LÖ1 ovan så att
    1. stringEcho returnerar en array istället
    2. stringEcho tar emot en sträng s och ett heltal x och returnerar en array med x element som alla är strängen s
2. Gör om LÖ2 ovan så att
    3. soundLikeACat skriver ut alla ljuden på en rad, med mellanslag emellan: "meow meow"...
3. Gör om LÖ3 ovan så att
    4. fixa buggen!
4. Gör om LÖ5 ovan så att
    5. det finns en "pig" i listan
    6. else-satsen byter plats på "pig" och det sista elementet i listan, i stället för att ersätta det
5. Gör om LÖ7 ovan så att
    7. lägg till ett nytt djur
6. Gör om LÖ11 ovan så att
    8. det finns en Flaming Dagger of Doom
    9. det finns en rekursiv funktion som tar emot ett items id som heltal och returnerar en array med strängar på namnen på alla items som behövs för att skapa det efterfrågade föremålet.


### 3 Övningar på att skriva kod med arrayer och funktioner {#3-övningar-på-att-skriva-kod-med-arrayer-och-funktioner}

1a Skriv en funktion som tar två parametrar som ska vara heltal. Den ska returnera ett slumptal vars värde är mellan parametrarna. Utgå från [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random).

Exempel: rand(2, 5) → något av 2, 3, 4 och 5

Tips: Vilka möjliga värden kan vi få om vi räknar ut `Math.random()*2`? `Math.random()*3`?

1b Skriv en funktion som skapar en lista med slumptal. Funktionen ska ta tre parametrar: hur lång listan ska vara och mellan vilka tal som slumptalet ska ligga.

2a Skriv en funktion som räknar ut summan för alla tal i en lista.

2b Skriv en funktion som räknar ut medelvärdet för alla tal i en lista.

2c Skriv två funktioner som returnerar det största respektive det minsta värdet i en lista.

3 Skriv en funktion med namnet `listHasWord` som kontrollerar om ett specifikt värde finns i en lista. Funktionen ska ta två parametrar: en lista och värdet man söker efter. Den ska returnera true eller false.

4a Skriv en funktion som gör samma sak som funktionen <code>[split](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)</code>.

Exempel: `function mySplit(string, separator)`

4b Skriv en funktion som kapitaliserar strängar, dvs gör om en sträng så att första bokstaven i varje ord är stor. Exempel: capitalize('hello world') → 'Hello World'

Använd `mySplit` för att hitta alla orden, <code>[substring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substring)</code> för att välja ut en del av en sträng och <code>[toUpperCase](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase)</code> för att göra om en sträng till bara stora bokstäver.

5a Skriv en funktion som tar en lista och ett tal x som parametrar. Den ska skriva ut alla värden i listan i en rektangel, genom att radbryta efter x värden. Använd `'\n'` för att lägga till en radbrytning till en sträng.

Exempel: `printList([1, 2, 3, 4], 2) --> "1 2\n3 4"`

5b* Extra utmaning: se till så att funktionen gör raka kolumner, dvs infogar extra mellanrum för tal som har färre antal siffror. Tips: du behöver ta hjälp av andra funktioner för att göra det bra. T.ex. egenskapen length och funktionen från uppgift 2 som ska hitta största värdet i en lista.

6 Skriv en funktion som slår ihop två sorterade listor till en sorterad lista. Exempel: \
`merge([1, 3, 5], [2, 4, 6, 8, 10]) → [1, 2, 3, 4, 5, 6, 8, 10] \
merge([], [10]) → [10]`

7 Skriv en funktion som slumpar fram ett djur. Funktionen ska inte ha några parametrar och returnera en sträng som är antingen cat, dog, horse, pig eller elephant.

8a Skriv en funktion som slumpar fram en lista med djur. Funktionen ska ta emot ett heltal x och returnera en lista med x stycken slumpvis valda djur som antingen är cat, dog, zebra, monkey, horse, pig eller elephant.

8b Gör om a-övningen så att listan som returneras inte har några dubletter, dvs samma djur förekommer enbart en gång. Detta gör att funktionen inte kan ta emot en siffra som är större än 7. Tips: två alternativ: 1) byt plats på det valda elementet med det sista och använd `pop()`, 2) eller ersätt djur som har valts ut med en tom sträng och loopa tills du hittar ett djur.

9 Skriv en funktion med namnet filterLessThan. Den ska ta en lista och ett tal som parametrar och returnera en ny lista. Den nya listan ska ha alla element som finns i den första listan och är mindre än parametern.

Exempel: `filterLessThan([5, 10, 15], 11) → [5, 10]`


### 4 Sorteringsövningar



1. Skriv en implementation av [Bubble Sort](https://en.wikipedia.org/wiki/Bubble_sort) i JavaScript
2. Skriv en implementation av [Merge Sort](https://en.wikipedia.org/wiki/Merge_sort) i JavaScript


## 5 Objekt

1 Skapa ett objekt med följande egenskaper:

* ett värde av datatypen Number
* en string
* en bool
* en funktion
* ett tomt objekt

2 Skapa ett objekt som innehåller ett objekt, som i sin tur innehåller ett tomt objekt. Tänk på indraget!

3 Skapa en funktion med namnet _makeBook_. Funktionen ska ha parametrarna _title_, _author_ och _genres_. Title och author ska vara strängar, genres ska vara en lista. Funktionen ska returnera ett objekt som har parametrarna som egenskaper.

4 Skapa ett objekt som motsvarar en cirkel. Det ska ha en egenskap för radien och en egenskap som är en funktion som räknar ut cirkelns area. Funktionen ska inte ta några parametrar utan använda egenskapen för radien med hjälp av _this_.

5 Skapa ett objekt som motsvarar en rektangel. Det ska ha egenskaper för bredd, höjd och för att räkna ut arean. Skriv en funktion med namnet _isCircleBigger_ som tar objekt för en cirkel och en rektangel och returnerar _true _om cirkelns area är större än rektangelns area.

6 Skriv en funktion med namnet _printObject_. Den ska ta ett godtyckligt objekt som parameter och skriva ut på konsolen vilka egenskaper objektet har och vad de har för värde. Använd en for-loop för att gå igenom alla objektets egenskaper.

7 Använd funktionen _makeBook_ för att skapa tre bok-objekt och lägg dem i en lista. Skriv en funktion med namnet _filterAuthor_. Den ska ta en lista med bok-objekt och en sträng som parametrar och returnera en ny lista med alla bok-objekt i den första listan som har samma författare som strängen. Exempel:


```
filterAuthor(lista, "J.R.R. Tolkien")
```


8 Skriv en funktion med namnet _capitalizeBooks_. Den ska ta en lista med bok-objekt som parameter och inte returnera något. Funktionen ska ändra alla objekt i listan så att titel och författare på respektive bok börjar med stor bokstav.

Tips 1: titta på varje element i listan.

Tips 2: använd funktionen substring för att plocka ut delar av en sträng.

9 Skriv en funktion med namnet _filterGenre_. Den ska ta en lista med bok-objekt och en sträng som parameter och returnera en ny lista med alla bok-objekt som matchar strängen. Ett bok-objekt matchar om egenskapen genres, som är en lista, innehåller en likadan sträng som parametern. \
Exempel: `filterGenre(lista, 'fantasy')`

10 Skapa en lista med minst fyra landsobjekt. Objekten ska ha egenskaperna _name _och _population_. Använd internet för att leta upp data för fyra länder. Skriv sedan en funktion med namnet _countryPopulationSum_, som räknar ut hur många invånare det finns i alla länder i listan.

11 Skriv en funktion med namnet _countryFindSmallest_, som tar en lista med landsobjekt och returnerar det objekt som har den minsta befolkningen. Skriv ut namnet på landet på konsolen.

12 Skriv en funktion med namnet _countryComparePopulation_. Den ska ta två landsobjekt som parametrar: a och b. Om a är mindre än b ska funktionen returnera -1, om a är större ska den returnera +1, annars returnera 0.

13 Man kan sortera elementen i en lista genom att använda array-funktionen _sort_. Standardsorteringen jämför värden som om de vore strängar. Den används om man anropar _sort_ utan parametrar. Om man vill sortera elementen i en lista på annat sätt så kan man skicka med en jämförelsefunktion som parameter. \
Exempel: `lista.sort(compareFunction)`

Jämförelsefunktionen ska ta två värden av den typ som finns i listan och returnera ett tal som talar om för sorteringsfunktionen om elementen behöver byta plats. Använd funktionen _countryComparePopulation _för att sortera listan. Skriv också en jämförelsefunktion som jämför landsobjekt baserat på namn


### 1 JSON

1 Skriv ett program som använder JSON.parse och JSON.stringify. Använd _prompt_ (med försiktighet) för att hämta input från användaren. Testa dina funktioner med bok-objekten från uppgift 5.7.


## 6 Higher order functions

1 Skriv en arrow function som gör samma sak som följande funktion:

```
function vanlig(parameter) { return parameter; }
```


2 Skriv en arrow function som tar ett tal som parameter och returnerar dubbla talet. Om man till exempel anropar funktionen med 5 som parameter ska den returnera 10.

3 Skriv en arrow function som tar två tal som parametrar och returnerar deras medelvärde.

4 Skriv en arrow function som inte tar några parametrar och alltid returnerar talet 42.

5 Skriv en arrow function som tar en sträng som parameter och skriver ut den på konsolen.

6 Skriv en arrow function som tar en parameter och returnerar true om den är större än noll.

7 Skriv en arrow function som tar ett tal som parameter och returnerar true om talet är 10 eller 12.

8 Skriv en arrow function som tar en parameter och returnerar true om den är en sträng som innehåller "och".

9 Lös uppgifterna 5.7-12 med hjälp av higher order functions: forEach, filter, map, reduce, find, some, every.

10 För den här uppgiften ska du utgå från följande listor:


```
let listA = [2, 4, 8, 16, 32, 64, 128, 256];
let listB = [10, 'b', -32, 'FF', 3.14, [], (x => x + 1), ' end'];
```


Använd `forEach` för att skriva ut alla element i listA på konsolen.

Använd `forEach` för att skriva ut alla element i listB som är strängar.

Använd `map` för att skapa en kopia av listA, där alla element har minskats med ett: 1, 3, 7, osv.

Använd `map` för att skapa en kopia av listB där varje element har konverterats till en sträng.

Använd `filter` för att skapa en lista som innehåller alla element i listB som har datatypen String eller Number.

Använd `find` för att hitta första elementet i listA som är större än 20.

Använd `reduce` för att räkna ut summan av alla element i listA.

Använd `filter` _och `reduce`_ för att konkatenera alla strängar i listB.

11 Skriv en funktion som returnerar en lista med tre slumpade heltal mellan 1 och 10. Ta reda på om listan innehåller några jämna tal, eller om rentav alla tal är jämna, med `some` och `every`. Skriv ut resultatet inklusive listan på konsolen.

Tips: Math.random()*10.


## 7 Git

Börja med att ladda ner Git till din dator.

[https://github.com/foundersandcoders/git-workflow-workshop-for-two](https://github.com/foundersandcoders/git-workflow-workshop-for-two) ← Obs! Man behöver vara med i en _organisation_ för att göra punkt 8 (tilldela en uppgift till teammedlem)

[https://www.codecademy.com/learn/learn-git](https://www.codecademy.com/learn/learn-git) - CodeAcademy-kurs om Git

.


## 8 HTML och CSS

Fler övningar


* [https://www.codecademy.com/catalog/language/html-css](https://www.codecademy.com/catalog/language/html-css)
* [https://www.w3schools.com/html/html_exercises.asp](https://www.w3schools.com/html/html_exercises.asp)  
* [https://www.khanacademy.org/computing/computer-programming/html-css/html-css-further-learning/e/quiz--validate-this-html](https://www.khanacademy.org/computing/computer-programming/html-css/html-css-further-learning/e/quiz--validate-this-html)
* [https://www.freecodecamp.org/](https://www.freecodecamp.org/)


### 1 Grundläggande HTML och CSS

1 Skapa en egen HTML-sida där du skriver upp vad vi gick igenom på första HTML-lektionen. Försök använda många olika HTML-element.

_Lägg upp övningarna 2-6 på din GitHub-sida när du är klar med dem. Index.html ska ha en länk till varje sida med namnet "exercise8.x" där X är övningens nummer._

2 Skapa en ny HTML-sida som är så lik [exemplet här](https://drive.google.com/open?id=0B6f5ao4RFptGV0ZlbnVndk56T2s) som möjligt. Fokusera på grunder och formatering. Det behöver inte vara samma text. Du kan använda vilken texteditor du vill.

3 Skapa en sida som är så lik [exemplet här](https://drive.google.com/file/d/0B6f5ao4RFptGUkF4MEJvcmFDSlk/view?usp=sharing) (textformatering) som möjligt.

4 Skapa en sida som är så lik [exemplet här](https://drive.google.com/file/d/0B6f5ao4RFptGVFZlTHZrR3AtY3M/view?usp=sharing) (tabell, kantlinjer) som möjligt.

5 Skapa en webbsida som är så lik [exemplet här](https://drive.google.com/file/d/0B6f5ao4RFptGYkd4alJXNXh3bGs/view?usp=sharing) (positionering) som möjligt. Använd elementet _div_ och sätt attributen `background-color, border, position, left, top, width, height` för att få rätt utseende. Tips: ändra storlek på webbläsarens fönster, zooma in/ut och scrolla, så ser du tydligt om du har gjort rätt.

6 Gör en ny version av övning 4 som använder flera _div_-element i stället för _table_. Tips: display: table;

7 Skapa en ny sida med namnet `html-exercises.html`. Flytta länkarna till övningarna dit, från `index.html`. Index-sidan ska vara en sida där du presenterar dig själv och de projekt du har arbetat med. Om du bygger vidare på den, kan du dela sidan till företag som du söker jobb hos. Några saker som är bra att ha med:

* presentation - vem är du
* länk till ditt LinkedIn-konto
* berätta om din utbildning
* berätta om det häftigaste projektet du har gjort hittills, med länk till GitHub-repot

8 Installera webbläsarna: Edge, Firefox och Chrome. Öppna dina GitHub pages i varje webbläsare och se om de ser likadana ut. Mac-användare ska testa i Safari också.

Kontrollera om sidorna validerar med [W3C Markup Validation Service](https://validator.w3.org/#validate_by_input).


### 2 CSS selektorer

1 Skriv HTML och CSS som testar följande uttryck. Du testar genom att lägga in en formatering, och se så att den syns på webbsidan. Kan du skriva HTML-kod som matchar alla selektorer?

Din HTML-kod behöver innehålla åtminstone taggarna p, div, span, ul, li och klasserna kategori, diagram och hello. När du är klar, jämför med en granne. Har ni löst uppgiften på samma sätt?


```
1  p span                  6  p > span
2  .kategori .diagram      7  .diagram span
3  p, div:hover            8  p.kategori
4  li + li                 9  li:last-child
5  [class*="sub"]          10 ul > li:nth-child(3).hello
```


2 Skapa en HTML-sida med en stor svart rektangel som är horisontellt centrerad och täcker ca 70% av skärmens bredd. Använd ett div-element och CSS för att placera det rätt. Lägg upp sidan på GitHub.

Skapa en vit rektangel som är inuti den svarta, men som följer med när man scrollar nedåt på sidan.

Skapa en grön rektangel som ligger delvis över den svarta och den vita, med hjälp av relativ positionering.

3 Gör en lista enligt exemplet nedan. Ändra den yttre listan till inline, så att elementen kommer efter varandra på en rad. Ta bort numreringen på båda listorna. Den inre listan ska ligga precis under "Redigera".

När man hovrar med musen över "Redigera" ska elementet få kantlinjer.

Extra utmaning: gör så att den inre listan bara visas när man hovrar med musen över "Redigera".



* Arkiv
* Redigera
    * Ångra
    * Gör om
    * Klipp ut
    * Kopiera
    * Klistra in
* Visa
* Infoga

4 Skapa en "header" som ligger högst upp på sidan och förblir synlig när man scrollar webbsidan. Lägg in en meny som fälls ner när man hovrar över den med musen. Tips: använd _ul_ för meny. Kombinera `:hover` med andra selektorer.

5 Skapa ett schackbräde (8x8 rutor som alternerar svart/vitt) med bredd och höjd 200px, inklusive kantlinjer. Använd en tabell. Tips: använd nth-child och border-collapse. `&lt;table style="border-collapse: collapse;">`

6 Gör ett element med kantlinjer och rundade hörn. Gör ett till element, som bara får rundade hörn när man hovrar över det. Tips: :hover, border-radius: ?px;

7 Hitta alla fel i följande HTML-kodexempel. (Minst 12 fel)


```
1.	<body>
2.	<style> ul { border: black solid 1px; } </style>
3.	<ul>
4.		<li>first item</li>
5.		<li><span class="strongly>second item</li>
6.	</ol>
7.	<div id="popup">Message that should be fixed in a corner<div/>
8.	<div id="layout">
9.		<main/>
10.			<section> <h1>The best images</h1>
11.				<p> Here's my favourite image:
12.					<img>http('server.com/image.gif')</img>
13.				</p> <!-- to do: add some more images
14.			</section>
15.		</main>
16.		<aside></aside>
17.	</div>
18.	<span>In conclusion: <p>To do</p> </span>
19.	</html>
```


8 Skapa två img-element för samma bild. Den första bilden ska vara en fix bredd som du bestämmer. Den andra bilden ska vara hälften så bred som webbsidan och ändra storlek när man ändrar webbläsarens bredd.

9 Gör en bild som fyller hela webbläsarens bredd men har en fast höjd.

10 Ta reda på vilka filformat som stöds i audio- och video-elementen. Skapa sedan ett element som spelar upp en ljudfil och ett som spelar upp ett videoklipp.

Du kan använda filer från [http://forverkliga.se/JavaScript/education/](http://forverkliga.se/JavaScript/education/)

Ladda ner filerna du använder så att de ligger i samma mapp som din HTML-sida.

11 Skriv CSS-selektorer som väljer ut…



1. alla tabellceller som är i andra raden i sin tabell
2. alla list items som finns i ett nav-element
3. alla element i en ordnad lista
4. alla div-element som kommer efter ett h1-element
5. alla bilder som finns i ett länk- eller i ett button-element

12 Rangordna följande CSS-selektorer med den som har högst prioritet överst. Räkna ut specificiteten för varje selektor.



1. p
2. div div
3. :hover
4. div > :hover
5. .one .two .three
6. .one > #something li
7. div.classy ul li
8. *

13 Skapa en meny med minst tre länkar. De ska ligga inuti en lista (ul eller ol) som i sin tur ska ligga inuti ett nav-element. Styla länkarna med CSS så att de ser ut som knappar och kommer på samma rad.

14 Skapa en webbsida med ett formulär. Tänk dig att det är en del av en webbshop, där man fyller i betalningsinformation. Du ska använda minst ett av varje av formulärelementen input, label, select, textarea och button. Använd CSS för att styla formuläret.

15 Gå till [http://www.csszengarden.com/](http://www.csszengarden.com/) och ladda ner exempelfilerna. Skapa en egen CSS-fil som gör om sidan som du vill. OBS: ändra inte i HTML-filen!

Den här uppgiften kan man lägga mycket tid på. Tanken är att du ska börja med den nu och återvända till uppgiften allteftersom vi går igenom nya saker i kursen.


### 3 Transition och transform

1 Skriv CSS som gör så att ett stycke text (&lt;p>) byter färg när musen hovrar över det.

2 Skapa ett button-element som växer när man hovrar över det med musen.

3a Skapa en textruta som är lite sned. (transform: skew) Positionera den längst till höger på sidan.

3b Lägg till en animering, så att textrutan glider in till vänsterkanten.

3c Gör dessutom så att texten rätar upp sig tills den har kommit fram.

4a Skapa en meny, där menyalternativen rullar ner när man hovrar över den. Dvs menyalternativen ska vara osynliga från början. Börja med att bara animera ~~display-egenskapen~~ _opacity_ eller _positionering med top/right/bottom/left_ för att göra så att de långsamt blir synliga.

4b Gör så att menyalternativen dessutom "faller ner". Från början (när de är osynliga) ska de vara ovanför menyn. När de slutar röra sig ska det översta elementet toucha nedre kanten av menyelementet.

4c Använd [z-index](https://www.w3schools.com/cssref/pr_pos_z-index.asp) för att se till att själva menyn alltid är överst.

5a Skapa en textruta som är roterad så att texten är vertikal. Det ska även finnas ett vanligt stycke med text. Placera den roterade textrutan till vänster om den vanliga texten och styla den så att den ser ut som en meny.

5b Gör så att textrutan åker ut till höger som en meny när man hovrar över den.


## 9 Layout med CSS
1 Skapa en webbsida där texten wrappar runt en bild som ligger antingen på höger eller vänster sida i en container (div). Använd _float_ och _clear_. Den ska ligga på GitHub. Exempel:

2 Skapa en webbsida med hjälp av _flexbox_, som är så lik den vänstra bilden i exemplet nedan som möjligt. Lägg till _media queries_ som ändrar layouten till den högra bilden om webbläsarens tillgängliga bredd är mindre än 800px.

3 Skriv en media query som gäller för skärmar med upplösning större än 1900. Det ska finnas en tag på sidan med textinnehållet "större än 1900px" som bara visas om skärmen är bredare än 1900px. Tips: zooma ut sidan för att testa, om du har en smalare skärm.

4 Skriv en media query som gäller för utskrift. Testa med webbläsarens förhandsgranskningsläge för utskrifter.

5 Skriv en media query som gäller för skärmar med upplösning mellan 500 och 800 pixlar.

6 Skapa en webbsida med ett div-element som har tre div som children. Den ska läggas upp på GitHub. Använd flex för att lägga ut dem på rad. Skriv en media query som ändrar så att elementen läggs ut vertikalt om webbläsaren är mellan 600 och 1050 pixlar bred.

7 Lägg till ett div-element på samma sida, som är 200 pixlar högt och fyller hela sidans bredd. Om webbläsaren är upp till 600 pixlar bred ska det ha vit bakgrundsfärg. Efter det ska bakgrunden byta färg varje gång storleken ökar med 150. Alltså 601-750, 751-900 och större än 900 pixlar.

8 Lägg till ett div-element på samma sida, som ska visa namnet (eller värdet) på den färg som visas i 1.2. (Tips: skapa fler div, använd display: none)

9 Skriv en html-fil som är länkad till två css-filer. Den ena filen ska användas om webbläsaren är bredare än 700 pixlar. Den andra css-filen ska användas om webbläsaren är smalare.

I html-filen ska det finnas en oordnad lista med fem element. Styla dem så de ser ut som fem rektanglar med kantlinje och bakgrundsfärg. Om webbläsaren är bredare än 700 pixlar ska boxarna ligga i en rad horisontellt. Om webbläsaren är smalare ska de ligga vertikalt under varandra.

10 Gör om webbsidan i uppgift 9.1 med hjälp av Bootstrap. Gör så att elementet som du gör float på flyter till vänster på små skärmar och till höger på större. Använd Bootstraps float-klasser i stället för vanlig CSS-float och media queries.

11 Undersök om det går att göra om webbsidan i uppgift 9.2 med hjälp av Bootstrap i stället för flex och media queries. Går det att göra alla webbsidor som man skulle kunna göra med flex och media queries även i Bootstrap, eller finns det begränsningar?

999 Fundera på och skriv ner med egna ord när man kan eller bör använda _float_, _flexbox_, _Bootstrap _och _CSS Grids_.


## 10 DOM-manipulation med JavaScript

I de här övningarna så behöver du bygga en webbsida med HTML och JavaScript. Använd JSBin, CodePen, eller en egen HTML-fil för att göra övningarna.

Obs! Om du använder en egen HTML-fil måste du köra din JavaScript efter att sidan laddats, med händelsen _window load_. Du kommer också att behöva använda klickhändelser för flera av uppgifterna.

1 Skapa en sida med en `div`. Ge div-elementet ett id. När sidan laddas ska du byta textinnehållet till något annat med hjälp av JavaScript och egenskapen innerHTML.

2 Skapa en sida med ett button-element och en lista. (ul eller ol) När man klickar på knappen ska det läggas till ett nytt li-element sist i listan med hjälp av `appendChild`. Ge button-elementet och listan varsitt id.

3 Skapa ett button-element med ett id och flera div-element som har samma CSS-klass. Skriv CSS för klassen. Gör så att alla div-element byter värde på `innerHTML` när man klickar på knappen. Använd `document.getElementsByClassName`.

Utöka exemplet så att när man klickar på knappen nästa gång ska den byta tillbaka värdet.

4a Skapa ett button-element som har ett id och en CSS-klass. När man klickar på knappen ska den byta till en annan CSS-klass.

4b Om man klickar en gång till ska knappen byta tillbaka till CSS-klassen den hade först.

5 Skapa ett button-element och flera section-element. När man klickar på knappen ska alla section-element byta CSS-klass, men du får inte använda id eller class på section-elementen. Använd `getElementsByTagName`.

6* Skapa ett button-element, en div och en lista med ul eller ol som har minst två element. När man klickar på knappen ska du skriva ut saker till div-elementet. (Alltså göra så att text läggs till inuti div-elementet.) Först ska du skriva ut hur många `childNodes` listan har. Skriv sedan ut vad varje "child node"-objekt har för värde på egenskapen `nodeName`. Poängen är att du ska jämföra egenskaperna `children` och `childNodes` och försöka upptäcka hur de skiljer sig åt.

Utöka funktionen så att den lägger till ett utropstecken sist på varje li-element.

7a Skapa en sida med ett button-element och ett annat element. Båda ska ha id. När man klickar på knappen ska det andra elementet tas bort. (inte göras osynligt, använd `element.removeChild`)

7b Utöka exemplet så att ett nytt element med samma id och textinnehåll som det borttagna läggs till på sidan, om man klickar en gång till på knappen.

8 Skapa en sida med ett button-element och två listor med flera element i den första. När man klickar på knappen ska det första li-elementet i den första listan flyttas till den andra listan. Tips: skapa en funktion som returnerar det första li-elementet i en html-lista.


## 11 Events {#11-events}

Det går lätt att "fuska" när man löser de här uppgifterna, genom att kopiera kod från nätet. Kopiera kod är inte förbjudet, men _ni lär er mindre_ på det än på att göra det själva. Meningen är att ni ska kunna lösa alla uppgifter med hjälp av _informationen i slides_. Däremot är det supertillåtet att arbeta tillsammans. Använd gärna verktyg som slack/discord för att diskutera uppgifterna med varandra när ni inte är i skolan.

_Observera att det är strängt förbjudet att använda <code>onclick="javascript"</code> i din HTML-fil!!</em>

1 Skapa en funktion som körs när HTML-dokumentet har laddats klart. Funktionen ska ändra textinnehåll på ett valfritt element på webbsidan. Du ska använda eventet _load_.

2 Skapa en HTML-sida med en button och ett div-element. Skapa en funktion som ska användas för att prenumerera på events. När funktionen anropas ska du skriva ut event.type och event.target till div-elementet. Samma funktion ska prenumerera både på sidans load-event och knappens klick-event.

3a Gör en sida med två knappar. På den ena ska det stå "+1" och på den andra "-1". Sidan ska också visa ett tal. När man klickar på +1 respektive -1 ska talet ändras. Talet ska finnas i en global variabel som heter `counterState`.

3b Gör en sida med två knappar. På den ena ska det stå "Start" och på den andra "Stopp". Stopp-knappen ska vara inaktiverad, använd `element.disabled=true` \
När man klickar på Start ska start-knappen inaktiveras och stopp-knappen aktiveras. När man klickar på Stopp ska det bli tvärtom.

4 Gör en sida som har en kryssruta med en label. När man klickar på label-elementet och kryssrutan blir ifylld ska ett annat element på sidan bli synligt. När man klickar igen ska elementet bli osynligt. Använd `element.style.display` för att göra saker synliga och osynliga. Använd absolut positionering för att undvika att de elementen som kommer efter byter plats när man togglar kryssrutan.

5 Gör en sida med "flikar". Ett system med flikar är när man har två eller flera element (använd div) som finns på samma plats på sidan, men bara ett är synligt åt gången. Det ska finnas knappar eller andra element (minst ett per div) som man klickar på för att göra motsvarande element synligt.

6 Gör en sida med element som ändrar för- eller bakgrundsfärg när musen rör sig över dem. Använd CSS-klasser och mouseenter och mouseleave events.

7 [utmaning] Gör ett element som ändrar storlek på texten inuti sig när muspekaren befinner sig över elementet, utan att hela elementet tar större plats. Det går att göra med bara CSS, men här ska du använda _mouse events_.

8 Gör en sida med ett textfält. När användaren håller nere en tangent ska du skriva ut i en div vilka knappar som hålls nere. Vilka events ska man använda? Tips: googla på MDN keyevent.

9 Gör ett textfält som validerar tal. När textfältet tappar fokus ska du kontrollera om texten i textfältet är ett giltigt tal. Du ska skriva ut resultatet i ett annat element som ligger i anslutning till textfältet, med grön text om det är ett giltigt tal och röd text annars.

10 Gör ett textfält som gör om texten medan man skriver, så att den gör om små bokstäver till stora. Använd keydown eller keypress event.

11 Poängen med den här uppgiften är att träna på att lägga till och ta bort event listeners.

Skapa en sida med två knappar och kryssrutor. Kryssrutorna ska vara bredvid varsin knapp, vara okryssade och ha texten "Event off". När man klickar på en kryssruta så att den blir ikryssad ska det läggas till en event listener på knappen bredvid, som lyssnar på klickhändelser. När man sedan klickar på knappen ska den ändra CSS-klass på något element på sidan. Byt även namn på kryssrutan.

Om användaren klickar igen på en kryssruta, för att ta bort krysset, så ska event listener på knappen tas bort.

Tips 1: Använd en label, så man kan klicka på kryssrutans text. Tips 2: Spara funktionerna som ska kopplas till knappens klickhändelse i variabler, annars kan du inte ta bort dem när du väl lagt till dem.

12 Skapa en sida med två kryssrutor. Idén är att det bara ska gå att kryssa i den ena rutan. Från början ska båda rutorna vara okryssade. När man klickar på den ena rutan ska den kryssas i om båda kryssrutorna är okryssade. Men om den andra rutan är ikryssad så ska klickhändelsen avbrytas med funktionen `event.preventDefault`. Visa gärna ett felmeddelande på sidan.

13 Skapa flera olika element med samma CSS-klass. Lägg till en funktion som lyssnar på klickhändelser på alla, utan att använda `getElementById`. Det ska alltså vara _samma _funktion för alla elementen. Funktionen ska byta bakgrundsfärg på det klickade elementet, med hjälp av `event.target`. Tips: använd parametern _event_.


## 12 AJAX

1 Gör en webbsida med en &lt;button> och en &lt;div>. När användaren klickar på knappen ska du göra ett GET request till följande URL och lägga resultatet i div-elementet. URL: "http://mardby.se/AJK15G/lorem_text.php"

2 Ändra koden så att den använder en querystring som är "numberOfWords=10" och URL "http://mardby.se/AJK15G/lorem_text_random.php"

3 Lägg till en textruta så att användaren kan välja vad numberOfWords ska ha för värde.

4 Ändra koden så att varje gång användaren klickar på knappen ska resultatet från AJAX-anropet läggas i en oordnad lista, &lt;ul>

5 Skapa en webbsida som använder [https://api.adviceslip.com/](https://api.adviceslip.com/), [https://api.chucknorris.io/](https://api.chucknorris.io/), [http://quotesondesign.com/wp-json/posts](http://quotesondesign.com/wp-json/posts), [https://placekitten.com/](https://placekitten.com/) eller [https://developers.giphy.com/docs/](https://developers.giphy.com/docs/) för att göra ett AJAX request och uppdatera webbsidan med resultatet.

6 Skapa en webbsida som använder ett oberäkneligt API: [https://forverkliga.se/JavaScript/api/unreliable.php](https://forverkliga.se/JavaScript/api/unreliable.php). Ibland returnerar det en sträng i JSON-format, ibland bara ett felmeddelande. Tips: använd try/catch.

7 Det finns länkar till API:er i Kursinfo under rubriken _Resurser_. Läs igenom dem och leta upp ett API som verkar intressant. Skriv ett JavaScript-program som hämtar data från API:et och presenterar på webbsidan. Tipsa andra i slack-kanalen #js1 om du hittar ett användbart API.


## 13 Promises

1 Skriv JavaScript som gör ett AJAX-anrop till https://forverkliga.se/JavaScript/api/simple.php med fetch. Gör så att resultatet skrivs ut i ett element på webbsidan.

2 Resultatet från uppgift 1 är i JSON-format. Gör om det till ett objekt. Skriv ut värdet på objektets egenskaper message och info. Resultatet ska bli en instruktion för hur man kan anropa API:et simple.php.

3 Se till att fetch körs från en button. Lägg till en textruta, där man ska kunna skriva in en querystring. Anropa API:et på de olika sätt som det stöder. Lägg till radio buttons, som användaren kan ha för att välja mellan användningsfallen: utan querystring, med rätt värde på _key_ och med _world_ i querystring.

4 Om du har gjort rätt så kommer du att antingen få veta vad klockan är på webbservern, få en lista med statistik över länder, eller få ett felmeddelande. Gör om programmet så att det visar landinformationen i en tabell. Använd antingen en riktig tabell eller display-table. Tips: använd higher order functions, map och forEach.

5 Skriv en executor-funktion (se slides om Promises) som räknar ut summan av två tal. Tänk på att den inte ska returnera värdet utan anropa succeed-funktionen. Använd sedan ett Promise för att anropa funktionen och räkna ut värdet.

6 Gör en HTML sida som gör ett fetch mot `https://pixabay.com/api/  ` (Det krävs en key, skapa konto för att få en) dokumentation för api:et finns på https://pixabay.com/api/docs/

Skapa ett img element för varje resultat och visa alla bilderna på sidan.

7 Utöka din fetch från uppgift 6 med att fetch körs när man klickar på en button. API:et kan ta en sökparameter, skapa ett input fält och skicka med värdet när du gör ett request. Utöka bildsökningen ytterligare med radio buttons för “image_type”.

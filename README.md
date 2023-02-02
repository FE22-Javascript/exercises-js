# exercises-js
Generella övningar i vanilla js

Övningar
JavaScript med ES6+
1 Interaktiva program
1 Klona repot https://github.com/folkuni-f22-js/console-template och kör script.js. Skriv om koden så att den frågar användaren vad man heter och var man kommer ifrån. Sedan ska det skrivas ut till användaren.
> node script.js
Who are you? Allan
Where do you live? Karlstad
Welcome Allan from Karlstad!


2 Skriv ett program som frågar användaren efter två tal och lägger ihop dem.
Tips: du behöver använda både question(…) och Number(…) 
> node script.js
Please enter a number: 10
Another one: 20
The sum is 30.


3 Skriv ett program som frågar användaren efter ett lösenord. Hitta på ett hemligt lösenord och spara det i en variabel. När användaren har skrivit in ett ord ska programmet jämföra med det sparade lösenordet och skriva ut om det var rätt eller inte. Använd en if-sats.


4 Skriv ett program som frågar användaren efter ett tal. Det ska skriva ut om talet är mindre än 100, lika med 100 eller större.


5a Använd följande kod för att generera ett slumpat tal mellan 1 och 100. Be användaren gissa vad talet är. Sedan ska programmet skriva ut om man gissade för högt, för lågt eller rätt.
let secret = Math.floor(Math.random() * 100) + 1

5b Upprepa 10 gånger, så att användaren får 10 försök.

5c Om man gissar rätt, så ska programmet sluta upprepa. Det ska visa hur många gissningar man behövde.
> node script.js
I have a secret number. What do you think it is? 20
Too low, try again. 35
Too high, try again. 21
21 is correct, well done! You guessed it in 3 tries.


6 Gör en miniräknare! Programmet ska be användaren om två tal, ett i taget. Sedan ska programmet berätta vad deras summa är.
> node calc.js
Please enter a number: 5
Another one: 10
The sum of 5+10 is 15.

6b Gör så att miniräknaren använder subtraktion, multiplikation och division också.
6c Programet ska fråga användaren vilket räknesätt man vill använda. Gör även så att miniräknaren kommer ihåg tidigare svar.
 
2 Datatyper och typomvandling
1 Vilka datatyper är följande uttryck? Tips: använd typeof för att kontrollera ditt svar. Arbeta gärna tillsammans med andra.
Exempelvis kan man svara att första uppgiften är datatypen Number och har värdet 1,01. Se till att du förstår varför resultatet blir som det blir.
1	1.01					          14	true + true + false
2	'false'					        15	5 && 8
3	null					          16	5 || 8
4	pancake				        	17	!5
5	1 / 0				          	18	!!5
6	false || true			    	19	true && false || false && true
7	"123" - 0				      	20	typeof (typeof true)
8	"1000" / 10				      21	1 + 2 * 3 + 4 * 5 + 6
9	123.4 - ''				    	22	2 < 3
10	'5' + "0" / '2'				23	'två' < 'tre'
11	'5' + "0" / '5' + 0				      24	17 === 17.0
12	'1' + '5' - '4' * '2' - '3'			25	17 === '17'
13	'kalle' - 5					            26	17.000000000000000000001 == 17
27	undefined || null || 0 || false || "foo"


2 Vilket värde kommer variabeln z att ha efter att respektive kodrad har körts?
Kör den här kodraden först: let x, y, z
z = 5;
z++;
--z;
z += 15;
x = 8;  y = 16;  z = y - x;
x = 10;  z = x++;
x = 2;  y = 5;  x = x + y;  y = x + y;  z = y;
 
3 Mera upprepning / iteration
För några av uppgifterna behöver du: Remainder (%) - JavaScript | MDN 

1a Skriv ett program som skriver ut talen 1 till 16 med hjälp av en loop. Gör sedan om det så att användaren får bestämma vilket tal programmet ska sluta på.

1b Skriv ett program som har talet 65536 i en variabel. Så länge som variabeln är större än 2 ska programmet loopa, skriva ut talet och sedan dela variabeln med 2.
Ändra sedan programmet, så att användaren kan ange vilket tal programmet ska börja med.


2 FizzBuzz är en vanlig uppgift på programmeringsintervjuer. Skriv ett program som skriver ut talen 1 till 20, med en twist:
Om talet är jämnt delbart med 3, skriv i stället ut strängen 'Fizz'
Om talet är jämnt delbart med 5, skriv ut 'Buzz'
Om talet är delbart med både 3 och 5, skriv ut 'FizzBuzz'
Exempel: 1, 2, Fizz, 4, Buzz, Fizz, 7… 


3 Skriv ett program som loopar och frågar användaren efter en sträng. Så länge som strängen inte är en tom sträng så ska programmet lägga ihop den med tidigare strängar, med ett mellanrum. Om användaren t.ex. har skrivit "ord1" tidigare och skriver "ord2" ska den nya strängen bli "ord1 ord2". Fortsätt loopa tills användaren skickar en tom sträng eller en punkt.


4 Skriv ett program som skriver ut de jämna talen 20 till 2 i den ordningen, med hjälp av en loop.
Alternativ ett: man måste inte öka loop-variabeln med 1. x = x + 2.
Alternativ två: använd modulo för att bara skriva ut jämna tal. if( x % 2 === 0 )

5 Skriv ett program som frågar användaren efter ett tal. Programmet ska loopa så länge som talet är större än 2. Sist i varje loop ska programmet skriva ut det nya talet. Varje loop ska programmet välja: 
Om talet är udda, multiplicera talet med 3 och lägg till 1
Om talet är jämnt, dela det med 2


6a Vad kommer följande kod att skriva ut?
let text = ''
for( let i=0; i<6; i++ ) {
    for( let j=0; j<8; j++ ) {
        if( (i + j) % 2 === 0)
            text += '#'
        else
            text += '.'
    }
    text += '\n';
}
console.log(text);

Med hjälp av koden ovan, skriv kod som skriver ut följande mönster på konsolen:
6b		6c		6d		6e		6f		6g
#.......	#.......	..###...	..#.....	....##..	#....#..
#.......	.#......	..###...	..#.....	....#...	.#..#...
#.......	..#.....	..###...	########	...##...	..##....
#.......	...#....	..###...	..#.....	..#.#...	..##....
#.......	....#...	..###...	..#.....	.#..#...	.#..#...
#.......	.....#..	..###...	..#.....	#...#...	#....#..

6h		6i		6j		6k
#.#.#.#.	........	.#O.#O.#	..#..#..
#.#.#.#.	.######.	O.#O.#O.	..#..#..
#.#.#.#.	.#....#.	#O.#O.#O	..#..#..
#.#.#.#.	.#....#.	.#O.#O.#	........
#.#.#.#.	.######.	O.#O.#O.	.#.#.#.#
#.#.#.#.	........	#O.#O.#O	#.#.#.#.
 
4 Funktioner
1 Vad skrivs ut av följande koder?

1a
1    function foo() {
2        console.log("test");
3    }
4    foo("hej");

1b
1    let a = foo(3);
2    console.log(a);
3    function foo(i) {
4        return i * i;
5    }

1c
1    console.log( foo(3, 5) );
2    function foo(x, y) {
3        return x * y;
4    }

1d
1    let x = 2;
2    let y = 3
3    let a = foo(foo(x) + foo(y));
4    console.log(a);
5    function foo(i) {
6        return 5 * i;
7    }

1e
1    let a = 5;
2    function foo(a) {
3        a++;
4    }
5    a += 2;   // a = a + 2
6    console.log(a);

1f
1    let foo = function(i) {
2        return 2*i*i;
3    };
4    let goo = function(x, y)
5    {
6        return x(y);
7    };
8    let a = goo(foo, 3);
9    console.log(a);



1.5 Skriv om funktionerna som:
1.5a Anonyma funktioner
1.5b Arrow functions
function f(x) {
    return x * 2 + 1
}
function g(x, y) {
    console.log(x + ', ' + y)
}


2a Skriv en funktion som tar tre parametrar: name, city och favoriteColor.  Den ska skriva ut informationen till konsolen i en fullständig mening. Exempel "Välkommen Namn från Göteborg med favvofärg blått". Skriv kod som anropar funktionen med lämpliga värden.
2b* Fråga användaren efter värden, som du anropar funktionen med.


3a Skriv en funktion med namnet add som lägger ihop två tal och returnerar resultatet.
3b Skriv en funktion med namnet multi som multiplicerar tre tal och returnerar resultatet. Vad händer om man anropar funktionen med färre än tre parametrar?
3c Skriv en funktion som tar fyra tal som parametrar. Den ska multiplicera de tre första och lägga ihop resultatet med den fjärde. Använd funktionerna add och multi.


4 Skriv en funktion som tar en parameter, som ska vara en sträng, och returnerar ett tal. Om det inte går att göra om parametern till ett tal ska funktionen returnera strängen oförändrad.
Varning! Alla jämförelser med NaN blir false. Man måste använda funktionen isNaN för att kontrollera ett värde. isNaN(NaN) === true
Tips: Number() och NaN.


5 Skriv en funktion som tar två parametrar och talar om ifall de är samma datatyp.
Tips: använd typeof.
Exempel: sameDataType('test', 'topp') == true  men  sameDataType(5, '5') == false.


6* Skriv en funktion som avrundar ett tal till två decimaler, med hjälp av Math.round. (Dokumentation på MDN.) Den bästa lösningen använder inga andra funktioner.
Tips: x * 100 / 100 === x.


7a Skriv en funktion med namnet paragraph, som tar en parameter. Den ska returnera en sträng enligt det här exemplet: paragraph('hej') == '<p>hej</p>' 

7b Skriv en funktion med namnet tag, som tar två parametrar. Den ska returnera en sträng som ser ut som en HTML-tag. Exempel: tag('banan', 'content') === '<banan>content</banan>


8 Skriv en funktion som säger hur många dagar en månad har. (Låtsas att skottår inte finns.) Funktionen ska ha en parameter, som är en sträng för varje månad. Strängen ska vara de tre första tecknen i månadens namn, dvs jan, feb, mar, apr osv. Funktionen ska returnera ett tal. Exempelvis så är daysInMonth("mar") == 31
Hur långa månaderna är: Lär dig år, kvartal, månader och datum · Kunskapat 


9a Skriv en funktion som returnerar de tre första tecknen i en sträng. Använd funktionen substring(startindex, endindex), som plockar ut en del av en sträng. Exempel:
'programmering'.substring(0,3) === 'pro'
'programmering'.substring(3,7) === 'gram'

9b Skriv en funktion som du kallar year som plockar ut året från en sträng i datumformat. Funktionen ska ta en parameter, som ska vara en sträng. Strängen ska alltid ha 10 tecken och följa mönstret 'YYYY-MM-DD'. Man ska kunna skriva year('2016-11-02') och få talet 2016 som resultat.

9c Skriv två funktioner med namnen month och day, som plockar ut månad respektive dag ur en datumsträng. Skriv med hjälp av dem en funktion med namnet daysBetween som räknar ut hur många dagar det är mellan två datum. Du kan förenkla funktionen genom att låtsas att alla månader har 30 dagar.
Exempel: daysBetween('2017-08-30', '2017-09-02') == 4 


10 Skriv en funktion som översätter en temperatur i Fahrenheit till Celsius. Den ska ta en parameter och returnera ett värde. Formeln finns på den här sidan.


11 Skriv en funktion som returnerar summan av de 100 första heltalen. Använd en loop. Förbättra sedan funktionen så att den tar en parameter, som är hur många tal som ska läggas ihop.


12 Skriv en funktion som tar en sträng som parameter och returnerar strängen baklänges.
Tips 1: använd funktionen string.substring och string.charAt.
Tips 2: använd en variabel, som du bygger på varje varv i loopen.


13 Skriv en funktion som returnerar ett slumpat heltal inom ett intervall. Dvs ett heltal mellan värdet på parametrarna min och max, inklusive.
function randomInt(min, max) {
    let r = Math.random()
    r = r * (max - min + 1)
    return Math.floor(r)
}


14* Extrauppgift. Skriv en funktion som tar ett tal som parameter och returnerar true om det är ett primtal. Ett primtal är ett heltal som bara är jämnt delbart med sig självt och 1. De första primtalen är 2, 3, 5, 7. 4 är inget primtal eftersom 4 / 2 == 2. 8 är inget primtal eftersom 8 / 2 == 4. 9 är inget primtal eftersom 9 / 3 == 3.
Obs! Det går att hitta färdiga lösningar på internet. Men om du plockar en färdig lösning så lär du dig mindre än om du försöker göra en själv.
När du hittat en fungerande lösning: vilket är det enklaste sättet att skriva funktionen? Hur effektiv är din lösning? Kan man göra den enklare eller snabbare?
 
5* Rekursion - funktion som anropar sig själv
1 Skriv en rekursiv funktion som räknar ut faktulteten n! för ett tal. Exempel:
1! === 1
2! === 2 * 1
3! === 3 * 2! === 3 * 2 * 1
4! === 4 * 3! === 4 * 3 * 2! === 4 * 3 * 2 * 1


2 Skriv en rekursiv funktion som räknar ut summan av talen från 1 till n.
function recurseSum(n)


3 Lös uppgift 6.12 med en rekursiv funktion.


4a Skriv en rekursiv funktion som räknar ut Fibonacci-tal.
// function fib(n)
fib(0) == 0
fib(1) == 1
fib(n) == fib(n-1) + fib(n-2)

4b Lös uppgiften med en loop.
// function fibLoop(n)
 
6 Objekt och modellering
1a Skapa ett objekt som innehåller information om en stad. Det ska innehålla till exempel stadens namn, antal invånare, latitud och longitud, vilket land den finns i.

1b Gör en funktion som heter move. När den anropas med objektet, ska den simulera att en person flyttar till en annna stad. Dvs antal invånare ska minskas med en.
function move(city) {
    // your code here
}



2 Skriv en funktion som returnerar en kopia av ett objekt. Alltså ett nytt objekt, som innehåller samma värden som det första.
Tips: spread syntax. En alternativ lösning är att använda for..of.


3* Skriv en funktion som skriver ut namnet på alla egenskaper (properties) i objektet från uppgift 1, och deras värden. Funktionen ska fungera på godtyckliga objekt.
Tips: for...in - JavaScript | MDN


4 Modellering handlar om att beskriva information på ett sådant sätt att man kan spara och hantera den med en dator. Detta är ofta något man gör tidigt, när man börjar med en webbapp.
Du ska skapa en variabel, med hjälp av objekt och listor, som innehåller all datan i beskrivningen. Prova att skriva ut värdet, för att kontrollera att du har korrekt syntax.
const incompleteExample = { teachers: 20 }
console.log(incompleteExample)

a En skola har 20 lärare och 256 elever. Den har adressen Skolgatan 1, Nyköping.

b Björn är lärare i musik, Benny har NO och teknik, Birgitta har artificell intelligens och svenska.

c Ett år har 12 månader. Följande har 31 dagar: januari, mars, maj, juli, augusti, oktober, december. Februari har 28 (29 om det är skottår) och övriga 30 dagar.

d Hasses Tamburinfabrik tillverkar musikinstrument. Den har tre tamburiner: T1 som kostar 200 kr, T2 för 250 kr och T3 för 320 kr. Fabriken har tre anställda: Hasse, Hedwig och Hermione.

e Hasses Tamburinfabrik får en ny kund: Horatio, som beställer en T1-tamburin. Horatio blir så nöjd så han lägger en ny beställning på två T2-tamburiner. (Av praktiska skäl måste beställningarna vara separata.)

f Ylvas bokaffär har följande produkter i sitt sortiment. Sagan om ringen, av J.R.R. Tolkien, som är klassad som fantasy. Stiftelsen, av Isaac Asimov, klassad som science fiction. Mistborn: the alloy of law, av Brandon Sanderson, klassade både som science fiction och fantasy. Samt slutligen The wheel of time, Robert Jordan, som de inte har hunnit klassificera än.
 
7 Listor / arrayer
1a Skapa en lista med talen 0 till 9. Skriv ut det femte elementet i listan med console.log.
1b Gör en funktion som byter plats på värdena 3 och 5 i listan.


2 Vad gör följande kod? Skriv ner din hypotes innan du testkör koden.
let list = [2]
for( let i=1; i<=5; i++ ) {
    let index = list[list.length - 1]
    let x = list[index]
    list.push(x + i)
}
console.log(list)


3 Hur kommer listan att se ut när koden körts? Skriv ner din hypotes innan du testkör koden.
let list = []
for( let i=1; i<=10; i++ ) {
    list.push(i)
    if( i > 3 && i < 6 ) {
        list.push(10 * i)
    }
}


4 Hur kommer list2 och list3 att se ut när koden körts? Skriv ner din hypotes innan du testkör koden.
let list1 = [2, 4, 8, 16, 32, 64, 128, 256, 512, 1024]
let list2 = [], list3 = []
for( let i=0; i<list1.length; i++ ) {
    if( list1[i] < 100 ) {
        list2.push( i )
        list3.push( list1[i] )
    }
}


5 Hur kommer list2 att se ut när koden körts? Skriv ner din hypotes innan du testkör koden.
let list1 = [10, 11, 12, 13, 14, 15,16]
let list2 = []
for( let i=0; i<list1.length; i++ ) {
    list2.push( list1[i] + 10 )
}


6 Skapa en lista med 10 slumpade tal mellan 20 och 30. Du kan använda funktionen randomInt från uppgift 6.13. Sedan ska du skapa funktioner som:
a Returnerar det största värdet i en lista. Testa den på din slumpade lista, tre gånger.
b Returnerar det minsta värdet.
c Returnerar medelvärdet.
d Returnerar det näst största värdet.

Tips: börja med att lösa uppgiften utan en funktion, om det är enklare.


7 Skapa en lista med talen mellan 1 och 100. Skriv en funktion som räknar ut summan av alla tal i  en lista. Använd funktionen för att kontrollera din lista. (Rätt summa är 5050.)


8 Orden i två kända visor har hamnat baklänges, i en lista. Skriv funktioner som:
8a Skapar en ny lista där orden kommer i rätt ordning.
8b Ändrar i den befintliga listan så orden kommer i rätt ordning.
let nautic = ['körde', 'jag', 'båt', 'min', 'natt', 'kulen', 'en']
let amphibic = ['se', 'att', 'lustiga', 'är', 'grodorna', 'små']



9 Skriv kod som svarar på frågorna med hjälp av higher order functions; forEach, map, find och filter. Man kan lösa alla frågor med forEach, eftersom man kan lösa dem med vanliga for-loopar. Men använd i stället de andra funktionerna så långt det är möjligt, eftersom de är bättre lämpade. Prova gärna att lösa någon av uppgifterna på flera sätt. (På vissa av uppgifterna kan man även använda reduce, som är mer komplicerad.)
Data till uppgiften:
const worldData = [
 { "name": "United Kingdom", "continent": "Europe", "population": 65270121, "pFemale": 0.508 },
 { "name": "Republic of Ireland", "continent": "Europe", "population": 4708209, "pFemale": 0.499 },
 { "name": "Australia", "continent": "Oceania", "population": 24482205, "pFemale": 0.502 },
 { "name": "Taiwan", "continent": "Asia", "population": 23522296, "pFemale": 0.501 },
 { "name": "Uruguay", "continent": "South America", "population": 3446772, "pFemale": 0.517 },
 { "name": "Morocco", "continent": "Africa", "population": 35010005, "pFemale": 0.510 },
 { "name": "Nigeria", "continent": "Africa", "population": 188688090, "pFemale": 0.494 },
 { "name": "Zimbabwe", "continent": "Africa", "population": 16051510, "pFemale": 0.507 },
 { "name": "China", "continent": "Asia", "population": 1381321335, "pFemale": 0.488 },
 { "name": "Mexico", "continent": "North America", "population": 129386794, "pFemale": 0.507 },
 { "name": "Canada", "continent": "North America", "population": 36446796, "pFemale": 0.504 },
{ "name":"Czech Republic", "continent":"Europe", "population":10556351, "pFemale": 0.509 },
 { "name": "Iceland", "continent": "Europe", "population": 332631, "pFemale": 0.496 }
];

a Skriv ut namnet på alla länder. (Här kan du använda forEach.)
a Vilka länder finns det data för? Tips: använd map för att skapa en ny lista med bara namnen på länderna.
b Vilket är första afrikanska landet i listan? Tips: filter kan välja ut alla afrikanska länder. Första elementet ligger på index noll i listan.
c Hur många kvinnor finns det i Australien? Tips: börja med filter. Sedan kan du använda forEach eller reduce.
d Gör en ny lista som innehåller egenskaperna "name", "men" och "women" med hjälp av map.
Tips: räkna ut antalet kvinnor i UK som x = 65270121 * 0.508. Avrunda med Math.round. Antalet män är population - x.
e Hur många bor det sammanlagt i Europa? Tips: samma sorts fråga som c.
f Hitta första landet som har över 100 miljoner invånare. Tips: find             .
g Finns det något land med färre än 49% kvinnor?
h Hur många bor det på Island? Tips: använd find för att hitta landsobjektet.

 
8 DOM-manipulation / vanilla JS
1 Skapa en ny webbsida. När sidan laddas, ska du lägga till ett element till webbsidan:
<p> Dynamiskt! </p>


2 Skapa en webbsida med ett button- och ett p-element. När man klickar på knappen ska texten i p-elementet uppdateras, så att den visar hur många gånger man har klickat på knappen.


3a Gör en webbsida som ska innehålla en lista (ul/ol) med ord. Det ska även finnas ett input-fält och en button. När användaren skriver ett ord i input-fältet och klickar på knappen, ska ordet läggas till i listan.
3b Input-fältet ska tömmas när man lagt till ett värde.
3c knappen ska bara gå att klicka på, när fältet inte är tomt.
3d Gör så att man även kan använda enter-tangenten för att lägga till ett ord.
.


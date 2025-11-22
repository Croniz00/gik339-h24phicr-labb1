/* Uppgift 2 - Variabler och scope */

{
    let a =10;
    const b = 20;
    var c = 30;

console.log("Inuti blocket", a, b, c);
}

console.log("Utanför blocket - var syns fortfarande:", c);

// consol.log(a); ger fel (let syns inte utanför sitt block)
//consol.log(b); ger fel (const syns inte utanför sitt block)

/* reflektion uppgift 2:

1. Var är inte blockscope, utan function/global scope. Därför är c tillgänligt utanför blocket.
   let och const är blockscope. Därför är a och b endast tillgänligt initu blocket.

2. Consol.log före blocket hittar inga varibalerna eftersom de är inte deklarerade än.
   Men inuti blocket fungerar alla 3. Efter blocket funkar bara var-variablen eftersom den inte är blockscope.
   */


/* Uppgift 3 - Jämförelser */

console.log( "'3' == 3:", '3'== 3);  //True 
console.log( "'3' === 3:", '3'=== 3); //False

console.log("NaN === NaN:", NaN === NaN); //false
console.log("null == undefined:", null == undefined); //True
console.log("null === undefined:", null === undefined); // False

let isUndefinedTruthy = undefined ? "Truthy" : "Falsy";
console.log( "undefined är:", isUndefinedTruthy);

/* reflektion uppgift 3:
1. == gör automatisk omvandling ("3" - 3).
   === jämför båda typ och värde.

2. I en ternary operator används värdet direkt som sant eller falskt.
   undefined är ett falskt (falsy) värde.

3. NaN = ogiltigt tal.
   undefined = saknar värde.
   null = "tomt" värde som någon programmerat in avsikligt.
*/

/* uppgift 4 - Funktioner */

//En enkel funktion:

function greet(name) {
    return "hej" + name;
}

// vi anropar funktionen (Glöm inte space mellan " och oscar så det ser bättre ut")
console.log(greet(" Oscar"));

//En variabel med samma nman som parametern
let name = "Anna";

console.log("Global variabel name:", name);

function testName() {
    console.log("Inuti funktionen, global name:", name);

}

testName();

/* Reflektion uppgift 4:
1. Funktionsdeklaration (function greet...) kan användas innan den skrivs i koden-
   Funktionsuttrycj och arrowfunktioner måste skrivas först innan de anropas.

2. Funktionsdeklaration hoistas - du kan kalla på dem innan de definieras.

3. Parametern name i greet påverkas inte dne globala variabeln name.
   Det blir två olka variabler med amma name.

4. Parameter = namnet i funktionens parenteser.
   Argument = värdet man skickar in när man anropar funktionen.
   Variabel = något du skapat med let/const/var.


*/
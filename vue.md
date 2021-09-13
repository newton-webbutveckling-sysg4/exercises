# Övningar ramverk: Vue

## 1 Data properties och metoder
*Förkunskaper: data properties, mustacher i template, v-show, metoder.*

1 Skapa ett nytt Vue-projekt. Det ska vara Vue 3 men du behöver inga tillval. Leta upp Hello World-komponenten och rensa den. Gör så att appen visar en rubrik, till exempel "Hello world".

2a Bygg en räknare. Komponenten ska visa talet 10. Lägg till en button på komponenten. När man klickar på talet ska värdet som visas öka med 1.

2b Lägg till buttons för att minska värdet och återställa till det ursprungliga värdet 10.

3a Ta reda på hur man använder direktivet `v-show`. Använd det för att göra en button som togglar ett annat HTML-element. När appen visas ska man se texten: "Now you see me". När man klickar på knappen ska elementet bli osynligt.

3b Ändra så att man kan klicka flera gånger på knappen för att göra elementet med texten synligt igen.

3c Lägg till ett element med texten "Now you don't". Det ska synas när texten i 3a *inte* syns.

4a Gör en button som kan vara i två lägen. Den ska börja med texten "Lights on". När man klickar på den ska texten bytas till "Lights off".

4b Ta reda på hur man kan använda data properties för att ange CSS-klass. Styla button så att den byter till ett mörkare färgschema när den är "lights off".

5a Bygg en carousel. En "karusell" är en ganska vanlig UI-komponent som visar en bild, men låter användaren bläddra till nästa. (Du kan använda p-element med text i, om du inte vill leta efter bilder.) Första versionen ska ha minst två bilder och två knappar underst med texten: Nästa respektive Föregående. Tips: du behöver två data properties.

5b Lägg till att komponenten visar vilken bild man är på och hur många det finns. Till exempel kan man visa en text: "Bild 3 av 5".

5c Gör så att Nästa och Föregående-knapparna bara är klickbara om man inte är på sista respektive första bilden.


## 2 Skicka data mellan komponenter

1 Lägg din räknare i en egen komponent. (uppgift 1.2 ovan) Testa att använda den nya komponenten tre gånger i App.vue. Kontrollera att du har tre oberoende räknare.

2a Gör en komponent som visar en `<span>` med text. Texten ska skickas från dess parent, med hjälp av props.

2b När man klickar på `<span>` ska elementet bytas mot ett input-fält. Man ska kunna ändra texten genom att skriva i input-fältet. När man klickar utanför fältet ska det bytas tillbaka till ett `<span>` element. (Tips 1: använd v-model. Tips 2: blur-händelsen.)

2c Gör så att komponenten emittar ett event när man ändrat texten.

2d* Gör så att man kan trycka Enter i input-fältet också.

3 Skapa komponenter av uppgift 2.3, 2.4 och 2.5.

4a Fruktsallad - gör en app som visar två listor. Den första ska ha namn på frukter, den andra ska vara tom. När man klickar på ett fruktnamn i första listan, ska den frukten läggas till den tomma listan.

4b Nu ska frukterna flyttas, alltså inte ligga kvar utan tas bort ur den första arrayen.

4c Lägg listorna i varsin komponent, om du inte redan gjort det. Tips: kan du använda samma komponent till båda listorna?

5 Gör [MyTunes](webbprojekt.md) som en Vue-app. Lägg till nya komponenter när filerna blir för stora. (Försök hålla dina komponenter under 200 rader kod.)


## 3
1a Skapa en Vue-app som skickar ett GET request till https://forverkliga.se/JavaScript/api/simple.php?world. Den ska visa informationen i en lista eller en tabell. (`<ul>` eller `<table>`.) Visa namn och befolkningsmängd.

1b Formatera datan så att befolkningen visas i antal miljoner, med två decimaler. (Tips: Number.toFixed(2) och Math.round() är användbara. )

2 Skapa en Vue-app som skickar ett request till [sunrise/sunset API](https://sunrise-sunset.org/api). Den ska visa när solen går upp och ner idag i Göteborg.

3 URL:en https://forverkliga.se/JavaScript/api/crud.php är ett API som simulerar en databas. Gör en Vue-app som använder det för att låta användaren spara data i databasen. Antingen kan du utöka MyTunes så att det använder API:et, eller hitta på något eget.

4 https://github.com/public-apis/public-apis innehåller länkar till öppna API:er. Bygg en Vue-app som använder något intressant API. (Tips: välj ett med Auth=No/apiKey och CORS=Yes.)

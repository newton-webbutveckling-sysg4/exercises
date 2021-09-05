# Övningar ramverk: Vue

## 1 Data properties och metoder
*Förkunskaper: data properties, mustacher i template, v-show, metoder.*

1 Skapa ett nytt Vue-projekt. Det ska vara Vue 3 men du behöver inga tillval. Leta upp Hello World-komponenten och rensa den. Gör så att appen visar en rubrik, till exempel "Hello world".

2a Bygg en räknare. Komponenten ska visa talet 10. Lägg till en button på komponenten. När man klickar på talet ska värdet som visas öka med 1.

2b Lägg till buttons för att minska värdet och återställa till det ursprungliga värdet 10.

3a Ta reda på hur man använder direktivet `v-show`. Använd det för att göra en button som togglar ett annat HTML-element. När appen visas ska man se texten: "Now you see me". När man klickar på knappen ska elementet bli osynligt.

3b Ändra så att man kan klicka flera gånger på elementet för att göra elementet med texten synligt igen.

3c Lägg till ett element med texten "Now you don't". Det ska synas när texten i 3a *inte* syns.

4a Gör en button som kan vara i två lägen. Den ska börja med texten "Lights on". När man klickar på den ska texten bytas till "Lights off".

4b Ta reda på hur man kan använda data properties för att ange CSS-klass. Styla button så att den byter till ett mörkare färgschema när den är "lights off".

5a Bygg en carousel. En "karusell" är en ganska vanlig UI-komponent som visar en bild, men låter användaren bläddra till nästa. (Du kan använda p-element med text i, om du inte vill leta efter bilder.) Första versionen ska ha minst två bilder och två knappar underst med texten: Nästa respektive Föregående. Tips: du behöver två data properties.

5b Lägg till att komponenten visar vilken bild man är på och hur många det finns. Till exempel kan man visa en text: "Bild 3 av 5".

5c Gör så att Nästa och Föregående-knapparna bara är klickbara om man inte är på sista respektive första bilden.


## 2 Skicka data mellan komponenter

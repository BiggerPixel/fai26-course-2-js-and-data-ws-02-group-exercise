# Mål

Vi bygger en varukorgskalkyl som visar produkt, delsumma, frakt och totalsumma. Vi använder ett objekt, arrow functions och `if`-satser för att skapa hela flödet från data till gränssnitt.

# Startpunkt

Vi arbetar i grupper med dessa filer:

- `index.html` innehåller det färdiga gränssnittet och laddar Tailwind CSS v4.
- `script.js` innehåller varukorgens data och tydliga platser där logiken ska skrivas.

Vi öppnar `index.html` i webbläsaren och har DevTools Console synlig. Ingen installation behövs.

# Regler för varukorgen

- Delsumman är `quantity * unitPrice`.
- En medlem får fri frakt.
- En varukorg med en delsumma på minst `500` får också fri frakt.
- Annars kostar frakten `49` kronor.
- Totalsumman är delsumma plus frakt.

Med startvärdena ska kalkylen visa:

- Produkten `Webbkamera`.
- Antalet `2`.
- Delsumman `498 kr`.
- Frakten `49 kr`.
- Totalsumman `547 kr`.

# Del 1: Räkna ut delsumman

1. Läs objektet `cart` i `script.js`.
2. Färdigställ `calculateSubtotal`. Funktionen tar emot `quantity` och `unitPrice` och returnerar delsumman.
3. Anropa funktionen med värden från `cart` och spara returvärdet i `subtotal`.
4. Skriv ut `subtotal` i Console. Resultatet ska vara `498`.

# Del 2: Bestäm frakten

1. Färdigställ `getShippingCost`. Funktionen tar emot `subtotal` och `isMember`.
2. Använd `if` och `else` för att följa fraktreglerna.
3. Anropa funktionen och spara returvärdet i `shippingCost`.
4. Skriv ut `shippingCost` i Console. Resultatet ska vara `49`.

Här är det upp till oss själva att i gruppen diskutera hur villkoren ska ordnas. Vi använder dessa frågor:

- Vilket villkor kontrollerar medlemskapet?
- Vilket villkor kontrollerar delsumman?
- När ska funktionen returnera `49`?

# Del 3: Räkna ut totalen

1. Färdigställ `calculateTotal`. Funktionen tar emot `subtotal` och `shippingCost`.
2. Returnera summan av värdena.
3. Anropa funktionen och spara returvärdet i `total`.
4. Skriv ut `total` i Console. Resultatet ska vara `547`.

# Del 4: Visa kalkylen

Visa dessa värden i rätt HTML-element med `textContent`:

- `cart.productName`.
- `cart.quantity`.
- `subtotal` följt av ` kr`.
- `shippingCost` följt av ` kr`.
- `total` följt av ` kr`.

När sidan laddas ska hela varukorgskalkylen visas utan fel i Console.

# Om resultatet inte stämmer

Om ett värde blir fel kontrollerar vi först argumenten i funktionsanropet, funktionens `return` och ID:t i HTML-elementet där värdet visas.

# Kontroll när vi är klara

Vi är klara när:

- Objektet `cart` levererar produktdata till kalkylen.
- Tre arrow functions returnerar delsumma, frakt och totalsumma.
- `getShippingCost` använder `if` och `else` för fraktreglerna.
- Gränssnittet visar `Webbkamera`, `2`, `498 kr`, `49 kr` och `547 kr`.
- Console visar de tre beräknade värdena utan fel.

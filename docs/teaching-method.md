# Tanítási módszertan

## Cél

A DelphiTeacher nem feladatmegoldó automatizmus, hanem mentorálási rendszer. A tanuló aktív résztvevő: elemez, dönt, kódol, tesztel és javít.

## Oktatási ciklus

### 1. Diagnose

A mentor először felméri, hogy a probléma mely rétege okozza a nehézséget:

- programozási logika;
- Object Pascal szintaxis;
- Delphi RTL/VCL/FMX API;
- IDE használat;
- adatbázis/SQL;
- architektúra;
- debugging;
- meglévő kód értelmezése.

Ugyanazt a hibát másképp kell tanítani, ha a tanuló az algoritmust nem érti, mint ha csak egy `for` ciklus Delphi-szintaxisa hiányzik.

### 2. Explain

A mentor egy új fogalmat a következő sorrendben magyarázzon:

1. mire való;
2. mikor használjuk;
3. hogyan néz ki Delphiben;
4. rövid példa;
5. gyakori hiba;
6. kis gyakorlófeladat.

### 3. Demonstrate

Új koncepció esetén használható kis, izolált példa. A példa ne tartalmazzon egyszerre több olyan új elemet, amelyet még nem tanultunk.

### 4. Guided practice

A mentor adjon részfeladatot és szükség esetén fokozatos hintet.

Példa:

**Feladat:** számold meg egy `TArray<Integer>` pozitív elemeit.

Első hint:

> Milyen ciklussal tudnál minden elemen egyszer végigmenni?

Második hint:

> Használhatsz `for..in` ciklust és egy számláló változót.

Csak ezután jöjjön kódváz.

### 5. Independent practice

Az adott koncepció után legyen olyan feladat, amelyet a tanuló már lényegében önállóan old meg.

### 6. Review

A mentor értékelje:

- helyesség;
- olvashatóság;
- Delphi idiomatikusság;
- memóriakezelés;
- exception safety;
- tesztelhetőség.

## „Miért?” szabály

Fontosabb kódmódosításnál legalább egyszer válaszoljunk arra, hogy **miért** ezt a megoldást használjuk.

Nem elegendő:

> Tedd bele `try..finally` blokkba.

Jobb:

> A `TStringList` manuálisan létrehozott objektum. Ha a feldolgozás közben exception keletkezik, a `finally` akkor is lefut, ezért garantálja az objektum felszabadítását.

## Fogalom → példa → módosítás

Hatékony minta:

1. fogalom bemutatása;
2. minimális működő példa;
3. a tanuló módosítja a példát.

Így elkerülhető a passzív copy-paste tanulás.

## Hibák kezelése

A fordítási hibákat tananyagként kell használni.

A mentor először magyarázza el:

- compiler error vagy runtime error;
- melyik sorhoz kapcsolódik;
- mit jelent az üzenet;
- milyen szabály sérült.

Csak utána következzen a javítás.

## Debugger-központú tanítás

A tanuló ne csak `ShowMessage` alapú hibakeresést tanuljon.

Fokozatosan használjuk:

- breakpoint;
- Step Into;
- Step Over;
- Run to Cursor;
- Evaluate/Modify;
- Local Variables;
- Watches;
- Call Stack;
- exception breakpointokat.

## Kódkiegészítés vs. generálás

Ha a tanuló már elkezdett egy megoldást, elsőként az ő struktúráját próbáljuk továbbvinni. Ne cseréljük le automatikusan teljesen más architektúrára.

Refaktor csak akkor javasolt, ha annak konkrét előnye van, például:

- csökkenti a duplikációt;
- egyszerűsíti a kontrollfolyamot;
- javítja a tesztelhetőséget;
- megszüntet resource leaket;
- elválasztja az UI-t az üzleti logikától.

## Valós vállalati példák

A kezdő példák után fokozatosan használjunk olyan feladatokat, mint:

- CSV rendeléslista beolvasása;
- cikkszám validálása;
- BOM adatok összevetése;
- adatbázisból riport lekérdezése;
- Excel export;
- fájlok feldolgozása mappából;
- JSON konfiguráció;
- SQL query paraméterezése;
- VCL form és üzleti logika szétválasztása;
- régi eljárás debugolása.

A konkrét céges kód vagy bizalmas adat használatakor a mentor ösztönözze a minimalizált, anonimizált reprodukció készítését.

## Tempó

Egy oktatási lépés lehetőleg egy fő új koncepció köré épüljön.

Ha egy feladat egyszerre igényel például:

- classokat;
- interfészeket;
- generics-et;
- FireDAC-ot;
- JSON-t;

akkor a mentor bontsa modulokra, és határozza meg a tanulási sorrendet.

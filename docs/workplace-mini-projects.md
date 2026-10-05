# Munkahelyi mini-projektek – mentor workflow

Ez a dokumentum a szakmai vezetőtől kapott valódi fejlesztési feladatok közös feldolgozásának munkamódszerét írja le.

## Alapelv

A mini-project tulajdonosa a tanuló. A DelphiTeacher nem veszi át a fejlesztést, hanem segít a követelmény megértésében, tervezésben, implementációban, debuggingban, code review-ban és átadásban.

A cél kettős:

1. a munkahelyi feladat haladjon;
2. minden feladatból újra felhasználható Delphi tudás épüljön.

## 1. Intake – amikor megérkezik a feladat

A feladat eredeti szövegét lehetőleg változtatás nélkül rögzítsük.

Az első elemzésben különítsük el:

- üzleti cél;
- elvárt eredmény;
- bemenet;
- kimenet;
- meglévő rendszer/kód;
- adatforrás;
- technológiai megkötés;
- határidő, ha releváns;
- elfogadási feltétel;
- ismeretlen vagy kétértelmű pontok.

A mentor ne találja ki a hiányzó üzleti szabályokat.

## 2. Biztos tény / feltételezés / kérdés

Minden bizonytalan projektben használható három kategória:

### Biztosan tudjuk

A specifikációból, meglévő kódból, adatbázisból vagy a szakmai vezető közléséből igazolható tény.

### Feltételezés

Olyan munkahipotézis, amely segít a továbblépésben, de még nincs megerősítve.

### Tisztázandó

Olyan kérdés, amelyet a kódból nem lehet biztonságosan eldönteni, ezért a szakmai vezetővel kell tisztázni.

## 3. Technikai felbontás

A teljes feladatot kis munkacsomagokra bontjuk. Egy munkacsomag lehetőleg egyetlen világos célt tartalmazzon.

Tipikus bontás:

1. meglévő projekt feltérképezése;
2. releváns unit/form/class azonosítása;
3. adatforrás megértése;
4. domain/üzleti szabály leírása;
5. szükséges Delphi fogalmak azonosítása;
6. algoritmus vagy adatfolyam megtervezése;
7. minimális működő implementáció;
8. integráció;
9. exception és hibakezelés;
10. tesztelés;
11. cleanup/refactor;
12. átadás.

## 4. Munkamenet

Egy implementációs körben lehetőleg egy problémára koncentráljunk.

Ajánlott ciklus:

**Understand → Plan → Implement → Run → Observe → Debug → Review → Commit**

A mentor minden körben csak annyi segítséget adjon, amennyi a következő érdemi lépéshez szükséges.

## 5. Ha kódot küldök

A review ne egyszerű javított kód legyen.

A mentor vizsgálja:

- helyesség;
- olvashatóság;
- Delphi idiomatikusság;
- típusbiztonság;
- objektumélettartam;
- exception safety;
- komponens ownership;
- SQL/adatbázis kezelés;
- edge case-ek;
- karbantarthatóság.

A problémákat súlyosság szerint érdemes jelölni:

- **BLOCKER** – hibás működés/adatvesztés/komoly kockázat;
- **IMPORTANT** – javítandó tervezési vagy megbízhatósági probléma;
- **IMPROVEMENT** – jobb megoldás, de nem blokkolja a működést;
- **STYLE** – olvashatóság vagy konvenció.

## 6. Ha elakadok

A mentor először az elakadás típusát azonosítsa:

- nem értem a követelményt;
- nem tudom, hol van a releváns kód;
- nem ismerem a szükséges Delphi elemet;
- tudom az algoritmust, de nem tudom Object Pascalban kifejezni;
- compiler error;
- runtime exception;
- rossz eredmény;
- adatbázis/SQL probléma;
- komponens/UI probléma;
- architekturális döntés.

Ezután célzott segítséget adjon, ne általános tutorialt.

## 7. Debugging napló

Komolyabb hibánál rögzítsük röviden:

- elvárt viselkedés;
- tényleges viselkedés;
- reprodukció lépései;
- hibaüzenet/exception;
- releváns input;
- breakpoint helye;
- megfigyelt változóértékek;
- gyökérok;
- javítás;
- regressziós teszt.

Ez később személyes hibakeresési tudásbázissá válhat.

## 8. Definition of Done

A mini-project nem attól kész, hogy egyszer lefutott.

Minimum ellenőrzés:

- [ ] Az eredeti követelmény teljesül.
- [ ] Normál eset működik.
- [ ] Releváns edge case-ek kezelve vannak.
- [ ] Hibás input nem okoz kontrollálatlan állapotot.
- [ ] Resource/objektum életciklus rendben van.
- [ ] Adatbázis műveletek biztonságosak.
- [ ] Nincs nyilvánvaló regresszió.
- [ ] A kód érthető és illeszkedik a meglévő projekt stílusához.
- [ ] A tanuló el tudja magyarázni a megoldást.

## 9. Átadás a szakmai vezetőnek

A tanuló legyen képes röviden összefoglalni:

1. mi volt a feladat;
2. hol történt a módosítás;
3. hogyan működik a megoldás;
4. milyen döntéseket hozott és miért;
5. hogyan tesztelte;
6. van-e ismert korlát vagy nyitott kérdés.

Ha ezt nem tudja elmagyarázni, a feladat tanulási szempontból még nincs lezárva.

## 10. Tudáskinyerés a projektből

A lezárt mini-projectből különítsük el a projekt-specifikus és az általánosítható tudást.

Példa:

**Projekt-specifikus:** egy adott céges tábla vagy form működése.

**Általánosítható:** `TQuery`/FireDAC paraméterezés, `try..finally`, dataset iteráció, CSV export, dependency separation, debugger használata.

Az általánosítható részt érdemes hozzáadni a tanulási progresshez és későbbi gyakorlófeladatokhoz.

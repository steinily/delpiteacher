# Delphi 13 tanulási útvonal

## Cél

A cél nem pusztán az Object Pascal szintaxis megtanulása, hanem olyan gyakorlati tudás megszerzése, amellyel meglévő vállalati Delphi alkalmazások olvashatók, módosíthatók, debugolhatók és fokozatosan önállóan fejleszthetők.

## 0. szint – IDE és programstruktúra

### Témák

- Delphi 13 IDE
- Project / Project Group
- `.dpr`, `.pas`, `.dfm`
- unit felépítése
- `interface` / `implementation`
- `uses`
- build / compile / run
- debugger alapok

### Kimeneti kompetencia

A tanuló képes legyen létrehozni, lefordítani és debugolni egy minimális Delphi projektet.

---

## 1. szint – Object Pascal alapok

### Témák

- változók
- konstansok
- erős típusosság
- alap adattípusok
- operátorok
- `if`, `case`
- `for`, `for..in`, `while`, `repeat`
- procedure / function
- paraméterek
- scope
- stringkezelés

### Gyakorlati irány

Kis adatfeldolgozási feladatok, nem GUI-központú példák.

### Kimeneti kompetencia

A tanuló önállóan meg tud írni kisebb függvényeket és ciklusos/feltételes feldolgozásokat.

---

## 2. szint – Strukturált adatok

### Témák

- array
- dynamic array
- `TArray<T>`
- `record`
- enum
- set
- `TList<T>`
- `TDictionary<TKey,TValue>`
- `TStringList`

### Kimeneti kompetencia

A tanuló képes megfelelő adattípust választani egyszerű üzleti problémákhoz.

---

## 3. szint – OOP Delphiben

### Témák

- class
- object lifecycle
- constructor / destructor
- visibility
- property
- inheritance
- virtual / override
- interface
- composition
- ownership

### Kiemelt kérdés

Minden objektumnál:

> Ki hozza létre és ki szabadítja fel?

### Kimeneti kompetencia

A tanuló képes kisebb domain modelleket létrehozni és az objektumok életciklusát biztonságosan kezelni.

---

## 4. szint – Exception és resource management

### Témák

- `try..finally`
- `try..except`
- `raise`
- saját exception
- cleanup
- file / stream / object lifecycle

### Kimeneti kompetencia

A tanuló felismeri a resource leak veszélyét, és exception-safe kódot tud írni.

---

## 5. szint – Fájl- és adatfeldolgozás

### Témák

- text files
- `TFile`
- `TStringList`
- stream-ek
- CSV
- JSON
- XML
- encoding
- mappák és fájlok bejárása

### Projektpéldák

- rendeléslista import
- log feldolgozás
- konfigurációs fájl
- BOM lista összehasonlítás

---

## 6. szint – VCL

### Témák

- Form
- controls
- events
- properties
- data binding alapgondolat
- UI és üzleti logika szétválasztása
- modal forms
- dialogs
- timers
- actions

### Kimeneti kompetencia

A tanuló képes kisebb Windows desktop funkciót építeni úgy, hogy a logika ne kizárólag event handlerekben éljen.

---

## 7. szint – SQL és FireDAC

### Témák

- kapcsolat
- query
- parameter
- dataset
- field
- transaction
- prepared statements
- error handling
- connection lifecycle

### Kötelező szemlélet

Mindig különítsük el:

1. SQL;
2. Delphi adat-hozzáférés;
3. üzleti logika;
4. UI.

### Kimeneti kompetencia

A tanuló képes adatot lekérdezni, paraméterezni, feldolgozni és biztonságosan kezelni.

---

## 8. szint – Debugging és legacy kód

### Témák

- breakpoint
- conditional breakpoint
- watches
- evaluate/modify
- locals
- call stack
- execution flow
- code navigation
- keresés nagy projektben
- adat eredetének visszakövetése

### Gyakorlati feladat

Meglévő metódus működésének dokumentálása kódmódosítás nélkül.

### Kimeneti kompetencia

A tanuló képes ismeretlen kódbázisban célzottan nyomozni.

---

## 9. szint – Tesztelhető és karbantartható kód

### Témák

- separation of concerns
- dependency boundaries
- pure functions
- unit testing alapok
- test cases
- regression
- refactoring
- naming
- small methods

### Kimeneti kompetencia

A tanuló nemcsak működő, hanem módosítható kódot ír.

---

## 10. szint – Vállalati integráció

### Témák

- riportgenerálás
- Excel/CSV export
- adattranszformáció
- nagyobb adatállományok
- konfiguráció
- logging
- hibatűrés
- batch feldolgozás
- adatbázis + VCL + üzleti logika

### Projektpéldák

- rendelés és alkatrészlista összefésülése
- kritikus BOM elemek riportja
- automatikus riportgenerátor
- adatellenőrző desktop utility

---

## Haladási elv

Egy témát akkor tekintünk elsajátítottnak, ha a tanuló:

1. el tudja magyarázni saját szavaival;
2. minimális példát tud írni;
3. hibát tud benne keresni;
4. hasonló, de nem azonos feladatban is alkalmazni tudja.

A tanulási útvonal nem merev sorrend. Valós munkahelyi problémák miatt előre lehet ugrani egy témához, de a hiányzó alapfogalmakat külön vissza kell tölteni.

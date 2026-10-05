# 01 – Object Pascal alapok

## Miért kell ezt tudni?

A Delphi vizuális fejlesztőkörnyezet sok részletet el tud rejteni, de a valódi fejlesztési munka során folyamatosan Object Pascal kódot kell olvasni és írni.

Ebben a modulban nem az a cél, hogy kulcsszavakat magoljunk. A cél annak megértése, hogyan reprezentálja a program az adatokat és hogyan hajt végre műveleteket rajtuk.

## Témák

### 1. Program és kódblokk

- `begin..end`
- statement
- semicolon
- kommentek

### 2. Változó

Mentális modell:

> A változó egy névvel és típussal rendelkező hely, ahol a program futása közben értéket tárolunk.

```pascal
var
  Quantity: Integer;
  ProductName: string;
```

A deklaráció még nem üzleti művelet. Azt mondjuk meg a fordítónak, milyen adatot szeretnénk kezelni.

### 3. Strong typing

Object Pascal strongly typed language.

Ez azt jelenti, hogy a fordító számos hibát már fordításkor felismer, mert ismeri a változók típusát.

A kérdés ne az legyen, hogy „mit enged a compiler?”, hanem:

> Milyen adatot modellez ez a változó?

### 4. Alapvető típusok

Első körben:

- `Integer`
- `Int64`
- `Double`
- `Currency`
- `Boolean`
- `Char`
- `string`
- `TDateTime`

Nem kell az összes Delphi típust egyszerre megtanulni.

### 5. Értékadás

```pascal
Quantity := 10;
ProductName := 'KSOH';
```

Fontos különbség:

```text
=   összehasonlítás / egyenlőség bizonyos kifejezésekben
:=  értékadás
```

### 6. Kifejezések

```pascal
Total := Quantity * UnitPrice;
```

Ezt balról jobbra olvasás helyett gondolatilag bontsd:

1. `Quantity * UnitPrice` kiszámít egy értéket;
2. az eredmény típusa meghatározható;
3. az eredményt `Total` kapja meg.

### 7. Konverzió

Valódi alkalmazásban a UI-ból és fájlból érkező adat gyakran szöveg.

Ezért fontos lesz megérteni a különbséget például ezek között:

- `string`
- `Integer`
- `StrToInt`
- `TryStrToInt`
- `IntToStr`

A konverziót nem csak szintaktikai műveletként tanuljuk: hibakezelési döntés is.

## Első gyakorlati probléma

Egy gyártási rendeléshez rendelkezésre áll:

- cikkszám;
- rendelt mennyiség;
- elkészült mennyiség.

A programnak ki kell számítania a hátralévő mennyiséget.

### Mielőtt kódolnál

Határozd meg:

1. milyen adatokat kell tárolni;
2. milyen típust választanál hozzájuk;
3. melyik adat bemenet;
4. melyik adat számított érték;
5. milyen üzleti szabály lehet szükséges, ha az elkészült mennyiség nagyobb a rendelt mennyiségnél.

Csak ezután írjuk meg a kódot.

## Gyakori kezdő hibák

- minden adatot `string` típusban tárolni;
- típusválasztás helyett csak azt nézni, mi fordul le;
- `=` és `:=` összekeverése;
- változónév, amely nem mondja meg, mit tárol;
- UI komponens értékét üzleti adatként kezelni külön változó/model nélkül;
- konverziós hiba figyelmen kívül hagyása.

## Checkpoint

A modul végén saját szavaiddal el kell tudnod magyarázni:

- mi a változó;
- miért van típusa;
- mit jelent a strong typing;
- miért más a `string` és az `Integer`;
- mit csinál a `:=`;
- miért lehet veszélyes a `StrToInt` ellenőrizetlen felhasználása.

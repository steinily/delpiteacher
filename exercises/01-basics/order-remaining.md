# Gyakorlat 01 – Rendelés hátralévő mennyisége

## Szint

Foundation / kezdő

## Cél

Gyakorolni:

- változók deklarálását;
- megfelelő adattípus kiválasztását;
- értékadást;
- egyszerű aritmetikai kifejezést;
- eredmény ellenőrzését.

## Feladat

Egy rendelés adatai:

```text
Cikkszám: KSOH-2713
Rendelt mennyiség: 120
Elkészült mennyiség: 83
```

Számítsd ki, hány darabot kell még legyártani.

## Fontos

Ne kezdd rögtön UI-val.

Először csak az adatokat és a számítást modellezzük.

## 1. lépés – tervezés

Írd le, milyen változókat hoznál létre.

Minden változóhoz add meg:

- a nevét;
- a Delphi típusát;
- mit tárol.

## 2. lépés – deklaráció

Írd meg a `var` blokkot.

A mentor első körben ne adja meg a kész blokkot, hanem review-zza a tanuló próbálkozását.

## 3. lépés – értékadás

Add a változóknak a feladatban megadott értékeket.

## 4. lépés – számítás

Számítsd ki a hátralévő mennyiséget.

## 5. lépés – ellenőrzés

A várt eredmény:

```text
37
```

Ne csak azt ellenőrizd, hogy 37 lett-e. Magyarázd el, melyik kifejezés állította elő ezt az értéket.

## Edge case

Mi történjen, ha:

```text
Rendelt: 120
Elkészült: 125
```

Még ne implementáld automatikusan. Először fogalmazd meg, szerinted üzletileg mit jelenthet ez az állapot.

## Mentor szabály

Ehhez a gyakorlathoz a mentor alapértelmezésben L1–L2 segítséget használjon. Kész megoldást csak több sikertelen próbálkozás vagy kifejezett kérés után adjon.

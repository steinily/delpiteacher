# Kódreview szabályok

## Cél

A review célja nem pusztán a hibák felsorolása. A tanulónak a review végére értenie kell, hogy miért probléma az adott megoldás, hogyan lehet felismerni hasonló helyzetet, és milyen javítási stratégia használható.

## Review sorrend

### 1. Fordul és fut?

Először különítsük el:

- compiler error;
- warning/hint;
- runtime exception;
- logikai hiba;
- design probléma.

### 2. Helyesség

Ellenőrizzük:

- megfelelő eredményt ad-e;
- kezeli-e a szélső eseteket;
- helyes-e a kontrollfolyam;
- lehet-e inicializálatlan vagy érvénytelen állapot.

### 3. Resource management

Minden manuálisan létrehozott objektumnál vizsgáljuk:

- hol történik a `Create`;
- van-e owner;
- hol történik a felszabadítás;
- exception esetén is megtörténik-e.

Kiemelt anti-pattern:

```pascal
List := TStringList.Create;
List.LoadFromFile(FileName);
List.Free;
```

Ha a `LoadFromFile` exceptiont dob, a `Free` nem fut le.

Tanítandó minta:

```pascal
List := TStringList.Create;
try
  List.LoadFromFile(FileName);
finally
  List.Free;
end;
```

### 4. Olvashatóság

Vizsgáljuk:

- változónevek;
- metódushossz;
- beágyazott feltételek;
- duplikáció;
- magic number/string;
- kommentek minősége.

A komment ne azt ismételje meg, amit a kód egyértelműen mond. Inkább az okot, üzleti szabályt vagy nem nyilvánvaló döntést dokumentálja.

### 5. Delphi idiomatikusság

Vizsgáljuk, hogy a megoldás természetesen illeszkedik-e Object Pascalhoz és Delphihez.

Példák:

- enum stringek helyett, ha zárt állapothalmazról van szó;
- `for..in`, ha nincs szükség indexre;
- paraméterezett query string-összefűzés helyett;
- `try..finally` resource felszabadításhoz;
- jól definiált record vagy class párhuzamos tömbök helyett.

## Severity szintek

A review észrevételeket lehetőség szerint jelöld:

- **Critical** – hibás eredmény, crash, adatvesztés, resource leak, SQL injection vagy hasonló komoly probléma.
- **Major** – jelentős karbantarthatósági vagy logikai kockázat.
- **Minor** – javítható stílus vagy egyszerűsítés.
- **Suggestion** – alternatíva, nem kötelező módosítás.

## Ne javíts mindent egyszerre

Kezdő vagy középhaladó kódnál a mentor a legnagyobb tanulási értékű 2–4 problémát emelje ki először.

Túl sok apró észrevétel elfedi a fontos koncepciókat.

## Review formátum

Ajánlott forma:

### Ami jó

Röviden emeld ki a helyes döntéseket.

### Első javítandó pont

- probléma;
- miért probléma;
- hogyan tudod felismerni;
- hint a javításhoz.

### Második javítandó pont

Ugyanez.

### Következő lépés

A tanuló módosítsa először saját maga a kódot.

## Teljes javított kód

A teljes javított verzió ne legyen automatikus. Előbb adj lehetőséget a tanulónak a korrekcióra.

Ha teljes verzió szükséges, a változtatásokat magyarázd meg, és lehetőleg mutasd meg a lényegi különbséget az eredetihez képest.

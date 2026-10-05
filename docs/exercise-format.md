# Gyakorlófeladat-formátum

## Cél

A gyakorlófeladatok ne pusztán kódírási feladatok legyenek. Minden feladatnak azt kell mérnie, hogy a tanuló megértett-e egy konkrét Delphi/Object Pascal koncepciót.

## Kötelező szerkezet

### Cím

Rövid, konkrét feladatnév.

### Tanulási cél

Legfeljebb 1–3 fő koncepció.

Példa:

- `for..in` ciklus;
- `Integer` számláló;
- feltételes vizsgálat.

### Feladat

A megoldandó probléma természetes nyelven.

### Bemenet

Pontosan definiált bemenet.

### Elvárt eredmény

Pontosan definiált kimenet vagy viselkedés.

### Korlátozások

Például:

- ne használj kész sorting függvényt;
- ne írj UI-kódot;
- CE-compatible legyen;
- a logika külön függvényben legyen.

### Példa

Legalább egy bemenet/kimenet példa.

### Első hint

Koncepcionális segítség, kész kód nélkül.

### Második hint

Konkrétabb Delphi iránymutatás.

### Kódváz

Csak akkor, ha szükséges.

### Tesztesetek

Legalább:

- normál eset;
- edge case;
- hibás bemenet, ha releváns.

### Késznek tekinthető, ha

Rövid acceptance criteria.

## Nehézségi szintek

### Level 1 – Syntax

Egy nyelvi elem gyakorlása izolált környezetben.

### Level 2 – Logic

2–3 ismert nyelvi elem kombinálása.

### Level 3 – Small feature

Kisebb, valós alkalmazásrészlet.

### Level 4 – Integration

Több komponens vagy réteg összekapcsolása.

### Level 5 – Maintenance

Meglévő/legacy kód megértése, debugolása vagy módosítása.

## Mintafeladat

### Cím

Pozitív értékek megszámolása

### Tanulási cél

- tömb bejárása;
- `for..in`;
- `if`;
- számláló.

### Feladat

Írj egy függvényt, amely egy egész számokat tartalmazó tömbből visszaadja, hány elem nagyobb nullánál.

### Bemenet

`TArray<Integer>`

### Kimenet

`Integer`

### Példa

`[-2, 3, 0, 8]` → `2`

### Első hint

Minden elemet pontosan egyszer kell megvizsgálnod.

### Második hint

Használhatsz `for..in` ciklust és egy nulláról induló számlálót.

### Késznek tekinthető, ha

- üres tömbre 0-t ad;
- a 0 nem számít pozitívnak;
- negatív számokat nem számolja bele.

# Delphi környezetek

## Használt környezetek

### Munkahely

- Delphi 13 / RAD Studio Enterprise
- vállalati projektek
- valós adatbázisok, komponensek és meglévő kódbázisok

### Otthon

- Delphi 13 Community Edition
- gyakorlás
- saját projektek
- nyelvi és VCL-alapok
- reprodukciós példák

## Mentor szabály

Minden olyan megoldásnál, ahol az edition különbség számíthat, a mentor jelölje:

- `CE-compatible`
- `Enterprise-only`
- `Check edition availability`

Ne használjunk Enterprise-specifikus képességet észrevétlenül olyan gyakorlatban, amelyet a tanulónak otthon kell megoldania.

## Portábilis tanulási mag

A tananyag lehető legnagyobb része olyan technológiákra épüljön, amelyek mindkét környezetben tanulhatók:

- Object Pascal nyelv;
- RTL;
- generics;
- collections;
- exceptions;
- file I/O;
- JSON/XML;
- VCL alapok;
- OOP;
- debugging;
- unitok;
- algoritmusok;
- tesztelhető üzleti logika.

## Enterprise-specifikus gyakorlatok

Ha egy munkahelyi feladat Enterprise-specifikus eszközt vagy komponenst használ, két rétegre bontsuk:

1. a mögöttes programozási koncepció;
2. az Enterprise eszköz konkrét használata.

Így a koncepció otthon is gyakorolható marad.

## Példa

Ha a céges program adatbázis-hozzáférést végez:

- először tanuljuk meg a query, parameter, dataset és transaction fogalmát;
- utána nézzük meg a konkrét FireDAC/Enterprise környezetet;
- gyakorláshoz lehet kisebb lokális adatforrást vagy mockolt adatot használni.

## Verziószabály

Példák alapértelmezett célverziója: Delphi 13.

Régebbi Delphi kód elemzésekor külön jelezzük:

- legacy syntax;
- deprecated API;
- kompatibilitási okból megtartott minta;
- modern Delphi alternatíva.

A mentor ne írjon át működő legacy kódot pusztán azért, mert létezik újabb szintaxis. Először a funkciót és a kockázatot kell megérteni.

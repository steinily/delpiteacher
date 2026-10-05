# 00 – Delphi 13 környezet és IDE

## Cél

A Delphi IDE ne csak egy hely legyen, ahol megnyomod a Run gombot. A cél, hogy tudd, hol találod a projekt szerkezetét, a forráskódot, a formot, a compiler üzeneteket és a debugging eszközöket.

## Amit a modul végére tudni kell

- Project és Project Group közötti különbség.
- `.dproj`, `.dpr`, `.pas`, `.dfm` alapvető szerepe.
- Code Editor és Form Designer közötti váltás.
- Object Inspector szerepe.
- Tool Palette szerepe.
- Build, Compile és Run fogalma.
- compiler error és warning megtalálása.
- breakpoint elhelyezése.
- Step Over és Step Into alapvető használata.
- Local Variables és Watches helye.

## Fontos mentális modell

Egy VCL Delphi alkalmazás nem „a Form”.

A projekt több együttműködő elemből áll:

```text
Project (.dpr / .dproj)
        |
        +-- Unit (.pas)
        |      |
        |      +-- Form class
        |      +-- methods
        |      +-- business/application code
        |
        +-- Form resource (.dfm)
        |
        +-- további unitok
```

A Form Designer vizuális szerkesztő. Amit ott elhelyezel, annak Delphi objektum megfelelője is van.

## Első IDE-gyakorlat

Hozz létre egy új **VCL Application** projektet.

Még ne építs alkalmazást.

Vizsgáld meg:

1. milyen fájlokat hozott létre Delphi;
2. mi látható a Project Managerben;
3. keresd meg a projekt `.dpr` forrását;
4. keresd meg a Form unit `.pas` fájlját;
5. válts a Form Designer és Code Editor között;
6. helyezz el egy `TButton` komponenst;
7. nézd meg az Object Inspectorban a `Name`, `Caption` és `Events` részeket.

## Mentor checkpoint

A következő modul előtt saját szavaiddal el kell tudnod mondani:

- mi a különbség egy Form és egy Unit között;
- mire való a `.dpr`;
- mit csinál az Object Inspector;
- mi történik nagy vonalakban, amikor megnyomod az F9-et.

Nem szükséges még minden részletet ismerni.
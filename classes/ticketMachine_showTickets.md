```mermaid
---
title: Biletomat - Pokaz bilety
---
classDiagram
    class EkranDotykowy {
    }

    class Kategoria {
        <<Enum>>
        Ulgowe
        Normalne
    }

    class Biletomat {
        +wybierzKategorieBiletow(kategoria)
        -wybudz()
        -wyswietlKomunikat(komunikat)
        -wyswietlKategorieBiletow(kategoria)
        -wyswietlSzczegolyBiletowDlaKategorii()
        -wyswietlKomunikatOBledziePolaczenia()
        -wrocDoEkranuStartowego()
        -zatwierdzKomunikat()
    }

    class SystemCentralny {
        +wyslijZapytanieOListeBiletow(): listaBiletow
    }

    Biletomat --> SystemCentralny : odpytuje
    EkranDotykowy --* Biletomat : jestCzescia
    BazaDanych ..> Kategoria : przechowuje
    Biletomat ..> Kategoria : przetwarza
```

```mermaid
classDiagram
    class Uzytkownik {
        <<Actor>>
        +wybierzOpcjeWyswietleniaInstrukcji()
        +wybierzDalej()
        +wybierzZamknij()
    }

    class Biletomat {
        -List~String~ stronyInstrukcji
        -int aktualnyNumerStrony
        -boolean czyKoniecInstrukcji
        +wyswietlInstrukcje()
        +przejdzDalej()
        +zamknijOknoInstrukcji()
        -wyswietlKomunikatPomocniczy()
        -wyswietlKolejnaInstrukcje()
    }

    Uzytkownik --> Biletomat : wchodzi w interakcję
```mermaid
    requirementDiagram

    element system_biletowy {
    }

    requirement aktualizacja_taryf {
    }

    requirement wprowadzenie_danych_do_bazy_taryf {
    }

    requirement powiadomienie_biletomatów_o_niezgodności_taryf {
    }

    aktualizacja_taryf - contains -> wprowadzenie_danych_do_bazy_taryf
    aktualizacja_taryf <- refines - powiadomienie_biletomatów_o_niezgodności_taryf
    system_biletowy - traces -> aktualizacja_taryf
```
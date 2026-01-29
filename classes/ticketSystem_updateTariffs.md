```mermaid
classDiagram
    class AdministratorSystemu {
        <<Actor>>
        +AktualizujTaryfe(Taryfa nowaTaryfa)
        +poprawDaneTaryfy(Taryfa nowaTaryfa)
    }

    class Taryfa {
        +String nazwa
        +Double cennik
        +Date dataWaznosci
    }

    class SystemBiletowy {
        +aktualizujTaryfe(Taryfa nowaTaryfa)
        -boolean weryfikacjaPoprawnosciDanych(Taryfa taryfa)
        -poprosONoweDane()
        +przeslijDaneDoBazy(Taryfa taryfa)
        +zlecAktualizacjeBiletomatu(Taryfa taryfa)
    }

    class BazaDanych {
        -Map~String, Taryfa~ obecneTaryfy
        +zapiszDaneTaryfy(Taryfa taryfa)
        +boolean sprawdzSpojnosc()
    }

    class Biletomat {
        -Taryfa aktualnaTaryfaLokalna
        +zaktualizujTaryfe(Taryfa nowaTaryfa)
    }

    AdministratorSystemu ..> Taryfa : definiuje
    AdministratorSystemu --> SystemBiletowy : inicjuje proces
    SystemBiletowy ..> Taryfa : przetwarza
    SystemBiletowy --> BazaDanych : zapisuje dane
    SystemBiletowy --> Biletomat : propaguje zmiany
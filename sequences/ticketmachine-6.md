```mermaid
sequenceDiagram
    participant U as Użytkownik
    participant B as Biletomat

    U ->> B: Wybranie opcji Wyświetlenia instrukcji
    loop Dopoki uzytkownik nie dojdzie do konca
        U ->> B: Wybranie opcji Dalej
        opt Wykryto problem użytkownika
            B ->> E: Wyświetlenie komunikatu pomocniczego
        end
        B ->> B: Wyświetlenie kolejnej instrukcji
        B -->> U
    end

    U ->> B: Wybranie przycisku zamknij
    B ->> B: zamknij okno instrukcji
    B -->> U
```

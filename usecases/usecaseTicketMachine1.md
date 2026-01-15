```mermaid
requirementDiagram

element biletomat {
}
requirement Wyświetlenie_dostępnych_biletów {
}

requirement Ostrzeżenie_o_braku_danych {
}
requirement Aktualizacja_biletów {
}

biletomat - traces -> Wyświetlenie_dostępnych_biletów
Wyświetlenie_dostępnych_biletów - contains -> Aktualizacja_biletów
Wyświetlenie_dostępnych_biletów <- refines - Ostrzeżenie_o_braku_danych
```

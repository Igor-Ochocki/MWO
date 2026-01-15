```mermaid
requirementDiagram

element system_biletowy {
}
requirement Dostarczanie_listy_dostępnych_biletów {
}
requirement Weryfikacja_taryf {
}
requirement Błąd_połączenia {
}

system_biletowy - traces -> Dostarczanie_listy_dostępnych_biletów

Dostarczanie_listy_dostępnych_biletów - contains -> Weryfikacja_taryf
Dostarczanie_listy_dostępnych_biletów <- refines - Błąd_połączenia
```

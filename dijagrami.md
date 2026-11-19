#Današnja lekcija
```mermaid
journey
  title Narucivanje hrane putem aplikacije
  section Odabir
    Trazim restoran: 4: Kupac
    Slazem kosaricu: 5: Kupac
    Pregledavam kosaricu: 5: Kupac
    Validira kosaricu u 19.30: 5: Aplikacija #ne stavit dvotocku gdje su sati
  section Placanje
    Unosim adresu: 3: Kupac
    Placanje ne prolazi: 1: Kupac, Aplikacija
  section Dostava
    Pratim dostavljaca na krati: 4: Kupac, Dostavljac
    Hrana stize hladna: 2: Kupac, Restoran
  section Reklamacija
    Salje reklamaciju restoranu: 1: Kupac, FINA, Porezna uprava
```
---
```mermaid
flowchart TD
  A([Narudzba slozena]) --> E([Platim karticom])
  E --> F{Placanje proslo?}
  F --> |Da| G[Restoran potvrduje]
  F --> |Ne| H[Aplikacija javlja pogresku]
  H --> |Druga kartica| E
  H --> |Gotovina| G
  G --> K([Hrana stize])
```
---
```mermaid
flowchart LR
  A([Narudzba slozena]) --> E([Platim karticom])
  E --> F{Placanje proslo?}
  F --> |Da| G[Restoran potvrduje]
  F --> |Ne| H[Aplikacija javlja pogresku]
  H --> |Druga kartica| E
  H --> |Gotovina| G
  G --> K([Hrana stize])
```
---
```mermaid
sequenceDiagram
  actor K as Kupac
  participant A as Aplikacija
  participant R as Restoran
  participant D as Dostavljac
  K->>A: Narudzba i placanje
  A->>R: Nova Narudzba
  R-->>A: Prihvaceno, gotovo za 25 minuta
  A-->>K: Narudzba potvrdena
  A->>D: Preuzmi narudzbu u restoranu
  D->>R: Preuzimanje hrane
  D->>K: Dostava
  K->>A: Ocjena dostave
```
---
```mermaid
flowchart TD
  A([Datoteka je u polju za predaju]) --> B[Kliknite spremi promjene]
  B --> C{Status je predano?}
  C --> |Da| K([Kraj: zadatak je predan])
  C --> |Ne, piše Skica| D["Kliknem Predaj zadatak (Submit assignment)"]
  D --> E{Traži se potvrda?}
  E --> |Da| F[Označim izjavu i potvrdim]
  F --> C
  E --> |Ne| C 
  ```
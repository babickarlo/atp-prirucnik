# Dnevnik izvođenja: MkDocs prema službenoj dokumentaciji

**Ime i prezime:** Karlo Babić

Sva mjesta u uglatim zagradama zamijenite svojim podacima.

## 1. Okruženje (prije početka)

| | |
|---|---|
| Računalo | MacBook Air M5 13,6" |
| Operacijski sustav | macOS 27.2 Golden Gate |
| Terminal | zsh |

## 2. Procjena (prije nego što otvorite upute)

- **Vrijeme početka:** 17:28
- **Koliko mislim da će mi trebati do razine 2:** 5 min

## 3. Razine

| Razina | Kako znam da sam uspio | Vrijeme |
|---|---|---|
| 1 | `mkdocs --version` ispisuje verziju | 17:28 |
| 2 | na `http://127.0.0.1:8000` vidim stranicu | 17:33 |
| 3 | druga stranica u izborniku; tema `readthedocs` | 17:35 |
| 4 | postoji mapa `site/` | 17:46 |

## 4. Dnevnik koraka

Jedan redak po koraku, i za korake koji su uspjeli. **Prvi korak:** provjerite koju verziju Pythona imate. Dulji ispis kopirajte na dno dnevnika, a u tablicu upišite „vidi ispis 1”.

**Vrsta:** K = korisnik, O = okruženje, S = sustav, D = dokumentacija, ? = nisam siguran, – = nema problema.

| Vrijeme | Što sam napravio | Dogodilo se (doslovno) | Kako sam riješio (izvor) | Vrsta |
|---|---|---|---|---|
| 17:28 | python3 --version | Python 3.15.0  | - | - |
| 17:28 | curl -L -O https://raw.githubusercontent.com/mkdocs/mkdocs/master/docs/getting-started.md  | vidi ispis 1 | - | - |
| 17:29 | mkdocs --version | vidi ispis 2 | - | - |
| 17:29 | mkdocs new my-project | vidi ispis 3 | - | - |
| 17:33 | mkdocs serve | vidi ispis 4| - | - |
| 17:36 | curl 'https://jaspervdj.be/lorem-markdownum/markdown.txt' > docs/about.md | vidi ispis 5 | - | - |
| 17:39 | Dodao sam ekstra tabulator unutar mkdocs.yml, linija 5. | vidi ispis 6 | Izbrisao sam nepotrebni tabulator.| K |
| 17:46 | mkdocs build | vidi ispis 7 | - | - |
| 17:47 | ls site | vidi ispis 8 | - | - |
| 17:48 | echo "site/" >> .gitignore | - | - | - |

## 5. Analiza (zadnjih 15 minuta)

### 5.1. Procjena i stvarnost

Procijenio sam 5 min do razine 2. Stvarno: 6 min. Razlika je nastala zato što sam sporo i pažljivo čitao upute.

### 5.2. Tri najveće prepreke

| Prepreka (što se dogodilo) | Vrsta | Zašto mislim da je ta vrsta |
|---|---|---|
| An error happened during the rebuild. The server will appear stuck until build errors are resolved. | K | Dodao sam nepotrebni ekstra tabulator. |
| Ispis koraka u markdownu. (greška pri formatiranju tablice) | K | Greškom sam izbrisao jednu ravnu crtu. |
| Instalacija MkDocs-a putem pip-a | O | Instalirao sam putem Homebrew-a. |

### 5.3. Ocjena dokumentacije

**Ocjena:** 1 = ne zadovoljava, 2 = djelomično, 3 = u potpunosti.

| Kriterij | Ocjena | Primjer iz uputa |
|---|---|---|
| Pronalazivost | 3 | jasno istaknute poveznice |
| Preduvjeti | 2 | potrebna instalacija MkDocs-a putem terminala |
| Točnost | 3 | jasni i važeći koraci |
| Očekivani rezultat | 3 | stranica izgleda identično poput u uputstvu |
| Pomoć kod pogreške | 1 | jednostavne i nepregledne naredbe poput "mkdocs --help" |
| Verzija i datum | 1 | vrijeme i datum nisu jasno označeni |

### 5.4. Jedna preporuka autorima

U odjeljku "Installation" piše da se iskoristi naredba ```pip install mkdocs```. Kod mene ta naredba nije radila jer koristim MacBook. Predlažem dodatak naredbe za instalaciju na macOS-u: ```brew install mkdocs```.

## Ispisi

### Ispis 1

```text
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  6529  100  6529    0     0  82864      0 --:--:-- --:--:-- --:--:-- 83705
```

### Ispis 2

```text
mkdocs, version 1.6.1 from /opt/homebrew/Cellar/mkdocs/1.6.1_3/libexec/lib/python3.15/site-packages/mkdocs (Python 3.15)
```

### Ispis 3

```text
INFO    -  Creating project directory: my-project
INFO    -  Writing config file: my-project/mkdocs.yml
INFO    -  Writing initial docs: my-project/docs/index.md
```

### Ispis 4

```text
INFO    -  Building documentation...
INFO    -  Cleaning site directory
INFO    -  Documentation built in 0.05 seconds
INFO    -  [17:33:44] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO    -  [17:33:44] Serving on http://127.0.0.1:8000/
INFO    -  [17:33:52] Browser connected: http://127.0.0.1:8000/
WARNING -  [17:33:52] "GET /apple-touch-icon-precomposed.png HTTP/1.1" code 404
WARNING -  [17:33:52] "GET /apple-touch-icon.png HTTP/1.1" code 404
```

### Ispis 5

```text
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  2506    0  2506    0     0  10591      0 --:--:-- --:--:-- --:--:-- 10618
```

### Ispis 6

```text
An error happened during the rebuild. The server will appear stuck until build errors are resolved.
```

### Ispis 7

```text
INFO    -  Cleaning site directory
INFO    -  Building documentation to directory: /Users/karlo/Documents/UniZD/ATP/zagrijavanje/atp-prirucnik/05-predavanje/my-project/site
INFO    -  Documentation built in 0.06 seconds
```

### Ispis 8

```text
404.html        css             index.html      search          sitemap.xml
about           img             js              search.html     sitemap.xml.gz
```
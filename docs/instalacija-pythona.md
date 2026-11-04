# Instalacija Pythona i prvi program

Kratka praktična uputa za instalaciju Pythona, provjeru verzije i pokretanje prve skripte.

## Razlike po operacijskim sustavima

| Operacijski sustav | Najkraći put do instalacije |
|---|---|
| **Windows** | Preuzmite i pokrenite `.exe` instalacijsku datoteku sa službene stranice [python.org](https://www.python.org/downloads/). **Obavezno označite kvačicu *"Add python.exe to PATH"*** prije klika na *Install Now*. |
| **macOS** | Preuzmite i pokrenite `.pkg` instalacijsku datoteku sa stranice [python.org](https://www.python.org/downloads/) ili instalirajte preko Homebrew-a naredbom `brew install python`. |

---

## Provjera instalacije

Nakon instalacije otvorite terminal (ili ponovno pokrenite VS Code ako je već bio otvoren) i upišite:


**Windows**
```bash
python --version
```
**macOS**
```
python3 --version
```

**Očekivani rezultat:** `Python 3.15.0`

---

## Prvi program

Ovaj odjeljak vodi vas kroz korake stvaranja jednostavne Python skripte koja ispisuje jedan redak teksta u terminalu.

### Kod programa

Kod koji ispisuje poruku glasi:

```python
print("Hello World!")
```

### Upute za rad u terminalu

1. **Stvaranje datoteke s kodom:**
   Upišite sljedeću naredbu u terminal kako biste stvorili datoteku `pozdrav.py` s navedenim kodom:

   ```bash
   echo 'print("Hello World!")' > pozdrav.py
   ```

   **Očekivani rezultat:**
   Naredba se izvršava bez ispisa poruka o pogrešci. Stvorena je nova datoteka `pozdrav.py` u vašoj mapi.

2. **Provjera sadržaja stvorene datoteke:**
   Provjerite je li kod točno upisan u datoteku:

   ```bash
   cat pozdrav.py
   ```

   **Očekivani rezultat:**
   ```text
   print("Hello World!")
   ```

3. **Pokretanje programa:**
   Pokrenite vaš prvi Python program naredbom:


   **Windows**
    ```bash
    python pozdrav.py
    ```
    **macOS**
    ```
    python3 pozdrav.py
    ``` 

   **Očekivani rezultat:**
   `Hello World!`

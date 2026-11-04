# Prvi koraci u terminalu

Naučit ćete osnovne naredbe za kretanje kroz mapu i upravljanje datotekama u terminalu. Postupak traje oko 20 minuta.

## Prije početka

- Radim na macOS-u u VS Code ugrađenom zsh terminalu.
- Visual Studio Code je pokrenut, a u njemu je otvorena mapa atp-prirucnik.

## 1. Otvorite terminal

U izborniku **Terminal** odaberite **New Terminal**.

**Očekivani rezultat:** karlo@Karlos-MacBook-Air atp-prirucnik %

## 2. Provjerite gdje se nalazite

```bash
pwd
```

**Očekivani rezultat:** /Users/karlo/Documents/UniZD/ATP/zagrijavanje/atp-prirucnik

## 3. Napravite mapu i uđite u nju

```bash
mkdir proba-terminala
cd proba-terminala
pwd
```

**Očekivani rezultat:** Putanja sada završava s nazivom mape `proba-terminala`.

## 4. Napravite datoteku i upišite u nju tekst

```bash
echo "# Moje bilješke" > biljeske.md
cat biljeske.md
```

**Očekivani rezultat:** `# Moje bilješke`

## 5. Dodajte još jedan redak

```bash
echo "- Naredba pwd ispisuje gdje se nalazim." >> biljeske.md
cat biljeske.md
```

**Očekivani rezultat:** 
```bash
# Moje bilješke
- Naredba pwd ispisuje gdje se nalazim.
```

Znak `>` stvara novu datoteku ili u potpunosti prepisuje sadržaj postojeće datoteke novim podatcima. Znak `>>` nadopunjuje (appenda) nove podatke na sam kraj postojeće datoteke bez brisanja njezina dosadašnjeg sadržaja.

## 6. Kopirajte, preimenujte i izbrišite datoteku

```bash
cp biljeske.md kopija.md
mv kopija.md stara.md
rm stara.md
ls
```

**Očekivani rezultat:** `biljeske.md`

**VAŽNO:** Budite izuzetno oprezni s naredbom `rm` jer trajno briše datoteke i mape bez premještanja u smeće (Trash). Jednom kada se izvrši, obrisane podatke nije moguće jednostavno vratiti.

## Ako ne radi

| Poruka | Što znači | Što učiniti |
|---|---|---|
| `No such file or directory` | Tražena datoteka ili direktorij (mapa) ne postoji na navedenoj putanji ili ste pogriješili u pisanju imena. | Provjerite jeste li točno upisali naziv, provjerite gdje se nalazite pomoću naredbe `pwd` ili izlistajte sadržaj mape s `ls`. |
| is a directory | Pokušali ste obrisati mapu (direktorij) običnom naredbom `rm` koja je namijenjena samo za datoteke. | Upotrijebite prisilno brisanje mape dodavanjem opcija `-rf` (npr. `rm -rf [naziv_mape]`). |

## Što dalje

**Gdje naučiti više**
- Priručnik Srca *Uvod u Linux*, poglavlja 2 i 3 (osnovne naredbe ljuske i upravljanje datotekama).
- Službena dokumentacija alata Pandoc: [Pandoc manual](https://pandoc.org/MANUAL.html)
- Priručnik za Git i GitHub: [Git manual](https://git-scm.com/doc)




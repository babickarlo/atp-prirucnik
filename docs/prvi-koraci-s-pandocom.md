# Prvi koraci s Pandocom

Naučit ćete kako instalirati Pandoc te pretvarati Markdown dokumente u Word i HTML formate. Postupak traje oko 25 minuta.

Provjereno s Pandocom 3.13 na macOS 27.2 Golden Gate-u u zsh terminalu.

## Prije početka

- Instaliran VS Code s otvorenim terminalom (`Terminal → New Terminal`).
- Postavljen i inicijaliziran Git repozitorij `atp-prirucnik` s izrađenom datotekom `README.md`.


## 1. Instalirajte Pandoc

### Windows

[Koraci za Windows. Ako ste radili na računalu u učionici, opišite put sa ZIP-om i PATH-om.]

### macOS

1. Preuzmite instalacijski paket `pandoc-3.13-arm64-macOS.pkg` (za Apple Silicon) ili `x86_64-macOS.pkg` (za Intel Mac) sa službenih stranica.
2. Pokrenite preuzetu datoteku i pratite korake instalacijskog čarobnjaka. Ako koristite Homebrew, upišite `brew install pandoc`.

## 2. Provjerite instalaciju

```bash
pandoc --version
```

**Očekivani rezultat:** `pandoc 3.13`

## 3. Pretvorite Markdown u Word
```bash
mkdir izlaz
pandoc README.md -o izlaz/README.docx
```
**Očekivani rezultat:** U mapi `izlaz` stvorena je datoteka `README.docx`. Kada je otvorite u Wordu, primijetit ćete da su naslovi automatski pretvoreni u Word-ove stilove Heading 1 i Heading 2.

## 4. Pretvorite Markdown u web-stranicu

```bash
pandoc README.md -s --toc -o izlaz/README-samostalno.html
```
Očekivani rezultat: Oznaka -s govori Pandocu da generira cjelovitu HTML stranicu koja uključuje zaglavlje i metapodatke, a ne samo osnovni sadržaj.

## Ako ne radi

| Poruka | Što znači | Što učiniti |
|---|---|---|
| `command not found` | Sustav ne prepoznaje naredbu pandoc | Provjerite jeste li pravilno instalirali Pandoc |

## Što ste napravili

Uspješno ste instalirali alat Pandoc i svladali osnovne pretvorbe dokumenata iz Markdowna u Word i HTML. Sada možete jednostavno izrađivati različite formate iz jedinstvenog izvornog koda.

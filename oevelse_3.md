# Workshop Øvelse 3: Introduktion til VS Code og Markdown

I denne øvelse skal du lære at bruge **Visual Studio Code (VS Code)** som din primære teksteditor og opbygge strukturerede dokumenter med **Markdown**. 

Markdown er et simpelt og populært format til at skrive noter, dokumentation (f.eks. `README.md` på GitHub) og websider.

---

## Formål

Når du er færdig med denne øvelse, kan du:
- Navigere og bruge de vigtigste funktioner i VS Code.
- Oprette og redigere `.md`-filer.
- Åbne og bruge **Markdown Preview** ved siden af din kode.
- Formatere tekst med overskrifter, lister, links, billeder, fremhævninger og kodeblokke.
- Bruge effektive genveje i VS Code.

---

## Del 1: Lær VS Code at kende

VS Code er en af verdens mest populære kode- og teksteditorer. Lad os se på opbygningen.

### 1.1 Brugerfladen i VS Code
Brugerfladen er opdelt i 5 hovedområder:
1. **Activity Bar (Venstre side):** Ikoner til Explorer (filer), Search, Source Control (Git) og Extensions.
2. **Side Bar:** Viser filerne i dit projekt eller dine søgeresultater.
3. **Editor:** Selve vinduet hvor du skiver din tekst/kode.
4. **Status Bar (I bunden):** Viser info om filtype, fejl, Git-branch osv.
5. **Terminal / Panel (I bunden, kan åbnes):** Integreret kommandolinje.

### 1.2 Nyttige extensions (Udvidelser)
Extensions gør VS Code endnu bedre til Markdown.

1. Klik på **Extensions**-ikonet i venstre side (eller tryk `Ctrl + Shift + X` / `Cmd + Shift + X`).
2. Søg efter **Markdown All in One** og klik **Install**.
3. (Valgfri) Søg efter **Markdownlint** og klik **Install** *(hjælper med at holde din Markdown flot og korrekt)*.

---

## Del 2: Opret din første Markdown-fil

1. Åbn VS Code.
2. Opret en ny fil ved at trykke `Ctrl + N` (Windows) / `Cmd + N` (Mac).
3. Gem filen med det samme: Tryk `Ctrl + S` / `Cmd + S` og kald den `min_foerste_note.md`.
   > **Vigtigt:** Filendelsen `.md` fortæller VS Code, at dette er et Markdown-dokument!

### 2.3 Åbn Markdown Preview (Forhåndsvisning)
Markdown viser råtekst i editoren. For at se, hvordan det færdige resultat ser ud:

1. Åbn filen `min_foerste_note.md`.
2. Klik på **Preview-ikonet** i øverste højre hjørne af VS Code (en bog med et forstørrelsesglas).
   * *Alternativ genvej:* Tryk `Ctrl + KV` (Windows) eller `Cmd + K V` (Mac).
3. Du har nu skærmen delt i to: Din editor til venstre og din live forhåndsvisning til højre!

---

## Del 3: Markdown Syntaks (Praktisk øvelse)

Kopier eller skriv nedenstående eksempler ind i din `min_foerste_note.md`-fil, og se hvordan det ser ud i din Preview-visning i højre side.

### 3.1 Overskrifter
Grebene bruges til overskrifter (fra 1 til 6 `#`):

```markdown
# Overskrift 1 (Hovedoverskrift)
## Overskrift 2 (Underoverskrift)
### Overskrift 3
#### Overskrift 4
```

### 3.2 Tekstformatering
Fremhæv din tekst med stjerner `*` eller underscores `_`:

```markdown
Dette er **fed skrift** (eller __fed skrift__).
Dette er *kursiv skrift* (eller _kursiv skrift_).
Dette er ***både fed og kursiv***.
Dette er ~~gennemstreget tekst~~.
```

### 3.3 Lister
Opret punktopstillinger eller nummererede lister:

```markdown
### Min huskeliste (Uordnet liste)
- Første punkt
- Andet punkt
  - Et underpunkt (lavet med indrykning/Tab)
  - Et underpunkt mere
* Man kan også bruge stjerner i stedet for bindestreger

### Rækkefølge (Ordnet liste)
1. Åbn VS Code
2. Skriv Markdown
3. Bliv en ekspert!
```

### 3.4 Citater og Vandrette linjer
Brug `>` til citater og `---` til at lave en adskillelseslinje:

```markdown
> "Markdown er enkelt, hurtigt og effektivt."
> — En glad udvikler

---
```

### 3.5 Links og Billeder
Links og billeder følger en meget ens opbygning: `[tekst](URL)` for links, og `![beskrivelse](URL)` for billeder.

```markdown
### Links
Besøg min favorit side: [GitHub](https://github.com)

### Billeder
Herefter kommer et billede fra nettet:
![GitHub Logo](https://github.githubassets.com/assets/GitHub-Mark-ea29e0e11ac1.png)
```

### 3.6 Kode og Kodeblokke
Hvis du skal vise kode eller kommandoer:

```markdown
Brug `inline kode` direkte i en sætning ved at omslutte med backticks ( " ` " ).

For større kodeblokke bruges tre backticks (```):

```python
def sig_hej(navn):
    print(f"Hej {navn}, velkommen til VS Code!")

sig_hej("Deltager")
```
```

---

## Del 4: Smarte VS Code Genveje

Brug disse genveje til at skrive hurtigere i VS Code:

| Handling | Windows | Mac |
| :--- | :--- | :--- |
| **Åbn Command Palette** | `Ctrl + Shift + P` | `Cmd + Shift + P` |
| **Åbn / Luk Sidepanel** | `Ctrl + B` | `Cmd + B` |
| **Åbn Live Preview** | `Ctrl + K` derefter `V` | `Cmd + K` derefter `V` |
| **Flyt en linje op/ned** | `Alt + PiL OP/NED` | `Option + PIL OP/NED` |
| **Dupliker linje** | `Shift + Alt + PIL NED` | `Shift + Option + PIL NED` |
| **Slet linje** | `Ctrl + Shift + K` | `Cmd + Shift + K` |
| **Søg i filen** | `Ctrl + F` | `Cmd + F` |

---

## Opsamling og Tjekliste for Øvelse 3

Du kan nu kalde dig selv fortrolig med VS Code og Markdown! Tjek at du kan følgende:

- [ ] Navigere i VS Code brugerfladen og installeret en extension.
- [ ] Oprette og gemme en `.md`-fil.
- [ ] Åbne live forhåndsvisning (Markdown Preview) ved siden af din fil.
- [ ] Bygge et dokument med overskrifter, lister, links, billeder og kodeblokke.
- [ ] Bruge mindst 2 tastaturgenveje i VS Code.
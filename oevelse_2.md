# Workshop Øvelse 2: Git Integration i Visual Studio Code

I denne øvelse skal du flytte dit arbejde fra browseren og over på din egen computer. Du vil lære, hvordan du forbinder Visual Studio Code (VS Code) til GitHub, kloner et repository, laver ændringer lokalt og synkroniserer dem sikkert tilbage til GitHub.

---

## Formål
Når du er færdig med denne øvelse, kan du:
- Forbinde din VS Code til din GitHub-konto.
- Klone et repository fra GitHub ned på din computer.
- Lave lokale ændringer, oprette `commits` og `pushe` dem til GitHub direkte fra VS Code.
- Bruge **Sync Changes** og forstå forskellen på `pull` og `push`.
- Indstille Git til at håndtere divergerende branches (`pull.rebase false`).
- Løse en flettekonflikt (merge conflict) visuelt i VS Code.

---

## Forudsætninger

Inden du starter, skal du have installeret:
1. **Visual Studio Code (VS Code)**, [https://code.visualstudio.com](https://code.visualstudio.com).
2. **Git** på din computer, åben en ```terminal``` og skriv ```git --version```. Hvis der ikke er noget installeret skal du følge guiden på mac og følge linket [https://git-scm.com/install/windows](https://git-scm.com/install/windows) med windows.

---

## Del 1: Engangsopsætning af Git og VS Code

Første gang du arbejder med Git på din computer, skal Git vide, hvem du er, så dine `commits` får det rigtige navn på GitHub.

### 1.1 Sæt dit navn og e-mail i Git
1. Åbn **VS Code**.
2. Åbn terminalen inde i VS Code ved at vælge **Terminal > New Terminal** i topmenuen.
3. Indtast følgende to kommandoer én ad gangen (erstat med dine egne oplysninger fra GitHub):

```bash
git config --global user.name "Dit GitHub Brugernavn"
git config --global user.email "din-email@eksempel.dk"
```

### 1.2 Undgå advarsler om "Divergent Branches"
Når du laver ændringer både online og lokalt, vil Git bede dig vælge en sammenfletningsstrategi. Kør denne kommando én gang for at sætte standarden til en almindelig `merge`:

```bash
git config --global pull.rebase false
```

> **Hvorfor gøre dette?** Dette sikrer, at `git pull` altid forsøger at flette dine online- og lokale ændringer sammen uden at fejle eller vise lange advarsler.

---

## Del 2: Klone et Repository til din computer

At *klone* betyder at hente en komplet kopi af et GitHub-repository ned på din egen harddisk.

1. Åbn **GitHub.com** i din browser og gå ind på det repo, du oprettede i Øvelse 1 (eller dit forkede repo).
2. Klik på den grønne knap **`< > Code`**.
3. Kopier URL'en under **HTTPS** (f.eks. `https://github.com/dit-brugernavn/min-foerste-workshop.git`).
4. Åbn **VS Code**.
5. Tryk på genvejen `Ctrl + Shift + P` (Windows) eller `Cmd + Shift + P` (Mac) for at åbne Command Palette.
6. Skriv `Git: Clone` og tryk på **Enter**.
7. Indsæt URL'en, du lige kopierede, og tryk på **Enter**.
8. Vælg en mappe på din computer, hvor projektet skal gemmes (f.eks. din *Dokumenter*-mappe).
9. Når VS Code spørger *"Would you like to open the cloned repository?"*, klikker du på **Open**.

> **Note:** Hvis VS Code spørger, om du stoler på forfatterne (*"Do you trust the authors?"*), trykker du på **Yes, I trust the authors**.

---

## Del 3: Lokal redigering, Commit og Push i VS Code

Nu skal vi lave ændringer lokalt på din computer og sende dem op til GitHub.

### 3.1 Rediger og gem en fil
1. I venstre sidemenu i VS Code (Explorer / Mappevisning) klikker du på filen `README.md` eller opretter en ny fil kaldet `noter.md`.
2. Skriv lidt ny tekst i filen, f.eks.:
   ```markdown
   ## Mine noter fra VS Code
   Dette er skrevet lokalt på min computer i VS Code!
   ```
3. Gem filen (`Ctrl + S` / `Cmd + S`).

### 3.2 Commit og Push via VS Code UI
1. Klik på **Source Control**-ikonet i venstre sidemenu.
2. Du vil se dine ændrede filer under overskriften **Changes**.
3. I tekstfeltet foroven (*"Message"*), skriv en kort commit-besked, f.eks. `Tilfoejede noter fra VS Code`.
4. Klik på den blå knap **Commit**.
5. Efter du har committet, ændres knappen til **Sync Changes** (eller der står en blå knap med **Publish Branch / Push**).
6. Klik på **Sync Changes**. 
7. Gå ind på dit repository på GitHub.com i browseren og genindlæs siden – du kan nu se din nye tekst online!

---

## Del 4: Hent ændringer ned med Pull og Sync

Hvad sker der, hvis du redigerer noget direkte på GitHub, mens du har projektet åbent på computeren?

1. Gå til **GitHub.com** i din browser.
2. Åbn din `noter.md` (eller `README.md`), klik på blyantsikonet, tilføj en ny linje online og tryk **Commit changes...**.
3. Gå tilbage til **VS Code** på din computer.
4. Læg mærke til statuslinjen helt nede i bunden til venstre. Ved siden af din branch `main` kan der stå et lille ikon med `↓1` (betyder: 1 ændring ligger klar online).
5. Klik på **Sync Changes**-knappen i Source Control-panelet (eller klik på genopfriskningsikonet helt nede i bunden).
6. VS Code henter nu automatiske ændringerne ned til din computer (**Pull**).

---

## Del 5: Håndtering af Merge-konflikter (Udfordringen)

Det mest almindelige problem i Git opstår, når der er lavet ændringer på **den samme linje i den samme fil** både online og lokalt.

### 5.1 Fremprovokér en konflikt
1. **Online:** Gå til GitHub.com, rediger linje 1 i `noter.md` til at skrive *"Dette er udgaven fra WEB"*, og lav en **Commit**.
2. **Lokalt:** Uden at køre Sync/Pull i VS Code først, redigerer du linje 1 i `noter.md` i VS Code til at skrive *"Dette er udgaven fra MIN COMPUTER"*.
3. Gem filen lokalt (`Ctrl + S`).
4. Skriv en commit-besked i VS Code og tryk **Commit**.
5. Tryk derefter på **Sync Changes**.

### 5.2 Løs konflikten i VS Code
VS Code vil stoppe og vise dig en advarsel om en konflikt. Indholdet i filen vil ændre sig og vise fremhævede farveblokke:

* **Current Change (Grøn/Blå):** Det indhold du skrev lokalt på computeren.
* **Incoming Change (Lilla/Grøn):** Det indhold der kom fra GitHub.

Ovenover teksten viser VS Code dig 4 direkte valgmuligheder:
* **Accept Current Change:** Beholder din lokale version.
* **Accept Incoming Change:** Overoverskriver med GitHub-versionen.
* **Accept Both Changes:** Beholder begge linjer efter hinanden.

**Trin til at afslutte:**
1. Klik på den mulighed, du ønsker (f.eks. **Accept Both Changes**).
2. Gem filen (`Ctrl + S`).
3. Gå til **Source Control**-panelet.
4. Klik på `+` ved siden af filen for at stagede den (eller skriv blot en commit-besked som *"Løst merge-konflikt"*).
5. Klik **Commit** og derefter **Sync Changes**.

---

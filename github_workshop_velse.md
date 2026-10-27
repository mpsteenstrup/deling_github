# Workshop: Introduktion til GitHub og Deling af Materiale

Velkommen til denne praktiske øvelse! I denne øvelse skal du lære grundlæggende GitHub-koncepter: at oprette en bruger, oprette et repository (arkiv), hente det ned på din egen computer (clone), redigere en fil online og lave ændringer via git-flowet (push/pull).

---

## Formål
Når du er færdig med denne øvelse, kan du:
- Navigere i GitHubs grænseflade.
- Oprette og administrere et online repository.
- Klon et repository til din egen maskine.
- Ændre filer direkte på web samt lokalt.
- Forstå det grundlæggende workflow med `commit`, `push` og `pull request`.

---

## Del 1: Opret en GitHub-bruger

Hvis du ikke allerede har en GitHub-konto, skal du oprette en nu.

1. Gå til [github.com](https://github.com/).
2. Klik på **Sign up**.
3. Indtast din e-mailadresse, opret en adgangskode og vælg et brugernavn.
4. Gennemfør den korte sikkerheds-tjek (captcha) og klik på **Create account**.
5. Tjek din e-mail for en verifikationskode og indtast den på GitHub.

> **Tip:** Vælg et brugernavn, du også har lyst til at vise i en professionel eller uddannelsesmæssig sammenhæng!

---

## Del 2: Opret dit første Repository

Et *repository* (ofte kaldet et "repo") er som en projektmappe, hvor alle dine filer og deres ændringshistorik gemmes.

1. Når du er logget ind på GitHub, skal du klikke på **`+`** ikonet i øverste højre hjørne og vælge **New repository** (eller klikke på den grønne knap **Create repository**).
2. Udfyld følgende felter:
   - **Repository name:** Giv dit repo et navn, f.eks. `min-foerste-workshop` eller `github-oevelse`.
   - **Description (valgfri):** En kort beskrivelse, f.eks. *Øvelse i GitHub på workshop*.
   - **Visibility:** Vælg **Public** (så andre i workshops kan se det).
   - **Initialize this repository with:**
     - Tjekmark feltet **Add a README file** af. *(En README-fil beskriver, hvad projektet handler om).*
     - Tjekmark feltet **license** du ønsker, det kan være *CC zero*.
3. Klik på den grønne knap **Create repository** nederst på siden.

Du har nu oprettet dit første online repository!

---

## Del 3: Rediger en fil online (Online Edit)

Du kan redigere filer direkte i din browser på GitHub.

1. Gå til forsiden af dit nye repository.
2. Klik på filen `README.md`.
3. Klik på **blyant-ikonet** (Edit this file) i øverste højre hjørne af filvisningen.
4. Tilføj en smule tekst under overskriften, for eksempel:
   ```markdown
   Dette er min første ændring lavet direkte i browseren!
   
   ## Om mig
   - Navn: [Dit Navn]
   - Rolle: Deltager i GitHub workshop
   ```
5. Rul ned til sektionen **Commit changes...**.
6. Skriv en kort besked i feltet (f.eks. `Update README.md with bio`).
7. Sørg for at **Commit directly to the `main` branch** er valgt.
8. Klik på **Commit changes**.

---

## Del 4: Klon 


## Del 4: Clone dit Repository (Hent det ned på din computer)

For at arbejde med filerne lokalt på din egen computer skal du *klone* dit repository.

### Metode A: Brug GitHub Desktop (Anbefalet til begyndere)
1. Hent og installer [GitHub Desktop](https://desktop.github.com/), hvis du ikke har det.
2. Log ind med din GitHub-konto i GitHub Desktop.
3. På GitHub.com inde på dit repo: Klik på den grønne knap **`< > Code`**.
4. Vælg **Open with GitHub Desktop**.
5. Vælg, hvor på din computer mappen skal gemmes, og klik **Clone**.

### Metode B: Brug Terminal / Kommandoprompt (Git CLI)
1. Åbn din terminal eller kommandoprompt.
2. På GitHub.com inde på dit repo: Klik på **`< > Code`** og kopier URL'en under HTTPS (f.eks. `https://github.com/dit-brugernavn/min-foerste-workshop.git`).
3. Kør følgende kommando i terminalen:
   ```bash
   git clone https://github.com/dit-brugernavn/min-foerste-workshop.git
   ```
4. Gå ind i mappen:
   ```bash
   cd min-foerste-workshop
   ```

---

## Del 5: Push og Pull Requests (Samarbejde)

Nu skal vi prøve at dele materiale og sende ændringer ind via et **Pull Request (PR)**.

### Øvelse A: Opret en ændring på en makkers repository
1. Find sammen med en makker i workshoppen.
2. Find din makkers GitHub-brugernavn og gå ind på deres repository.
3. Åbn deres `README.md`-fil og klik på blyantsikonet (Edit).
4. Tilføj en lille hilsen nederst i filen, f.eks.:
   > *Hilsen fra [Dit Navn] - Tak for en god workshop!*
5. Rul ned til **Commit changes...**.
6. Læg mærke til, at GitHub automatisk forslår at oprette en ny *branch* og sende et **Pull Request**, fordi du ikke ejer arkivet.
7. Klik på **Propose changes**.
8. Klik derefter på **Create pull request**.

### Øvelse B: Modtag og godkend et Pull Request (Merge)
1. Gå tilbage til dit eget repository på GitHub.
2. Klik på fanen **Pull requests** øverst.
3. Du bør nu se et modtaget Pull Request fra din makker. Klik på det.
4. Gå ind under fanen **Files changed** for at se, hvad din makker har ændret.
5. Gå tilbage til **Conversation** og klik på den grønne knap **Merge pull request**, og derefter **Confirm merge**.
6. Tillykke! Du har nu accepteret en ændring fra en anden person.

---

## Opsamling og Tjekliste

Du har nu gennemført:
- [x] Oprettet en GitHub-bruger.
- [x] Oprettet dit eget repository med en README-fil.
- [x] Redigeret en fil direkte online.
- [x] Klonet arkivet til din egen PC.
- [x] Sendt et Pull Request til en makker og godkendt et modtaget Pull Request.
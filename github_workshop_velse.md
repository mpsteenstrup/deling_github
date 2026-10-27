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

## Del 4: Fork et eksisterende repo

Når man kopiere et repository kaldes det at man laver en ```fork```. Der bliver lavet en kopi at et repository som du har fuld redigeringsrettigheder til.

1. Åbn linket til workshop repository  [https://github.com/mpsteenstrup/deling_github/tree/main](https://github.com/mpsteenstrup/deling_github/tree/main).

Fork repositoriet:

2. Klik på den lille knap Fork øverst til højre på siden.
3. Vælg din egen konto som destination, og klik Create fork.

Nu har du din helt egen kopi af projektet ligger under din egen GitHub-profil!

Rediger en fil online:

4. Inde i dit nye forkede repository, klik på filen README.md.
5. Klik på blyant-ikonet (Edit this file) i øverste højre hjørne af filvisningen.
6. Tilføj dit navn eller en linje tekst.
7. Gem dine ændringer (Commit):
8. Klik på den grønne knap Commit changes... øverst til højre.
9. Skriv en kort besked (f.eks. "Tilføjede mit navn") og klik Commit changes.

## Del 5: makkeropgave: opret, fork og pull

I skal nu oprette et repo, så skal en anden forke det, redigere det og foreslå at ændringerne bliver implementeret i det oprindelige repo. Jeg kalder jer person A og B.

1. A opretter et repo som ovenfor, med en fil eks README.MD.
2. B opretter fork repo.
3. B rediger README.MD filen i det nye repo og commit.

For at opdatere det oprindelige repo skal I

4. B sender rettelser tilbage ved at trykke på ```Compare and pull requests``` og derefter trykke på ```Create pull request```.
5. A trykker på ```pull request``` øverst og vælger den request der er. 
6. Hvis der ikke er nogen konflikt kan de to repos ```merges``` direkte, ellers skal man forholde sig til hvilken version man foretrækker.


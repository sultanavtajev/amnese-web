Notion lenke: https://www.notion.so/Anamnese-1027c2dfb0eb802fbebed0d875035e3b

### Trinn 1: Oppdater din lokale `main`-gren og deretter din egen gren før du begynner å programmere

Følg disse trinnene

1. **Sjekk ut main-grenen og trekk ned de nyeste endringene:**

   ```bash
   git checkout main
   git pull origin main
   ```

2. **Sjekk ut din egen gren:**

   ```bash
   git checkout <din-gren>
   ```

3. **Oppdater din gren med de nyeste endringene fra main:**

   ```bash
   git merge main
   ```

4. **Start å kode på din egen gren!**

### Trinn 2: Oppdatere `main`-grenen med endringer fra en annen gren

Følg disse trinnene for å slå sammen endringene fra en vilkårlig gren inn i `main`-grenen:

1. **Sjekk ut den grenen du vil slå sammen, og push eventuelle endringer til det eksterne repoet:**

   ```bash
   git checkout <din-gren>
   git add .
   git commit -m "Din commit-melding her"
   git push origin <din-gren>
   ```

2. **Bytt til `main`-grenen:**

   ```bash
   git checkout main
   ```

3. **Trekk ned de nyeste endringene fra det eksterne repoet på `main`:**

   ```bash
   git pull origin main
   ```

4. **Slå sammen endringene fra din gren inn i `main`:**

   ```bash
   git merge <din-gren>
   ```

   Hvis det oppstår sammenslåingskonflikter, må du løse dem manuelt, legge til endringene, og deretter fortsette sammenslåingen.

5. **Push de oppdaterte endringene til `main`-grenen i det eksterne repoet:**

   ```bash
   git push origin main
   ```

### Trinn 3: Rens, oppdater avhengigheter og bygg opp prosjektet på nytt (Kjør ved store endringer eller bugs, før du begynner å lete etter feil/debugge)

Kjør følgende kommandoer i terminalen

    ```bash
    Remove-Item -Recurse -Force node_modules
    Remove-Item -Force package-lock.json
    npm install -g npm-check-updates
    ncu -u
    npm install
    npm cache clean --force
    npm run build
    ```

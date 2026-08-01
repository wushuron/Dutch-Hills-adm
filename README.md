# 🚐 Ritten & Uren Tracker

Vanilla HTML/CSS/JavaScript app om km's en uren per order bij te houden — voor facturatie aan klanten én je eigen boekhouding. Geen dependencies, geen build step, werkt volledig offline via localStorage.

## Bestanden om te uploaden naar GitHub

- `index.html` — de volledige app (HTML + CSS + JS in één bestand)
- `manifest.json` — PWA manifest (installeerbaar als app-icoon op je telefoon)
- `README.md` — dit bestand (optioneel, maar handig)

## Stap voor stap: nieuwe GitHub repo + Netlify

### 1. Nieuwe repo aanmaken op GitHub
1. Ga naar https://github.com/new
2. Repository naam, bijv. `ritten-tracker`
3. Zet op **Public** of **Private** (maakt niet uit voor Netlify)
4. **Geen** README/gitignore aanvinken (die upload je zelf)
5. Klik **Create repository**

### 2. Bestanden uploaden
De makkelijkste manier zonder git-commando's:
1. Open je nieuwe repo op GitHub
2. Klik **Add file → Upload files**
3. Sleep `index.html`, `manifest.json` en `README.md` erin
4. Klik **Commit changes**

*(Of via terminal, als je dat gewend bent van je Uren Tracker:)*
```bash
git clone https://github.com/JOUW-GEBRUIKERSNAAM/ritten-tracker
cd ritten-tracker
# kopieer index.html, manifest.json, README.md hierin
git add .
git commit -m "Eerste versie Ritten & Uren Tracker"
git push origin main
```

### 3. Deployen op Netlify
1. Ga naar https://app.netlify.com
2. **Add new site → Import an existing project**
3. Kies GitHub → selecteer je `ritten-tracker` repo
4. Build settings: laat leeg (geen build command, geen publish directory nodig — of zet publish directory op `/`)
5. Klik **Deploy**
6. Je krijgt een URL zoals `https://jouw-app-naam.netlify.app`

### 4. Op je telefoon installeren
**Android (Chrome):** open de URL → menu (⋮) → "Add to home screen"
**iOS (Safari):** open de URL → deel-knop (↗) → "Add to home screen"

## Belangrijk: data blijft lokaal

Alle gegevens (regels, adresboek, tarieven) staan in de **localStorage** van je browser/telefoon — niet in de cloud. Maak dus regelmatig een backup:

- **💾 Backup & Export → 📥 JSON Export** downloadt een volledige backup
- Bij een nieuwe telefoon: open de app → **JSON Importeren** → kies je backup-bestand

## Functionaliteit

- **Regels loggen** (geen vaste orderlijst): order/klant, km, uren, tarief/km, tarief/uur, materiaalkosten, omschrijving
- **Adresboek**: vaste locaties met afkorting en km enkele reis — typ een afkorting in het locatieveld en de km (retour) wordt automatisch ingevuld
- **Periode-filter**: per maand of custom datumbereik
- **Totalen per order**: voor facturatie
- **Totalen per periode**: km, uren, materiaal, omzet — voor je boekhouding
- **CSV-export**: alle regels + totalen per order + periodetotaal, te openen in Excel/Sheets
- **JSON-export/import**: volledige backup en herstel

## Toekomstige uitbreidingen (ideeën)

- Order "afsluiten"/archiveren zodra gefactureerd
- Meerdere valuta/tarieven per klant opslaan
- Jaaroverzicht zoals in de Uren Tracker

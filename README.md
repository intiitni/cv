# Hugo CV site — handleiding

Deze repo bevat een Hugo-site die jouw CV als single-page website toont.

## Snel starten
1. **Installeer Hugo (extended)**: https://gohugo.io/getting-started/installing/
2. Download/Unzip dit project en open een terminal in de map.
3. Start een lokale server:
   ```bash
   hugo server -D
   ```
   De site draait dan op http://localhost:1313/

## Publiceren op GitHub Pages (main branch /docs)
Deze site is geconfigureerd met `publishDir = "docs"`. Dat betekent:
- De gegenereerde site komt in de map `docs/` terecht.
- GitHub Pages kan direct uit `docs/` serveren vanaf de `main` branch.

### Stappen
1. Maak een **nieuwe GitHub-repository** (bijv. `cv-site`).
2. Commit en push alle bestanden naar `main`.
3. Genereer de `docs/` map lokaal:
   ```bash
   hugo --minify
   ```
4. Push opnieuw (zodat `docs/` in de repo staat).
5. Ga naar **Settings → Pages → Build and deployment**:
   - **Source**: *Deploy from a branch*
   - **Branch**: `main` en **Folder**: `/docs`
6. Wacht een minuut en bezoek: `https://<jouw-gebruikersnaam>.github.io/<repo-naam>/`

### Aanpassen
- **Titel & contact**: pas `config.toml` aan (naam, e-mail, telefoon, kleuren).
- **Profieltekst**: `content/_index.md`.
- **Vaardigheden/Talen/Hobby’s**: `data/skills.json`.
- **Werkervaring**: `data/experience.json`.
- **Opleiding**: `data/education.json`.
- **Kleuren/lay-out**: `assets/css/main.css` of de templates in `layouts/`.

Veel succes!

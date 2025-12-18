# Smedslättsskolans Föräldraförening – Webbplats

En minimal, responsiv Jekyll-webbplats för GitHub Pages.

## Konfiguration

Webbplatsen använder:
- **Jekyll** med temat **minima** (stöds av GitHub Pages)
- **GitHub Pages** kompatibel – inga otillåtna plugins
- Responsiv design med hamburger-meny för mobil
- Innehållet är på **svenska**

## Lokal utveckling

### Förutsättningar
- Ruby 2.7+ (kontrollera med `ruby --version`)
- Bundler (installera med `gem install bundler` om behövs)

### Installation och körning

```bash
# Installera dependencies
bundle install

# Starta lokal server med live-reload
bundle exec jekyll serve --livereload

# Eller utan live-reload:
# bundle exec jekyll serve
```

Webbplatsen är då tillgänglig på `http://localhost:4000`

### Bygga för produktion

```bash
bundle exec jekyll build
```

Detta skapar `_site/`-katalogen med den färdiga webbplatsen.

## GitHub Pages-inställningar

Följ dessa steg i ditt GitHub-repository:

1. Gå till **Settings** → **Pages**
2. Under **Source**, välj:
   - **Branch**: `main`
   - **Folder**: `/ (root)`
3. Klicka **Save**

GitHub Pages bygger och publicerar sajten automatiskt när du pushar ändringar.

### Egna domäner

Om du vill använda en egen domän (t.ex. `smedslattsforaldrar.se`):

1. Lägg till en `CNAME`-fil i roten med domännamnet:
   ```
   smedslattsforaldrar.se
   ```
2. Uppdatera DNS-inställningarna hos din domänregistrator
3. GitHub Pages verifierar domänen automatiskt

## Filstruktur

```
.
├── _config.yml           # Jekyll-konfiguration
├── _layouts/
│   └── default.html      # Bas-layoutmall
├── _includes/
│   ├── header.html       # Sidhuvud med navigation
│   └── footer.html       # Sidfot
├── assets/
│   ├── css/main.css      # Responsiv styling
│   ├── js/main.js        # Hamburger-meny-logik
│   └── images/           # Logga och bilder
├── index.md              # Startsida
├── klassforaldrar.md     # Klassföräldrar
├── lankar.md             # Länkar
├── lathund.md            # Lathund
├── om-skolan.md          # Om skolan
└── trafikforaldrar.md    # Trafikföräldrar
```

## Framtida anpassningar

- **Logo**: Lägg en PNG-fil i `assets/images/logo.png`
- **Färger**: Uppdatera CSS-variabler i `assets/css/main.css`:
  ```css
  :root{
    --bg: #ffffff;
    --text: #222222;
    --accent: #0b74de;
    /* etc. */
  }
  ```
- **Innehål**: Redigera `.md`-filerna direkt eller via GitHub-gränssnittet

## GitHub Pages-kompatibilitet

✅ **Godkänd för GitHub Pages**
- Temat `minima` är officiellt stödd
- Inga egna plugins används
- Struktur följer Jekyll-standard
- `.gitignore` är korrekt konfigurerad

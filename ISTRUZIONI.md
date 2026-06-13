# Editor Spartito — PWA per iPad

## Struttura pacchetto
```
spartito-pwa/
├── index.html       ← app completa
├── manifest.json    ← configurazione PWA
├── sw.js            ← service worker (offline)
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── ISTRUZIONI.md
```

## Installazione su iPad (metodo consigliato)

### Opzione A — Netlify Drop (gratis, 2 minuti)
1. Vai su **netlify.com/drop** da computer
2. Trascina l'intera cartella `spartito-pwa` nella finestra
3. Copia l'URL che ti dà (es. `https://abc123.netlify.app`)
4. Su iPad, apri Safari e vai all'URL
5. Tocca **Condividi → Aggiungi a schermata Home**
6. L'app appare come icona, funziona offline

### Opzione B — Server locale (stesso WiFi)
```bash
cd spartito-pwa
python3 -m http.server 8080
# oppure: npx serve .
```
Su iPad: `http://[IP-computer]:8080`
(Non installa come PWA senza HTTPS, ma funziona nel browser)

### Opzione C — GitHub Pages (gratuito, permanente)
1. Crea repo GitHub, carica i file
2. Settings → Pages → Deploy from main branch
3. URL sarà `https://[username].github.io/[repo]`

---

## Funzionalità AirDrop

### Esportare via AirDrop su iPad
1. Premi **Archivio** (in alto a destra)
2. Scegli:
   - **Esporta archivio completo** → tutti gli spartiti + scalette
   - **Esporta spartito corrente** → solo lo spartito aperto
3. Il file .json viene scaricato
4. Vai su **Files** app → trova il file nella cartella Download
5. Tieni premuto → **Condividi → AirDrop**

### Importare su altro dispositivo
1. Ricevi il file via AirDrop → si apre in Files
2. Apri l'app Spartito sul secondo dispositivo
3. Premi **Archivio → Importa**
4. Seleziona il file ricevuto
5. Gli spartiti vengono uniti senza sovrascrivere

---

## Offline
Una volta installata come PWA, l'app funziona completamente
senza connessione internet. I dati sono salvati nel browser (localStorage).


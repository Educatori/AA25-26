# Convitto 2025 — Istruzioni deployment restyling

## File modificati

### CSS (cartella `css/`)
| File | Ruolo |
|------|-------|
| `campus-theme.css` | ⭐ NUOVO — tema base condiviso da tutte le pagine |

### HTML (root)
Tutti gli HTML sono stati aggiornati per:
1. Importare `css/campus-theme.css` **prima** del CSS specifico
2. Aggiungere `<img src="assets/Logo.png" class="print-logo">` nell'header (visibile solo in stampa)
3. Titoli ripuliti (rimossi i `••••`)
4. Login screen del cruscotto adattato al tema dark

## Come fare il deploy su GitHub

1. Sostituisci i file HTML nella root del repo con quelli di questa cartella
2. Sostituisci i file in `css/` con quelli di questa cartella
3. Aggiungi il file `assets/Logo.png` (già preparato)
4. I file in `js/` non vanno toccati — nessuna modifica alla logica

## Struttura file attesa nel repo

```
root/
├── index.html
├── campus_hub.html
├── roomcloud.html
├── assets/
│   └── Logo.png           ← il tuo logo (già pronto)
├── css/
│   ├── campus-theme.css
│   ├── campus_hub-style.css
└── js/
    ├── firebase-cruscotto-sync.js
    ├── firebase-cruscotto-config.js
    ├── firebase-roomcloud-config.js
    └── campus_hub-script.js
    
```

## Note sul tema

- **Font**: DM Sans (Google Fonts, caricato da CDN) + JetBrains Mono per orologi e codici
- **Sfondo**: `#0f1117` (quasi nero blu)
- **Accenti**: blu elettrico `#4f8ef7` + verde acqua `#38d9a9`
- **Logo in stampa**: `class="print-logo"` — visibile solo con `@media print`, nascosto a schermo
- Tutte le variabili CSS (`--accent`, `--ok`, `--absent`, ecc.) sono definite in `convitto-theme.css`
  e sovrascritte dove necessario nei file specifici

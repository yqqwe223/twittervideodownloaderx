# 🐦 Strumento di Analisi Video per X.com

> Uno strumento leggero, veloce e multifunzionale per estrarre contenuti video da X (precedentemente Twitter)

[🌐 Demo online](https://twittervideodownloaderx.com/it) • [📝 Guida all'uso](#-guida-alluso) • [❓ Domande frequenti](#-domande-frequenti)

---

## 📋 Panoramica del progetto

Questo progetto è uno strumento di analisi video basato sul web, progettato per estrarre in modo sicuro risorse video da post pubblici su X.com (precedentemente Twitter), offrendo opzioni di conversione e download in diversi formati. Non richiede installazione di software client né registrazione di account: utilizzalo direttamente dal tuo browser.

> ⚠️ **Avviso importante**: Questo strumento è destinato esclusivamente all'apprendimento personale, alla ricerca tecnica e all'uso entro limiti ragionevoli. Si prega di rispettare l'[Accordo per sviluppatori della piattaforma X](https://developer.twitter.com/en/developer-terms/agreement) e le leggi sul copyright applicabili nel proprio paese. È severamente vietato l'utilizzo per scopi che violino i diritti di terzi.

---

## ✨ Funzionalità principali

- 🔗 **Analisi dei link**: Compatibile con URL standard dei post X.com; rilevamento automatico di video e GIF animate
- 📥 **Esportazione multi-formato**:
  - Video MP4 con qualità originale
  - Estrazione audio → Formato MP3
  - Clip video → Conversione in GIF animata
- 🌍 **Interfaccia multilingue**: Supporto per italiano, inglese, cinese, giapponese, coreano e fino a 16 lingue in totale
- 📱 **Compatibilità multipiattaforma**: Funziona perfettamente su Chrome / Firefox / Safari / Edge; esperienza ottimizzata per mobile e tablet
- 🔒 **Privacy prioritaria**: Nessuna registrazione richiesta, nessuna raccolta di dati personali; processo di analisi completamente anonimo
- ⚡ **Elaborazione rapida**: Analisi completata in media in meno di 5 secondi; supporto per richieste simultanee

---

## 🚀 Avvio rapido

### Utilizzo online (consigliato)
1. Accedi a [https://twittervideodownloaderx.com/it](https://twittervideodownloaderx.com/it)
2. Copia il link del post di destinazione (esempio: `https://x.com/user/status/123456789`)
3. Incolla il link nel campo di input → Clicca sul pulsante 「Analizza」
4. Seleziona il formato desiderato → Salva il file seguendo le indicazioni del browser

### Distribuzione locale (per sviluppatori)
```bash
# Clonare il repository
git clone https://github.com/your-repo/x-video-parser.git

# Installare le dipendenze
cd x-video-parser && npm install

# Configurare le variabili d'ambiente (opzionale)
cp .env.example .env

# Avviare il server di sviluppo
npm run dev
```

> 💡 Nota: Questo progetto utilizza un'architettura basata su Node.js + Express. Consulta la documentazione dettagliata di distribuzione in `/docs/DEPLOY.md`

---

## 🛠 Stack tecnologico

| Modulo | Tecnologie utilizzate |
|--------|------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Elaborazione video | ffmpeg.wasm (conversione leggera lato frontend) |
| Proxy di inoltro | Cloudflare Workers / Middleware personalizzato |
| Internazionalizzazione | vue-i18n + Pacchetti lingua JSON |

---

## 📚 Guida all'uso

### Flusso operativo di base
```
1. Ottenere il link del post
   └─ Apri il post di destinazione su X.com → Copia l'URL dalla barra degli indirizzi del browser

2. Inviare la richiesta di analisi
   └─ Incolla il link nel campo di input dello strumento → Clicca su 「Scarica video」

3. Selezionare il formato di output
   ├─ 🎬 Scarica come MP4: Salva con qualità originale
   ├─ 🎵 Converti in MP3: Estrai la traccia audio
   └─ 🎞 Converti in GIF: Genera un'animazione breve (consigliato: ≤15 secondi)

4. Salvare il file
   └─ La risorsa si aprirà in una nuova scheda → Clic destro/menu → 「Salva con nome」
```

### Consigli per l'uso su dispositivi mobili
- iOS Safari: Pulsante Condividi → 「Salva in File」
- Android Chrome: Tenere premuto sul video → 「Scarica video」
- Se il video si riproduce automaticamente: Clicca su `⋮` nell'angolo in alto a destra del player → Seleziona 「Scarica」

---

## ❓ Domande frequenti

**D: Dove vengono salvati i file scaricati?**  
R: I file vengono salvati nella cartella di download configurata nel tuo browser. Puoi verificare o modificare questo percorso nelle impostazioni del browser.

**D: Posso analizzare account privati o contenuti limitati?**  
R: No. Questo strumento funziona solo con post impostati come pubblici e rispetta le impostazioni di accesso del contenuto originale.

**D: La qualità immagine/audio viene ridotta dopo la conversione?**  
R: Il formato MP4 mantiene la qualità originale. Il formato MP3 utilizza una codifica standard a 128 kbps. Il formato GIF ottimizza il framerate in base alla durata per bilanciare dimensioni del file e fluidità.

**D: La cronologia dei download o la cache vengono memorizzate?**  
R: No. Tutte le risorse vengono trasmesse direttamente al dispositivo dell'utente tramite un proxy temporaneo; il server non conserva alcuna richiesta o file multimediale.

**D: Cosa fare se l'analisi fallisce?**  
R: Si prega di verificare: ① Che il link corrisponda a un post pubblico valido ② Che la connessione internet sia stabile ③ Provare con un altro browser. Se il problema persiste, non esitare a segnalarlo tramite una Issue.

---

## ⚖️ Conformità normativa e Clausola di esonero da responsabilità

- Questo strumento **non elude né viola alcuna misura di protezione tecnica** delle piattaforme; si limita a ottenere metadati tramite interfacce pubbliche
- L'utente è responsabile di verificare che il proprio utilizzo sia conforme alla legislazione locale e ai termini di servizio della piattaforma
- Casi d'uso consigliati: Archiviazione personale, dimostrazioni educative, materiale di riferimento per la creazione di contenuti... sempre nel quadro dell'uso equo (Fair Use)
- Se si individuano contenuti che potrebbero violare diritti, si prega di contattare il canale ufficiale di [X tramite questo modulo di segnalazione copyright](https://help.twitter.com/forms/dmca)

---

## 🤝 Guida ai contributi

Accogliamo con piacere le tue Pull Request e segnalazioni di Issue! Prima di contribuire, si prega di consultare:
- [Standard di codice](/CONTRIBUTING.md)
- [Guida alla traduzione multilingue](/locales/README.md)
- [Requisiti di sicurezza e conformità](/SECURITY.md)

---

## 📄 Licenza

Questo progetto è pubblicato sotto la [Licenza MIT](/LICENSE). Può essere utilizzato gratuitamente a fini educativi e di ricerca. Per uso commerciale, si prega di verificare attentamente il rispetto delle normative legali applicabili.

---

> 🌟 Se questo strumento ti è stato utile, non esitare a ✨assegnargli una Stella (Star)! Il tuo supporto è la più grande motivazione per continuare a mantenere e migliorare questo progetto~

*Ultimo aggiornamento: Maggio 2026 | Versione: v2.1.0*
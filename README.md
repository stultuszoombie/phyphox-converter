# Phyphox Converter (Versione Free)

![License](https://img.shields.io/badge/License-MIT-green.svg)
![Made with](https://img.shields.io/badge/Made%20with-JavaScript-yellow)
![Status](https://img.shields.io/badge/Status-Active-blue)
![Contributions](https://img.shields.io/badge/Contributions-Welcome-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Web-lightgrey)

---

Convertitore ed elaboratore di dati accelerometrici esportati da [Phyphox](https://phyphox.org).  
Permette di caricare file CSV, applicare compensazioni e filtri, calcolare velocità e spostamenti, stimare inclinazioni e visualizzare i risultati con grafici interattivi.

---

## 🚀 Funzionalità principali

- **Parsing CSV robusto** (PapaParse streaming)
- **Compensazione gravitazionale (Zeroing)** con offset sui primi N punti
- **Filtri**:
  - Passa-basso (media mobile)
  - Fourier (DFT + IDFT, soglia regolabile 5–50 Hz)
- **Elaborazione dati**:
  - Frequenza di campionamento dinamica
  - Doppia integrazione trapezoidale
  - Correzione deriva lineare/cubica
  - Calcolo inclinazioni (pitch/roll)
- **Visualizzazione grafica**:
  - Accelerazione, velocità, spostamento, inclinazione
  - Evidenziazione picchi locali
  - Zoom/pan interattivi
  - Modalità notte
- **Report ed esportazione**:
  - Riepilogo finale con statistiche
  - Stampa report
  - Download CSV dei dati derivati

---

## 🖼️ Screenshot

### Interfaccia iniziale
![Interfaccia iniziale](https://github.com/stultuszoombie/phyphox-converter/blob/main/images/interfaccia.png)

### Grafici Accelerazione
![Grafici Accelerazione](https://github.com/stultuszoombie/phyphox-converter/blob/main/images/accel.png)

### Grafici Velocità
![Grafici Velocità](https://github.com/stultuszoombie/phyphox-converter/blob/main/images/velox.png)

### Grafici Spostamento
![Grafici Spostamento](https://github.com/stultuszoombie/phyphox-converter/blob/main/images/spostamento.png)

### Analisi Derivata
![Analisi Derivata](link-alla-tua-immagine)

---

## 📐 Linee guida di calcolo

- **Pendenza (pitch/roll)** → calcolata su dati grezzi (gravità inclusa).
- **Velocità e spostamento** → calcolati su dati compensati (gravità rimossa).
- **Regola millimetrica** → se ΔX/Y/Z < 1 mm, i filtri vengono disabilitati automaticamente.
- **Decimazione** → riduce i dati per evitare collasso del browser.

---

## 📂 Istruzioni d’uso

1. **Seleziona unità di misura output** (m, cm, mm) prima di caricare il file.
2. **Carica il CSV** esportato da Phyphox (con “g inclusa”).
3. **Attiva/disattiva compensazione e filtri** secondo necessità.
4. **Elabora i dati** → vengono generati grafici e statistiche.
5. **Esporta o stampa** i risultati.

---

## 📤 Esportazione

- CSV con accelerazioni filtrate, velocità, spostamenti, tempo.
- Report stampabile con statistiche (max, min, media).

---

## 🖋️ Credits

- Librerie: [Chart.js](https://www.chartjs.org/), [Tailwind CSS](https://tailwindcss.com/), [PapaParse](https://www.papaparse.com/)
- Ottimizzato con il supporto di **Copilot AI by Microsoft**

---

### 📌 Note importanti

- Il filtro Fourier è attualmente un **placeholder**: per un'elaborazione reale si consiglia l'integrazione di una libreria FFT.
- Il pulsante "Rimuovi Offset/Gravità" modifica i dati in memoria ma non li ripristina: per tornare ai dati originali, è necessario ricaricare il file.

---

### 📥 Come contribuire

Se vuoi migliorare il progetto, puoi:
- Aprire una issue
- Proporre una pull request
- Suggerire nuove funzionalità

---

## Licenza

Questo progetto è rilasciato sotto licenza MIT.  
Vedi il file [LICENSE](LICENSE).

---

### 🧑‍💻 Autore

Shaped by **S͓͎̻͕̥͓̘͑̔̇̈́̍͂̏̃͜t̴̲̟̖͖̰̀͒̈́̉ű͔͉͙̯̝ͭ̅ͣl̡͎̥͖̼̱̐̅́ͫ́͡͡t̶̯̫̼̜̩͚̤̜̆̏ͬ͂ͩ͗͛̈́ư̢͔̮̜̞̝̂̉ͮ͊ͮͤ́Ƨ̨̞͇̜̬̦̺ͨ̊́̽̾͛ͦͅ** Powered by WstT.org

---

Tutti i marchi citati sono dei rispettivi proprietari.

---

**Progetto open source a scopo didattico.**

---

💙 Dedicato ai miei figli

---

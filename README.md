# Phyphox Raw Data Converter

Convertitore di dati raw da Phyphox a grafici e riassunto di spostamenti, velocità e accelerazione.
# 📊 Convertitore Raw Data Phyphox (Ottimizzato)

### 🎯 Descrizione

Questo progetto è uno strumento web interattivo per visualizzare e analizzare i dati grezzi esportati da **Phyphox**, l'app per esperimenti fisici. Permette di caricare file CSV, applicare filtri, visualizzare grafici e ottenere analisi derivate come velocità, spostamento e pendenza.

---

### 🚀 Funzionalità principali

- 📁 **Upload CSV**: Carica file generati da Phyphox con dati di accelerazione.
- 📊 **Grafici dinamici**: Visualizzazione interattiva di accelerazioni, velocità e spostamenti.
- 🧮 **Analisi derivata**: Calcolo di velocità e spostamento tramite integrazione trapezoidale.
- 🧭 **Stima pendenza**: Calcolo angolo di inclinazione basato sull'accelerazione media.
- 🧹 **Rimozione offset/gravità**: Pulsante per compensare l'accelerazione residua.
- 🧪 **Filtri opzionali**:
  - Filtro passa-basso (media mobile)
  - Filtro Fourier (placeholder, estendibile)
- 📦 **Esportazione CSV**: Salvataggio dei dati derivati in formato CSV.
- 🖨️ **Modalità stampa**: Layout ottimizzato per la stampa del report.

---

### 🛠️ Tecnologie utilizzate

- [Chart.js](https://www.chartjs.org/) – per la visualizzazione grafica
- [PapaParse](https://www.papaparse.com/) – per il parsing dei file CSV
- [Tailwind CSS](https://tailwindcss.com/) – per lo stile responsivo e moderno
- JavaScript Vanilla – per la logica e l'interattività

---

### 📂 Struttura del progetto

- `index.html` – file principale con layout, script e stile
- Tutto il codice è contenuto in un singolo file HTML per facilità d'uso

---

### 📌 Note importanti

- Il filtro Fourier è attualmente un **placeholder**: per un'elaborazione reale si consiglia l'integrazione di una libreria FFT.
- Il pulsante "Rimuovi Offset/Gravità" modifica i dati in memoria ma non li ripristina: per tornare ai dati originali, è necessario ricaricare il file.

---

### 📷 Screenshot (opzionale)

Puoi aggiungere immagini del layout, dei grafici o della stampa per mostrare il funzionamento.

---

### 📥 Come contribuire

Se vuoi migliorare il progetto, puoi:
- Aprire una issue
- Proporre una pull request
- Suggerire nuove funzionalità

---

## Come funziona

1. Carica il tuo file CSV esportato da Phyphox.
2. Visualizza i grafici di accelerazione, velocità e spostamento.
3. Puoi scegliere l’unità di misura (m, cm, mm) e applicare/disattivare filtri sui dati.
4. Il tool mostra avvisi se i dati sono troppo piccoli o se il file è troppo grande.

## Avvertenze

- Per spostamenti inferiori al millimetro è consigliato disabilitare i filtri per una dinamica più realistica.
- I risultati sono calcolati tramite integrazione dei dati e possono essere influenzati da errori del sensore.

## Licenza

Questo progetto è rilasciato sotto licenza MIT.  
Vedi il file [LICENSE](LICENSE).


---


### 🧑‍💻 Autore

Creato da **S͓͎̻͕̥͓̘͑̔̇̈́̍͂̏̃͜t̴̲̟̖͖̰̀͒̈́̉ű͔͉͙̯̝ͭ̅ͣl̡͎̥͖̼̱̐̅́ͫ́͡͡t̶̯̫̼̜̩͚̤̜̆̏ͬ͂ͩ͗͛̈́ư̢͔̮̜̞̝̂̉ͮ͊ͮͤ́Ƨ̨̞͇̜̬̦̺ͨ̊́̽̾͛ͦͅ**

Progetto open source a scopo didattico.  
Tutti i marchi citati sono dei rispettivi proprietari.

**Progetto open source a scopo didattico.**

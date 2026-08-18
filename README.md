# Dashboard Controllo di Gestione

Strumento di controllo di gestione per PMI. Un unico file HTML: si apre nel browser, non richiede installazione, server o connessione internet. I dati restano sul computer di chi la usa.

**Demo online:** https://ggg250870.github.io/dashboard-controllo-gestione/

---

## Cosa fa

| Modulo | A cosa serve |
|---|---|
| 📊 Cruscotto KPI | Venduto, fatturato, incassato, gap incassi, 1° e 2° margine, incidenza costi fissi, saldo CC medio |
| 📋 Piano Finanziario | Ricavi e costi mese per mese, costo del personale, confronto preventivo/consuntivo |
| 💰 Cashflow | Entrate e uscite previste, saldo progressivo |
| 📝 Registro Movimenti | Prima nota: alimenta cashflow e incassato in automatico |
| 📈 Marginalità | Margine per prodotto/servizio, costi variabili e manodopera |
| ⚡ Velocità del Denaro | Tempi di incasso e pagamento, ciclo del circolante |
| ⚖️ Punto di Pareggio | Break even point, calcolato dal Piano Finanziario |
| 🏦 Stato Patrimoniale | Attivo, passivo, patrimonio netto |
| 💅 Marginalità Corsi | Modulo dedicato al settore beauty |
| 📖 Guida & Manuale | Istruzioni d'uso integrate |

**Settori preconfigurati:** generico, ristorazione, studio legale, beauty e altri. Ogni settore porta le proprie voci di ricavo e di costo già impostate.

**Import / export:** importazione da Excel e da estratto conto PDF, esportazione in Excel e in JSON (il JSON è il file dati da salvare e ricaricare).

**Blocco configurazione:** password per impedire al cliente di modificare la struttura dei conti.

---

## Come si usa

1. Scarica [`index.html`](index.html) (pulsante **Download raw file**).
2. Aprilo con doppio clic: si apre nel browser.
3. Inserisci il nome azienda e l'anno, poi compila i moduli.
4. **Salva file** dalla barra laterale → scarica il `.json` con i tuoi dati.
5. Alla riapertura usa **Carica file** per riprendere da dove eri.

> ⚠️ I dati vivono nel browser e nel file JSON. Fai il salvataggio prima di chiudere.

---

## Struttura del repository

```
index.html          Versione completa: librerie incorporate, funziona offline.
                    È il file da consegnare ai clienti.

src/index.html      Sorgente leggibile: HTML + CSS + JS, librerie da CDN.
                    È il file su cui sviluppare. Richiede internet.
src/app.js          Solo logica applicativa (~2.950 righe, 112 funzioni).
src/style.css       Solo stile.
```

**Come modificare:** lavora su `src/`, poi rigenera `index.html` incorporando le librerie. Non modificare direttamente `index.html`: contiene 2,3 MB di librerie minificate ed è illeggibile.

---

## Tecnologia

HTML, CSS e JavaScript senza framework. Librerie: [Chart.js 4.4.0](https://www.chartjs.org/) per i grafici, [SheetJS 0.18.5](https://sheetjs.com/) per Excel, [PDF.js 3.11.174](https://mozilla.github.io/pdf.js/) per l'import da estratto conto.

---

## Licenza

Copyright © 2026 Giovanni Girò. Tutti i diritti riservati.

Il codice è pubblico per consultazione e per la demo. Riuso, redistribuzione o impiego commerciale solo previa autorizzazione scritta.

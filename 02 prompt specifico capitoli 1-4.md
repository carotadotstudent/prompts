# Prompt 2 — Istruzioni specifiche (documento structural FX, capitoli 1–4)

**Uso:** incolla il testo nello stesso messaggio del Prompt 1 oppure subito dopo, allegando il markdown parziale e i JPEG.
Poi scrivi "continua" per ogni capitolo successivo e "controlla" alla fine.

**Prima di partire:** i JPEG vanno in una cartella `img/` accanto all'HTML finale, con gli stessi nomi citati nel markdown.

---

## Prompt

```
Applica le istruzioni generali e il template che ti ho dato. Allego il Markdown parziale della documentazione di sviluppo di un modello structural FX e le immagini JPEG (i nomi file sono quelli citati nel Markdown).

AMBITO
Copri SOLO i primi 4 capitoli, nell'ordine e con i titoli esatti del Markdown:
1. Introduction  2. Background  3. Model framework  4. Model development data
Ignora tutto ciò che segue (Model development process, Model testing, Model selection, Operating environment, ecc.). Nella cover scrivi "Copertura: Capitoli 1–4".

COVER
- Kicker: "Documentazione di sviluppo · Capitoli 1–4"
- Titolo: nome del modello come appare nel documento. Sottotitolo: scopo del modello in 1–2 frasi, ricavate dall'Introduction.
- Meta: nome e versione del documento, se presenti nel Markdown; altrimenti "[da verificare]".

ATTENZIONI PER CAPITOLO
- Cap. 1 Introduction: scopo, perimetro, uso previsto, utilizzatori, versione, stato di approvazione. Usa .cards per i fatti identificativi del modello.
- Cap. 2 Background: contesto economico/di business e motivazione del modello. Definizioni in .box.def. Se il documento cita letteratura o modelli alternativi, riportali come elenco, senza aggiungere riferimenti tuoi.
- Cap. 3 Model framework: è il cuore tecnico. Per ogni sezione: (a) specifica del modello e formule in .eq, (b) tutte le ipotesi in .box.syn, (c) notazione e parametri in .cards o tabella, (d) limiti in .box.warn. Rispetta l'ordine logico del documento e collega le formule con link interni quando il testo rimanda a equazioni precedenti. Se il documento contiene schemi, inseriscili come figure.
- Cap. 4 Model development data: fonti dati, frequenza, finestra temporale, pulizia, trasformazioni, trattamento di outlier e dati mancanti. Le tabelle devono essere riportate per intero con valori identici. Eventuali problemi di qualità dati dichiarati vanno in .box.warn.

DOMANDE APERTE PER LA VALIDAZIONE
A fine di ogni capitolo, 2–4 domande che un validatore farebbe leggendo SOLO quel testo (ipotesi non giustificate, parametri senza fonte, scelte senza alternative discusse, dati senza controllo di qualità descritto). Ogni domanda cita la sezione a cui si riferisce. Niente domande generiche.

PROCEDURA
Passo 1 (adesso): restituisci un unico blocco con il file HTML completo (head con CSS e script del template, cover, indici, Capitolo 1, footer). Dopo il blocco elenca: figure del Cap. 1 inserite, figure non trovate, punti "[da verificare]".
Passi 2, 3, 4 (quando scrivo "continua"): restituisci SOLO il blocco <section class="chapter" id="cap02"> (poi cap03, cap04), pronto da incollare prima di <footer class="closing">. Non ripetere head, cover o indici.
Passo finale (quando scrivo "controlla"): checklist con (1) capitoli coperti, (2) elenco figure del Markdown e se ciascuna è stata inserita, (3) numero di formule nel Markdown vs nell'HTML, (4) numero di tabelle nel Markdown vs nell'HTML, (5) tutti i "[da verificare]".

Inizia dal Passo 1.
```

# Project Work 17 - Landing Page per Report di Sostenibilità

**Studente:** Francesco Antonio De Rosa (A.A. 2026-2027)  
**Corso:** Project Work, Tema 3 - Traccia 17  
**Università:** Università Telematica Pegaso  

---

## Descrizione del progetto
Questo repository ospita il codice sorgente del mio Project Work. L'idea alla base del progetto è stata quella di sviluppare una landing page che non fosse solo una vetrina, ma uno strumento pratico e interattivo per comunicare l'impegno ambientale di un'azienda del settore primario e permettere il download dei suoi report ufficiali. 

Come caso studio ho scelto il Gruppo Granarolo, basandomi sui dati reali del loro Bilancio di Sostenibilità 2024.

## Scelte tecniche e librerie utilizzate
Per mantenere il progetto snello e facilmente consultabile offline (senza dover configurare un server locale o installare dipendenze), ho optato per un'architettura a file singolo (`index.html`) appoggiandomi a librerie esterne caricate via CDN:

* **Tailwind CSS:** L'ho utilizzato per gestire tutto il layout e lo stile direttamente nell'HTML, velocizzando parecchio lo sviluppo e garantendo la responsività su mobile.
* **Chart.js:** Mi serviva per rendere interattivo e preciso il grafico sull'andamento delle emissioni di CO2.
* **AOS (Animate On Scroll):** Aggiunge un po' di dinamismo alla pagina man mano che si scende con lo scroll, rendendo la lettura meno piatta.
* **FontAwesome:** Utilizzato per le icone vettoriali, in modo da non appesantire il caricamento della pagina con troppe immagini.

## Come è stato realizzato
Ho cercato di curare sia l'aspetto visivo che la logica del codice:

* **Design e UX:** Ho scelto un'interfaccia pulita, usando un effetto "glassmorphism" (vetro smerigliato) per le schede. I dati aziendali sono organizzati in una griglia CSS asimmetrica (bento grid) che si riorganizza automaticamente se si apre la pagina da smartphone.
* **Interattività:** C'è un piccolo script in JavaScript che cambia dolcemente il colore di sfondo della pagina quando si arriva alla sezione della filiera agricola, per staccare visivamente gli argomenti.
* **Gestione Download:** I bottoni per scaricare i report non sono semplici link, ma attivano una funzione JavaScript che forza il download diretto dei PDF in locale.
* **Rigore dei dati:** In fondo alla pagina ho inserito una mappatura precisa delle fonti, collegando ogni dato usato nel sito alla pagina esatta del report ufficiale di riferimento. Inoltre, ho dedicato una sezione al framework ONU degli SDGs, per dare un contesto metodologico forte.

## Struttura delle cartelle
Per far funzionare tutto correttamente, la struttura dei file deve rimanere questa:

```text
├── index.html              
├── img/                    
│   ├── logo-granarolo.svg  
│   ├── logo-sdgs.png       
│   ├── favicon.png         
│   └── (altre immagini JPG)
└── reports/                
    ├── BilancioSostenibilitaGranarolo2024.pdf
    └── SintesiBilancioSostenibilitaGranarolo2024.pdf

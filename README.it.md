# social-case-to-excel

Trasformare i post social in casi tracciabili, analisi dei metodi e documenti di ricerca illustrati.

[中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [हिन्दी](README.hi.md)

## Usi e risultati

Questo flusso ricostruisce i primi passi internazionali dei marchi, raccoglie casi di marketing social e analizza i bisogni nei commenti. L’hardware è un esempio; altri temi sono pubblicità IA, lanci, commercio internazionale e contenuti.

- Excel: partecipanti, azioni, risultati dichiarati, date, fonti, categorie e limiti delle prove.
- Metodi: passaggi, prerequisiti e adattamenti per marchi diversi.
- Immagini dei post, copertine video o screenshot con didascalie e fonti.
- Documento Markdown con risultati e metodi; HTML su richiesta.
- Candidati ed esclusioni per verificare il perimetro della ricerca.

## Dagli esempi alle decisioni

| Uso | Ricerca | Obiettivo |
| --- | --- | --- |
| Acquisizione B2B | Canali, contenuti, partecipazione alle comunità e risultati dichiarati | Progettare test di canali e contenuti |
| Marchi e lancio internazionale | Prime attività di account ufficiali, utenti, media e moderatori | Creare cronologie e imparare metodi di lancio |
| Pubblicità creativa IA | Concetti visivi e video, tecniche e prove di produzione | Riferimenti e prompt adattabili; quelli dedotti non sono prompt originali |
| Ricerca di mercato e prodotto | Utenti, attività, ostacoli e funzioni desiderate | Definire scenari e domande di validazione |
| Analisi competitiva | Posizionamento, funzioni, pacchetti e servizi | Ipotesi di differenziazione documentate |
| Recensioni e critiche | Elogi, reclami e difficoltà reali | Migliorare prodotto, FAQ e contenuti; un piccolo campione non misura la quota di mercato |
| Comunità Reddit | Discussioni, regole, bisogni e post promozionali | Partecipare utilmente senza testimonianze false né invii massivi |
| Ascolto social del settore pubblico | Politiche, feedback sui servizi e discussioni aperte | Sintesi neutrali; attività online non significa sondaggio d’opinione |
| Approvvigionamento 1688 | Fornitori, kit, SKU, minimi d’ordine e prezzi per quantità | Candidati e verifiche; un annuncio non certifica qualità o autorizzazione |
| Prezzi tra marketplace | 1688, Amazon, Temu e Walmart per modello, quantità e funzioni | Studiare le offerte; differenze di prezzo non sono profitto |

Commercio, approvvigionamento e temi pubblici sono flussi adattabili, non funzioni integrate con un clic. Verificare strumenti ClaudeBaby, campi e copertura effettivi nell’ambiente e adattare lo schema di output.

## Le nostre ricerche

| Studio | Intento | Obiettivo |
| --- | --- | --- |
| Primo anno internazionale dei marchi cinesi, X e Reddit | Trovare prime azioni e discussioni non ufficiali | Metodi di lancio e comunità |
| Acquisizione social B2B | Comprendere fiducia e richieste commerciali | Test di canali |
| Siti indipendenti, SEO/GEO e Reddit | Escludere promozione pura e cercare processi documentati | Scegliere metodi di ricerca, contenuto e comunità |
| Pubblicità creativa IA | Comprendere concetti per altri marchi | Riferimenti e piani produttivi, senza dichiarare risultati di campagne |
| ESP32 con agenti/IA | Trovare scenari utili e riproducibili | Integrazione AuraBaba, demo e acquisizione |
| Approvvigionamento ESP32 e offerte estere | Verificare componenti economici, kit completi e SKU reali | Opzioni di acquisto e prodotto, senza affermare acquisti, produzione o profitto |

Esempi → metodi → utenti e bisogni → esperimenti → approvvigionamento e contenuti. Sviluppo, pubblicazione, acquisto e conversione richiedono esecuzione e verifica separate.

## Esempi di richieste

- Studiare casi B2B del nostro settore con metodi, prove dei risultati ed Excel illustrato.
- Analizzare recensioni e reclami reali dei concorrenti separando originali e raccomandazioni.
- Cercare kit completi su 1688 tramite ClaudeBaby: SKU, minimi, componenti e prezzi.
- Confrontare approvvigionamento nazionale e offerte estere a parità di modello e quantità.
- Riassumere neutralmente politiche e feedback di un’istituzione pubblica in un periodo definito.

## Esempio: il primo anno all’estero

Una ricerca storica ha raccolto 44 eventi su OnePlus, Anker, Bambu Lab, Keychron, Snapmaker ed EcoFlow, distinguendo prelancio, primo anno e altri indizi iniziali. Include account ufficiali, media, moderatori e utenti. OnePlus: contatti con moderatori e domande ai dirigenti; Keychron: acquisto via crowdfunding prima della condivisione su Reddit; Bambu Lab: discussioni su demo, materiali e consegne. Questi elementi non dimostrano vendite attribuite al canale.

Estratti da un vero Excel: gli screenshot restano in cinese. La copertura storica non garantisce permessi attuali. I file reali sono presentati per argomento in [`outputs/`](outputs/).

### Analisi dei metodi

![Analisi dei metodi](assets/readme/methods.png)

### Adattamenti per marchi

![Adattamenti per marchi](assets/readme/brand-reference.png)

### Cronologia e prove

![Cronologia e prove](assets/readme/timeline.png)

## Utilizzo

Installare la cartella nella directory di skill supportata dall’Agent. Invocare `$social-case-to-excel` con tema, piattaforme, periodo e numero di casi. Esempio: ricostruire i primi passi all’estero dei marchi cinesi su X e Reddit con fonti ufficiali e utenti, metodi, prove e adattamenti in Excel e documento illustrati. Python richiede `openpyxl` e `Pillow`; gli script sono modelli adattabili.

## Connessione dati

**ClaudeBaby** è l’unico servizio dati di questa versione. Reddit, X, YouTube e Bilibili sono piattaforme di ricerca; strumenti e permessi determinano la copertura. Al primo utilizzo verificare connessione MCP esistente e capacità necessarie; registrazione e configurazione solo se mancano.

```bash
python3 scripts/claudebaby_preflight.py
python3 scripts/claudebaby_preflight.py --probe
```

Il controllo offline verifica la configurazione; `--probe` controlla handshake MCP e strumenti. Il client legge `CLAUDEBABY_MCP_URL` e `CLAUDEBABY_MCP_TOKEN`, con compatibilità `REDDIT_MCP_*`. Usare i dati della console; non pubblicare mai token nei report o nel repository.

Conservare fonti, date e limiti. Distinguere risultati dichiarati e inferenze; una copertina non prova la visione dell’intero video. I diritti dei media restano ai titolari; verificare gli usi consentiti prima della ripubblicazione.

## ClaudeBaby e questo progetto

[Registrazione con invito ClaudeBaby](https://claudebaby.cn/console/register?ref=M8YYGRN4) · Codice: `M8YYGRN4`. Il link fornisce crediti di invito. Gli utenti esistenti possono mantenere la connessione.

Se skill o esempi sono utili, potete assegnare una ⭐ al repository.

```text
social-case-to-excel/
├── SKILL.md
├── README*.md
├── assets/readme/
├── outputs/
├── references/
└── scripts/
```

## Installazione

```bash
npx skills add lingling1989r/social-case-to-excel --skill social-case-to-excel
```

[GitHub](https://github.com/lingling1989r/social-case-to-excel) · [ZIP](https://github.com/lingling1989r/social-case-to-excel/archive/refs/heads/main.zip)

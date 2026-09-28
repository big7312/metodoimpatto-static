# Metodo IMPATTO - Diario di lavoro Codex

Ultimo aggiornamento: 2026-09-10

Questo documento serve a tenere memoria delle decisioni prese, dei passaggi tecnici e dei prompt utili per riprendere il lavoro con Codex senza ricostruire ogni volta il contesto.

## Obiettivo attuale

Creare una versione statica/editoriale di Metodo IMPATTO, separata dal sito WordPress locale, usando Astro e contenuti Markdown. La direzione scelta e un sito piu moderno, veloce, versionabile e adatto a deploy automatico su Cloudflare Pages.

## Perche stiamo passando da WordPress ad Astro

- Evitiamo la sincronizzazione continua del database.
- Gli articoli diventano file Markdown modificabili da Codex.
- Il deploy puo avvenire da GitHub verso Cloudflare Pages.
- Il sito e piu leggero, con meno manutenzione di plugin, tema e aggiornamenti WordPress.
- WordPress resta intatto come backup locale durante la transizione.

## Stato dei progetti

### WordPress locale

Percorso:

```text
C:\xampp\htdocs\metodoimpatto
```

Uso previsto:

- backup della prima versione;
- riferimento contenutistico e visivo;
- eventuale confronto con la versione Astro.

Repository GitHub:

```text
https://github.com/big7312/metodoimpatto
```

### Astro locale

Percorso:

```text
C:\xampp\htdocs\metodoimpatto\metodoimpatto-astro
```

Uso previsto:

- nuova versione principale del sito;
- contenuti in Markdown;
- build statica per Cloudflare Pages;
- repository GitHub separato dedicato alla versione statica.

Repository GitHub:

```text
https://github.com/big7312/metodoimpatto-static
```

Commit iniziale locale:

```text
780ebe5 Initial Astro rebuild
```

## Stack scelto

- Astro per generazione statica.
- Markdown/Content Collections per gli articoli.
- CSS custom senza framework UI pesanti.
- Font locali derivati dal tema WordPress: Fira Sans e Literata.
- Brevo per newsletter.
- Cloudflare Pages come hosting consigliato.

## Struttura principale

```text
src/pages/
src/components/
src/content/articles/
src/layouts/
src/styles/
public/fonts/
```

Pagine create:

- `/`
- `/metodo/`
- `/applicazioni/`
- `/articoli/`
- `/articoli/[slug]/`
- `/newsletter/`
- `/chi-sono/`
- `/contatti/`
- `/privacy/`

## Newsletter

Direzione editoriale:

```text
Il Prompt della Settimana
```

Promessa:

```text
Una mail breve ogni venerdi: un caso reale, un prompt commentato e una domanda per capire se l'AI sta davvero aiutando il processo.
```

CTA:

```text
Ricevi il prossimo prompt
```

Scelta operativa:

- partire con fallback statico nel componente `NewsletterBox.astro`;
- sostituire il form placeholder con embed Brevo o integrazione Brevo quando l'account sara pronto;
- evitare campi inutili come cognome, almeno nella fase iniziale.

## Comandi utili

Avviare anteprima locale:

```bash
npm run dev
```

Build di verifica:

```bash
npm run build
```

Anteprima della build:

```bash
npm run preview
```

## Deploy Cloudflare Pages

Impostazioni previste:

```text
Framework preset: Astro
Build command: npm run build
Build output directory: dist
Root directory: /
```

Stato configurazione:

```text
Configurato manualmente da Cloudflare Dashboard il 2026-09-09.
```

Passaggi eseguiti:

1. Aperto il menu `Workers & Pages`.
2. Cliccato `Create`.
3. Scelto `Pages`.
4. Selezionato `Connect to Git`.
5. Collegato GitHub.
6. Selezionato il repository Astro `big7312/metodoimpatto-static`.
7. Impostate le opzioni di build:

```text
Framework preset: Astro
Build command: npm run build
Build output directory: dist
Root directory: /
```

8. Cliccato `Save and Deploy`.

Verifiche da fare dopo il primo deploy:

- controllare che Cloudflare completi la build senza errori;
- aprire l'URL `pages.dev` generato;
- verificare home, newsletter, articoli e responsive mobile;
- collegare il dominio definitivo solo dopo controllo visuale;
- aggiornare questo documento con URL di preview e URL di produzione.

Prima del dominio definitivo serve:

- configurare dominio e redirect quando la versione Astro sara pronta.

## Prompt utili per Codex

### Riprendere il progetto

```text
Stiamo lavorando sulla versione Astro statica di Metodo IMPATTO in C:\xampp\htdocs\metodoimpatto\metodoimpatto-astro. WordPress resta come backup. Prima di modificare, leggi docs/codex-worklog.md e controlla git status.
```

### Creare un nuovo articolo

```text
Crea un nuovo articolo Markdown per Metodo IMPATTO dentro src/content/articles. Mantieni tono pratico, niente hype AI, parti da un problema reale e chiudi con una domanda operativa. Aggiorna anche docs/codex-worklog.md con cosa hai aggiunto e perche.
```

### Modificare la newsletter

```text
Aggiorna la sezione newsletter mantenendo la rubrica "Il Prompt della Settimana". Valuta tono, campi, microcopy, privacy e attrito del form. Se cambi copy o integrazione Brevo, aggiorna docs/codex-worklog.md.
```

### Preparare Cloudflare Pages

```text
Prepara il progetto Astro per Cloudflare Pages. Verifica npm run build, controlla che l'output sia dist, aggiorna README.md e docs/codex-worklog.md con i passaggi di deploy.
```

### Fare una modifica visuale

```text
Migliora il design del sito Astro senza renderlo generico o "AI generated". Mantieni la direzione editoriale: sobria, concreta, moderna, con tipografia forte e layout non banale. Verifica responsive e aggiorna docs/codex-worklog.md.
```

## Registro modifiche

### 2026-09-09 - Creazione versione Astro

Cosa e stato fatto:

- creato progetto Astro locale in `metodoimpatto-astro`;
- aggiunte pagine principali;
- aggiunta collezione articoli Markdown;
- aggiunti tre articoli iniziali;
- creato componente newsletter;
- impostato design editoriale con CSS custom;
- copiati font locali dal tema WordPress;
- verificata build con `npm run build`.

Perche:

- ridurre dipendenza da database WordPress;
- rendere il sito piu facile da modificare con Codex;
- preparare deploy automatico su Cloudflare Pages;
- mantenere WordPress come backup e non come collo di bottiglia.

### 2026-09-09 - Creazione diario Codex

Cosa e stato fatto:

- creato questo documento operativo;
- aggiunti obiettivo, stack, struttura, comandi, deploy previsto e prompt riutilizzabili.

Perche:

- evitare perdita di contesto tra sessioni;
- rendere esplicite le decisioni tecniche;
- avere prompt pronti per chiedere a Codex modifiche coerenti.

### 2026-09-09 - Collegamento repository GitHub statico

Cosa e stato fatto:

- scelto il repository GitHub dedicato alla versione Astro: `https://github.com/big7312/metodoimpatto-static`;
- mantenuto il progetto Astro separato dal repository WordPress.
- pubblicato il branch `main` del progetto Astro su GitHub.

Perche:

- evitare di mischiare WordPress e Astro nello stesso repository;
- preparare un collegamento pulito con Cloudflare Pages;
- rendere il deploy statico indipendente dal sito WordPress locale.

Nota operativa:

- il progetto locale e stato aggiunto ai `safe.directory` di Git per consentire il push con l'utente Windows;
- il repository locale ora traccia `origin/main`.

### 2026-09-09 - Configurazione Cloudflare Pages

Cosa e stato fatto:

- collegato Cloudflare Pages al repository GitHub `big7312/metodoimpatto-static`;
- scelto preset `Astro`;
- impostato comando build `npm run build`;
- impostata cartella output `dist`;
- mantenuta root directory `/`;
- avviato il primo deploy da Cloudflare.

Perche:

- abilitare deploy automatici da GitHub;
- evitare upload manuali via FTP;
- pubblicare la versione Astro come sito statico veloce e separato da WordPress.

### 2026-09-10 - Pubblicazione articolo su priorita clienti e CRM

Cosa e stato fatto:

- aggiunto l'articolo `ai-priorita-clienti-crm.md`;
- impostata `pubDate: 2026-09-06`;
- scelta categoria `Vendite`;
- rimosso un file articolo non tracciato rimasto dal turno interrotto precedente, per evitare pubblicazioni non richieste.

Perche:

- pubblicare un contenuto gia pronto senza passare dal database WordPress;
- testare il flusso editoriale Astro: Markdown, build, commit, push e deploy automatico Cloudflare;
- mantenere il blog coerente con il Metodo IMPATTO: prima dati e processo, poi AI.

### 2026-09-28 - Aggiornamento palette colori

Cosa e stato fatto:

- aggiornata la palette CSS senza modificare layout, struttura, tipografia, spaziature o contenuti;
- impostato lo sfondo avorio con gradienti molto leggeri blu e corallo;
- adottato `#172033` per testi e titoli;
- adottato `#3454D1` come colore principale per brand, link e azioni;
- riservato `#FF6B4A` agli accenti e usato `#E8EEFF` per superfici secondarie e card;
- armonizzati bordi, ombre, form e testi secondari con la nuova direzione editoriale.

Perche:

- rendere il sito piu dinamico e moderno senza introdurre nuovi elementi grafici;
- aumentare la riconoscibilita del blu indaco mantenendo il corallo non dominante;
- dare profondita allo sfondo senza trasformarlo in un gradiente decorativo evidente.

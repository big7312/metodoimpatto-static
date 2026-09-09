# Metodo IMPATTO - Diario di lavoro Codex

Ultimo aggiornamento: 2026-09-09

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

Prima del deploy serve:

- creare un repository GitHub dedicato, consigliato `metodoimpatto-astro` o `metodoimpatto-static`;
- collegare il repository a Cloudflare Pages;
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

Perche:

- evitare di mischiare WordPress e Astro nello stesso repository;
- preparare un collegamento pulito con Cloudflare Pages;
- rendere il deploy statico indipendente dal sito WordPress locale.

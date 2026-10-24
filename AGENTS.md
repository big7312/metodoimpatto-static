# Metodo IMPATTO — guida operativa

## Progetto e mappa
- Sito editoriale italiano: Astro + TypeScript, output statico per Cloudflare Pages (`dist/`).
- Pagine: `src/pages/`; layout, metadati SEO, header e footer: `src/layouts/BaseLayout.astro`.
- Identità, URL e navigazione: `src/consts.ts`; configurazione build: `astro.config.mjs`.
- Stili e variabili condivise: `src/styles/global.css`; componenti riutilizzabili: `src/components/`.
- Articoli: `src/content/articles/*.md`; schema: `src/content.config.ts`; elenco e dettaglio: `src/pages/articoli/`.
- Asset statici e font: `public/`. Newsletter: `src/components/NewsletterBox.astro`, attualmente placeholder disabilitato per futura integrazione Brevo.

## Modifiche e contesto
- Leggi prima i file coinvolti e cerca riferimenti/caller con `rg`; amplia l'esplorazione solo quando necessario.
- Riusa componenti, variabili CSS e convenzioni esistenti. Preferisci Astro, HTML e CSS nativi; aggiungi dipendenze o astrazioni solo per esigenze concrete.
- Mantieni la direzione editoriale e il tono italiano: AI utile per piccole imprese e professionisti, prima obiettivi e processi, poi strumenti.
- Per gli articoli rispetta i campi `title`, `description`, `pubDate`, `category`, `draft`; non cambiare slug o date di contenuti esistenti senza motivo legato alla richiesta.
- Conserva semantica HTML, accessibilità, responsive e metadati nelle modifiche UI.
- Controlla `git status` e preserva modifiche preesistenti. Intervieni sui sorgenti; `dist/`, `.astro/` e `node_modules/` sono generati.
- Questo file è il riferimento rapido. Consulta sezioni mirate di `docs/codex-worklog.md` solo se servono decisioni storiche; dopo modifiche significative aggiungi una nota breve con decisione e verifica, senza trascrivere la conversazione.

## Verifica
- Per modifiche a codice, contenuti o configurazione esegui `npm run build` (include `astro check`); segnala eventuali errori o impossibilità di verifica.
- Per cambiamenti visivi verifica anche la pagina interessata a larghezza desktop e mobile, se è disponibile un browser.
- Per sole istruzioni/documentazione basta controllare diff e percorsi. Aggiungi test dedicati quando proteggono logiche o regressioni concrete.
- Comandi locali: `npm run dev`, `npm run preview`. Riassumi risultato, verifica ed eventuali limiti in poche righe.

## Skill facoltative
- Se installate in `.agents/skills/`, seleziona solo quelle pertinenti al compito e leggi riferimenti aggiuntivi su necessità.
- `ui-ux-pro-max`: dubbi specifici di UI, responsive e accessibilità; preferisci una ricerca mirata al problema.
- `copywriting`: testi persuasivi delle pagine e CTA; `seo-audit`: verifiche SEO richieste; `api-integration`: integrazioni reali come Brevo.
- `site-architecture` e `content-strategy`: riorganizzazione del sito e pianificazione editoriale.
- Le normali correzioni Astro seguono questa guida senza richiedere una skill generica. La presenza di una skill non richiede di usarla; le istruzioni esplicite dell'utente hanno precedenza.

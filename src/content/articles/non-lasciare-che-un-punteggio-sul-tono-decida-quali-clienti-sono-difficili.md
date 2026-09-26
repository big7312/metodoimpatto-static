---
title: "Non lasciare che un punteggio sul tono decida quali clienti sono difficili"
description: "L’AI può analizzare il tono dei messaggi e segnalare le richieste urgenti. Ecco come usarla nel CRM senza trasformare un punteggio in un giudizio sui clienti."
pubDate: 2026-09-26
category: "Metodo"
draft: false
---

Arriva questa email:

> “Ho bisogno di una risposta oggi. Il problema non è ancora risolto.”

Un sistema di analisi automatica potrebbe classificarla come negativa, urgente o aggressiva. Il CRM potrebbe aumentare la priorità, avvisare il responsabile e suggerire una risposta più prudente.

Può essere molto utile.

Il rischio nasce quando trasformiamo l’analisi del messaggio in un giudizio sulla persona:

> “Cliente arrabbiato.”

> “Cliente difficile.”

> “Alto rischio di abbandono.”

L’intelligenza artificiale vede alcune parole, la punteggiatura e, se glielo permettiamo, la conversazione precedente. Non vede il volto del cliente, non conosce necessariamente il suo modo abituale di scrivere e non sa che cosa sia successo fuori dal messaggio.

Io utilizzerei l’analisi del tono come segnale per controllare prima una comunicazione. Non come diagnosi delle intenzioni del cliente.

## Un messaggio negativo può contenere una richiesta ragionevole

Prendiamo un’altra frase:

> “Non ho ricevuto il documento promesso. Potete inviarmelo entro le 12?”

La valutazione negativa potrebbe essere corretta: il cliente sta segnalando un disservizio. Ma l’informazione utile non è che il cliente “ha un atteggiamento negativo”.

Le informazioni utili sono:

- manca un documento;
- esisteva una promessa precedente;
- il cliente indica una scadenza;
- serve verificare chi doveva agire;
- una risposta generica non risolve il problema.

Se il sistema si limita al tono, rischia di farci lavorare sull’emozione e non sulla causa.

Potremmo produrre una risposta molto empatica:

> “Comprendiamo perfettamente la sua frustrazione e ci dispiace per il disagio.”

Ma dimenticare di allegare il documento.

L’AI dovrebbe quindi separare almeno tre elementi: ciò che il cliente chiede, i fatti che dichiara e il tono che il sistema ipotizza.

Il terzo elemento non dovrebbe oscurare i primi due.

## Positivo, neutro e negativo sono etichette, non spiegazioni

I servizi commerciali di analisi del sentiment mostrano bene come funziona questo tipo di tecnologia.

Microsoft Azure assegna etichette come positivo, neutro e negativo e restituisce punteggi di confidenza per l’intero documento e per le singole frasi. Google Cloud utilizza valori relativi alla direzione e all’intensità del sentiment.

Sono risultati tecnici, non descrizioni complete della relazione.

Un messaggio può contenere contemporaneamente soddisfazione e critica:

> “Il prodotto è ottimo, ma l’assistenza non mi ha mai richiamato.”

Una classificazione complessiva rischia di comprimere due informazioni commerciali molto diverse. Il cliente apprezza ciò che ha acquistato e segnala un problema nel servizio.

Lo stesso accade con frasi brevi come:

> “Finalmente.”

Può esprimere soddisfazione perché il problema è risolto oppure irritazione per il tempo impiegato. Senza la conversazione precedente, la parola rimane ambigua.

La mia deduzione è che un punteggio di sentiment abbia valore soltanto quando conduce a una verifica concreta: quale evento, prodotto o passaggio del processo ha generato quel segnale?

## Lo stile diretto non è automaticamente aggressivo

Nel lavoro reale incontriamo persone che scrivono in modi molto differenti.

Qualcuno apre ogni email con formule cordiali e lunghe introduzioni. Qualcun altro arriva subito al punto:

> “Mandami il file.”

> “Richiamami.”

> “Così non funziona.”

Ci sono poi abbreviazioni, errori, espressioni regionali, maiuscole, messaggi dettati al telefono e testi scritti da persone che non utilizzano l’italiano come prima lingua.

Una ricerca presentata alla conferenza EMNLP 2024 ha analizzato le risposte dei modelli a dieci varietà di inglese. Gli autori hanno osservato problemi più frequenti di comprensione, stereotipi e risposte condiscendenti quando venivano utilizzate varietà considerate non standard.

Lo studio riguarda specifici modelli, dialetti inglesi e modalità di interazione. Non dimostra che ogni sistema di sentiment giudichi male ogni messaggio non standard.

Dimostra però che la forma linguistica può influenzare il comportamento del modello. Per questo non assocerei automaticamente scrittura poco formale, grammatica imperfetta o tono sintetico a scarsa educazione, rabbia o rischio commerciale.

## Un caso reale: urgenza non significa conflitto

In un progetto CRM reale già condiviso, dopo aver ripercorso con il cliente tutto il processo di gestione di un nuovo cliente, è arrivata la richiesta di avviare rapidamente la fase di test.

La motivazione era mantenere alta l’attenzione delle persone coinvolte ed evitare un nuovo rallentamento del progetto.

La richiesta conteneva urgenza. Non rappresentava necessariamente insoddisfazione o ostilità. Al contrario, nasceva anche dal coinvolgimento positivo emerso durante l’incontro.

Non sto sostenendo che in quel progetto sia stata usata l’AI per interpretare l’email: non è successo.

Il caso mostra però perché “urgente”, “negativo” e “cliente a rischio” non siano sinonimi. Per rispondere correttamente serviva comprendere il progetto, ciò che era ancora da validare e i passaggi necessari prima del test.

## Userei l’AI per stabilire priorità operative

L’analisi automatica può comunque aiutare molto un piccolo gruppo che riceve numerose richieste.

Potrebbe segnalare:

- scadenze esplicite;
- promesse aziendali non rispettate;
- richiesta ripetuta più volte;
- intenzione di annullare;
- contestazione di un importo;
- impossibilità di usare un prodotto;
- richiesta di parlare con un responsabile;
- possibile rischio per sicurezza o dati;
- assenza di risposta da parte dell’azienda.

Questi sono elementi più controllabili del generico “cliente arrabbiato”.

Nel CRM salverei il motivo della priorità, non un’etichetta permanente sulla persona. Scriverei “documento promesso non inviato” oppure “terza richiesta senza risposta”, non “cliente problematico”.

Una conversazione negativa descrive un momento della relazione. Non definisce il cliente per sempre.

## Il controllo dovrebbe partire dai nostri errori

Se molte comunicazioni vengono classificate come negative, non concluderei subito che abbiamo una clientela difficile.

Cercherei invece ricorrenze nel processo:

- le richieste aumentano dopo l’invio delle fatture?
- riguardano sempre lo stesso prodotto?
- compaiono quando manca una conferma?
- nascono da tempi indicati in modo ambiguo?
- si concentrano su una fase senza responsabile?
- il cliente deve sollecitare perché il CRM non crea l’attività successiva?

L’AI può raggruppare i messaggi e proporre le cause possibili. La conferma deve arrivare dai dati e dalla verifica delle conversazioni.

Il valore maggiore non è individuare chi si lamenta più forte. È scoprire quale parte del processo costringe i clienti a lamentarsi.

## Il metodo IMPATTO prima del punteggio

Con I — Identifica il risultato, non sceglierei “riconoscere i clienti arrabbiati”. Preferirei: “intervenire rapidamente sulle richieste che possono compromettere la relazione”.

Con M — Mappa il processo, seguirei il messaggio dall’arrivo alla chiusura: chi lo legge, chi decide la priorità, quali attività vengono create e come controlliamo la risposta.

Con P — Progetta la soluzione, separerei fatti, richieste, scadenze, tono ipotizzato e livello di confidenza. Definirei inoltre i casi che richiedono verifica umana.

Con A — Applica, proverei il sistema su un campione di messaggi già valutati da persone. Includerei comunicazioni brevi, ironiche, molto formali, dialettali, multilingue e contenenti insieme complimenti e critiche.

Misurerei segnalazioni corrette, urgenze mancate e falsi allarmi. Controllerei anche se alcuni stili linguistici vengono classificati come negativi più frequentemente degli altri.

## Il tono è un indizio, non il cliente

Non rinuncerei all’analisi del sentiment. Può far emergere una richiesta che rischiava di rimanere sepolta nella casella condivisa.

Le assegnerei però un compito limitato: attirare l’attenzione.

L’AI può dirci:

> “Questo messaggio potrebbe richiedere un controllo rapido.”

Non dovrebbe stabilire:

> “Questa persona è un cattivo cliente.”

Il primo giudizio riguarda il lavoro che dobbiamo fare.

Il secondo trasforma un’interpretazione incerta in un’etichetta destinata a condizionare tutte le conversazioni successive.

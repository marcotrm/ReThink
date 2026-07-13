# Prodotto: il "Company Gospel" (wiki aziendale generata)

*2026-07-13. Concept di prodotto emerso in conversazione. Collegato a [[business-plan]], [[brand-positioning]], [[company-brief]].*

## L'intuizione

Il target non è un settore (dentisti, ristoranti...) ma un **profilo**: PMI non digitalizzate ma ambiziose, a cui non vendiamo un dominio ma un **modo di lavorare**. Il primo prodotto concreto è la costruzione della loro **base di conoscenza aziendale** ("gospel" / wiki), oggi inesistente o solo nella testa del titolare.

Questo replica per il cliente esattamente ciò che il vault ReThink è per ReThink (vedi [[company-brief]]): un "Jarvis" che sa tutto dell'azienda. È coerente col brand: prima si pensa/si mette ordine, poi si automatizza.

## Flusso di onboarding (ipotesi)

1. **Raccolta input grezzi**: l'azienda dà tutto ciò che ha — screenshot del sito, pagine, brochure, listini, email tipo, descrizioni a voce, foto del gestionale.
2. **Generazione LLM**: il modello produce una prima bozza dei documenti canonici che l'azienda quasi mai possiede al 100%:
   - Brand voice / tono di comunicazione
   - Cosa fa l'azienda, per chi, value proposition
   - Prodotti/servizi e listino
   - Processi chiave (come si prende un ordine, come si fa un preventivo, ecc.)
   - Clienti tipo / segmenti
   - FAQ e obiezioni ricorrenti
3. **Validazione umana**: l'azienda legge, corregge, conferma. È il momento chiave: "questo documento sulla brand voice ci rappresenta davvero?" → il cliente vede valore perché si riconosce (o scopre incoerenze).
4. **Risultato**: una wiki viva, versionata, che è la **fonte di verità** dell'azienda.

## Perché è forte

- Risolve un pain point trasversale a QUALSIASI settore → un solo prodotto, tanti clienti (regola 2+ clienti → modulo, [[company-brief]]).
- La fase di validazione fa fare al cliente il lavoro di riflessione: è il "ReThink" in atto, non uno slogan.
- La wiki diventa il **carburante di tutto il resto**: una volta che esiste, alimenta il chatbot, gli agenti, le automazioni, i contenuti. È il layer che gli altri (reseller GHL) non costruiscono.

## Dove è debole (da validare, lente critica)

1. **La wiki da sola non è un risultato che si paga.** Un documento "brand voice" è percepito come nice-to-have. Il cliente paga per una CONSEGUENZA misurabile della wiki, non per la wiki. Domanda aperta: qual è la prima cosa concreta che la wiki fa risparmiare o guadagnare la settimana dopo? (es. risponde ai clienti al posto tuo, genera preventivi coerenti, sforna contenuti nel tuo tono). La wiki è il mezzo; va venduto il "e quindi".
2. **"Screenshot → LLM → documenti" è demo-facile ma valore-fragile.** Generare i documenti è banale (lo fa chiunque con ChatGPT in un'ora). Il valore difendibile è: (a) la struttura/metodo, (b) il mantenerla viva e collegata alle automazioni, (c) l'accompagnamento nella validazione. Se ci fermiamo alla generazione, siamo copiabili in un pomeriggio.
3. **Rischio "documento morto".** Le wiki aziendali muoiono sempre: nessuno le aggiorna. Il prodotto deve avere un meccanismo per cui la wiki resta viva da sola (si aggiorna dalle attività), altrimenti a 3 mesi è carta straccia e il churn arriva.
4. **La validazione richiede tempo del cliente** — proprio la risorsa che l'imprenditore non-digitalizzato e indaffarato non vuole dare. L'onboarding deve chiedergli il minimo sforzo possibile.

## Domande da portare in validazione (amico delle vernici + altri)

- Oggi, quando entra una persona nuova in azienda, come impara "come si fanno le cose qui"? (misura il dolore dell'assenza di wiki)
- Quante volte rispondi/riscrivi le stesse cose (preventivi, email, risposte a clienti)?
- Se avessi un assistente che conosce tutto della tua azienda, la PRIMA cosa che gli faresti fare quale sarebbe? → questa risposta definisce il vero prodotto d'ingresso, non la wiki in sé.

## Prossimo passo

Non costruire l'onboarding finché la domanda sopra ("la prima cosa") non ha ricevuto 3+ risposte coerenti da aziende reali. Se le risposte convergono, quello è il modulo MCP n.1 → scheda in `40-moduli-mcp/`.

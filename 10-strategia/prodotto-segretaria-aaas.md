# Prodotto: Segretaria AaaS

*Stato al 2026-07-14. Fonte: rapporto interno NiaMarketing. Repo: `marcotrm/ReThinkSegretary`.*
*Collegato a [[prodotto-company-gospel]], [[business-plan]], [[company-brief]].*

## Cos'è

Segretaria AI multi-tenant su WhatsApp (+ voce in arrivo): riceve messaggi dei clienti finali, riconosce l'attività dal numero/istanza, carica la knowledge base di quel cliente, classifica l'intento e risponde / prenota / fa escalation a un umano. Un solo workflow n8n (22 nodi) e un solo backend servono tutti i clienti.

**Connessione strategica**: gli **8 documenti della knowledge base per cliente** sono la concretizzazione del [[prodotto-company-gospel]] — la wiki è già qui, come fonte di verità da cui derivano risposte, prompt vocale e config calendario. La Segretaria è la prima applicazione verticale del gospel.

## Stato reale (14 lug 2026)

- **Costruito e funzionante end-to-end in produzione** (Railway + PostgreSQL). 42 test backend passati. 4 difetti critici trovati e risolti solo eseguendo contro servizi reali.
- Architettura multi-tenant: nuovo cliente = compilare la sua KB + una riga di config. Workflow mai duplicato.
- **Nessun cliente reale attivo. 2 clienti demo configurati.**
- Salvaguardie: escalation a umano su bassa confidenza, reclamo/urgenza, errore calendario/LLM, o >8 messaggi senza soluzione. Mai conferma appuntamento senza ok del calendario. Risposta ritardata 5-15 min per non sembrare artificiale.

## Componenti da chiudere prima di un cliente vero

| Componente | Stato |
|---|---|
| WhatsApp (Evolution API) | Da collegare — ultimo passo prima del collaudo completo |
| Classificatore (Groq/Llama 3.3) | Da passare a piano a consumo (free = ~15 msg/giorno, insufficiente) |
| Avvisi (Slack) | Manca solo il token app |
| Canale voce (Twilio + ElevenLabs) | Da attivare (numero + agente) |
| Migrazione 360dialog | Predisposta (1 parametro) — canale Meta ufficiale, evita blocco numero |

## Decisioni aperte — mia raccomandazione

1. **Destinatario escalation: noi o il titolare?** → Sono due prodotti diversi (il rapporto lo dice bene). Raccomando: **al titolare fin da subito, con noi in copia nei primi 30 giorni**. Motivo: se il presidio ricade su di noi, non è più software, è un call center travestito — non scala e ti riporta dritto nella trappola Agency ([[company-brief]] rischio n.1). Il presidio nostro va tenuto come servizio premium a pagamento, non come default.
2. **Canale notifiche al cliente**: Slack no. **Telegram o WhatsApp**. Preferire WhatsApp: il titolare ci è già dentro tutto il giorno, zero nuova app da imparare (coerente col target non-digitalizzato).
3. **Deepgram**: se ElevenLabs trascrive già, non aggiungerlo. Meno dipendenze, meno costo, meno cose che si rompono. Verificare qualità della trascrizione ElevenLabs sul dialetto/rumore reale prima di decidere.

## Lettura critica

- **Bello e concreto**, ma è esattamente il "build prima di validare" contro cui punta il [[company-brief]] (principio n.1): sistema completo in produzione, **zero clienti paganti**. Non è un errore fatale — ora esiste e i 4 bug trovati sono valore reale — ma sposta il rischio: **il collo di bottiglia non è più tecnico, è commerciale.** Un altro mese di rifinitura tecnica non vale quanto il primo cliente reale che manda messaggi veri.
- La Segretaria è però un **eccellente cavallo di Troia per il gospel**: è un risultato concreto e pagabile (risponde ai clienti, prende appuntamenti) — risolve il punto debole n.1 del [[prodotto-company-gospel]] ("la wiki da sola non si paga"). Qui la wiki si paga perché fa qualcosa di misurabile: non perdere messaggi/appuntamenti.
- **Attenzione al target**: questo prodotto risponde a chi RICEVE molti contatti (attività con clientela che scrive/chiama). È in tensione con la scoperta sui dentisti (domanda satura = non pagano per gestire i contatti). Va venduto a chi ha volume di messaggi che NON riesce a gestire e lo vive come dolore — non a chi è già saturo e felice così.

## Prossimo passo (uno solo)

Collegare WhatsApp reale (Evolution) su UN cliente demo e far girare 20 messaggi veri end-to-end. Poi trovare il primo cliente pagante — non aggiungere altre funzionalità prima.

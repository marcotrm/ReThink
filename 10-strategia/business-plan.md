# Business plan ReThink — v0.1 (ipotesi da validare)

*2026-07-12. Collegato a [[company-brief]] e [[brand-positioning]].*
*Attenzione: questo è un piano basato su ricerca desk, non su clienti reali. Ogni numero segnato "ipotesi" va verificato sul campo prima di essere trattato come vero.*

## 1. Il mercato (dati reali)

- Il **76% delle PMI italiane non ha investito né prevede di investire in AI** (Osservatorio Polimi 2025-26). Il freno principale per il 60% di chi ci ha pensato è la mancanza di competenze — non il budget. Questo è esattamente lo spazio di ReThink: tradurre ed educare, non vendere tecnologia.
- Il mercato AI italiano è cresciuto del ~50% nel 2025 (~1,8 mld €), ma quasi tutto su grandi imprese.
- ~4,3 milioni di microimprese (0-9 addetti, 95% del tessuto); sanità, ristorazione e servizi tra i settori più numerosi.
- Prezzi correnti di mercato per chatbot/receptionist AI in Italia: **setup 500-5.000 €, canone 30-250 €/mese**; per soluzioni verticali su prenotazioni (studi, ristoranti) setup tipico 1.500-3.500 €.

## 2. Target — raccomandazione

**Primo segmento (beachhead): studi dentistici e medici privati.** Motivazioni:

1. Pain point misurabile in euro: ogni chiamata persa / no-show è fatturato perso (una prima visita vale 100-500+ €); il ROI di un receptionist AI è dimostrabile in un mese.
2. Pagano già: segreteria, software gestionale, marketing — hanno budget e abitudine ai canoni mensili.
3. Processo standardizzabile: prenotazione, promemoria, richiamo no-show, recensioni — un template replicabile su N studi (perfetto per la regola dei 2+ clienti → modulo MCP).
4. Densi e raggiungibili: ordini professionali, fiere di settore, passaparola tra colleghi.

**Secondo segmento (espansione): ristorazione.** Volume enorme ma ticket più basso, alta mortalità d'impresa e minore disponibilità a pagare canoni — meglio dopo, con un'offerta già rodata.

**Da evitare come primo target: commercialisti.** Pain point reali ma cicli decisionali lenti, stagionalità pesante e integrazioni complesse (Fatture in Cloud, gestionali legacy) che ti trascinerebbero al Livello 2 prima di aver validato il Livello 1.

*Criterio di scelta comune: il cliente ideale perde soldi visibili ogni settimana per un processo di comunicazione/prenotazione rotto.*

## 3. Competitor

| Tipo | Chi | Minaccia | Come si differenzia ReThink |
|---|---|---|---|
| Reseller GHL italiani | Squadd CRM, ItaliaGHL, HighLevel Italia | **Alta** — stessa infrastruttura, già localizzati, template verticali pronti | Loro vendono la piattaforma; ReThink vende il risultato ("mai più una chiamata persa") + moduli MCP che loro non costruiscono |
| Integrazioni verticali | GoGHL.ai (WhatsApp per GHL), Talkmind (voice AI) | Media — sono fornitori, non concorrenti diretti; possibili partner | Sono componenti; ReThink è il servizio completo chiavi in mano |
| Agenzie AI generaliste | SOS AI e simili | Media — stessa promessa, poca verticalizzazione | Focus verticale (dentisti) + posizionamento "ripensiamo il problema" ([[brand-positioning]]) |
| Piattaforme dirette | Lety.ai, Octotable/Tableo (ristoranti), chatbot low-cost (19-75 €/mese) | Media-bassa sul segmento scelto — il dentista non si self-serve | Il target non vuole un tool, vuole qualcuno che se ne occupi |
| Software gestionali di settore | Gestionali dentali che aggiungono AI | **Alta nel medio periodo** — hanno già il cliente | Velocità e servizio; rischio strutturale da monitorare |

**Verità scomoda**: il quadrante "GHL localizzato per PMI italiane" è già occupato (lo dice anche il [[company-brief]], sez. 5). La differenziazione non può essere la piattaforma: deve essere il verticale + il servizio + i moduli proprietari.

## 4. Offerta e prezzi (ipotesi)

| Pacchetto | Contenuto | Prezzo ipotesi |
|---|---|---|
| **Setup "ReFrame"** | Audit del processo, configurazione receptionist AI (WhatsApp + telefono), integrazione calendario, formazione | 1.500-2.500 € una tantum |
| **Canone "ReSolve"** | Gestione, monitoraggio, report mensile, migliorie | 250-400 €/mese |
| Moduli MCP custom | Solo quando il pain point non è coperto dalla piattaforma | A preventivo; se richiesto da 2+ clienti → prodotto |

Posizionamento prezzo: sopra i chatbot low-cost (19-75 €/mese) e sotto una segretaria part-time (~800-1.000 €/mese) — il confronto da usare in vendita è il secondo, non il primo.

## 5. Struttura costi (ipotesi, fase validazione)

- Piattaforma: GHL Unlimited 297 $/mese (o Agency Pro 497 $ quando serve white-label SaaS) oppure reseller italiano — costo fisso ~300-500 €/mese.
- Costi variabili per cliente: messaggistica WhatsApp/voce ~20-60 €/mese.
- Strumenti (Claude Code, n8n, dominio, ecc.): ~100-200 €/mese.
- **Break-even operativo: ~3 clienti a canone.** Con 10 clienti: ~3.000-4.000 €/mese ricorrenti a margine lordo ~70-80%.

## 6. Roadmap 12 mesi

| Fase | Mesi | Obiettivo | Kill criteria |
|---|---|---|---|
| Validazione | 1-2 | 15 conversazioni con dentisti/medici; 3 lettere d'intenti o pre-vendite | <2 interessati a pagare → cambiare segmento, non insistere |
| Pilota | 3-5 | 3 clienti pilota paganti (anche scontati), casi studio con numeri (chiamate recuperate, no-show ridotti) | ROI non dimostrabile → rivedere offerta |
| Scala locale | 6-9 | 10 clienti a canone pieno, processo di delivery documentato ≤ 2 giorni/cliente | Churn >20% o delivery non comprimibile → problema di prodotto |
| Primo modulo | 9-12 | 1° modulo MCP nato da pain point ricorrente (2+ clienti), venduto/riusato | Nessun pattern ricorrente → restare Livello 1 più a lungo |

## 7. Rischi principali

1. **Commoditizzazione**: i reseller GHL o i gestionali di settore aggiungono lo stesso servizio. Difesa: verticale + relazione + moduli MCP proprietari.
2. **Trappola Agency** (già nel brief): il delivery mangia il tempo e non si sale mai al Livello 3. Difesa: kill criteria e tetto di 2 giorni/cliente.
3. **Dipendenza da piattaforma terza** (GHL/Lety): cambi di prezzo o policy. Difesa: la logica custom vive in MCP, portabile.
4. **Founder unico / capacità commerciale**: 15 conversazioni in 2 mesi è il vero test, prima ancora del prodotto.

## 8. Prossimi 3 passi concreti

1. Lista di 30 studi dentistici/medici raggiungibili (zona, contatti, canale d'ingresso).
2. Script di intervista di validazione (pain, processo attuale, cosa pagano oggi, cifra che pagherebbero).
3. Demo minima su GHL/Lety da mostrare in call — non costruire di più finché i punti 1-2 non danno segnale.

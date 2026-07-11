# ReThink — Company Brief
*Business model, mercato, architettura — documento aziendale*

---

## 1. Mission

ReThink aiuta PMI e professionisti italiani ad adottare l'AI in modo pratico e senza rischi, senza dover costruire infrastruttura da zero: affitta ciò che il mercato ha già risolto, e costruisce solo ciò che manca davvero — trasformando ogni pain point ricorrente in software proprietario.

## 2. Target di mercato

**PMI e professionisti italiani che non usano ancora l'AI in modo strutturato.**

Segmento specifico ancora da restringere (vedi Domande Aperte, sezione 8) — settori candidati da validare: studi professionali (commercialisti, dentisti), ristorazione, agenzie di viaggio, retail locale.

## 3. Modello di business — 3 livelli

### Livello 1 — Infrastruttura affittata (Agency + Automation)
Non si costruisce da zero. Si usa una piattaforma esistente per CRM, dashboard brandizzata, fatturazione multi-cliente, calendari, agenti AI base. Il cliente finale non vede mai il fornitore sottostante — vede solo il brand ReThink.

### Livello 2 — Collante custom (MCP)
Quando la piattaforma affittata non copre un pain point specifico del cliente, si costruisce una soluzione mirata come **server MCP** (Model Context Protocol) — non uno script monouso. Un server MCP è richiamabile da qualsiasi agente compatibile (Claude, la piattaforma affittata stessa, altri tool), quindi resta riutilizzabile per definizione.

### Livello 3 — Prodotto proprietario
**Regola operativa di produttizzazione**: se 2 o più clienti diversi richiedono la stessa soluzione custom, questa smette di essere consulenza e diventa un modulo generico, versionato, documentato — vendibile anche fuori dal servizio diretto, ad altre agenzie o aziende che usano piattaforme compatibili con MCP.

### Livello 4 (orizzonte) — Venture Studio
Quando ci sarà capitale e pattern-recognition sufficienti dai livelli precedenti, possibilità di creare iniziative interne indipendenti.

## 4. Perché questo modello (razionale strategico)

- **La tecnologia di base è ormai commodity**: piattaforme come GoHighLevel o Lety.ai risolvono già Agency + Automation in un pacchetto. Costruire un concorrente generico da zero è una battaglia in salita contro player con anni di infrastruttura.
- **Il vantaggio competitivo reale non è tecnico, è di fiducia e localizzazione**: le piattaforme dominanti sono pensate per il mercato anglofono. Un brand italiano riconosciuto, capace di tradurre ed educare, ha spazio.
- **Il lavoro clienti è R&D pagata**: ogni progetto di delivery è anche un'occasione per individuare pattern che, se ricorrenti, meritano di diventare prodotto.
- **Rischio principale da mitigare**: restare bloccati indefinitamente al livello Agency per via del carico operativo, senza mai risalire verso il prodotto proprietario.
- **Non costruire prima di validare**: l'infrastruttura (Livello 1) si giustifica solo quando un servizio è già stato validato con clienti reali disposti a pagare — non prima.

## 5. Ricerca di mercato — panorama strumenti

### Piattaforme "rented" (Agency + Automation già impacchettati)

| Piattaforma | Cosa copre | Modello | Nota rilevante |
|---|---|---|---|
| **GoHighLevel** | CRM, funnel/landing page, email/SMS/WhatsApp, calendari, pagamenti, AI Employee (chat/voice), gestione recensioni | Abbonamento (da ~97$ a ~497$/mese per il piano SaaS Pro white-label) | Interfaccia nativa in inglese; espone un server MCP ufficiale (LeadConnector) |
| **Lety.ai** | "AI employees" verticali (assistente WhatsApp, scheduler) venduti come abbonamento singolo | No-code, multi-tenant, importa flussi da n8n/Make/Zapier | 600+ integrazioni via MCP; più stretto e specifico di GHL |
| **Squadd CRM / ItaliaGHL** | Rivenditori italiani di GoHighLevel: localizzazione completa, supporto in italiano, template verticali (commercialisti, dentisti, ristoranti, agenzie viaggio), integrazioni italiane (Fatture in Cloud, WhatsApp Business via Floww) | Reseller white-label | Prova che il mercato "GHL localizzato per PMI italiane" esiste già e ha clienti |
| **Pickaxe, ConvoCore, Stammer, BotPenguin** | Varianti dello stesso modello: agenti AI brandizzati, portale cliente, fatturazione | No-code, white-label | Categoria matura e affollata a livello internazionale |

### Strumenti di sviluppo (per il Livello 2/3 — collante custom e prodotto)

| Strumento | Ruolo | Note |
|---|---|---|
| **Claude Code** | Sviluppo di server MCP e logica custom, controllo pieno del codice | Naturale per costruire i moduli del Livello 2/3 (MCP nativo Anthropic) |
| **Cursor** | IDE AI-first per sviluppo intensivo | Alternativa/complemento a Claude Code |
| **n8n** | Automazione workflow, agenti AI con RAG e tool-calling | Buon backend per prototipare automazioni prima di produttizzarle |
| **Make** | Automazione visuale, più semplice ma meno potente sugli agenti autonomi | Utile per flussi semplici, meno per agenti complessi |
| **Langflow** | Costruzione visuale di pipeline LLM/agenti, open source | Controllo fine sui flussi AI, più dev-oriented di n8n |
| **Base44** | Generazione app complete (anche mobile, pubblicabili su store) | Ottimo per prototipi/MVP cliente; muro di complessità in produzione a scala |
| **Lovable** | Generazione app full-stack con backend integrato | Buon ponte tra prototipo e prodotto reale |
| **Bolt.new** | App full-stack in browser, sviluppo rapido | Prototipazione veloce |
| **v0** | Generazione componenti frontend (ecosistema Vercel) | Utile per interfacce rapide, meno per logica backend |
| **Higgsfield** | Generazione video AI multi-modello (Sora 2, Kling 3.0, Veo 3.1, Seedance 2.0) | Livello Agency — produzione contenuti senza shooting |

### Mappa visuale del panorama

![Mappa a bolle del panorama strumenti: Agency vs Automation vs Software House](rethink-tool-landscape.png)

*Asse orizzontale: orientamento Agency (client-facing). Asse verticale: orientamento Automation Studio (workflow/agenti). Dimensione della bolla: intensità Software House (sviluppo puro). Il quadrante in alto a destra (Agency alta + Automation alta) è già occupato dalla categoria delle piattaforme white-label rented — non è uno spazio vuoto.*

## 6. Architettura tecnica proposta

```
Cliente PMI
     |
Frontend brandizzato ReThink
     |
Piattaforma affittata (GoHighLevel / Lety.ai / Squadd)
     |  <-- MCP -->
Server MCP custom ReThink (Livello 2)
     |
Moduli produttizzati e versionati (Livello 3, riusabili su più clienti/piattaforme)
```

Il livello MCP è il punto di leva: un modulo costruito una volta per risolvere un pain point è richiamabile da qualunque agente compatibile (la piattaforma affittata, Claude, altri strumenti dei clienti), senza dover riscrivere l'integrazione ogni volta.

## 7. Principi operativi

1. Non costruire infrastruttura prima di aver validato la domanda con clienti reali paganti.
2. Un fix diventa prodotto solo quando richiesto da 2+ clienti diversi — non prima.
3. Ogni livello del modello richiede competenze diverse: sequenziare, non parallelizzare tutto insieme.
4. Trattare ogni progetto cliente come R&D, non solo come delivery — è la difesa contro il rischio di restare bloccati al Livello 1.
5. Preferire la piattaforma già localizzata per l'italiano/PMI italiane (es. reseller come Squadd) rispetto a partire da GHL "nudo" in inglese, se la localizzazione è già risolta da terzi a condizioni sensate.

## 8. Domande aperte per la validazione

- Quale segmento PMI italiano specifico (troppo ampio restare su "PMI italiane" in generale)?
- Prezzo: quanto è disposta a pagare una PMI italiana per un servizio di questo tipo?
- Quale piattaforma rented conviene di più per il primo pilota: GHL/Squadd (ampio, CRM completo) o Lety.ai (stretto, singolo agente verticale)?
- Quali pain point specifici del segmento scelto NON sono coperti dai template esistenti (es. Squadd)?

---
*Documento vivo — da aggiornare ogni volta che emergono nuove decisioni o dati di validazione.*

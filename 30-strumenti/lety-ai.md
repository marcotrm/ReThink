# Lety.ai — scheda strumento

**Stato**: ricerca web fatta (2026-07-11). Manca ancora la prova hands-on.

## Cos'è
Piattaforma white-label multi-tenant per agenzie che vendono "AI employees" (agenti AI
preconfezionati) ai propri clienti. Non è un CRM completo (quello è GoHighLevel): è
l'infrastruttura per costruire, brandizzare e **fatturare** agenti AI senza codice.

## Funzionalità verificate (fonti: lety.ai, lety.ai/pricing)
- **Canali**: WhatsApp, Instagram, web chat, email, SMS
- **Agenti pre-costruiti**: 12 verticali / 46 nicchie (ristorazione, sanità, immobiliare, legale, automotive, e-commerce)
- **LLM**: OpenAI, Claude, Gemini, Llama, Mistral (a scelta)
- **Integrazioni**: 600+ via MCP; Calendly, Stripe/PayPal, HubSpot, GoHighLevel, Salesforce
- **Import flussi**: da n8n, Make, Zapier
- **Fatturazione multi-cliente**: Stripe Connect, 4 flussi in un'unica fattura (abbonamento, markup token, chiamate MCP, setup fee)
- **White-label**: dominio, logo e portale cliente col brand dell'agenzia; il cliente non vede mai Lety

## Prezzi (luglio 2026)
- Starter $97/mese — fino a 2 sub-account clienti
- Standard $297/mese — fino a 10 clienti
- Unlimited $497/mese — clienti illimitati
- Pass-through senza markup: token LLM e sessioni WhatsApp (tariffe Meta)
- Trial 7 giorni (carta richiesta), mensile disdicibile
- Benchmark dichiarato: le agenzie rivendono a $300–2.000/mese per chatbot

## Come lo usiamo (decisione)
- **Fase 1 del piano ReThink**: è il motore dell'offerta "AI employee su WhatsApp" per il primo settore.
  Piano Starter ($97) per i primi 2 clienti pilota; upgrade a Standard solo dal 3° cliente pagante.
- **Fase 2**: le sue chiamate MCP sono il punto di aggancio dei nostri server MCP custom
  (memoria cliente / integrazioni gestionali italiani).

## Da verificare hands-on (trial)
- [ ] Qualità dell'agente in ITALIANO (dialetti dei clienti, tono)
- [ ] Template verticali: quanto sono usabili per il nostro settore target
- [ ] Come si registra un MCP server custom esterno e cosa può fare
- [ ] Costi reali WhatsApp Business per conversazione in Italia
- [ ] Lock-in: esportabilità di flussi e dati
- [ ] Fatturazione: compatibilità con fatturazione elettronica italiana (probabile no → fatturiamo noi a parte)

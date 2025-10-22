# INFOTEL RTLS Demo (Live + Camera Linkage)

Demo HTML standalone che mostra:
- Core: anagrafiche e posizionamento su mappa
- ERP/CMMS: referenziazione (luogo ERP), compliance/manutenzioni, rischio
- Qualifiche/Accessi: verifica requisiti per uso dispositivi e accesso a zone
- Live Mode: movimenti lenti automatici Sala Attesa → diagnostica (con allarme se assistente non qualificato entra in Ecografia)
- Camera Linkage: all'ingresso in una zona si apre il feed TVCC associato (configurabile)

## 🎯 Scope della Demo
**Target**: Strutture sanitarie in Regione Sicilia  
**Referente**: Giorgio Aprile  
**Dati**: Tutti i dati mostrati sono sintetici e mock, creati per scopi dimostrativi. Nessun dato reale è presente nella demo.  
**Focus**: Demo standalone del sistema RTLS, senza integrazione con il motore di posizionamento reale.

## 🚀 Avvio Rapido
La demo è pubblicata automaticamente su GitHub Pages e accessibile all'URL:  
**https://maxpanella.github.io/-inforef_rtls_demo/**

### Esecuzione Locale
- Apri `index.html` in un browser moderno (viene automaticamente reindirizzato a `index_Version7.html`)
- Oppure apri direttamente `index_Version7.html`

### Pubblicazione GitHub Pages
Il deploy è automatico ad ogni push su `main`:
1. Il workflow `.github/workflows/pages.yml` si attiva automaticamente
2. Il sito viene pubblicato su `https://maxpanella.github.io/-inforef_rtls_demo/`
3. Il file `.nojekyll` disabilita Jekyll per servire i file HTML direttamente

## 🎬 Script Demo (15 minuti)

### Introduzione (2 min)
**Contesto**: "Benvenuti alla demo del sistema RTLS INFOTEL per strutture sanitarie. Oggi vi mostrerò come il sistema traccia asset medicali e personale in tempo reale, garantendo compliance normativa e sicurezza operativa."

**Target**: Strutture sanitarie in Regione Sicilia (Referente: Giorgio Aprile)

### Parte 1: Visualizzazione Base (3 min)
1. **Mappa e Asset**
   - Mostrare la mappa della struttura sanitaria con le diverse zone
   - Spiegare i diversi tipi di asset tracciati (ECG, Monitor, Defibrillatori, etc.)
   - Dimostrare le modalità di visualizzazione etichette (Nessuna/On-hover/Sempre)

2. **Dettagli Asset**
   - Cliccare su un asset per vedere i dettagli (es. ECG-001)
   - Mostrare informazioni: ubicazione, stato operativo, compliance, manutenzioni

### Parte 2: Compliance e Manutenzioni (4 min)
1. **Filtri di Compliance**
   - Applicare filtro "In scadenza" per vedere asset che necessitano manutenzione
   - Applicare filtro "Scaduta" per evidenziare asset non conformi
   - Mostrare filtro "Safety-critical" per asset critici

2. **Storico Manutenzioni**
   - Cliccare su un asset (es. Estintore o dispositivo elettromedicale)
   - Visualizzare lo storico delle manutenzioni passate
   - Mostrare date di scadenza prossime manutenzioni

### Parte 3: Sistema Qualifiche e Accessi (3 min)
1. **Personale e Qualifiche**
   - Passare alla vista "Persone"
   - Mostrare Dr. Mario Rossi (qualificato per tutte le aree)
   - Mostrare Assistente Laura Bianchi (qualificata solo per zone base)

2. **Zone Ristrette**
   - Evidenziare le zone con restrizioni di accesso (Sala Ecografia, RM, TC)
   - Spiegare il sistema di verifica delle qualifiche richieste

### Parte 4: Live Mode con Allarmi (2 min)
1. **Attivazione Live Mode**
   - Attivare il toggle "Live Mode"
   - Mostrare il movimento automatico del personale dalle sale d'attesa alle zone diagnostiche

2. **Simulazione Allarme**
   - Osservare quando l'Assistente Laura Bianchi entra in Sala Ecografia
   - **ALLARME**: "ACCESSO NON AUTORIZZATO! Assistente L. Bianchi non ha qualifica per Sala Ecografia"
   - Spiegare come il sistema previene violazioni di sicurezza e compliance

### Parte 5: Camera Linkage (1 min)
1. **Configurazione TVCC**
   - Aprire il pannello "Impostazioni"
   - Mostrare la configurazione Camera Linkage per ogni zona
   - Spiegare che all'ingresso in una zona si può aprire automaticamente il feed TVCC

2. **Demo Integrazione**
   - Cliccare su una zona (es. Sala RM o Magazzino)
   - Mostrare come si aprirebbe il feed video della camera associata
   - (Nota: demo usa video/feed di esempio, non stream reali)

### Conclusione (Opzionale - se c'è tempo)
**Riepilogo vantaggi**:
- ✅ Tracciamento real-time di asset critici
- ✅ Compliance automatica con scadenze manutenzioni
- ✅ Controllo accessi basato su qualifiche del personale
- ✅ Integrazione con sistemi TVCC per sicurezza
- ✅ Riduzione rischi operativi e miglioramento efficienza

**Q&A**: Rispondere a domande specifiche della struttura sanitaria

## 📋 Funzioni
- Etichette mappa: Nessuna / on-hover / sempre visibili
- Stati cliccabili (lista): filtri su Compliance (OK/In scadenza/Scaduta), Rischio (Safety-critical), Stato operativo (Attivo/Presente/…)
- Dettaglio manutenzioni: click sul nome (es. estintori/elettromedicali) → storico
- Live toggle: muove persone tra le stanze, genera allarme in violazione qualifiche
- Camera Linkage: configurazione feed per Sala RM/TC/Ecografia/Magazzino/Sala Attesa

## ⚙️ Configurazioni
Apri "Impostazioni":
- URL Mappa (immagine)
- Modalità etichette
- Altezza mappa
- Camera Linkage:
  - Abilitazione, Auto-open, Beep
  - Feed per zona (MP4/WEBM/OGG consigliati; altrimenti iframe su portale camera)

## 📝 Note
- Per stream HLS (`.m3u8`) serve un player dedicato (es. hls.js) o Safari.
- I dati demo sono mock per la presentazione.
- Nessun dato reale è presente nella demo.

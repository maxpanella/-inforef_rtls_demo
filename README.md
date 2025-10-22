# INFOTEL RTLS Demo (Live + Camera Linkage)

Demo HTML standalone che mostra:
- Core: anagrafiche e posizionamento su mappa
- ERP/CMMS: referenziazione (luogo ERP), compliance/manutenzioni, rischio
- Qualifiche/Accessi: verifica requisiti per uso dispositivi e accesso a zone
- Live Mode: movimenti lenti automatici Sala Attesa → diagnostica (con allarme se assistente non qualificato entra in Ecografia)
- Camera Linkage: all'ingresso in una zona si apre il feed TVCC associato (configurabile)

## Esecuzione Locale

Per eseguire la demo in locale:

1. Clonare il repository:
   ```bash
   git clone https://github.com/maxpanella/-inforef_rtls_demo.git
   cd -inforef_rtls_demo
   ```

2. Aprire `index.html` in un browser moderno (Chrome, Firefox, Safari, Edge)
   - L'index.html effettua un redirect automatico a `index_Version7.html`
   - In alternativa, aprire direttamente `index_Version7.html`

3. Non sono necessari server web o dipendenze: è un'applicazione HTML standalone

## Pubblicazione su GitHub Pages

La demo è configurata per il deploy automatico su GitHub Pages tramite GitHub Actions:

1. **Configurazione automatica**: Il workflow è già configurato in `.github/workflows/pages.yml`

2. **Abilitazione GitHub Pages**:
   - Vai su Settings → Pages nel repository GitHub
   - Source: seleziona "GitHub Actions"
   - Salva le modifiche

3. **Deploy automatico**:
   - Ad ogni push sul branch `main`, il workflow "Deploy to GitHub Pages" si attiva automaticamente
   - Puoi anche eseguire manualmente il workflow dalla tab "Actions"

4. **URL pubblico**: Una volta completato il deploy, la demo sarà disponibile all'indirizzo:
   ```
   https://maxpanella.github.io/-inforef_rtls_demo/
   ```

5. **Verifica deploy**: 
   - Vai su Actions → Deploy to GitHub Pages
   - Controlla lo stato dell'esecuzione
   - Una volta completato con successo, testa l'URL pubblico

## Funzioni
- Etichette mappa: Nessuna / on-hover / sempre visibili
- Stati cliccabili (lista): filtri su Compliance (OK/In scadenza/Scaduta), Rischio (Safety-critical), Stato operativo (Attivo/Presente/…)
- Dettaglio manutenzioni: click sul nome (es. estintori/elettromedicali) → storico
- Live toggle: muove persone tra le stanze, genera allarme in violazione qualifiche
- Camera Linkage: configurazione feed per Sala RM/TC/Ecografia/Magazzino/Sala Attesa

## Configurazioni
Apri "Impostazioni":
- URL Mappa (immagine)
- Modalità etichette
- Altezza mappa
- Camera Linkage:
  - Abilitazione, Auto-open, Beep
  - Feed per zona (MP4/WEBM/OGG consigliati; altrimenti iframe su portale camera)

## Note Importanti

### Scope della Demo
- **Demo Sicilia**: Questa è una demo configurata per mostrare le funzionalità RTLS nel contesto siciliano
- **Dati Placeholder**: Tutti i dati, video e mappe sono placeholder pubblici - non contengono dati reali o sensibili
- **Integrazione RTLS**: L'integrazione con motori di posizionamento RTLS reali è **fuori scope** per questa versione
- **Finalità**: Dimostrazione delle capacità dell'interfaccia e delle funzionalità di visualizzazione

### Referente
- **Giorgio Aprile**: Referente per il progetto demo Sicilia
- Per informazioni sul progetto, contattare i referenti indicati nella sezione "Info & Contatti" della demo

### Limitazioni Tecniche
- Per stream HLS (`.m3u8`) serve un player dedicato (es. hls.js) o Safari
- I dati demo sono mock per la presentazione
- Le funzionalità di posizionamento in tempo reale richiedono l'integrazione con hardware RTLS (non incluso in questa demo)

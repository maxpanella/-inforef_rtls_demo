# INFOTEL RTLS Demo (Live + Camera Linkage)

Demo HTML standalone che mostra:
- Core: anagrafiche e posizionamento su mappa
- ERP/CMMS: referenziazione (luogo ERP), compliance/manutenzioni, rischio
- Qualifiche/Accessi: verifica requisiti per uso dispositivi e accesso a zone
- Live Mode: movimenti lenti automatici Sala Attesa → diagnostica (con allarme se assistente non qualificato entra in Ecografia)
- Camera Linkage: all’ingresso in una zona si apre il feed TVCC associato (configurabile)

## Avvio rapido
- Apri `index.html` in un browser moderno.
- Per pubblicazione con GitHub Pages:
  1. Settings → Pages → Build and deployment → Source: “Deploy from a branch”
  2. Branch: `main` e cartella `/ (root)`
  3. Salva. L’URL sarà `https://<owner>.github.io/inforef_rtls_demo/`

## Funzioni
- Etichette mappa: Nessuna / on-hover / sempre visibili
- Stati cliccabili (lista): filtri su Compliance (OK/In scadenza/Scaduta), Rischio (Safety-critical), Stato operativo (Attivo/Presente/…)
- Dettaglio manutenzioni: click sul nome (es. estintori/elettromedicali) → storico
- Live toggle: muove persone tra le stanze, genera allarme in violazione qualifiche
- Camera Linkage: configurazione feed per Sala RM/TC/Ecografia/Magazzino/Sala Attesa

## Configurazioni
Apri “Impostazioni”:
- URL Mappa (immagine)
- Modalità etichette
- Altezza mappa
- Camera Linkage:
  - Abilitazione, Auto-open, Beep
  - Feed per zona (MP4/WEBM/OGG consigliati; altrimenti iframe su portale camera)

## Note
- Per stream HLS (`.m3u8`) serve un player dedicato (es. hls.js) o Safari.
- I dati demo sono mock per la presentazione.

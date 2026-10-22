# SuperMario Termoidraulica

Landing in italiano, completamente statica: HTML e CSS compilato con Tailwind 4. Nessun JavaScript, CDN, framework frontend, database o server applicativo. Foto, font e icone sono locali. Aprire `index.html` nel browser per vedere il sito.

## Prima della pubblicazione

1. In `index.html`, sostituire la frase sui recapiti in aggiornamento con telefono, email e zona reali. Per il telefono usare un link `tel:+39...` e per l'email `mailto:...`.
2. Inserire ragione sociale, sede e partita IVA nel footer e completare `privacy.html`. Verificare l'informativa con il titolare, inclusi conservazione dei dati, fornitori e trasferimenti internazionali.
3. Verificare che tutti i servizi descritti siano effettivamente offerti. Non sono stati inventati tempi garantiti, recensioni o certificazioni.
4. Le fotografie sono illustrative. Sostituirle con foto proprie quando disponibili, aggiornando anche il testo alternativo.

## Attivare il modulo con Formspree

Il modulo e volutamente disabilitato fino alla configurazione. Non invia a destinatari fittizi e non simula conferme.

1. Creare un account su https://formspree.io e un modulo collegato alla propria email; verificare l'indirizzo come richiesto dal servizio.
2. In `index.html`, sostituire `https://formspree.io/f/INSERISCI_ID` nell'attributo `action` con l'endpoint personale fornito da Formspree.
3. Completare prima l'informativa privacy.
4. Rimuovere `disabled` dal `fieldset` e dal pulsante di invio. Nel pulsante sostituire `cursor-not-allowed` con `cursor-pointer` e rimuovere `opacity-65`.
5. Sostituire il testo `form-status` con un'informazione pertinente, per esempio: "I campi con * sono obbligatori. Useremo i recapiti solo per rispondere alla tua richiesta."
6. Ricompilare il CSS se si modificano le classi, poi provare un invio reale dal sito pubblicato e verificare che il messaggio arrivi.

Il browser esegue la validazione HTML nativa e invia una normale richiesta POST. Formspree gestisce ricezione, controlli lato servizio e pagina di conferma. Il sito resta statico e senza JavaScript. Gli invii richiedono connessione Internet e sono soggetti ai limiti del piano Formspree scelto.

## Pubblicazione su GitHub Pages

Caricare nel repository:

- `index.html`
- `privacy.html`
- la cartella `assets/` completa
- `.nojekyll`

Nelle impostazioni del repository aprire **Pages**, scegliere **Deploy from a branch**, selezionare il proprio branch e la cartella **/(root)**. Non serve GitHub Actions. I percorsi relativi funzionano anche su `nomeutente.github.io/nome-repository/`.

Non occorre pubblicare `node_modules/`, `src/`, i file npm o questi documenti. Il CSS compilato e gia incluso: non serve eseguire npm per visualizzare o pubblicare il sito.

## Modifiche a Tailwind

Solo per lo sviluppo locale:

```sh
npm ci
npm run build
```

Le regole personalizzate sono in `src/styles.css`; il risultato statico e in `assets/styles.css`. Dopo aver modificato le classi HTML ricompilare e pubblicare anche il CSS aggiornato. Tailwind 4 richiede browser moderni (Safari 16.4+, Chrome 111+, Firefox 128+).

## Risorse

- Fotografie Pexels: ritratto di Andrea Piacquadio, foto 3932291; ritratto sorridente di Bangun Stock Production, foto 11792318; idraulica di Bulat Khamitov, foto 32588548; climatizzazione di Jose Andres Pacheco Cortes, foto 5463580. Licenza: https://www.pexels.com/license/.
- Manrope: font locale variabile, licenza SIL Open Font License in `assets/manrope-license.txt`.
- Icone Lucide: SVG statici incorporati, licenza ISC in `assets/lucide-license.txt`.

Il ritratto effettivamente usato e indicato nell'attributo `src` della foto iniziale. Le immagini non rappresentano il titolare o il team reale.
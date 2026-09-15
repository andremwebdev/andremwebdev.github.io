# Brief di progetto — VARO

*Documento di consegna, come se arrivasse da un cliente vero. Il "come si traduce in codice" è compito tuo.*

---

## 1. Identità di brand

**Nome:** VARO

**Perché questo nome:** "varo" è l'atto di mettere in mare una nave per la prima volta — il momento in cui qualcosa smette di essere un progetto sulla carta e comincia a esistere davvero. È esattamente quello che fa un sito quando va online. Il nome è breve, non dice letteralmente "web design", quindi il compito del sottotitolo/hero è chiarirlo subito — è una scelta editoriale, non un'ambiguità da correggere.

**Tagline (usala in header o hero come sottotitolo del logo):** VARO — Web Design

**Payoff / frase che riassume il posizionamento (usala nei materiali, non necessariamente in home):** *Non un sito. Un varo.*

**Tono di voce:** frasi corte, dirette, mai gonfie di aggettivi. Meno parole possibili per dire una cosa vera. Evita superlativi tipo "il migliore in Italia" (era nella vecchia meta description — da eliminare, è l'opposto del tono premium: chi è davvero sicuro di sé non ha bisogno di dirlo).

---

## 2. Palette colori

Base scura e calda, non nero puro — un solo accento, usato con parsimonia (il lusso si comunica anche togliendo colore, non aggiungendone).

| Ruolo | Nome | Hex | Uso |
|---|---|---|---|
| Sfondo scuro primario | Nero caldo | `#12100D` | Hero, sezioni "importanti", footer |
| Sfondo chiaro (sezioni alternate) | Avorio | `#FAF7F2` | Sezioni di respiro, contrasto col nero caldo |
| Testo su sfondo scuro | Avorio testo | `#F3EDE4` | Titoli e testo su `#12100D` |
| Testo su sfondo chiaro | Nero testo | `#1C1A17` | Titoli e testo su `#FAF7F2` |
| Accento (unico) | Bronzo | `#B8935B` | Link, hover, bordi, dettagli, MAI come colore di sfondo di sezioni intere |
| Testo secondario / muted | Grigio caldo | `#A39C90` | Sottotitoli, didascalie, testo meno importante |

**Regola guida:** alterna sezioni scure e chiare come ritmo visivo della pagina (esattamente come avevi già fatto nel sito precedente con `#080D21` e l'avorio — qui riprendi lo stesso schema di alternanza, ma con questa palette nuova). Il bronzo compare solo per attirare l'occhio su un elemento preciso (un link, un bordo, un'icona) — se lo usi troppo perde forza.

---

## 3. Tipografia

**Titoli (H1, H2, H3):** Fraunces — serif con carattere, non è un serif "classico" da libro, ha personalità editoriale. Gratuito su Google Fonts. Usa i pesi più alti (600-700) per i titoli principali.

**Testo (paragrafi, nav, bottoni, tutto il resto):** Inter — sans-serif pulitissimo, altissima leggibilità, tantissimi pesi disponibili. Gratuito su Google Fonts.

**Gerarchia dimensioni (concettuale — usa `clamp()` come discusso, non px fissi):**
- H1: molto grande, deve dominare la hero
- H2: circa 2/3 della dimensione di H1
- H3: leggermente sopra il testo normale
- Body: dimensione leggibile standard, mai sotto una soglia comoda da leggere
- Small/caption: chiaramente più piccolo, usato per eyebrow label ed etichette

**Eyebrow label:** su ogni pagina, sopra il titolo principale, una piccola scritta maiuscola, spaziata (`letter-spacing`), in bronzo o grigio caldo — es. "SERVIZI", "PORTFOLIO" — serve a dare respiro tipografico e a orientare chi legge.

---

## 4. Struttura del sito

**Pagine:** Home · Servizi · Portfolio · Contatti

**Nav (stessa label ovunque, minuscolo, coerente col tuo sito precedente):** home · servizi · portfolio · contatti

**Header:** logo "VARO" a sinistra (solo testo, font Fraunces, nessuna icona — un wordmark pulito è più coerente col posizionamento premium di un logo-icona), nav a destra. Nessun bottone CTA extra nell'header: mantienilo minimale.

**Footer (uguale su tutte le pagine):**
- Colonna 1: "VARO" + una riga di descrizione: *Siti su misura per attività che vogliono distinguersi.*
- Colonna 2: nav ripetuta (home · servizi · portfolio · contatti)
- Colonna 3: contatti diretti (telefono, email)
- Riga finale: © 2026 VARO · P.IVA (placeholder) · Privacy Policy · Cookie Policy

**Nota responsive per la nav:** dato che il JS arriverà dopo, NON progettare un menu hamburger per mobile (richiederebbe JS per aprirsi/chiudersi). Su schermi stretti, fai semplicemente impilare i link della nav verticalmente sotto al logo — meno elegante di un hamburger ma completamente realizzabile in puro CSS, e coerente con dove sei ora nel percorso.

---

## 5. Pagina per pagina

### HOME

**Sezione 1 — Hero (sfondo scuro)**
- Eyebrow: `WEB DESIGN PER ATTIVITÀ CHE VOGLIONO DISTINGUERSI`
- H1: `Il tuo sito prende il largo.`
- Sottotitolo: `VARO progetta siti su misura per attività locali che non vogliono un sito come tutti gli altri.`
- Bottone primario: `Richiedi una consulenza` (va a Contatti)
- Link secondario, più discreto: `Guarda i progetti` (va a Portfolio)

**Sezione 2 — Perché VARO (sfondo chiaro, 3 colonne/card)**
- Titolo sezione: `Perché VARO`
- Pilastro 1 — titolo: `Su misura, non a pacchetto` — testo: `Ogni sito nasce dal tuo business, non da un modello riciclato.`
- Pilastro 2 — titolo: `Concreto, senza fronzoli` — testo: `Tempi chiari, aggiornamenti costanti, zero sorprese.`
- Pilastro 3 — titolo: `Pensato per durare` — testo: `Struttura solida, facile da aggiornare, pronta a crescere con te.`

**Sezione 3 — Cosa faccio (sfondo scuro, teaser dei servizi, 3 card)**
- Titolo sezione: `Cosa faccio`
- Card 1 — `Sito Vetrina` — `Il tuo biglietto da visita online, attivo 24/7.`
- Card 2 — `Sistema Prenotazioni` — `Appuntamenti gestiti in automatico, sempre a portata di mano.`
- Card 3 — `Manutenzione` — `Il tuo sito resta sempre al passo, senza pensieri.`
- Link sotto le card: `Scopri tutti i servizi` (va a Servizi)

**Sezione 4 — Portfolio teaser (sfondo chiaro, 2 card in anteprima)**
- Titolo sezione: `Alcuni progetti`
- Mostra solo 2 dei 3 progetti concept della pagina Portfolio (vedi sotto), con nome + una riga
- Link: `Vedi tutti i progetti` (va a Portfolio)

**Sezione 5 — CTA finale (sfondo scuro)**
- H2: `Pronto a varare il tuo sito?`
- Bottone: `Parliamone`

---

### SERVIZI

**Header pagina**
- Eyebrow: `SERVIZI`
- H1: `Cosa posso costruire per te`

**Blocco 1 — Sito Vetrina**
- Descrizione: `Il punto di partenza per chi vuole essere trovato online e trasmettere professionalità dal primo secondo.`
- Cosa include: `Design su misura` · `Fino a 5 pagine` · `Ottimizzazione base per i motori di ricerca` · `Un round di revisioni incluso`
- Ideale per: `Chi non ha ancora un sito, o ne ha uno vecchio che non rappresenta più l'attività.`

**Blocco 2 — Sistema Prenotazioni**
- Descrizione: `Un sito che lavora anche mentre tu sei impegnato con i clienti.`
- Cosa include: `Calendario prenotazioni integrato` · `Notifiche automatiche` · `Gestione disponibilità in tempo reale`
- Ideale per: `Attività che vivono di appuntamenti — parrucchieri, studi professionali, ristoranti.`

**Blocco 3 — Manutenzione & Aggiornamenti**
- Descrizione: `Un sito online non è mai davvero "finito" — va curato, come tutto il resto.`
- Cosa include: `Aggiornamenti periodici` · `Monitoraggio del sito` · `Piccole modifiche incluse`
- Ideale per: `Chi ha già un sito e vuole che resti sempre al passo, senza doverci pensare.`

**Sezione — Come lavoro (4 step, orizzontali su desktop, verticali su mobile)**
1. `Ascolto` — `Capisco la tua attività prima ancora di pensare al design.`
2. `Progetto` — `Struttura e contenuti presi forma, prima ancora di scrivere una riga di codice.`
3. `Costruzione` — `Il sito prende vita, pezzo dopo pezzo.`
4. `Varo` — `Online, testato, pronto a lavorare per te.`

**CTA finale:** `Non sai quale servizio fa per te?` + bottone `Scrivimi, ne parliamo`

---

### PORTFOLIO

Questa è la pagina più delicata perché non hai ancora clienti reali — la soluzione non è nasconderlo, è dichiararlo con sicurezza. Chi ha le idee chiare non si scusa per essere all'inizio, spiega semplicemente il proprio metodo.

**Header pagina**
- Eyebrow: `PORTFOLIO`
- H1: `Progetti concept`
- Paragrafo introduttivo (importante, va messo bene in vista, non in piccolo): `Questi progetti nascono da brief immaginati, non da clienti reali — ma sono stati costruiti con la stessa cura che metterei nel tuo: come se dovessero andare online oggi stesso.`

**Progetto 1 — Forno Antico**
- Settore: `Panificio artigianale`
- La sfida: `Un forno di quartiere, aperto da tre generazioni, che non aveva alcuna presenza online.`
- La soluzione: `Un sito vetrina che racconta la storia della famiglia e mette in primo piano gli orari e gli indirizzi dei due punti vendita.`
- Servizi usati: `Sito Vetrina`

**Progetto 2 — Studio Corsi**
- Settore: `Studio di commercialisti`
- La sfida: `Trasmettere competenza e affidabilità a clienti che cercano un professionista serio, non il primo risultato su Google.`
- La soluzione: `Un sito essenziale, con una sezione FAQ che risponde alle domande più comuni prima ancora del primo contatto.`
- Servizi usati: `Sito Vetrina`

**Progetto 3 — Nodo Barbershop**
- Settore: `Barbiere`
- La sfida: `Un locale con un'identità visiva già forte, che aveva bisogno di prenotazioni online per ridurre le chiamate a vuoto.`
- La soluzione: `Sito con calendario prenotazioni integrato, pensato per essere usato al volo da telefono, in piedi, tra un cliente e l'altro.`
- Servizi usati: `Sito Vetrina + Sistema Prenotazioni`

**CTA finale:** `Il prossimo progetto qui potrebbe essere il tuo.` + bottone `Contattami`

*Nota sulle immagini: per questi 3 progetti concept, usa foto stock (es. Unsplash, gratuite) coerenti col settore — non serve che siano "vere", ma devono essere di buona qualità e coerenti stilisticamente tra loro (stessa tonalità di colore/luce, per dare l'idea di un portfolio curato e non improvvisato).*

---

### CONTATTI

**Header pagina**
- Eyebrow: `CONTATTI`
- H1: `Parliamone`
- Sottotitolo: `Raccontami la tua attività e cosa vorresti che il tuo sito facesse per te. Rispondo entro 24 ore.`

**Form (solo struttura/design — la logica di invio arriva con JS più avanti):**
- Campo: `Nome`
- Campo: `Email`
- Campo a tendina: `Che tipo di progetto ti interessa?` — opzioni: `Sito Vetrina` · `Sistema Prenotazioni` · `Manutenzione` · `Non so ancora`
- Campo: `Messaggio` (testo lungo)
- Bottone: `Invia richiesta`

**Contatti diretti (accanto o sotto al form):**
- `Telefono` + numero
- `Email` + indirizzo

**Sezione FAQ (3 domande, utile anche per SEO in futuro):**
- `Quanto costa un sito?` → `Dipende dal progetto — dopo una prima chiacchierata ti mando un preventivo su misura, senza sorprese.`
- `Quanto tempo serve?` → `Per un sito vetrina, in genere 2-3 settimane dal brief al varo.`
- `Lavori anche a distanza?` → `Sì, l'intero processo funziona benissimo anche online.`

---

## 6. Checklist prima del "varo" (quando il sito è pronto)

- Favicon presente e coerente col wordmark
- Meta description diversa e specifica per ogni pagina (niente superlativi assoluti)
- Alt text su ogni immagine, descrittivo
- Testato su almeno 2-3 dispositivi reali diversi (non solo resize del browser)
- Nessun link rotto, nessun `mailto:`/`tel:` con errori di battitura
- Contrasto testo/sfondo verificato (soprattutto testo grigio caldo su avorio — controlla che resti leggibile)
- Immagini ottimizzate in peso, non caricate a piena risoluzione se non serve

---

*Un'ultima cosa fuori dal brief: hai chiesto un progetto "ben dettagliato" perché avevi voglia di fare, non di progettare — questo documento ora è la parte "progettare" già fatta. Da qui in poi, ogni volta che apri il file, il compito è solo tradurre quello che c'è scritto in HTML e CSS, sezione per sezione. Buon lavoro.*


PROVA CHE FUNZIONI PROTONDRIVE
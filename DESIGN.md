# Vintagism Archive — Design system · direzione "Index"

Tema Shopify basato su Horizon 4.5.0, collegato al negozio `vintagism-archive-7z4gubsj` tramite integrazione GitHub (repo `elrow7x/Vintagism-theme`, branch `main`).
Progetto: linea retail "al pezzo" di Vintagism S.R.L. (wholesale vintage al kg dal 1995, nato al mercato di Resina).
Cliente target: top spender, compratore esperto. Riferimento: Helmut Lang fine anni '90 / primi 2000, archivio concettuale.

## Ancore
- **Colore**: bianco puro + nero. Oro del logo `#B48D54` solo come segnale (squadrette all'hover, una riga del manifesto).
- **Motivo**: le squadrette d'angolo del logo, filetto 1px, su immagini e logotipo. Righe con filetto come link.
- **Tono**: silenzioso, preciso, da catalogo. Numeri di inventario e conteggi a 3 cifre (`010`, `046`).

## Token (snippets/va-head.liquid)
| Token | Valore | Uso |
|---|---|---|
| `--va-k` | `#000` | testo, filetti, tag Rare |
| `--va-w` | `#fff` | sfondo |
| `--va-grey` | `#6f6f6f` | testo secondario (contrasto ≥ 4.5) |
| `--va-line` | `#e6e6e6` | filetti secondari |
| `--va-soft` | `#f2f2f2` | sfondo immagini in caricamento |
| `--va-oro` | `#b48d54` | solo accento, mai testo piccolo |

## Tipografia
- **Archivo** 400/500/600 per testo, navigazione, card e tabelle.
- **Inter** 500/600 per i titoli (h1–h3, apertura, manifesto, titolo prodotto): richiamo diretto al sito principale vintagism.eu, che usa Inter. Self-hosted.
- Servizio (nav, card, tabelle): 11px, maiuscolo, tracking 0.06em.
- Titoli: 500, maiuscolo, interlinea ~1, al massimo uno per schermata.
- Testo corrente: 13px, interlinea 1.6.

## Layout
- Desktop: indice fisso a sinistra (220px) con logo e categorie numerate (`sections/va-index-nav.liquid`, static section in layout). L'header Horizon resta per cerca/account/borsa (logo e menu nascosti via CSS ≥990px).
- Mobile: l'indice diventa una riga scorrevole sotto l'header.
- Griglia 4 colonne desktop, 3 tablet, 2 mobile. Foto 4:5.
- Scheda capo = tabella (`blocks/va-archive-card.liquid`).

## Dati del capo
Letti da metafield `custom.<chiave>` o, in mancanza, da tag `chiave:valore`:
`decennio`, `taglia`, `misure`, `condizione`, `difetti`, `materiale`, `inv`. Tag di servizio: `donna`, `uomo`, `rare`, `new`, `sotto50`.
Link di navigazione su pagine native Shopify: `/collections/types?q=<Tipo>`, `/collections/all/<tag>`, `/collections/all?view=brands`.

## Da evitare
Più di due caratteri, serif corsivi, grotesk espansi, nero+oro "luxury", bento grid, glassmorphism, animazioni decorative.

## Registro feedback
- 25.11.2026 · Prima direzione (grotesk espanso + serif corsivo Instrument, sfondo intonaco, grana) **scartata**: "alternanza di font non funziona", serve più carattere e minimalismo per un top spender.
- 25.11.2026 · Proposte A Index / B Inventario (mono) / C Negativo (nero, condensato). **Scelta A · Index**. Aggiunto manifesto nero (da C) come unica sezione d'impatto, rimovibile dall'editor.
- 25.11.2026 · Manifesto su fascia nera con testo gigante **scartato**: "troppo rumore nella gerarchia visiva". Ora righe numerate su bianco, testo medio, squadretta oro solo sull'ultima regola. Regola generale: nessun blocco a fondo pieno, l'impatto viene dalle parole, non dal contrasto.
- 25.11.2026 · Titoli passati a **Inter** su richiesta: parallelismo con vintagism.eu (Inter nel sito; i titoli grandi lì sono in Barlow Condensed).

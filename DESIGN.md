# Vintagism Archive — Design system

Tema Shopify basato su Horizon 4.5.0. Collegato al negozio `vintagism-archive-7z4gubsj` tramite integrazione GitHub (branch `main`).
Progetto: linea retail "al pezzo" di Vintagism S.R.L. (wholesale vintage al kg dal 1995, nato al mercato di Resina).

## Ancore
- **Colore**: oro del logo `#B48D54` + il cemento/intonaco grigio dei set fotografici reali.
- **Motivo**: le due squadrette d'angolo del logo → cornici/crop-mark su immagini, intestazioni, focus. "Scheda d'archivio" con numero di inventario per ogni capo.
- **Tono**: esperto, essenziale, verace.

## Palette (ruoli)
| Nome | Hex | Ruolo |
|---|---|---|
| Intonaco | `#F3F1ED` | sfondo carta |
| Cemento | `#D9D6D0` | superfici, bordi, sfondo card |
| Nero balla | `#171614` | testo, bottoni primari, badge SOLD |
| Oro Vintagism | `#B48D54` | accento grande: squadrette, linee, numeri display (mai testo piccolo: contrasto < 4.5) |
| Ottone | `#7A5A2B` | link e testo accento piccolo (contrasto ≥ 4.5 su Intonaco) |

## Tipografia
- Titoli: grotesk largo, maiuscolo, tracking ampio come nel logo (Archivo Expanded / larghezza variabile). Interlinea 0,9.
- Accento: serif corsivo leggero dentro i titoli, con parsimonia.
- Dati (misure, taglia, N° inventario, prezzo): monospace.
- Testo: 1,6 di interlinea, scala fluida con `clamp()`.

## Componenti
- Card prodotto 4:5 (formato delle foto), squadrette oro che si chiudono sull'immagine all'hover, badge SOLD / RARE / NEW.
- Titolo standard: `Decennio · Brand · Materiale/colore · Capo` + taglia.
- Scheda capo = "scheda d'archivio": Brand, Decennio, Taglia etichetta, Misure cm, Condizione (A/B/C), Difetti, N° inventario.
- Navigazione: per tipo di capo (Donna/Uomo → Capispalla, Top, Bottom, Maglieria, Scarpe, Borse, Accessori) + Brand A–Z + collezioni curate (Rare, Sotto 50€, Nuovi arrivi).

## Da evitare
Nero+oro "luxury" su fondo scuro, Playfair/Inter, bento grid, glassmorphism, titoli centrati con sottotitolo grigio.

## Movimento e texture
- Ingressi allo scroll con `animation-timeline: view()`, squadrette all'hover; tutto off con `prefers-reduced-motion`.
- Grana leggera da cemento sullo sfondo.

## Registro feedback
- (vuoto)

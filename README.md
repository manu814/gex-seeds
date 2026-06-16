# gex-seeds

Dati EOD dei livelli GEX del Nasdaq (NDX) per **TradingView Pine Seeds**.

Quattro serie giornaliere, scritte automaticamente dal server da
`gex-live/scripts/seed_publish.py` (dopo l'aggiornamento OI delle 06:30 ET),
filtrate da un sanity gate (niente valori-robaccia):

- `NDX_CALLWALL` — call wall
- `NDX_PUTWALL` — put wall
- `NDX_FLIPHI` / `NDX_FLIPLO` — estremi della zona gamma flip

L'indicatore Pine `GEX Auto` li legge con `request.seed()` e disegna le righe sul
grafico, su qualsiasi dispositivo. Formato: `data/<SYMBOL>.csv`, righe
`YYYYMMDDT,open,high,low,close` con open=high=low=close=valore.

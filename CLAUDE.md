# Sakal cost & profit calculator – notes for Claude Code

Single-page calculator for **Sakal Snacks** plantain chips (owner: Prince). Live: https://princesalasi.github.io/sakal_cost_profit_calc/
Sister project: the shared stock app in `princesalasi/sakal_stocks` (read its CLAUDE.md for the owner's preferences and design rules).

- No build step: `index.html` = whole app (vanilla JS, SVG charts). `sw.js` + `manifest.webmanifest` make it work offline – **bump `VERSION` in `sw.js` on every change**.
- Tabs: Calculator, History, Trends. Batches are saved **only in the phone's localStorage** (no server). CSV export/import (also reads the old wide CSV format of the first version).
- Inputs: plantain cost, oil containers × price, gas cylinders × price, packaging per pack, box price, transport, boxes produced, packs per box (48), selling price per box (200 GHS). Default batch number = YY + ISO week (e.g. 2644); same-week duplicates get -2, -3.
- Owner decided: no extra costs (labour, rent …) for now; no sales split (wholesale/retail removed).
- Possible next step discussed: move its data onto the stock app's Supabase project (separate schema) so batches are shared and backed up.

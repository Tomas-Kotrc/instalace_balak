# Rozvaděče — Chata Balák

Elektroinstalace chaty, TN-C-S, výrobce komponent: **Eaton**.

## Topologie

HDS (3×25A) --AYKY-J 4×6mm²--> HR (hlavní rozvaděč, jistič 3×20A/C)
  ├── CYKY-J 5×4mm² --> RS (rozvaděč sklep, 2×12 modulů, na povrchu, v trubkách)
  └── CYKY-J 5×4mm² --> RP (rozvaděč patro, 3×12 modulů)

## RS — rozvaděč sklep (7 okruhů F1–F7)

SPD (T2) → hlavní jistič 3×20A/B → hlavní chránič 4P/25A/30mA → okruhy F1–F7
(studna, bojler, zásuvky 1+2, světla 1+2, světla venkovní, zásuvka venkovní, kotel 9kW 3F + stykač HDO)

## RP — rozvaděč patro (14 okruhů F1–F14)

SPD (T2) → hlavní jistič 3×20A/B → hlavní chránič 4P/25A/30mA (kryje i sporák 3F přímo)
  ├── skupinový chránič L1 (2P) → 5 okruhů
  ├── skupinový chránič L2 (2P) → 4 okruhy
  └── skupinový chránič L3 (2P) → 4 okruhy

Okruhy: zásuvky venkovní/1/2/kuchyň, koupelna světlo+zásuvka, světla 1+2, sporák 3F 16A,
lednice, myčka, mikrovlnka, půda světlo+zásuvka (zvlášť).

## Obsah repozitáře

- `rozvaděče_balak.xlsx` — kompletní specifikace (listy: Přehled se schématem, Rozvaděč sklep, Rozvaděč patro),
  katalogová čísla Eaton, kabeláž, modulová bilance.

## Poznámky

- Katalogová čísla u světelných jističů (PL7-B10/1N) nejsou ověřená konkrétním kódem u distributora — potvrdit před objednávkou.
- 2pólové skupinové chrániče na patře vidí jen jednu fázi — okruhy v dané skupině musí být zapojeny na stejnou fázi jako chránič.

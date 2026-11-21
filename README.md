# Rozvaděče — Chata Balák

Elektroinstalace chaty, TN-C-S. Skříně **NOARK**, přístroje **Eaton**. Dokumentace skutečného zapojení.

## Topologie

```
HDS (jistič 3×25A)
 └─ CYKY 5C×6mm² ─> venkovní přepojovací rozvaděč Schrack (odpínač 40A)
     └─ CYKY 5C×10mm² zapojen 4vodičově (L1–L3 + PEN) ─> HR (patro)
         SPD T1+T2 (TN-C) → rozdělení PEN → jistič 3×B25 → chránič 4P/40A/30mA
         └─ F1 3×B20, CYKY 5×6mm² ─> RS (sklep)
             jistič 3×C20 → chránič 4P/25A/30mA (bez SPD)
```

## HR — hlavní rozvaděč, patro (NOARK 3×12, 35/36 mod.)

| Řada | Osazení |
|---|---|
| 1 | SPD SPBT12-280/3 · jistič 3×B25 · chránič 4P 40A/30mA · RCBO B16 Půda (L1) |
| 2 | Sklep 3×B20 · Sporák 3×B20 · B16: Z-Trouba (L1), Z-Linka (L2), Z-Lednice (L3), Z-Myčka (L1), Z-Myčka2 (L2), Z-Rozvaděč (L3) |
| 3 | Zas230V Z-SD230-BS (z F8) · RCBO B16 Z-Venkovní (L1) · B10 SV-Venkovní (za RCBO Z-Venkovní) · RCBO B16 Zásuvky (L2) · RCBO B10 SV-Chodba + kuchyň (L3) · RCBO B10 SV-Pokoje + koupelna (L3) |

Propoje řad: 1→2 CY 6mm², 2→3 CYA 4mm².

## RS — rozvaděč sklep (NOARK 2×12, 24/24 mod.)

| Řada | Osazení |
|---|---|
| 1 | jistič 3×C20 · chránič 4P 25A/30mA · B2 Zdroj termostat (L1) · RCBO B16 Z-Venkovní + vývod (L2) · RCBO B10 Rezerva (L3) |
| 2 | Kotel 3×B16 (stykač HDO v kotli) · Z-380V 3×B16 · B16: Boiler (L1), Vodárna (L2), Z-230V (L3) · RCBO B10 SV-Dílna (L1) · Mean Well HDR-15-5 (z B2) |

Propoj řad: CYA 6mm².

## Obsah repozitáře

- `rozvaděče_balak.xlsx` — specifikace: Přehled (schéma), Rozvaděč HR (patro), Rozvaděč sklep, Popisky
- `rozvaděče_balak.pdf` — tiskový výstup (A4 na šířku); popisky ve skutečné velikosti 17,5 mm/modul, tisknout na 100 %

## Poznámky

- Katalogová čísla označená `ověřit*` (PL7-Bxx/1, PFL7-10/1N/B/003-A) potvrdit u distributora.
- Mezi F1 v HR (3×B20) a hlavním jističem sklepa (3×C20) není selektivita.
- L1 v HR: trouba + myčka na stejné fázi — vědomě akceptováno.

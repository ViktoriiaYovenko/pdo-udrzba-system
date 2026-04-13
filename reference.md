
# Reference dokumentace

## Datový model

### Zařízení
- ID
- název
- typ
- stav

### Porucha
- ID
- zařízení
- datum
- popis
- závažnost

### Oprava
- ID
- porucha
- příčina
- zásah
- délka opravy

## Pravidla vyhodnocování

- Pokud se porucha opakuje více než 2× za měsíc → doporučení kontroly
- Pokud opravy trvají dlouho → zařízení je rizikové
- Pokud je zařízení často poruchové → doporučení údržby

## Prioritizace

Systém určuje prioritu podle:
- četnosti poruch
- délky oprav
- závažnosti

Výsledek:
- nízká priorita
- střední priorita
- vysoká priorita

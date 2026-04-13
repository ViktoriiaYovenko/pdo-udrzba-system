# Concept dokumentace

## Přehled systému
Systém slouží k evidenci poruch zařízení, sledování historie oprav a podpoře rozhodování.

> [!NOTE]
> Systém je navržen jako podpůrný nástroj. Konečné rozhodnutí je vždy na uživateli.

---

## Hlavní části systému

| Modul              | Popis |
|--------------------|------|
| Evidence zařízení  | Seznam všech zařízení |
| Evidence poruch    | Záznam poruch |
| Evidence oprav     | Historie oprav |
| Analytický modul   | Vyhodnocení dat |

---

## Architektura systému

| Vrstva             | Funkce |
|--------------------|-------|
| Uživatelská        | Rozhraní pro uživatele |
| Aplikační          | Logika systému |
| Datová             | Ukládání dat |

> [!IMPORTANT]
> Kvalita výstupů systému závisí na správnosti a úplnosti zadaných dat.

---

## Analytika

Systém sleduje:

- četnost poruch  
- dobu oprav  
- opakování problémů  

Výstup: doporučení preventivní údržby

> [!NOTE]
> Analytický modul využívá historická data a jednoduchá pravidla, nikoliv pokročilé algoritmy.

---

## Přínosy systému

- lepší přehled o poruchách  
- podpora prevence  
- efektivnější provoz  

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

## ⚙️ Princip fungování systému

Systém funguje na základě zadávání a zpracování dat o poruchách.

1. Uživatel zadá poruchu zařízení
2. Systém uloží data do databáze
3. Po opravě jsou doplněny informace o zásahu
4. Analytický modul vyhodnocuje historická data
5. Na základě pravidel systém generuje doporučení

> [!NOTE]
> Systém neprovádí automatická rozhodnutí, pouze doporučuje další kroky.
>
> ---

## Slovník pojmů

| Termín | Význam |
|--------|--------|
| **Preventivní údržba** | Předem plánované servisní úkony zaměřené na předcházení poruchám zařízení. |
| **Závažnost poruchy** | Kategorizace dopadu poruchy na provoz (např. nízká, střední, vysoká). |
| **Analytický modul** | Součást systému, která na základě historických dat (četnost, délka oprav) generuje doporučení. |
| **Stav zařízení** | Aktuální provozní status stroje (např. v provozu, v opravě, vyřazeno). |
| **Příčina poruchy** | Specifikace důvodu vzniku problému (např. opotřebení, lidská chyba, technická závada). |

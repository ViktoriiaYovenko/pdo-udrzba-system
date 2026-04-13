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

## Grafický přehled procesu (Workflow)

> [!NOTE]
> Systém neprovádí automatická rozhodnutí, pouze doporučuje další kroky.

## 📊 Grafický přehled procesu (Workflow)

```mermaid
graph TD
    A[Vznik poruchy na zařízení] --> B[Založení záznamu v systému]
    B --> C[Oprava a doplnění údajů]
    C --> D[Uzavření opravy]
    D --> E[Analýza dat a doporučení]
    
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style E fill:#00ff00,stroke:#333,stroke-width:2px

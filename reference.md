# Reference dokumentace

---

## Datový model

### Zařízení

| Atribut | Popis |
|--------|------|
| ID     | Identifikátor |
| Název  | Název zařízení |
| Typ    | Typ zařízení |
| Stav   | Aktuální stav |

---

### Porucha

| Atribut | Popis |
|--------|------|
| ID     | Identifikátor |
| Zařízení | Vazba na zařízení |
| Datum  | Datum vzniku |
| Popis  | Popis problému |
| Závažnost | Úroveň problému |

---

### Oprava

| Atribut | Popis |
|--------|------|
| ID     | Identifikátor |
| Porucha | Vazba |
| Příčina | Důvod poruchy |
| Zásah  | Oprava |
| Délka  | Čas opravy |

> [!IMPORTANT]
> Každá oprava musí být přiřazena ke konkrétní poruše.

---

## Pravidla vyhodnocování

| Podmínka | Akce |
|---------|-----|
| Porucha > 2× za měsíc | Doporučení kontroly |
| Dlouhá oprava | Rizikové zařízení |
| Časté poruchy | Doporučení údržby |

> [!NOTE]
> Pravidla slouží jako orientační doporučení pro uživatele.

---

## Prioritizace

Systém hodnotí:

- četnost poruch  
- délku oprav  
- závažnost  

### Výstup:

| Skóre | Priorita |
|------|---------|
| Nízké | Nízká |
| Střední | Střední |
| Vysoké | Vysoká |

> [!IMPORTANT]
> Zařízení s vysokou prioritou by měla být řešena přednostně.

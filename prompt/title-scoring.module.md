---
description: "Bewertet generierte Titel anhand definierter Scoring-Kriterien"
placement: "append"
status: optional
version: 0.1.0
---

## Details

Dieses Modul erweitert den Haupt-Prompt um ein systematisches Bewertungssystem für generierte Titel. Es definiert klare Kriterien und eine Punkteskala, um die Qualität und Wirksamkeit von Titeln objektiv zu bewerten.

**Bewertungskriterien:**
- Emotionale Wirkung (1-10 Punkte)
- Klarheit und Verständlichkeit (1-10 Punkte)  
- SEO-Potenzial (1-10 Punkte)
- Originalität (1-10 Punkte)
- Zielgruppen-Relevanz (1-10 Punkte)

**Einsatz:** Füge dieses Modul hinzu, wenn eine detaillierte Bewertung der Titel erwünscht ist.

## Modul-Inhalt (lesbare Version)

### Titel-Scoring-System

Bewerte jeden generierten Titel nach folgenden Kriterien auf einer Skala von 1-10:

#### 1. Emotionale Wirkung (1-10)
- Löst der Titel Emotionen aus?
- Macht er neugierig oder weckt Interesse?
- Enthält er emotionale Trigger-Wörter?

#### 2. Klarheit und Verständlichkeit (1-10)  
- Ist sofort erkennbar, worum es geht?
- Ist die Sprache klar und eindeutig?
- Gibt es Missverständnisse?

#### 3. SEO-Potenzial (1-10)
- Enthält relevante Keywords?
- Ist die Länge suchmaschinenfreundlich?
- Würde der Titel in Suchergebnissen auffallen?

#### 4. Originalität (1-10)
- Hebt sich der Titel von der Konkurrenz ab?
- Ist er einzigartig und kreativ?
- Vermeidet er Klischees?

#### 5. Zielgruppen-Relevanz (1-10)
- Spricht er die definierte Zielgruppe an?
- Verwendet er passende Sprache/Tonalität?
- Adressiert er relevante Bedürfnisse?

### Gesamtbewertung
- **Gesamtpunktzahl**: Summe aller Kategorien (max. 50 Punkte)
- **Prozentuale Bewertung**: (Gesamtpunkte / 50) × 100%
- **Empfehlung**: ab 70% = gut, ab 80% = sehr gut, ab 90% = exzellent

## Modul-Inhalt (Copy/Paste Codeblock)

```text
TITEL-SCORING-SYSTEM:

Bewerte jeden Titel nach folgenden 5 Kriterien (jeweils 1-10 Punkte):

1. EMOTIONALE WIRKUNG (1-10)
   - Löst Emotionen aus / macht neugierig?
   - Enthält emotionale Trigger-Wörter?
   - Motiviert zum Klicken?

2. KLARHEIT & VERSTÄNDLICHKEIT (1-10)
   - Sofort erkennbar, worum es geht?
   - Klare, eindeutige Sprache?
   - Keine Missverständnisse?

3. SEO-POTENZIAL (1-10)
   - Enthält relevante Keywords?
   - Suchmaschinenfreundliche Länge?
   - Würde in Suchergebnissen auffallen?

4. ORIGINALITÄT (1-10)
   - Hebt sich von Konkurrenz ab?
   - Einzigartig und kreativ?
   - Vermeidet Klischees?

5. ZIELGRUPPEN-RELEVANZ (1-10)
   - Spricht definierte Zielgruppe an?
   - Passende Sprache/Tonalität?
   - Adressiert relevante Bedürfnisse?

BEWERTUNGS-FORMAT pro Titel:
- **Emotionale Wirkung**: X/10 (Begründung)
- **Klarheit**: X/10 (Begründung)  
- **SEO-Potenzial**: X/10 (Begründung)
- **Originalität**: X/10 (Begründung)
- **Zielgruppen-Relevanz**: X/10 (Begründung)
- **GESAMT**: XX/50 Punkte (XX%)

QUALITÄTSSTUFEN:
- 70-79%: Gut (verwendbar)
- 80-89%: Sehr gut (empfehlenswert)  
- 90-100%: Exzellent (herausragend)
```

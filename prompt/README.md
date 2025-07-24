# Prompt-Dokumentation & Regelwerk

## Formatvorgaben („Prompt-Lint")

### Pflicht-Frontmatter
Jede Prompt- und Modul-Datei muss valides YAML-Frontmatter enthalten:

**Für Prompts:**
```yaml
---
description: "Kurzbeschreibung des Prompts"
arguments:
  - name: example_arg
    type: string|integer|boolean|array|object
    required: false
    default: null
    description: "Wofür ist dieses Argument?"
version: 0.1.0
status: draft|optional|required|deprecated
includes: []   # optionale Liste von Modul-Dateien
---
```

**Für Module:**
```yaml
---
description: "Kurzbeschreibung des Moduls"
placement: "prepend|append|after:<section>|replace:<selector>|line:<n>"
status: draft|optional|required|deprecated
version: 0.1.0
---
```

### Struktur-Anforderungen

#### Prompt-Dateien
- **Klare Sections**: `Kontext`, `Rollen`, `Regeln`, `Schritte`, `Output-Check` (konsistente Überschriften)
- **Details-Block** nach Frontmatter
- **Doppelung**: Prompt sowohl lesbar als auch als Copy/Paste-Codeblock

#### Modul-Dateien
- **Details-Block** nach Frontmatter
- **Modul-Inhalt** sowohl lesbar als auch als Copy/Paste-Codeblock

### Versionierung
- **Explizite SemVer-Versionierung** (0.1.0, 1.0.0, etc.)
- **Version bump** bei jeder Änderung
- **Breaking Changes** explizit markieren

### Naming-Konventionen
- **Prompt-Dateien**: immer kleingeschrieben, enden auf `.prompt.md`
  - Beispiel: `title-generation.prompt.md`
- **Modul-Dateien**: immer kleingeschrieben, enden auf `-modul.prompt.md`
  - Beispiel: `seo-optimization-modul.prompt.md`
  - Beispiel: `scoring-system-modul.prompt.md`

### Sprach- & Formatregeln
- **Keine gemischten Sprachen** innerhalb einer Datei
- **Argumente vollständig dokumentieren** (keine „magischen Defaults")
- **Includes müssen eindeutig sein**

## Änderungs-Workflow

### Branch-Konventionen
- `feature/prompt-name` für neue Prompts
- `feature/module-name` für neue Module  
- `fix/issue-description` für Bugfixes
- `docs/update-description` für Dokumentation

### Commit-Konventionen
- `feat: add new title-generation prompt`
- `fix: correct placement syntax in module`
- `docs: update README with new guidelines`
- `chore: bump version to 1.0.0`

### Manuelle Checkliste vor PR
- [ ] Frontmatter ist valides YAML
- [ ] Version wurde erhöht
- [ ] Breaking Changes dokumentiert
- [ ] Alle Pflichtfelder ausgefüllt
- [ ] Includes-Referenzen existieren
- [ ] Copy/Paste-Codeblock ist identisch mit lesbarer Version

## Modul-Handling

### Einbindung
Module werden über das `includes`-Array im Prompt-Frontmatter referenziert:
```yaml
includes: ["scoring-system-modul.prompt.md", "seo-optimization-modul.prompt.md"]
```

### Platzierung
Das `placement`-Feld definiert, wo das Modul eingefügt wird:
- `prepend`: Am Anfang des Prompts
- `append`: Am Ende des Prompts  
- `after:<section>`: Nach einer bestimmten Section
- `replace:<selector>`: Ersetzt einen bestimmten Bereich
- `line:<n>`: An einer bestimmten Zeilennummer

### Versionierung
- Module haben eigene Versionen
- **TBD**: Kompatibilitätsmatrix zwischen Prompt- und Modul-Versionen

## Status-Taxonomie
- `draft`: In Entwicklung, nicht produktionsreif
- `optional`: Kann verwendet werden, aber nicht erforderlich
- `required`: Muss verwendet werden
- `deprecated`: Veraltet, wird entfernt

## Argument-Typen
- `string`: Textuelle Eingabe
- `integer`: Ganzzahl
- `boolean`: true/false Werte
- `array`: Liste von Werten
- `object`: Strukturierte Datensammlung

---

**TBD/Offen:**
- Exakte `placement`-Syntax für komplexere Fälle
- Automatisierung via `.cursorrules` / `.prompt-lint.yaml`
- PR-Template & CI-Integration

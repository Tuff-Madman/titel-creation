\<!--
It is mandatory for the receiving AI to refer to custom-instructions.md. The instructions there must be followed without exception to act and behave as specified for this project.
-->
**Important:** See [custom-instructions.md](./custom-instructions.md) for mandatory workflow and AI guidance.





Die Aufgabe fokussiert auf präzise, regelgeleitete Ausgaben (z. B. Produkttitel oder Spezifikationen) und weniger auf etwas Stilistisches oder auf Audience-spezifische Anpassungen. 
 und nicht auf marken- oder zielgruppenspezifisches Storytelling. Deshalb sind ausführliche Rollen- oder Brandbeschreibungen (z. B. „porta“-Kontext) hier weniger hilfreich als  harte, deterministische Regeln, die definieren, welche Attribute in welcher Reihenfolge zu verwenden sind. 
 Messbare Regeln (z. B. maximale Zeichenlänge, exakte Maßeinheiten, feste Reihenfolgen)  So erzwingst du deterministisches Verhalten statt stilistischer Kreativität.

## Ist sichergestellt das immer nur nur einen Titel ausgegen wird?
Bei LLMs können strukturierte Ausgaben grundsätzlich vorgegeben werden – das bedeutet, dass beim Abruf festgelegt wird, ob die Ausgabe in einem vordefinierten, maschinenlesbaren Format oder Schema erfolgen soll. Obwohl Contentserve diese Möglichkeit nicht bietet, gibt es erprobte Methoden, um mit sehr hoher Zuverlässigkeit sicherzustellen, dass ausschließlich der gewünschte Titel ausgegeben wird:

1. Systematische Wiederholung und explizite Vorgabe "nur Titel ausgeben" verstärkt die Erwartungshaltung
2. Imperative Formulierung der zwingend notwendigen Ausgabe – durch Großschreibung wird zusätzlich Wichtigkeit signalisiert  
3. Konkrete, exemplarische Vorgaben des erwarteten Outputs in Beispielabschnitten platzieren
4. "Double Down" oder "Key Reminder" am Ende zur Verstärkung der Intention und Nutzung von Modell-Mechanismen

Welchen Anteil jede Maßnahme hat und was weggelassen werden kann, lässt sich schwer vorhersagen. Wahrscheinlich erreichen auch fortschrittliche Modelle ohne einzelne Komponenten hohe Zuverlässigkeit. Da diese Instruktionen jedoch sehr token-sparsam sind, bewegen wir uns im Mikro-Kostenbereich. Der potenzielle Nutzen ist so hoch, dass Verzicht unrentabel wäre.

**Fallback-Option für leere/fehlende Felder:** Falls Pflichtfelder fehlen oder leer sind, soll nur dann eine vordefinierte, exakt formatierte Fehlermeldung ausgegeben werden (z.B. "Missing Data: brand, model"). Die exakte Formulierung – idealerweise in Anführungszeichen und mit Beispiel – reduziert das Risiko, dass das Modell andere "schönere" Texte erfindet oder inkonsistente Fehlermeldungen produziert.

 Beispiele richtig verwenden
Beispiele sind für diese Aufgabe ein essenzielles, vielleicht sogar das wichtigste und zugleich am einfachsten zu handhabende Mittel, um die gewünschten Ergebnisse zu erzielen. Für Beispiele gelten nach wie vor die etablierten Grundprinzipien:
 Beispiele sollen repräsentativ für unterschiedliche Prinzipien sein (vollständige Daten, teilweise Daten, fehlende Pflichtattribute, Grenzfälle wie zu lange Titel).
Jedes Beispiel steht für genau eine Lektion/Regel.
Um die Format- und Bezeichnungstreue sicherzustellen, sollten die Beispiele die Original-Attributbezeichnungen exakt im Original-Format (z. B. JSON Key-Value-Paar) verwenden (keine Stichpunkte, keine alternativen Namen oder Synonyme für Keys).
Redundante Beispiele für fast identische Produkte sind zu vermeiden – stattdessen sollte die Breite abgedeckt werden, sodass sich aus den Beispielen übertragbare Muster analog ableiten lassen, was eine der Kernstärken des sogenannten "In-Context Transfer Learning" durch "Few-Shots" nutzt.

 Negativliste & harte Grenzen
Neben der "Double-Down"-Wiederholung hilft eine explizite Negativliste (keine Erklärungen, Kommentare etc.).


Die Frage nach der idealen Platzhalter-Syntax ([] vs. {} vs. {{}}) ist am Ende relativ komplex und Gegenstand von Forschung. Für viele Anwendungen besteht der entscheidende Faktor letztlich in der Konsistenz und Eindeutigkeit im Prompt. Zudem sind aktuelle, kapazitätsstarke LLMs ausgereift genug, um verschiedene Konventionen effektiv zu handhaben, solange sie nur logisch, widerspruchsfrei und konsistent angewendet werden. There are many references on using single, double, curly, or square brackets for templating in prompt/title generation.
Letztlich gibt es nicht den einen richtigen Weg; die Methode sollte einfach und klar angewendet werden.


Menschliche Lesbarkeit: Die Verwendung von [eckigen Klammern] ist dabei vor allem eine visuell klare Möglichkeit zu signalisieren: "Hier gehört eine Variable hin."
Vermeidung unnötiger Komplexität: Als einfacher, fester Standard minimiert dies gewissermaßen auch potenzielle Fehlinterpretationen, Fehlgebrauch oder einen Syntax-Mischmasch, der bei komplexeren Systemen wie `{{#if anweisung}}...{{/if}}` schnell entstehen kann, da dieser bei der Generierung ohnehin nicht programmatisch verarbeitet wird.
Verständlichkeit: Die Anweisungen bleiben auch für Nicht-Experten im Prompt-Engineering unmittelbar verständlich. Beispiel: Erstelle einen Titel nach dem Schema: `[Marke] [Produktkategorie] '[Serie]' in [Farbe]`.

When using this in the prompt, you should specify further details about attribute references inside square brackets to indicate where and how each piece of input data should feed into the generated content.



[01-title-generation.prompt.md](./prompt/01-title-generation.prompt.md)
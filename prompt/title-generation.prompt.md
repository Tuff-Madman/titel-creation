---
description: "Generiert präzise H1-Titel für Möbelprodukte basierend auf Produktdaten und Bildern"
arguments:

status: draft

---


YOUR GOAL IS TO CRAFT ONE LINE THAT CLEARLY IDENTIFIES the Produkt, surfaces the main keyword early, highlights genuine benefits, and remains friendly to search engines. Keep customer value in mind as background context.


YOU RECEIVE  
<PRODUCT_FACTSHEET>{{Produkt FACTSHEET}}</PRODUCT_FACTSHEET>  
<PRODUCT_ATTACHMENT>{{IMAGE ATTACHMENT}}</PRODUCT_ATTACHMENT>  


KEY COMPONENTS OF AN EFFECTIVE FURNITURE H1  
- Titles should be informative, easy to scan, and free from filler words or redundancy  
- Surface the main keyword early, highlight genuine benefits, and remain friendly to search engines  
- Immediate product clarity for users & Google  
- Main search keyword (Produkt-Typ) placed early  
- High-value attributes: Marke, Größe, Farbe, Material, Stil, Feature  
- Natural, hype-free wording; avoid keyword stuffing  
- Titel-Länge: zwischen 50 und 55 Zeichen (harte Obergrenze: maximal 60 Zeichen)


# TITLE CREATION INSTRUCTIONS
Create titles that are naturally derived from the most important Merkmale and Attributes, so that they appear logical to German furniture shoppers. Follow the guidelines and Attribute-Priorität below to achieve consistent, clear, and SEO-friendly results.


## GUIDELINES

Structure heuristic based on available entities:
- If Marke + Produkt-Typ + Serie present: Marke Produkt-Typ Serie ... - Farbe
- If Marke + Produkt-Typ present: Marke Produkt-Typ ... - Farbe  
- If only Produkt-Typ present: Produkt-Typ ... - Farbe
- If Serie/Produktname is missing: ... skip to the next relevant key attribute ...
- If Farbe is missing: ... end without hyphen separator

• Include the Produkt-Typ if a Marke is originally present, immediately after it  
• Include the Produktname/Serie if a Marke is present, directly after the Produkt-Typ where possible  
• Farben should always appear at the end, separated by a hyphen  


### ATTRIBUTE-PRIORITÄT  

USE WHEN CONFIDENTLY PRESENT (GUIDELINE, NOT STRICT)  
1 Marke 2 Produkt-Typ 3 Serie/Modell 4 Setgröße/Konfiguration  
5 Maße 6 Material 7 Farbe (" / " for two colors; if >2, keep the main color)  
8 Besonderes Feature/Oberfläche  

Note: You will find further details and examples in the respective sections below.


## Ambiguity and Conflict Resolution for Product Information
It may occur that information between the Produkt factsheet attribute data and visual image information is contradictory, confusing, or ambiguous. Only if title-essential information conflicts between sources, prioritize the source that provides objectively correct and logically consistent Produkt characteristics.

If a higher-priority entity is missing, move to the next one **that makes sense**.  

Visual evidence from the attached images should:
- Take precedence for form, shape, and design elements when absolute certainty exists about visual characteristics
- Be used for supplementary corrective interpretation when high confidence can be established
- Apply only according to the specific scenarios listed below:


### SCENARIOS

Round vs. Rectangular Data: IF visual shows round table BUT factsheet provides only Höhe [H] cm, Breite [B] cm (no Durchmesser):
→ Transform using max(H, B) as Durchmesser

REMEMBER: Return exactly one line in correct German: the finished H1 Titel.

# CONSTRAINTS  
• Collapse multiple spaces; avoid trailing punctuation  
• Only include information that is clearly evident from the inputs—no hallucination  
• The title must be between 50 and 55 characters long (never more than 60 characters; hard limit).  
• Never output "null" or placeholders.  
• Include only attributes that can be clearly derived from the Produkt image or data.


# EXAMPLES AND REFERENCES

## EXAMPLES
<!-- 
Each of following XML tags contains a complete input-output pair and rationale for a specific Produkt Titel. The description attribute in the XML tag describes the specific example case.
-->

<schlafzimmer_bett description="Ambiguity resolution – handling unclear Produkt specifications with fallback logic">

**Product Fact Sheet Input:**
[Placeholder for Produkt data]

**Titel Output:**
"Placeholder for H1 Titel"

**Rationale:**
[Placeholder for reasoning behind Titel construction]

</schlafzimmer_bett>


<wohnzimmer_sofa description="Optimal structure – complete attribute set with proper Marke-Typ-Serie ordering">

**Input Attribute:**
[Placeholder for Produkt data]

**Generated Titel:**
[Placeholder for H1 Titel]

**Rationale:**
[Placeholder for reasoning behind Titel construction]

</wohnzimmer_sofa>


## HOW GOOD TITLES LOOK LIKE

- 'Placeholder for well-structured H1 Titel' (kurze Begründung, warum das example as good)
- 'Weitere Beispiel für guten H1-Titel' (other brief rationale)


## HOW A BAD TITLE LOOKS LIKE

- 'Placeholder for poor H1 Titel' (kurze Begründung, warum das example as bad)
- 'Schlechtes Beispiel für H1-Titel' (further possible rationale)



---
description: "Generiert präzise H1-Titel für Möbelprodukte basierend auf Produktdaten und Bildern"
arguments:
  PRODUCT_FACT_SHEET: 

status: draft
---

```
Your goal is to craft one line that clearly identifies the Produkt, surfaces the main keyword early, highlights genuine benefits, and remains friendly to search engines. Keep customer value in mind as background context.


YOU RECEIVE  
<PRODUCT_FACTSHEET>{{Produkt FACTSHEET}}</PRODUCT_FACTSHEET>  
<PRODUCT_ATTACHMENT>{{IMAGE ATTACHMENT}}</PRODUCT_ATTACHMENT>  


KEY COMPONENTS OF AN EFFECTIVE FURNITURE H1  
- Surface main keyword (Produkt-Typ) early for immediate product clarity
- Include high-value attributes: Marke, Größe, Farbe, Material, Stil, Feature  
- Natural, hype-free wording; avoid keyword stuffing and filler words
- Titel-Länge: zwischen 50 und 55 Zeichen (harte Obergrenze: maximal 60 Zeichen)


# INSTRUCTIONS
Structure and format the title according to the following guidelines, using only original product information from the product factsheet or clearly derived from the attached product image. 

[[## FORMATTING REQUIREMENTS]]


## TITLE CREATION GUIDELINES

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


## AMBIGUITY AND CONFLICT RESOLUTION

It may occur that information between the Produkt factsheet attribute data and visual image information is contradictory, confusing, or ambiguous. Only if title-essential information conflicts between sources, prioritize the source that provides objectively correct and logically consistent Produkt characteristics.

If a higher-priority entity is missing, move to the next one **that makes sense**.  

Visual evidence from the attached product images should:
- Take precedence for form, shape, and design elements when absolute certainty exists about visual characteristics
- Be used for supplementary corrective interpretation when high confidence can be established
- Apply only according to the specific scenarios listed below:


### SCENARIOS

1. Image with round Table vs. rectangular Attribute Data: IF visual shows round table BUT factsheet provides only Höhe [H] cm, Breite [B] cm (no Durchmesser):
→ Transform using max(H, B) as Durchmesser (e.g. ".... 80 cm Durchmesser ...")

## CONSTRAINTS

• Collapse multiple spaces; avoid trailing punctuation  
• Only include information that is clearly evident from the inputs—no hallucination  
• The title must be between 50 and 55 characters long (never more than 60 characters; hard limit).  
• Never output "null" or placeholders.  
• Include only attributes that can be clearly derived from the Produkt image or data.

[[# EXAMPLES AND REFERENCES]]


REMEMBER: Return exactly one line in correct German: the finished H1 Titel.
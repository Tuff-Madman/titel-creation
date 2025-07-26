---
description: "Generiert präzise H1-Titel für Möbelprodukte basierend auf Produktdaten und Bildern"
arguments:
  PRODUCT_FACT_SHEET: 

status: draft
---

```
Your goal is to craft one line H1 title for product page that clearly identifies the Produkt, surfaces the main keyword early, highlights genuine benefits, and is optimized for search engines while keeping 


<PRODUCT_FACTSHEET>
{{Produkt FACTSHEET}}
</PRODUCT_FACTSHEET>  
 


KEY COMPONENTS OF AN EFFECTIVE FURNITURE H1  
- Surface main keyword (Produkt-Typ) early for immediate product clarity
- Include high-value attributes: Marke, Größe, Farbe, Material, Stil, Feature  
- Natural, hype-free wording; avoid keyword stuffing and filler words
- Titel-Länge: zwischen 50 und 55 Zeichen (harte Obergrenze: maximal 60 Zeichen)


# INSTRUCTIONS
Structure and format the title according to the following guidelines, using only original product information from the product factsheet or clearly inferred from the attached product image. 


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


## CONSTRAINTS

• Collapse multiple spaces; avoid trailing punctuation  
• Only include information that is clearly evident from the inputs—no hallucination  
• The title must be between 50 and 55 characters long  
• Never output "null", braces/syntax or placeholders.  
• Include only attributes that can be clearly derived from the given Produkt image or data.

[[# EXAMPLES AND REFERENCES]]


REMEMBER: It is crucial that you must Return ONLY a H1 Titel and nothing else.
If and only if you are not provided sufficient product information, you will strictly provide this output. 
```
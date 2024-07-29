---
recipe: breakfast ice cream
category: breakfast
appliance: none
total_mins: 7
portions: 1
ingredients: 
- item: "[[Greek yoghurt]]"
  quantity: 100
  units: g
- item: "[[Almond butter]]"
  quantity: 15
  units: g
- item: "[[Frozen blueberries]]"
  quantity: 50
  units: g
tags:
  - recipe
  - breakfast
---

## Ingredients (rendered from frontmatter using dataview)
```dataview
LIST WITHOUT ID (i.quantity + i.units + " " + i.item)
WHERE file = this.file
FLATTEN ingredients as i
```

## Method
1. In a bowl, mix the yoghurt and nut butter together until smooth
2. Stir in the frozen berries and leave the mixture to settle for 2-3 minutes before eating.
## Nutrition information
Current attempt has nutrition values per 100g.

```dataview
TABLE WITHOUT ID (i.quantity + i.units) as Quantity, i.item as Item, i.item.protein as "Protein per 100g", round((number(i.item.protein) / 100 * number(i.quantity)),1) as Protein
WHERE file = this.file
FLATTEN ingredients as i
```

```dataview
TABLE WITHOUT ID n.metric as Nutrition
WHERE file = this.file
FLATTEN ingredients as i
FLATTEN i.item.nutrition as n
```

Next steps:
- nutrition values to match item quantities
- how do you get a sum at the bottom of the page?
- can you orient the table in the other direction?
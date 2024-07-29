---
recipe: breakfast ice cream
category: breakfast
appliance: none
total_mins: 7
portions: 1
ingredients: 
  greek-yoghurt: 100 g
  almond-butter: 15 g
  frozen-blueberries: 50 g
tags:
  - recipe
  - breakfast
---

## Description
The original file. Ingredients stored as a nested list in YAML frontmatter

## Ingredients (rendered via dataview)
```dataview
TABLE WITHOUT ID ingredients, extract(ingredients, "greek-yoghurt", "almond-butter", "frozen-blueberries") AS extract, join(extract(ingredients, "greek-yoghurt", "almond-butter", "frozen-blueberries"), ":") AS join
WHERE file = this.file
```

## Ingredients (using inline DQL)

| Quantity                               | Ingredient                |
| -------------------------------------- | ------------------------- |
| `=this.ingredients.greek-yoghurt`      | `=this.ingredients.first` |
| `=this.ingredients.almond-butter`      | `=this.tags`              |
| `=this.ingredients.frozen-blueberries` |                           |

## Ingredients (manually typed)
100 g greek yoghurt
1 tbsp almond butter
50 g frozen blueberries

## Method
1. In a bowl, mix the yoghurt and nut butter together until smooth
2. Stir in the frozen berries and leave the mixture to settle for 2-3 minutes before eating.

## Tags
- breakfast
- gluten-free
- vegetarian

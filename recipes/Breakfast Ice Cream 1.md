---
recipe: breakfast ice cream
category: breakfast
appliance: none
total_mins: 7
portions: 1
tags:
  - recipe
  - breakfast
---

## Description
Plan B. Ingredients stored as inline key-value pairs.

## Ingredients as inline key-value pairs
#lucy
Define ingredients with key of 'ingredient' then value of eg 'oats, 50g'
- (ingredient:: greek yoghurt, "100 g")
- (ingredient:: almond butter, 15 g)
- (ingredient:: frozen blueberries, "50 g")

## Dataview test
Try to retrieve all inline ingredients with key 'ingredient' in a dataview query:
```dataview
TABLE WITHOUT ID ingredient
FROM #lucy
```
Note: if put separate quote marks around ingredient & quantity in key-value pairs above, then dataview treats the inline entry as a list. Doesn't help for the query above, but maybe for a non-list view? How to collate that info though, without using a LIST.

Try putting inline ingredients into a table instead
```dataview
TABLE ingredient, ingredient[0][0], ingredient[1][0]
WHERE file = this.file
```

Try to get data from frontmatter using dataview query:

```dataview
TABLE ingredients.greek-yoghurt
WHERE file = this.file
```

Try to pull through nutrition information from recipes

```dataview
TABLE ingredients
WHERE file = this.file
```

## Method
1. In a bowl, mix the yoghurt and nut butter together until smooth
2. Stir in the frozen berries and leave the mixture to settle for 2-3 minutes before eating.

## Tags
- breakfast
- gluten-free
- vegetarian

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
Plan C. Ingredients stored as key-value pairs, sitting within a tagged section.

## zone
#zone
Create specially-named section and add ingredients as key-value pairs, to see if you can return just data from a specific section of the page
- [Greek yoghurt:: 80 g]
- [[Almond butter]]:: 15 g
- [[Frozen blueberries]]:: "50 g"

## Dataview test
Try to retrieve ingredients stored within the 'zone' section of the page only.
```dataview
TABLE greek-yoghurt, [[Almond butter]].protein
FROM #zone
```

Note: have managed to retrieve protein amount for 100g greek yoghurt. In adding the link to the greek yoghurt page, though, I lost the ability to be able to retrieve the quantity of greek yoghurt in this recipe. 

Next step: investigate using file.outlinks. Can you iterate over them using map?

```dataview
TABLE file.outlinks
FROM #zone
```

## Method
1. In a bowl, mix the yoghurt and nut butter together until smooth
2. Stir in the frozen berries and leave the mixture to settle for 2-3 minutes before eating.

## Tags
- breakfast
- gluten-free
- vegetarian

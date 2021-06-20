---
layout: page
title: baking
description: explanation of baking conventions and personal sourdough recipes
---

There is a foundational problem within the sourdough baking community.  Bakers conventionally design and publish static, unscalable recipes without discussing how we can generate successful new recipes that meet our exact preferences. New bakers (and veteran ones) should embrace curiosity and experimentation with new sourdough ideas, and we can enable this by writing down a self-consistent formulation that makes recipe creation as simple and reproducible as possible.

This formulation allows bakers to encode environmental factors and taste preferences into their recipes from the beginning, eliminating the need for costly and disappointing experiments. This formulation also allows bakers to take a baseline recipe and make independent adjustments consistent with particular environmental conditions (high humidity, or clammy weather, ...) or simply adjustments to account for your personal crumb preference, or an addition of milk, butter, honey, etc. 

#### Definitions

Take the following definitions as our starting point, keeping in mind that we use grams as our singular measurement unit: 

- *Hydration* is the ratio of liquids to non-liquids (*e.g.* flour) in our doughball. This is denoted by <img src="https://render.githubusercontent.com/render/math?math=H">.
- *Levain* is the yeast culture used in sourdough baking. This is typically a 50%/50% mix of flours and water, fed a strict diet at specified intervals. The levain weight is denoted by <img src="https://render.githubusercontent.com/render/math?math=L">.
- *Un-fermented flour* is the amount of flour we mix directly into the dough, which is not part of the levain. This is denoted by <img src="https://render.githubusercontent.com/render/math?math=f_{auto}">. 
- The qualifier "auto" above refers to the *autolyse* step. The water added at this step is denoted respectively by <img src="https://render.githubusercontent.com/render/math?math=h_{auto}">.
- *Fermented flour* is the amount of flour included in the Levain. Typically this is 50% of the Levain weight, but depends on your feeding scheme.
- *Inoculation* is the ratio of un-fermented flour to fermented flour in the recipe. This represents how large your yeast culture is compared to how much food you provide to the culture. This is denoted by <img src="https://render.githubusercontent.com/render/math?math=I">.
 - *Weight* is the final weight of your raw doughball. This is denoted <img src="https://render.githubusercontent.com/render/math?math=W">, and is the sum of the core ingredients <img src="https://render.githubusercontent.com/render/math?math=W=f_{auto}%2Bh_{auto}%2BL">. Salt weight is comparatively tiny, and is thus neglected throughout.

#### Algorithm

<!--   <img src="https://render.githubusercontent.com/render/math?math=f_{auto}=2W/(1%2BH)(1%2BI)">

<!--  <img src="https://render.githubusercontent.com/render/math?math=L=\frac{2IW}{(1%2BI)(1%2BH)}">

<!--  <img src="https://render.githubusercontent.com/render/math?math=L=2IW\div(1%2BI)(1%2BH)">

#### Example Usage

#### Caveats and Clarifications

- As a side note, I like to distinguish between *starter* and *levain*. My starter is my base sourdough culture, which I branch off when needed. This lives in my refrigerator, and is regularly removed for feeding. The levain is the yeast culture that is prepared for a specific bake, which begins from my starter, and is then fed on a regiment for a few days leading up to bake day. 



jge 20 June 2021.

---
layout: page
title: baking
description: explanation of baking conventions and personal sourdough recipes
---

#### Basis
There is a foundational problem within the sourdough baking community.  Bakers conventionally design and publish static, unscalable recipes without discussing how we can generate successful new recipes that meet our exact preferences. New bakers (and veteran ones) should embrace curiosity and experimentation with new sourdough ideas, and we can enable this by writing down a self-consistent formulation that makes recipe creation as simple and reproducible as possible.

This formulation allows bakers to encode environmental factors and taste preferences into their recipes from the beginning, eliminating the need for costly and disappointing experiments. This formulation also allows bakers to take a baseline recipe and make independent adjustments consistent with particular environmental conditions (high humidity, or clammy weather, ...) or simply adjustments to account for your personal crumb preference, or an addition of milk, butter, honey, etc. 

The sourdough process is more complicated than typical yeast-bread baking, because in the latter we have a clear separation of flour and water and yeast. If we wish to increase hydration (as an example), we can increase the amount of water and decrease the amount of flour by the same amount. No matter what, we can achieve any imaginable bread by simply scaling the flour, water, and yeast because their quantity is always in direct proportion. This is not the case for sourdough baking. If we attempt to increase the hydration by simply adding more water ...

#### Definitions

Take the following definitions as our starting point, keeping in mind that we use grams as our singular measurement unit: 

- *Hydration* is the ratio of liquids to non-liquids (*e.g.* flour) in our doughball. This is denoted by <img src="https://render.githubusercontent.com/render/math?math=H">, and is normally written as a percentage.
- *Levain* is the yeast culture used in sourdough baking. This is typically a 50%/50% mix of flours and water, fed a strict diet at specified intervals. The levain weight is denoted by <img src="https://render.githubusercontent.com/render/math?math=L">.
- *Un-fermented flour* is the amount of flour we mix directly into the dough, which is not part of the levain. This is denoted by <img src="https://render.githubusercontent.com/render/math?math=f_{auto}">. 
- The qualifier "auto" above refers to the *autolyse* step. The water added at this step is denoted respectively by <img src="https://render.githubusercontent.com/render/math?math=h_{auto}">.
- *Fermented flour* is the amount of flour included in the levain. Typically this is 50% of the levain weight, but depends on your feeding scheme.
- *Inoculation* is the ratio of un-fermented flour to fermented flour in the recipe, usually written as a percentage. This represents how large your yeast culture is compared to how much food you provide it. This is denoted by <img src="https://render.githubusercontent.com/render/math?math=C">.
 - *Weight* is the final weight of your raw doughball. This is denoted <img src="https://render.githubusercontent.com/render/math?math=W">, and is the sum of the core ingredients <img src="https://render.githubusercontent.com/render/math?math=W=f_{auto}%2Bh_{auto}%2BL">. Salt weight is comparatively tiny, and is thus neglected throughout.

#### Algorithm

First choose your desired weight <img src="https://render.githubusercontent.com/render/math?math=W">. Now choose your hydration <img src="https://render.githubusercontent.com/render/math?math=H"> and inoculation <img src="https://render.githubusercontent.com/render/math?math=C"> based on your environment and preferences. The first step is to compute <img src="https://render.githubusercontent.com/render/math?math=f_{auto}"> and <img src="https://render.githubusercontent.com/render/math?math=h_{auto}"> for your autolyse:

<img src="https://render.githubusercontent.com/render/math?math=f_{auto}=W/(1%2BH)(1%2BC)">

<img src="https://render.githubusercontent.com/render/math?math=h_{auto}=f_{auto}[H(1%2BC)-C]">

The amount of levain needed is then

<img src="https://render.githubusercontent.com/render/math?math=L=2C f_{auto}">.



#### Example Usage

Under construction. 

#### Caveats, Clarifications, Good Practices

- As a side note, I like to distinguish between *starter* and *levain*. My starter is my base sourdough culture, which I branch off when needed. This lives in my refrigerator, and is regularly removed for feeding. The levain is the yeast culture that is prepared for a specific bake, which begins from my starter, and is then fed on a regiment for a few days leading up to bake day. 

- Best practice is to define your salt weight as a percentage of un-fermented flour weight. Most sourdough bakers fall in the range 2.0% - 2.8%. For typical recipes, a half-kilo loaf will call for 6g-8g salt. My personal preference is to stick to the 2.0% mark

- Vaporization will obviously occur during the baking process, resulting in a significant weight reduction for your sourdough. If you are targeting a specific final weight, expect a 20% weight loss. The process is influenced by your baking vessel, your baking oven, the loaf geometry, the local temperature and humidity (environmental vapor pressure), etc. You will find higher vapor loss for loaves with large ratios of surface area to volume, such as baguettes. 


jge 20 June 2021.

---
layout: page
title: sourdough
description: explanation of baking conventions and personal sourdough recipes
---

#### Motivation
There is a foundational problem within the sourdough baking literature.  Bakers conventionally design and publish static, unscalable recipes without discussing how we can generate successful new recipes that meet our exact preferences. New bakers (and veteran ones) should embrace curiosity and experimentation with new sourdough ideas, and we can enable this by writing down a self-consistent formulation that makes recipe creation as simple and reproducible as possible.

The process of developing a sourdough bread recipe is more complicated than typical yeast-bread baking. In both situations, the key independent variables are *hydration*--which controls the ratio of water to flour, and *inoculation*--which controls how much active yeast is present in the dough, and *total weight*. In typical yeast-breads, these three quantities are determined independently by the amounts of water, flour, and yeast in the dough. In sourdough however, the relationships are linear combinations, not simple scalar multiples of one another. 

The formulation provided here allows bakers to take a baseline recipe and make independent adjustments consistent with particular environmental conditions (high humidity, or clammy weather, ...) or to simply make adjustments to account for your personal crumb preference, or an addition of milk, butter, honey, etc. This method also allows bakers to encode environmental factors and taste preferences into their recipes from the beginning, creating a mathematically exact recipe from scratch, eliminating the need for costly and disappointing experiments, not to mention annoying iterative calculations. 



#### Definitions

Take the following definitions as our starting point, keeping in mind that we use grams as our singular measurement unit: 

- *Hydration* is the ratio of liquids to non-liquids (*e.g.* flour) in our doughball. This is denoted by <img src="https://render.githubusercontent.com/render/math?math=H">.
- *Levain* is the yeast culture used in sourdough baking. This is typically a mix 50% flours and 50% water, fed a strict diet at specified intervals. The levain weight is denoted by <img src="https://render.githubusercontent.com/render/math?math=L">.
- *Un-fermented flour* is the amount of flour we mix directly into the dough, which is not part of the levain. This is denoted by <img src="https://render.githubusercontent.com/render/math?math=f_{auto}">. 
- The qualifier "auto" above refers to the *autolyse* step. The water added at this step is denoted respectively by <img src="https://render.githubusercontent.com/render/math?math=h_{auto}">.
- *Fermented flour* is the amount of flour included in the levain. Typically this is 50% of the levain weight, but depends on your feeding scheme.
- *Inoculation* is the ratio of fermented flour to un-fermented flour in the recipe. This represents how large your yeast culture is compared to how much food you provide it, effectively a concentration. Inoculation is denoted by <img src="https://render.githubusercontent.com/render/math?math=C">.
 - *Weight* is the final weight of your raw doughball. This is denoted <img src="https://render.githubusercontent.com/render/math?math=W">, and is the sum of the core ingredients <img src="https://render.githubusercontent.com/render/math?math=W=f_{auto}%2Bh_{auto}%2BL">. Salt weight is comparatively tiny, and is thus neglected throughout.

Typical sourdough, regardless of practitioner or region or tradition, will use hydration in the range 0.72 (very low) to 0.84 (very high), and inoculation in the range 0.10 (generally for hot & humid weather) and 0.14 (very high). Good baseline values are 0.79 and 0.11 respectively. 

#### Key equations: standard case

First choose your desired weight <img src="https://render.githubusercontent.com/render/math?math=W">. Now choose your hydration <img src="https://render.githubusercontent.com/render/math?math=H"> and inoculation <img src="https://render.githubusercontent.com/render/math?math=C"> based on your environment and preferences. The first step is to compute <img src="https://render.githubusercontent.com/render/math?math=f_{auto}"> and <img src="https://render.githubusercontent.com/render/math?math=h_{auto}"> for your autolyse:

<img src="https://render.githubusercontent.com/render/math?math=f_{auto}=W/(1%2BH)(1%2BC)">

<img src="https://render.githubusercontent.com/render/math?math=h_{auto}=f_{auto}[H(1%2BC)-C]">

The amount of levain needed is then

<img src="https://render.githubusercontent.com/render/math?math=L=2C f_{auto}">.

#### Key equations: additional ingredients

The addition of non-standard ingredients modifies the standard equations in an intuitive way. The two use cases are for added solids <img src="https://render.githubusercontent.com/render/math?math=W_{solids}"> and added liquids <img src="https://render.githubusercontent.com/render/math?math=h_{add}">.

Including non-standard liquids like honey, milk, or butter requires a re-consideration of the 'standard case' equations. Here's how I estimate the solid/liquid breadown of typical added liquids:

* Honey: 85% solids + 15% liquid
* Milk: 12% solids + 88% liquid  
* Butter: 85% solids + 15% liquid 
* Molasses: 78% solids + 22% liquid

The key equations for arbitrary ingredients with solid and/or liquid components: 

<img src="https://render.githubusercontent.com/render/math?math=f_{auto}=(W-W_{add})/(1%2BH)(1%2BC)">

<img src="https://render.githubusercontent.com/render/math?math=h_{auto}=f_{auto}[H(1%2BC)-C]-h_{add}">

<img src="https://render.githubusercontent.com/render/math?math=L=2C f_{auto}">.

#### Typical workflow

Roughly 7 days before my chosen bake day, I pull my starter from the refrigerator and allow an hour to reach room temperature. The objective is to gradually feed the starter more food per feeding, to eventually make the culture vigorous enough to sufficiently inoculate our batch of bread. I always feed my starter the exact same meal of water and feeding flour, which is a specific mixture of individual flours. In my case, that is 90% high-quality bread flour, 9% dark rye flour, and 1% whole wheat flour.  

In the first feeding I combine 2 parts starter, 1 part feeding flour, 1 part water. I note the time required for this starter to reach peak volume (10-24 hrs). After it has peaked, I feed again but in a 1:1:1 ratio. Again when the mixture peaks, I take a small sample and re-feed that again. If the starter seems to grow somewhat slowly, I will feed 1:1:1 again, otherwise I proceed to increase the feeding ratio to 1:2:2. I typically repeat the 1:2:2 step, feed at 1:3:3 once, and finally to 1:4:4. The starter is then ready to build a levain from. 

2 days before bake day, aka 1 day before prep day, I do all of the needed calculations and write the exact recipe down. I first decide how many loaves to make, the weight <img src="https://render.githubusercontent.com/render/math?math=W"> of each, and the hydration <img src="https://render.githubusercontent.com/render/math?math=H"> and inoculation <img src="https://render.githubusercontent.com/render/math?math=C"> that I want. I can then compute the amount of flour and water for my autolyse per loaf, <img src="https://render.githubusercontent.com/render/math?math=f_{auto}"> and <img src="https://render.githubusercontent.com/render/math?math=h_{auto}">. I also calculate the amount of levain needed per loaf, given by <img src="https://render.githubusercontent.com/render/math?math=L">. I create the levain by combining the fed starter in a 1:4:4 ratio with the specific flour mix I want for the levain; this mix is almost always distinct from my feeding mixture. I let the levain rest overnight, usually 6-12 hours depending on conditions. At this point, I can decide what flour combination I am using for the autolyse.

The next morning, I mix the <img src="https://render.githubusercontent.com/render/math?math=f_{auto}"> and <img src="https://render.githubusercontent.com/render/math?math=h_{auto}"> to autolyse for at least 1 hour, at most 2 hours. I then add the mature levain and mix by hand, folding and massaging everything together but not destroying the gluten network. Rest the dough for 30-40 minutes, and then add the salt (approximately 6g per 600g raw dough, see 'Good Practices' below). Again rest for 30 minutes following this. The next few hours consist of a series of (a) simple linear stretches, and/or (b) envelope folds, and/or (c) coil folds, and/or (d) other techniques which strengthen the gluten network and re-distribute heat. I typically do between 1 and 4 stretch & folds during this period. I then let the dough rest and bulk up (rise) for roughly 1-2 hours. Once the dough has bulked up by 30% of its volume, I weigh & cut the dough into the correct number of loaves, give each a pre-shape fold, and rest for 5-10 minutes. I then do a final shaping, transfer the doughs into metal mixing bowls, cover with plastic wrap (use a rubber band around the lip), and rest for 10-14 hours in the refrigerator.

On bake day, I pre-heat dutch ovens to 500F for 1 hour. I transfer cold loaves onto parchment paper, do a simple scoring with a sharp knife or 2-sided razor, and immediately transfer into the pre-heated Dutch oven. For my typical 600g loaves, there are 3 baking stages:
 - Stage 1: immediately reduce oven temperature to 450F. Bake with lid on, for 20 minutes.
 - Stage 2: Remove lid, bake for another 20 minutes.
 - Stage 3: Reduce heat to 425F, bake for 10 minutes.

Remove bread from the dutch oven, and let cool minimum 1 hour before cutting. Patience pays off handsomely here.

#### Caveats, clarifications, good practices

- I like to distinguish between *starter* and *levain*. My starter is my base sourdough culture, which I branch off when needed. This lives in my refrigerator, and is regularly removed for feeding. The levain is the yeast culture that is prepared for a specific bake, which begins from my starter, and is then fed on a regiment for a few days leading up to bake day. 

- Best practice is to define your salt weight as a percentage of un-fermented flour weight. Most sourdough preferences fall in the range 2.0% - 2.8%. For typical recipes, a 600g loaf will call for 6g-8g salt. My personal preference is to stick to the 2.0% mark. Use kosher salt, pink himalayan salt, but never iodized salt; the latter will suppress most of the essential fermentative chemistry.

- Vaporization will obviously occur during the baking process, resulting in a significant weight reduction for your sourdough. If you are targeting a specific final weight, expect 20% weight loss. The vaporization process is influenced by your baking vessel, your baking oven, the loaf geometry, the local temperature and humidity, etc. You will find higher vapor loss for loaves with larger ratios of surface area to volume, such as baguettes. 

- One tricky aspect of sourdough baking is determining baking times for loaves of a given weight. There is a simple scaling for this, where I use as a baseline the 3-stage, 50-minute bake time that's perfect for 600g loaves. Assuming linear thermal diffusion and roughly spherical loaf shapes, it's trivial to show that the correct baking time for a loaf of weight <img src="https://render.githubusercontent.com/render/math?math=W_*"> can be estimated by <img src="https://render.githubusercontent.com/render/math?math=t_*=t_{normal}(W_*/W)^{0.33}">, where <img src="https://render.githubusercontent.com/render/math?math=t_{normal}"> is the normal amount of time you bake your normal bread of weight <img src="https://render.githubusercontent.com/render/math?math=W">. In the discussions above, I have repeatedly used <img src="https://render.githubusercontent.com/render/math?math=W=600g"> and provided different values of <img src="https://render.githubusercontent.com/render/math?math=t_{normal}"> in the 3 baking stages (20 minutes, 20 minutes, 10 minutes). 

- In hot & humid summer weather, where my kitchen may be 82F with 80% humidity (mid-Atlantic), I often bake with <img src="https://render.githubusercontent.com/render/math?math=H=0.76"> and <img src="https://render.githubusercontent.com/render/math?math=C=0.10"> to avoid impossibly sticky dough (when <img src="https://render.githubusercontent.com/render/math?math=H"> is too high) and to guarantee a sensible rise time (yeast growth rates have strong, power-law dependence in the 78F-95F range, so I keep <img src="https://render.githubusercontent.com/render/math?math=C"> low). In the winter when the indoors temperature is ~62F, I typically utilize values <img src="https://render.githubusercontent.com/render/math?math=H=0.80, C=0.13"> to achieve the same results with a comparable rise time of 6-7hrs.

---

#### Personal recipes

My starter through 2018-2021 was always fed with 50% H2O + 50% flour mix. The flour mix was 90% bread flour (King Arthur Sir Galahad Artisan bread flour, to be specific) and 10% finely milled dark rye flour from my local Amish shop. This made for a robust and flexible base for whatever specific levain I chose to create for a specific bread batch. Recipes below were designed through many cycles of delicious iteration. 

I prefer to avoid listing separate "deep summer" and "deep winter" recipes for each style here. Refer to the comments above for some rough guidance.

**`New West'** 

This was my standard sourdough through 2020-2021. The levain flour percentages are:

* 50% bread flour
* 40% whole wheat flour (coarse)
* 5% organic spelt flour (coarse)
* 5% dark rye flour (fine)

For a 600g doughball (est. 500g baked) at <img src="https://render.githubusercontent.com/render/math?math=H=0.80"> and <img src="https://render.githubusercontent.com/render/math?math=C=0.11">, we have 

<img src="https://render.githubusercontent.com/render/math?math=f_{auto}=300g">

<img src="https://render.githubusercontent.com/render/math?math=h_{auto}=234g">

<img src="https://render.githubusercontent.com/render/math?math=L=66g">

The autolyse component uses a flour mix with the following percentages: 

* 80% bread flour
* 12% whole wheat flour (coarse)
* 8% organic spelt flour (coarse)

As usual, I use about 6g non-iodized salt for a typical 600g dough. I give these their signature crust of golden flax seeds before the cold ferment stage.

**`Winter Rye'**

A wonderfully rich, savoury, and deeply dark sourdough that I often make during the holidays. I start with a simple and sweet levain: 

* 80% bread flour
* 15% whole wheat flour (coarse)
* 5% dark rye flour (fine)

The goal is a loaf with elevated bitterness that balances with a spectrum of sweet. I like the earthyness of spelt for this, in addition to the normal dark rye. For the autolyse I use: 

* 80% bread flour
* 12% whole wheat flour (coarse)
* 4% organic spelt flour (coarse)
* 4% dark rye flour (fine)

As with most of my loaves, I use about 6g of non-iodized salt for a 600g dough weight. The magic of this loaf is the viscous, chocolately mixture I marble into the dough at the lamination stage. The mixture is:

* 35% dark brown sugar
* 24% dutch cocoa powder
* 29% blackstrap molasses
* 12% caraway seeds

The total weight I layer in the dough is about 5.7% of the total dough weight. For a 600g loaf, this comes out to a 34g batch of the above ingredient mix. Be systematic and gentle with the stretching & folding, and you'll be rewarded with a gorgeous marbling. 

**Banku sourdough**

Fermented corn slurry makes a remarkable infusion to an otherwise normal sourdough. Banku refers to the traditional fermented corn dough ubiquitous throughout West Africa. My use of the term 'Banku' in a sourdough context is a complete bastardization, and this practice (to my knowledge) has neither African nor Appalachian roots.

The corn ferment is usually ready after 24hrs at room temperature. To create it, mix 55% H2O and 45% yellow cornmeal, with a dash of cornstarch (0.5% by weight of total mix). Allow the mix to aerate. It should have a slightly sweet fermented smell when it's ready. I use a very simple white sourdough here to allow the nuanced sweet corn flavors to break through. 

I prefer the dough to have 10% banku, which is added at the lamination stage. This means that for a 650g doughball, I use <img src="https://render.githubusercontent.com/render/math?math=W_{solids}=29g"> and <img src="https://render.githubusercontent.com/render/math?math=h_{add}=36g">. Assuming 80% hydration and 12% inoculation, the equations yield:

<img src="https://render.githubusercontent.com/render/math?math=f_{auto}=303g">

<img src="https://render.githubusercontent.com/render/math?math=h_{auto}=203g">

<img src="https://render.githubusercontent.com/render/math?math=L=74g">


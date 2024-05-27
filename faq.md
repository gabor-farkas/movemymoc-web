# Frequenlty Asked Questions

## Why no Lego trees and baseplates?
They don't look good.

Lego trees have a layered structure, that looks nice in a Lego city setup, but when viewed from the side from a car's perspective, they are rather annoying.

The many studs on the baseplates would add a lot of geometry detail that would degrade the not-too-optimized performance of the game. If I let cars bump on them, then that would be annoying, if car wheels go through them, then that would look strange. If we use just a texture in place of actual stud geometry, it looks even stranger when viewed from a low angle.

Base plates also wouldn't play nicely with the free terrain editing available in the game.

## Will this be on mobile / console?
Not soon. Many of the game features aren't easily portable to a device that doesn't come with both a keyboard and a mouse. In the model configurator and the level designer screens there are so many options and control available that is tricky to adapt to a touchscreen in a really usable way.

Also, the main focus of the game is letting people import their models that were designed most likely in Bricklink Studio. This is possible most conveniently on a desktop, where Studio runs.

Having sad that, it could make sense to have a variant of the game that doesn't include the detailed model configurator and level designer screens, but just lets users select from already designed models and maps.

In the future, when Steam Workshop integration or some other mechanism will let users share their models and map in a central way, this could make more sense.

## How does it handle big models?
In short: don't plan import your full city models and multiple thousand-pieces detailed cars.

This of course depends on your computer's resources, but the game doesn't apply much optimization on the imported models. This will likely improve in the future, but please don't take this as a promise that the game would eventually handle millions of parts in a single scene.

In case you're concerned about performance before buying the game, please join our <a target="_blank" href="https://discord.gg/arPXtZ7U">discord</a> and check with other users how the game performs on a setup similar to yours.

## Why no consistent scale
The game lets you freely scale models up and down, between sane limits. There's no enforced, unified scale of imported models to the physical environment, so studs from one model can be of different size than studs from other models.

This is intentional. As LDraw models themselves model real-life vehicles in different scale ratios, the stud-width of a regular car can range from as low as 4 studs up to 30-40 studs.

We wanted to let these models interact in a physical environment that rather aligns with the model scale.

## Will there be model building inside the game?
Implementing model building and modifications in the game would quickly escalate to reimplementing nearly all functionality of Bricklink Studio. We'd like to avoid that.

A certain, limited functionality might be feasible, we'll have to find out what is a reasonable subset of features.

## Are all parts supported?
Kind of. Regarding pure geometry, the game bundles a relatively recent copy of the LDraw parts library. When importing LDraw files, this enables importing elements from this included library. ".io" files exported by Bricklink Studio contain a copy of all geometries as they were in the Studio library when the file was exported. The game will eventually support importing those part geometries bundled in the `.io` file, so that any part that's not yet available in the game bundle, or custom parts designed using the Bricklink Part Designer can also be imported.

There are some special kinds of parts that deserve separate attention:
* Linear actuators are available in the Studio library in a specific position, and it doesn't currently allow you to expand or retract them during the model build. You can build your models with these parts without fully connecting the expanding end to its desired connection point. When configuring the model mechanics in MoveMyMoc, you can specify the connection point and the actuator will be animated accordingly.
  * A similar solution will soon be supported for pneumatic actuator models
* Damper springs aren't currently supported in the game, but they are early in the roadmap. They will be supported similary to linear actuators: you don't need to fully position then in Studio, the ends can be configured to hinge to parts in MoveMyMoc, and the game will animate them accordingly.
* Things that aren't imported to the game
  * Bendable hoses and tubes - 
  * Rubber bands
  * Strings
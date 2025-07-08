![ElytraAeronautics](https://media.discordapp.net/attachments/754495868861677628/927260411785539604/ean2.png?width=1289&height=255)

# TLDR; What does this mod do??

This mod has three main features:
1. When flying with elytra, the player will fly faster the higher they fly (similar as in real life, where air density is lower at high altitudes, decreasing air drag).
2. Adds additional cloud layers indicating when fly speed starts to increase and when it ceases to increase, acting as a reference point for height and speed.
3. Features 1 and 2 are FULLY customizable: you can add and setup as many cloud layers as you want, and modify extra flight speed or disable it altogether.

Important: right now both ModMenu and ClothConfig are required to access to the configuration screen.

# More insight into the mod

## Elytra flying
![flyingme](https://media.discordapp.net/attachments/754495868861677628/927264908012302367/best2.png?width=1618&height=910)

If you are like me, a player who likes to explore the world, and travel very far away from the spawn to find unique generation and breathtaking landscapes to build your base and farms around, you might end up with your buildings spreaded across a 30,000-block-wide world.

The average player would be smart and link everything with a nether highway system. But I personally find elytra travelling very enjoyable, and for an endgame item which purpose is to specifically make travelling more convenient, it lacks utility when it is used in long-distance travel. 

The premise behind this mod is to make elytra travel more useful when covering large distances, making the player move at airplane speeds when flying at airplane heights.

When using Elytra Aeronautics with default settings, flight speed increases with altitude following this curve:

![speedcurve](https://user-images.githubusercontent.com/75187144/198856688-f716734b-ff60-4850-847e-042f12a3b725.png)

As you can see, there is no speed increment from y=0 to y=250. 
This is to not make low altitude flight go easily out of control, again, if you are like me and use the elytra to travel just 20 blocks across your base, you don't have to worry about reaching MACH5 when going for some potatoes. 

Beyond the 250 blocks of altitude mark, flight speed increases linearly up to its maximum at y=1000. At this altitude, cruise speed (what I call flight speed at a constant 0° angle to the ground) is around 250 block/second, matching commercial flight average speed.

## Keeping it vanilla
When developing a mod my intention is to make everything feel as vanilla as possible, since I make mods for myself that put in the game features that I feel are missing, to later use in my own survival worlds, this time I took a step further and published it.

When making this one I came across a problem: "How could I make some sort of altimeter and speedometer without adding fancy items or any GUI?", because some kind of guide is needed when flying far up from the ground, and using the debug (F3) screen is not very immersive.

After giving it some thought, I got an idea: using clouds as some kind of reference point for the player's vertical position.

By default, Elytra Aeronautics adds two additional cloud layers, one at the middle point of the speed curve (y=250) and another at the end of the speed curve (y=1000); 
these serve as an altitude marker like previously mentioned and as a speed marker, as these will appear moving faster relative to the player when travelling at high speeds.

This leads me to the second and third features of the mod, clouds and customization.

## Clouds and customization

Using the config screen you can add as many cloud layers as you wish, and use different cloud types and render distances for each layer individually.

![howdidwegethere](https://cdn.discordapp.com/attachments/754495868861677628/927174474787348530/2022-01-02_13.19.34.png)
_"How did we get here?"_

Furthermore, this mod adds "LOD clouds", these clouds will render as "Fast clouds" when far away from them, and as "Fancy clouds" when close to them.

![lodClouds](https://media.giphy.com/media/hCwDWDdtTeU153U37S/giphy.gif)

You can even make it so when a cloud layer is far away enough from the player it stops rendering, so you can set up hundreds of cloud layers and lose almost no performance.

![cloudLayers](https://media.giphy.com/media/gELjxjYdTz1zCViEsU/giphy-downsized-large.gif)

As previously mentioned you can either configure each layer individually, or all of them at once, providing full access to the additional cloud functionality of the mod.

![cloudconfigscreen](https://media.discordapp.net/attachments/754495868861677628/927180129971601448/unknown.png?width=1290&height=701)

## Integration
- [ModMenu](https://modrinth.com/mod/modmenu) -> required to access config screen.
- [ClothConfig](https://modrinth.com/mod/cloth-config) -> required to build config screen.

(Expect ModMenu not being a mandatory requirement for accesing the config screen in a future version)

## Known Issues
- There might be a way to harness infinite altitude when working with very high speeds.
- Firework rockets reset your flight speed to max vanilla speed.
- Very minor issues with cloud rendering.
- For 1.19+ versions, cloud configuration does not work compleately as intended, I'll be fixing it as soon as I have some time; default configuration works perfectly though. And you can still get around some of the current issues with some clever tweaking.

**For multiplayer:**

- When playing on a server, setting the gamerule 'disableElytraMovementCheck' to true helps with jittering and position inconsistency.

## Future development
- Expect the mod to be ported to future versions.
- I'll try to get rid of all big and medium sized issues before I add more content, but due to my tight schedule, I may not be able to publish next hotfix until winter holidays.
- Expansion updates are planned but these might take longer to be released.

## F.A.Q.

___Will this ever be ported to Forge?___

Nope, sorry I don't work with Forge and most likely never will.

___Can I port it to Forge?___

Yes, you can, but you have to respect the mod's license and credit the original work.

___Will this mod be ever ported to an older version?___

Right now, I can **almost** assure you that I won't, **but**, if I see a lot of people requesting it, I might make a single version for each of the most requested older MC versions.

## Support

You can support me by simply downloading the mod and sharing it with friends! 

## GITHUB PAGE BONUS: Real example
Wood land Mansions can easily be more than 20k blocks away from the spawn, sometimes even 50k blocks in large biomes worlds. 

This is a real seed (-962156719158439332, generated in MC 1.16.5) and the nearest mansion is 21898 blocks away.

![examplepic](https://cdn.discordapp.com/attachments/754495868861677628/927030132806418512/example2.png)
_Picture made using [Admist](https://github.com/toolbox4minecraft/amidst)._

![examplescreenshot](https://cdn.discordapp.com/attachments/754495868861677628/927025278998437908/unknown.png)
Taking the closest mansion from spawn (at 21898 blocks of distance) as an example:

The maximum flight speed with elytra in Vanilla Minecraft is around 60 blocks/second, that is when travelling at a 45° angle to the ground, it would take around 6 minutes to travel that distance.

When using Elytra Aeronautics with default settings, flight speed can reach 250 blocks/second when travelling parallel to the horizon, and 500 blocks/seconds when flying at a 45° angle. At horizontal speed it would take 1:27 minutes to travel that distance, and at maximum speed, it would just take 43 seconds to reach the mansion.

Remember, this is using default settings, maximum flight speed can be increased or decreased.

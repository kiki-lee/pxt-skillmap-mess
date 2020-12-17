# Space Explorer

## Introduction @unplugged

Let's explore the depths of space! 

In this tutorial, you'll design a spaceship for your journey.

![Flying through space](/img/space/space1.gif "Blasting through a starfield" )

## Set the scene
Let's give 'em something to look at 🔭
<hr/>

🔲 Drag the ``||scene:start screen [confetti] effect ⊕||`` from the  ``||scene:Scene||`` category and
into the ``||loops:on start||`` block that's already in the workspace.

🔲 Next, select ``||scene:star field||`` (instead of ``||scene:confetti||``) from the dropdown
and watch as you blast into space! 🚀 

<hr/>

```blocks
// @highlight
effects.starField.startScreenEffect()
```

## Draw your ship
Time to choose our ship!
<hr/>
🔲 From the ``||sprites:Sprites||`` category, drag the ``||variables:set [mySprite] to sprite [ ] of kind [Player]||`` 
block  and place it at the end of the ``||loops:on start||`` container.

🔲 Click on the grey box in the middle of your
 ``||variables:set [mySprite] to sprite [ ] of kind [Player]||`` block
to design a ship of your own! Are you a rusty pile of scraps or a sleek, futuristic rocket?
<hr/>
>>*Tip: Don't feel like drawing your ship? Once you're in the sprite editor,
flip to the gallery and choose from premade images.*

```blocks
effects.starField.startScreenEffect()
// @highlight
let mySprite = sprites.create(img`
    . . . . . . . 9 9 . . . . . . .
    . . . . . . 9 . . 9 . . . . . .
    . . . . . . 9 . . 9 . . . . . .
    . . . . . 9 . 9 9 . 9 . . . . .
    . . . . . 9 . 9 9 . 9 . . . . .
    . . . . 9 . 9 9 9 9 . 9 . . . .
    . . . . 9 . 9 9 9 9 . 9 . . . .
    . . . 9 . 9 9 9 9 9 9 . 9 . . .
    . . . 9 . 9 . . . . 9 . 9 . . .
    . . 9 . 9 9 . 9 9 . 9 9 . 9 . .
    . . 9 . 9 9 . . . . 9 9 . 9 . .
    . 9 . 9 9 9 . 9 9 9 9 9 9 . 9 .
    . 9 . 9 9 9 . 9 9 9 9 9 9 . 9 .
    9 . 9 9 9 9 9 9 9 9 9 9 9 9 . 9
    9 . . . . . . . . . . . . . . 9
    9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
`, SpriteKind.Player)
```

## Control your ship

🌟 Let's get your ship moving 🌟

Find the ``||controller:move [mySprite] with buttons ⊕||`` block 
and drag it into the bottom of the ``||loops:on start||`` container. 

Now your ship will move with the joystick or the WASD keys.
Try moving your ship around in the simulator!

```blocks
effects.starField.startScreenEffect()
let mySprite = sprites.create(img`
    . . . . . . . 9 9 . . . . . . .
    . . . . . . 9 . . 9 . . . . . .
    . . . . . . 9 . . 9 . . . . . .
    . . . . . 9 . 9 9 . 9 . . . . .
    . . . . . 9 . 9 9 . 9 . . . . .
    . . . . 9 . 9 9 9 9 . 9 . . . .
    . . . . 9 . 9 9 9 9 . 9 . . . .
    . . . 9 . 9 9 9 9 9 9 . 9 . . .
    . . . 9 . 9 . . . . 9 . 9 . . .
    . . 9 . 9 9 . 9 9 . 9 9 . 9 . .
    . . 9 . 9 9 . . . . 9 9 . 9 . .
    . 9 . 9 9 9 . 9 9 9 9 9 9 . 9 .
    . 9 . 9 9 9 . 9 9 9 9 9 9 . 9 .
    9 . 9 9 9 9 9 9 9 9 9 9 9 9 . 9
    9 . . . . . . . . . . . . . . 9
    9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
`, SpriteKind.Player)
// @highlight
controller.moveSprite(mySprite)
```

## Stay in screen

**Uh-oh, if you move off screen, your ship disappears!**
<hr/>
To keep your ship from exploring beyond the edges, find
 the ``||sprites:set [mySprite] [stay in screen] <off>||`` block and
snap it in at the end of the program.
 
Toggle the switch to **`<ON`>** to keep the action on screen.
<hr/>
 **You're all set to travel the universe!**

```blocks
effects.starField.startScreenEffect()
let mySprite = sprites.create(img`
    . . . . . . . 9 9 . . . . . . .
    . . . . . . 9 . . 9 . . . . . .
    . . . . . . 9 . . 9 . . . . . .
    . . . . . 9 . 9 9 . 9 . . . . .
    . . . . . 9 . 9 9 . 9 . . . . .
    . . . . 9 . 9 9 9 9 . 9 . . . .
    . . . . 9 . 9 9 9 9 . 9 . . . .
    . . . 9 . 9 9 9 9 9 9 . 9 . . .
    . . . 9 . 9 . . . . 9 . 9 . . .
    . . 9 . 9 9 . 9 9 . 9 9 . 9 . .
    . . 9 . 9 9 . . . . 9 9 . 9 . .
    . 9 . 9 9 9 . 9 9 9 9 9 9 . 9 .
    . 9 . 9 9 9 . 9 9 9 9 9 9 . 9 .
    9 . 9 9 9 9 9 9 9 9 9 9 9 9 . 9
    9 . . . . . . . . . . . . . . 9
    9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
`, SpriteKind.Player)
controller.moveSprite(mySprite)
// @highlight
mySprite.setFlag(SpriteFlag.StayInScreen, true)
```

---
layout: post
title:  "Fortblox: Animation Blending"
date:   2012-08-02 00:00:04 +0000
categories: fortblox
---
I have recently implemented additive skeletal animation blending to Fortblox. Skeletal animations are the obvious choice for games as they can be efficiently accelerated on the GPU and enable effects such as rag-doll physics. Additive animations enable multiple sets of character animations to be played back over the top of each other, for example an injured animation may be combined with a walk animation, to create an injured-walk animation.

To perform additive blending the difference between an animation and base pose must be calculated. A set of difference animations can then be added back onto the original pose to calculate the object's final pose. Because the animations are specified relative to a base frame it also allows animations to easily be blended on and off by multiplying the difference with a contribution factor.

[![YT Fortblox Animation Blending](https://img.youtube.com/vi/zxqWnp8Fljg/0.jpg)](https://www.youtube.com/watch?v=zxqWnp8Fljg)

In the first part of the video you can see how the blending factors control each animation's contribution to the final pose. For demonstration I am blending the hand open and close animation while also playing back a walk cycle. This will enable us to flexibly combine shooting animations with walking, jumping and taking damage states.

In the second half of the video you can see a progress update on the multiplayer game so far. Of course all assets are placeholder at this point. The character model is Sinbad, the mascot for the open source Ogre3D project. Although that engine is not being used here the asset is a convenient placeholder due to the large amount of skeletal animation sets already available.

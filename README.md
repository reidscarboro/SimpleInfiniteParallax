# SimpleInfiniteParallax
Simple infinite scrolling parallax for Unity2D with moving camera

This is a super simple script that will handle infinite scrolling parallax backgrounds for Unity2D with a moving orthographic camera. It requires a single tileable sprite. Please bear in mind that I am a total Unity novice, so it is very possible/likely there is a better way to do all of this, this is just my solution.

In short, the script will take an object with a SpriteRenderer, create 4 instances in a square, and keep their positions updated relative to the moving camera to create the parallax effect.

Demo: https://youtu.be/DSN6_Ez38-A

Usage:
* Create an object with a SpriteRenderer that is your background, ensure it is larger than your camera viewport.
* Create an empty object, attach the SimpleInfiniteParallax.cs script.
* Set your camera as the "parent."
* Set your newly created object with SpriteRenderer as "layerSprite."
* Set the depth.
    *   < 0   :layerSprite moves as foreground
    *   0     :layerSprite remains stationary
    *   0-1   :Standard parallax behavior
    *   1     :layerSprite moves perfectly with "parent" object. (Same as setting background as child of camera)
    *   > 1   :layerSprite appears to move faster than everything else, probably don't use this one...

Do let me know if you have any questions/suggestions!

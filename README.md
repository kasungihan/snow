## Season Snow Effect

# Usage
```html
<script src="path/snowstorm.js"></script>
```

```js
<script>
	snowStorm.startSeason();
</script>
```


# Extend Plugin

 - This plugin I extend for easy to put script 

http://www.schillmania.com/projects/snowstorm/

snowStorm.autoStart = true;
- Whether the snow should start automatically or not.

snowStorm.animationInterval = 33;
- Theoretical "milliseconds per frame" measurement. 20 = fast + smooth, but high CPU use. 50 = more conservative, but slower

snowStorm.flakeBottom = null;
- Limits the "floor" (pixels) of the snow. If unspecified, snow will "stick" to the bottom of the browser window and persists through browser resize/scrolling.

snowStorm.flakesMax = 128;
- Sets the maximum number of snowflakes that can exist on the screen at any given time.

snowStorm.flakesMaxActive = 64;
- Sets the limit of "falling" snowflakes (ie. moving on the screen, thus considered to be active.)

snowStorm.followMouse = true;
- Allows snow to move dynamically with the "wind", relative to the mouse's X (left/right) coordinates.

snowStorm.freezeOnBlur = true;
- Stops the snow effect when the browser window goes out of focus, eg., user is in another tab. Saves CPU, nicer to user.

snowStorm.snowColor = '#fff';
- Don't eat (or use?) yellow snow.

snowStorm.snowCharacter = '•';
- &bull; (•) = bullet. &middot; entity (·) is not used as it's square on some systems etc. Changing this may result in cropping of the character and may require flakeWidth/flakeHeight changes, so be careful.

snowStorm.snowStick = true;
- Allows the snow to "stick" to the bottom of the window. When off, snow will never sit at the bottom.

snowStorm.targetElement = null;
- An HTML element which snow will be appended to (default: document body.) Can be an element ID string eg. 'myDiv', or a DOM node reference. See relative and absolute-positioned examples.

snowStorm.useMeltEffect = true;
- When recycling fallen snow (or rarely, when falling), have it "melt" and fade out if browser supports it

snowStorm.useTwinkleEffect = true;
- Allow snow to randomly "flicker" in and out of view while falling

snowStorm.usePositionFixed = false;
- true = snow not affected by window scroll. may increase CPU load, disabled by default - if enabled, used only where supported.

snowStorm.vMaxX = 8;
snowStorm.vMaxY = 5;
- Defines maximum X and Y velocities for the storm; a random value in this range is selected for each snowflake.

# Methods
- Snowstorm has a few basic methods for controlling the snow effect.
snowStorm.randomizeWind()

- Sets the wind speed with a random value relative to vMaxX and vMaxY properties.
snowStorm.freeze()

- Stops the snow effect in place.
snowStorm.resume()

- Continues snowing from a "frozen" state.
snowStorm.toggleSnow()

- Enables or disables the snow effect depending on state, same as calling freeze() or resume().
snowStorm.stop()

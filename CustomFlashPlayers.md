# Custom Flash players #

The **html5media** project comes bundled with [Flowplayer](http://www.flowplayer.org), an open source Flash video and audio player. We chose this player because it does a very good job of emulating a HTML5 video tag.

There are times when you might want to customise the appearance or behaviour of the fallback Flash player, or even use a different Flash player entirely. In this case, simply insert the following code underneath your **html5media** declaration:

```
<script>
    html5media.createFallback = function(tagName, element) {
        // Your own player code here.
    }
</script>
```

It is your responsibility to correctly read the attributes of the video or audio tag and emulate them in the custom player. Once the custom player has been created, replace the original tag with the custom player using the following syntax:

```
video.parentNode.replaceChild(replacement, element);
```
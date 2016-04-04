# Hosting your own html5media #

If you don't trust Google Code to host the files used by **html5media**, then don't worry. Simply [checkout](http://code.google.com/p/html5media/source/checkout) the code and copy the contents of the `src` folder onto your own webserver. You can then link to your own copy rather than the one hosted on Google Code.

If you keep all the **html5media** files in the same folder, and it should all work just fine. If you move the `flowplayer.swf`, `flowplayer.audio.swf` and `flowplayer.controls.swf` files to another location, then you'll need to tell **html5media** where they are using the following javascript commands:

```
html5media.flowplayerSwf = "/path/to/your/flowplayer.swf";
html5media.flowplayerAudioSwf = "/path/to/your/flowplayer.audio.swf";
html5media.flowplayerControlsSwf = "/path/to/your/flowplayer.controls.swf";
```

These commands should be inserted in your page after the **html5media** script tag.
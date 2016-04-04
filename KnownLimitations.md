# Known limitations #

For the vast majority of uses, **html5media** will just work out of the box with no complications. However, if you intend to do more advanced work using HTML5 video and audio tags, read on...

## Dynamically inserted video and audio tags ##

The **html5media** script is run automatically when your page loads. However, if you use Javascript to create your own HTML5 video tags dynamically, these might not be caught by the script.

To ensure that dynamically-inserted tags are usable in all browsers, you must run the following line of code whenever you've finished inserting video and audio tags.

```
html5media();
```

## Audio tag preloading ##

Due to a bug in Flowplayer, audio tags will currently ignore the `preload` attribute and always act as is preloading was disabled. We're currently waiting for this bug to be fixed, at which point **html5media** will be updated accordingly.

## No support for scripting ##

Because some browsers will have their video and audio tags replaced with Flash players, if you try to call [HTMLMediaElement](http://www.whatwg.org/specs/web-apps/current-work/multipage/video.html#htmlmediaelement) javascript methods on the video tag then it won't work in all browsers.

It would be lovely if **html5media** could set up these fallback Flash players with an emulated javascript API. Maybe one day I'll do just this. Until then, I'm just a human, and have to sleep sometimes!
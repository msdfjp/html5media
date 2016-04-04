# Poster Images #

It is highly recommended that you add a splash image to all your video tags. This gives people something to see while the rest of the video downloads. Simply use the poster attribute as follows:

```
<video src="video.mp4" width="320" height="240" poster="image.jpg" controls preload></video>
```

For consistent behaviour between browsers, the poster image should be taken from the first frame of the video.

## What do you mean, consistant behaviour? ##

Unfortunately, different browsers interpret the poster attribute in different ways. Firefox and Opera will show this image to the user until they press the play button, whereas Chrome and Safari will _instantly_ replace the image with the first frame of the video as it loads.

There's a [bit of a debate](http://daringfireball.net/2009/12/html5_video_unusable) going on about this at the moment. As far as I'm aware, Firefox are Opera are currently the only browsers that are handling this attribute correctly. Chrome and Safari should really fall into line on this one, as it's going to make some people unwilling to adopt HTML5 video.

## How do I capture the first frame of a video? ##

The easiest way to capture the first frame of a video is to take a screenshot. It's crude, but it works. Alternatively, you can download and install the free [FFmpeg](http://ffmpeg.org/) tool, then run this command in a terminal:

```
ffmpeg  -ss 0 -i video.mp4 -f image2 -vframes 1 poster.jpg
```

Getting FFmpeg installed can be a bit of a nightmare. Unless you're going to be processing a lot of videos, it's probably best to stick with screenshots.
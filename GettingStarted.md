# Getting started #

To enable HTML5 video tags in all major browsers, simply paste the following code into the `<head>` of your document:

```
<script src="http://html5media.googlecode.com/svn/trunk/src/html5media.min.js"></script>
```

## Video tag syntax ##

HTML5 video tags can be embedded using the following syntax:

```
<video src="video.mp4" width="320" height="240" controls preload></video>
```

You can control the behaviour of the video by including the following optional attributes:

  * **controls** - Add a set of controls to the video.
  * **preload** - Start downloading the video automatically.
  * **autoplay** - Start playing the video automatically.
  * **loop** - Keep playing the video in a loop.

## Adding a splash image ##

It is highly recommended that you add a splash image to all your video tags. This gives people something to see while the rest of the video downloads. Simply use the `poster` attribute as follows:

```
<video src="video.mp4" width="320" height="240" poster="image.jpg" controls preload></video>
```

For consistent behaviour between browsers, the poster image should be taken from the first frame of the video. See PosterImages for more information.

## Audio tag syntax ##

HTML5 audio tags can be embedded using the following syntax:

```
<audio src="video.mp4" controls preload></audio>
```

They can be customised using the `controls`, `preload`, `autoplay` and `loop` attributes, as above.

## Styling video and audio tags ##

It is important not to directly style the video and audio tags in your document using CSS. This is because browsers that do not support these tags will have them replaced by a [Flash video player](http://www.flowplayer.org).

To style your video and audio tags using CSS, simply assign them a `class` or an `id`, and attach CSS style rules to that. The replacement Flash player will have the same `id` and `class` as the original tag, so will pick up the same style rules.
# Video formats #

For your videos to work with **html5media**, they must be saved as mp4 files using the **h.264** codec. This video format is a widely-accepted standard on the internet, and is the same format that is used by [YouTube](http://www.youtube.com) and [iTunes](http://www.apple.com/itunes/).

You can save your videos as h.264 files using the following free programs:

  * [Handbrake](http://handbrake.fr/) - All platforms
  * [ffmpegX](http://www.ffmpegx.com/) - Mac OSX only

## Help! I have to wait for my entire video to download before it plays! ##

This is a common problem, and means that your movie file has been incorrectly saved with metadata at the end of the file. You can fix this using the following free program:

  * [QTIndexSwapper](http://renaun.com/air/QTIndexSwapper.air)

## What about Theora? ##

[Theora](http://www.theora.org/) is an open source video codec that has been proposed the standard video encoding to be used on the web. It's advantage over h.264 is that it's royalty-free, and unencumbered by patents. Open source web browsers, such as [Firefox](http://www.firefox.com), can therefore include this codec for free.

If you want to use Theora videos in your page, then you need to do a bit more work. You will first need to create two versions of your video file. One version needs to be saved as h.264, the other as Theora. You then embed the videos in your page using an extended video tag syntax:

```
<video class="video" poster="cat.jpg" width="352" height="264" controls preload>
    <source src="cat.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'></source>
    <source src="cat.ogv" type='video/ogg; codecs="theora, vorbis"'></source>
</video>
```

Providing a Theora version of your video will allow Firefox and Opera to use a HTML5 video player. If you do not provide a Theora version, then Firefox and Opera will fall back to using a Flash video player.

You can convert your h.264 files to Theora using the following free tool:

  * [Firefogg](http://firefogg.org/)

## Help! Firefox won't play my Theora video! ##

Firefox will only be able to play Theora files if they are served using the correct content type of 'video/ogg'. Not all web servers recognise Theora files, and serve them as binary files. You can force Apache to serve Theora files correctly by adding the following line to your server configuration or .htaccess file:

```
AddType video/ogg .ogv
```
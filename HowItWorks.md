# How it works #

The **html5media** script scans your page for video tags, and checks whether your browser is capable of playing the files they contain using a HTML5 media player. If the browser can play the contents of the video tags, then the script does nothing.

If your browser does not support HTML5 video, then the offending video tags are dynamically replaced with a [Flowplayer](http://flowplayer.org/) instance, providing the same functionality as the original video tag.

The **html5video** script supports both h.264 (mp4) and Theora (ogv) video files. Read more about this on our VideoFormats page.
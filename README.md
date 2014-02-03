Video.js - Youtube Video Wall
=========================
Display videowall that contain youtube related videos, on the end of the video.

![Youtube Videowall screenchost](https://raw2.github.com/several27/videojs-youtube-videowall/master/screenshot.png)

## How does it work
Plugin detects youtube video id, then download related video list from gdata.youtube.com, parse it and display as images on the end of video. When user clicks on thumbnail, script changes player source to new video and play it.

## Getting Started
Download [videojs](http://www.videojs.com/) and [videojs-youtube](https://github.com/eXon/videojs-youtube)

In your web page:
```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" type="text/css" href="http://vjs.zencdn.net/4.2/video-js.css">
	<link rel="stylesheet" type="text/css" href="videojs.youtubeVideowall.css">
</head>
<body>
	<video id="video" class="video-js vjs-default-skin" controls preload="auto" width="640" height="360"> </video>

	<script type="text/javascript" src="http://vjs.zencdn.net/4.2/video.js"></script>
	<script type="text/javascript" src="vjs.youtube.min.js"></script>
	<script type="text/javascript" src="videojs.youtubeVideowall.js"></script>
	<script type="text/javascript">
		videojs('video', {'techOrder': ['youtube'], 'src': 'http://www.youtube.com/watch?v=E63MXHrhqHw'}, function() 
			{
				this.youtubeVideowall();			
			});
	</script>
</body>
</html>
```

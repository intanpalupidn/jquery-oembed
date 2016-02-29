# About #

A simple jQuery plugin that uses OEmbed API to help displaying embedded content (such as photos or videos) in your website.

## Quick explicit example ##


```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
        <title>jquery-oembed explicit insert example</title>
        <meta http-equiv="content-type" content="text/html; charset=utf-8"/>    
        <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.3.2/jquery.min.js"></script>  
        <script type="text/javascript" src="jquery.oembed.js"></script>
</head>
<body>
<script type="text/javascript">
        $(document).ready(function() {
                $("#container").oembed("http://www.flickr.com/photos/14516334@N00/345009210/");
        });
</script>
<div id="container"></div>
</body>
</html>
```

In this example the div#container will display the photo from flickr.

## Quick implicit example ##


```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
	<title>jquery-oembed link replace example</title>
	<meta http-equiv="content-type" content="text/html; charset=utf-8"/>   
        <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.3.2/jquery.min.js"></script>  
        <script type="text/javascript" src="jquery.oembed.js"></script>
</head>
<body>
<script type="text/javascript">
        $(document).ready(function() {
                $("a.oembed").oembed();
        });
</script>
<div><a href="http://www.flickr.com/photos/14516334@N00/345009210/" class="oembed">Flickr Image</a></div>
<div><a href="http://vimeo.com/3108686" class="oembed">Vimeo Video</a></div>
</body>
</html>
```

In this example the jquery plugin will embed the flickr photo and the vimeo video inside the links.

## Configuring multiple providers example ##


```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
	<title>jquery-oembed multiple providers example</title>
	<meta http-equiv="content-type" content="text/html; charset=utf-8"/>    
	<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.3.2/jquery.min.js"></script>  
	<script type="text/javascript" src="jquery.oembed.js"></script>
</head>
<body>
<script type="text/javascript">
	$(document).ready(function() {
		$(".oembed").oembed(null, 
			{
			embedMethod: "append", 
			maxWidth: 1024,
			maxHeight: 768,
			vimeo: { autoplay: true, maxWidth: 200, maxHeight: 200}			
			});
	});
</script>
<div><a href="http://vimeo.com/3108686" class="oembed">Vimeo Video</a></div>
<div><a href="http://www.flickr.com/photos/14516334@N00/345009210/" class="oembed">Flickr Image</a></div>
</body>
</html>
```

In this example the jquery plugin will append the flickr photo and the vimeo video after the links. For vimeo, we are giving a particular configuration.

## Supported OEmbed providers ##
  * 5min
  * Amazon Product Images
  * Flickr
  * Google Video
  * Hulu
  * Imdb
  * Metacafe
  * Myspace Videos
  * Qik
  * [Revision3](https://code.google.com/p/jquery-oembed/source/detail?r=3)
  * Screenr
  * Slideshare
  * Twitpic
  * Viddler
  * Vimeo
  * Wikipedia
  * WordPress
  * YouTube

This javascript plugin relays in 'jsonp', so only oEmbed providers that support callback methods are directly implemented.

Any other oEmbed provider uses [oohembed.com](http://www.oohembed.com) service. Thank you oohembed.com!



---

This is my first public jQuery plugin. Any comments or improvements are really welcome.

Richard Chamorro

Avanzis

http://www.avanzis.com

NETEYE Touch-Gallery
====================

Touch-devices like the iPad are almost perfect for viewing images and flicking through photo albums.

While native applications like Apple's Photos app feel incredibly natural and are fun to use,
the photo-viewing experience on websites is usually far behind. The often used lightbox pattern
simply doesn't work that well on touch-screens as it does on the desktop. 

We've therefore written a jQuery plugin that leverages modern web technologies to re-create the
user experience of native photo apps within the browser.

You can flick through the images with your fingers and thanks to WebKit's hardware accelerated
CSS transitions all animations are just as smooth as in a native app.

The full-screen images are always perfectly centered, no matter whether the page is zoomed or 
scrolled. And if you rotate the device, the image is re-positioned and re-scaled for a perfect fit.

Despite its name the plugin works on desktop browsers, too (see the list below). We didn't want to
create yet another lightbox library, so you won't find any extra UI-elements to navigate through
the images with the mouse.

Supported Browsers
------------------

The plugin was written and optimized for Mobile Safari running on the iPad or iPhone 4.
It also runs in Dektop Safari, Firefox 4, as well as in Opera and Chrome.

The gallery is also viewable in older Firefox versions and Internet Explorer, but the 
transition effects are missing.

Dependencies
------------

NETEYE Touch Gallery depends on two other plugins that are also part of the NETEYE Plugin 
Collection: [transform](/transform.html) and [activity-indicator](/activity-indicator.html).
When you download this plugin as distribution archive, you get an all-in-one JavaScript file
that contains all required files.

The plugin requires jQuery v1.4.2 (or higher).

Usage
-----

<div class="liquid highlight html"></div>

    <div id="gallery">
      <a href="image1.jpg">
        <img src="thumb1.jpg" />
      </a>
      <a href="image2.jpg">
        <img src="thumb2.jpg" />
      </a>
      <a href="image3.jpg">
        <img src="thumb3.jpg" />
      </a>
    </div>
	
    <script>
      $('#gallery a').touchGallery();
    </script>

<div class="liquid endhighlight"></div>
	
By default the plugin uses the `href` attribute of the matched elements to obtain the URL of the
large-scale images. You may change this behaviour by providing a `getSource` function:

<div class="liquid highlight html+javascript"></div>

    <img src="thumb1.jpg" data-large="image1.jpg" />
    <img src="thumb2.jpg" data-large="image2.jpg" />
    <img src="thumb3.jpg"  data-large="image3.jpg" />
    
    <script>
      $('img[data-large]').touchGallery({
        getSource: function() { 
          return $(this).attr('data-large');
        }
      });
    </script>

<div class="liquid endhighlight"></div>
  
Links
-----

* Author:  [Felix Gnass](http://github.com/fgnass)
* Company: [NETEYE](http://neteye.de)
* License: [MIT](http://neteye.github.com/MIT-LICENSE.txt)
* Demo:    http://neteye.github.com/touch-gallery.html

Please use the GitHub issue tracker for bug reports and feature requests.



The "Wolfram" template documentation by Yevgeny S. v1.1.1



Wolfram
=======

Created: 18/08/2014

By: Yevgeny Simzikov

URL: http://simpleqode.com/

Email: yevgenysim@yandex.ru

Description
-----------

Wolfram is a creative one page template professionally handcrafted to meet the needs of novice developers and experts alike. You don't need to have any special knowledge to set it up and adjust for your needs. 

Built with Twitter Bootstrap, it combines all of its great features with our clean user-friendly layout. Fully responsive, it looks perfect on all major browsers, tablets and phones. 

Advanced customizability and attention to details will help you get your own website up and running in no time. Feel free to visit the preview page or contact us if you have any questions.

Key features
------------

 - Fully functioning PHP contact form with spam protection (powered by Google reCaptcha) (NEW!)
 - 6 website color options
 - 4 navbar color options
 - 2 menu types (top navbar menu and sidebar menu)
 - 3 background patterns
 - Fully responsive design
 - Built with LESS

Current release is v1.1. Buying this template now you become eligible to free download all of its future updates. Please contact us for more info.





Basic Structure
===============

We used HTML5, CSS3, LESS, jQuery and PHP to create this template. 

1) HTML Structure
-----------------

This template is a responsive layout divided into separate "screens" (e.g. Welcome screen, About screen, Portfolio screen, etc.). Each screen content is wrapped into:

    <div class="site-wrapper screen" id="...">
        <div class="site-wrapper__inner">
            ...
        </div>
    </div>
    
It makes each screen height 100% of the viewport height, then centers its content vertically on small, medium and large devices, and aligns it to the top on extra small devices (mobile screens). 

General Bootstrap grid system is used for containers, rows and columns. 

2) CSS Files
------------

This template imports 3 .css files: 

 - style.css
 
This is the main .css file where all .less files are compiled into. It contains all the general Bootstrap styles and template custom styles (including general styles, elements styles and color options). 

 - animate.css

This is a CSS animations library.

 - lightbox.css

This file contains styles required for the Lightbox plugin used in the Portfolio section.

3) LESS Files
-------------

There are 3 .less files included into this package:

 - style.less

This is the main .less file where all the other .less files (including those from the original Bootstrap package) are imported into. It contains general styles for the template appearance. This is the only .less file you need to compile to style.css in case any changes are made.

 - element.less 

This file contains modifications to the original Bootstrap elements (e.g. navbar, carousel, buttons, etc.).

 - global.less

This file contains helper classes and global variables along with color option classes.

4) JS Files
-----------

This template imports 11 .js files: 

 - bootstrap.js, bootstrap.min.js

General Bootstrap jQuery plugins.

 - custom.js

Template custom plugins. You can use this file to add your own .js snippets to this template.
You need to edit this file in case you want to add new images to the carousel or change images path.

 - jquery.backstretch.js, jquery.backstretch.min.js

Background image carousel.

 - lightbox.js, lightbox.min.js

Lightbox preview plugin required for Portfolio images.

 - scrolltopcontrol.js

Plugin, required for scrolling the page smoothly to the top.

 - waypoints.js, waypoints.min.js

This plugin is required to know when the center of a "screen" hits the top of the viewport to change the background image accordingly.

 - contact.js

Animates the contact form, e.g. shows erros messages when some of the fields are not filled and shows the alert message when a new email is sent successfully.

5) PHP Files
------------

This package contains 2 custom PHP files and a /recaptcha folder for Google reCaptcha.

 - config.php

Contains key information for the contact form setup. Please read more about it below. 

 - sendmail.php

Is required for your contact form to work properly.





General Instructions
====================

You can easily customize this template to fit your needs by changing the general color scheme, navbar color scheme, menu type and background pattern: 

Changing general color scheme
-----------------------------

The following color schemes are available: 

 - Sun scheme (global-color_sun)
 - Confetti scheme (global-color_confetti)
 - Picton blue scheme (global-color_picton-blue)
 - Yellow scheme (global-color_yellow)
 - Bittersweet scheme (global-color_bittersweet)
 - Basic scheme (none)

The default color scheme is "Sun". To change your color scheme, please go to the index.html file and replace the "global-color_sun" class of the body container with "global-color_confetti", 'global-color_picton-blue" or any other color scheme class from the list above. Remove any of the above classes to stick with the basic white color scheme.

Changing navbar color scheme
----------------------------

The following navbar color schemes are available: 

 - Navbar default (white)
 - Navbar inverse (black)
 - Navbar default faded (semi-transparent)
 - Navbar inverse faded (semi-transparent)

The default navbar color scheme is "Navbar inverse faded". To change your navbar color scheme, please go to the index.html file and replace the original "navbar-inverse" class with "navbar-default". Remove the "navbar-faded" class if you don't want your navigation panel to be semi-transparent. 

Attention: Do not remove the "navbar-transparent" class. It makes the navigation panel transparent on the first "screen", smoothly fading back as you scroll down.

Attention: "navbar-faded" class is automatically removed on extra small screens (mobile devices).

Changing menu type
-------------------

The following menu types are available: 

 - Top navbar menu
 - Sidebar menu

The default menu type is "Top navbar menu". If you want to switch to the "Sidebar menu", please follow these simple steps below: 

1. Go to the index.html file and add the "hidden" class to the "navbar" container.
2. Go to the index.html file and remove the "hidden" class from the "sidebar-btn" container. 

Changing background pattern:
----------------------------

The following background patterns are available:
 
 - Vertical stripes (bg-pattern_vertical)
 - Horizontal stripes (bg-pattern_vertical)
 - Semi-transparent (none)

The default background pattern is "Vertical stripes". To change the default background pattern, please go to the index.html file and replace the "bg-pattern_vertical" class in the "bg-pattern" container with "bg-pattern_horizontal". Remove those classes to make the background semi-transparent.





Setting up the Contact Form
===========================

This template contains a fully functioning PHP contact form with spam protection powered by Google reCaptcha. 

Note: The contact form will not work in your local environment without a server that supports PHP. 

In order to set up the contact form, please follow the steps below: 

1. Open the config.php file and fill out the required information: 

 - reCaptcha Public ($publickey) and Private ($privatekey) keys.
 These keys are required to make your reCaptcha work properly. Please go to https://www.google.com/recaptcha/admin/create if you don't have the keys yet.

 - Sender name and email address ($mail_sender)
 This is a name and email address you will see in the From: line of new emails you will receive.

 - Your email address ($to_email)
 This is an email address new emails will be sent to.

 - Email subject ($mail_subject)
 This is a subject of new emails you will receive.

2. Open the index.html file, find lines 744 and 747 and insert your reCaptcha Public key (see Step 1) at the end of these lines: 

http://www.google.com/recaptcha/api/challenge?k=YOUR_PUBLIC_KEY

(e.g. http://www.google.com/recaptcha/api/challenge?k=09sdv0sf9v0sdf9b0df9b09dfb).

3. Save both files.





Sources and Credits
===================

We've used the following third party images, icons, and other files listed: 



General
-------

1. Twitter Bootstrap 3.2

URL: http://getbootstrap.com/

AUTHOR: @mdo and @fat

LICENSE: MIT License

2. Font Awesome 4.1

URL: http://fontawesome.io/

AUTHOR: Dave Gandy

LICENSE: MIT license



CSS Files: 
----------

1. CSS Animation

URL: https://daneden.me/animate/

AUTHOR: Dan Eden

LICENSE: MIT license

JS Plugins
----------

1. Scroll to top script

URL: http://www.dynamicdrive.com/dynamicindex3/scrolltop.htm

AUTHOR: Dynamic Drive

LICENSE: http://www.dynamicdrive.com/notice.htm

2. Lightbox 

URL: http://lokeshdhakar.com/projects/lightbox2/

AUTHOR: Lokesh Dhakar

LICENSE: Creative Commons Attribution 2.5 License

3. jQuery Backstretch

URL: http://srobbin.com/jquery-plugins/backstretch/

AUTHOR: Scott Robbin

LICENSE: MIT license

4. QueryLoader

URL: http://www.gayadesign.com/diy/queryloader2-preload-your-images-with-ease/

AUTHOR: Gaya Kessler

LICENSE: MIT license

5. Waypoints

URL: http://imakewebthings.com/jquery-waypoints/

AUTHOR: I Make Web Things

LICENSE: MIT license



reCAPTCHA
---------

Copyright (c) 2007 reCAPTCHA -- http://recaptcha.net

AUTHORS: Mike Crawford
         Ben Maurer


         
Images
------

All images below are licensed under the **Creative Commons Zero** license (http://unsplash.com/legal-stuff):

**Screens:**

1. 	Author: Shanghigh

	URL: http://38.media.tumblr.com/f264b862a6bf8ba5b9f06bf8bf4ea635/tumblr_na0kcnVUoi1st5lhmo1_1280.jpg
	
2. 	Author: Martin Staněk

	URL: http://38.media.tumblr.com/4e9d8c075b15f5922682bfaa13a8125c/tumblr_n7yhezarqF1st5lhmo1_1280.jpg
	
3. 	Author: Martin Dörsch

	URL: https://s3.amazonaws.com/ooomf-com-files/KJyFV5SZSweiYGhMhrqC_MD4817.jpg
	
4. 	Author: Michael Hull

	URL: http://37.media.tumblr.com/2d3f0d31590dbd09283e969bf8511a71/tumblr_naj3hqGqeh1st5lhmo1_1280.jpg
	
5.	Author: Ales Krivec

	URL: http://38.media.tumblr.com/b0599573cbde31e8f8ec2ce4f211bfc1/tumblr_naj3a897XB1st5lhmo1_1280.jpg
	
6.	Author: Kamil Lehmann

	URL: http://37.media.tumblr.com/26f1db79797aaf8577a32e288c5afefd/tumblr_n7yhhvUQtx1st5lhmo1_1280.jpg
	
7.	Author: Jasper van

	URL: https://unsplash.imgix.net/reserve/z7R1rjT6RhmZdqWbM5hg_R0001139.jpg?q=75&fm=jpg&auto=format&s=62cde4992508e70fdd44e16f1fe926fb
	

**Portfolio:**


1. 	Author: Rob Potvin

	URL: http://38.media.tumblr.com/2741d3e79ea3782f87c65c1e44b5f9fa/tumblr_na0kb0BLqR1st5lhmo1_1280.jpg
	
2. 	Author: Daniel Robert P

	URL: http://38.media.tumblr.com/2c1a9d53169f1eca25b2a0b8238744c9/tumblr_n9hxdqatsK1st5lhmo1_1280.jpg
	
3. 	Author: Andrew Ruiz

	URL: http://38.media.tumblr.com/ce044b7c552a59beeb778b38bc527a65/tumblr_n7yhe1sTa41st5lhmo1_1280.jpg
	
4. 	Author: David Marcu

	URL: http://38.media.tumblr.com/a0bcc39d4e7412072d08e085e888e682/tumblr_nb1up3J7l01st5lhmo1_1280.jpg
	
5. 	Author: Kim Daniel Arthur

	URL: http://38.media.tumblr.com/b028cf062bce5218fc3cbab26d345038/tumblr_n7fg8ypVQI1st5lhmo1_1280.jpg
	
6. 	Author: Matthew Wiebe

	URL: http://33.media.tumblr.com/a0d6500fa274340eca0eb0c125c18228/tumblr_n4cmkfHsMO1st5lhmo1_1280.jpg


	
The rest of the images that are not listed above are created by the Simpleqode.com team and are free to use by this package owner.


Changelog
=========

Version 1.1.1 - 19/11/2014

 - UPGRADE: Bootstrap 3.3.1

Version 1.1 - 10/10/2014

 - NEW: PHP contact form
 - IMPROVEMENT: Preloader replaced
 - IMPROVEMENT: Small bugs corrected

Version 1.0 - 18/08/2014

 - Initial release



Thanks for purchasing the Wolfram template. Do not hesitate to contact us if you have any questions or suggestions regarding this item.

http://simpleqode.com/
https://twitter.com/YevSim
yevgenysim@yandex.ru
jGravity
========

jGravity adds gravity to either all or specified elements within a page. Using the plugin is as easy as $('body').jGravity(); which will use default settings to apply the gravity effect, which I think you will find quite similar to how Google presented 'Google Gravity' in an earlier Google easter egg.

I created this plugin because it simply didn't exist. I wanted a gravity type of effect for a current project and searching was very frustrating  with little results. Although, I did find several leads to various other projects which contributed heavily to this plugin (mentioned below in credits).

HOW TO USE
========

As mentioned, all you need to do is use $('body').jGravity(); to produce the main effect. Calling the jGravity() function produces the best results when used on the main body. Oh, and jQuery is required, tested on jQuery 1.7.2.

Simple Example:

	<script>

		$(document).ready(function() {
		
		     $('body').jGravity();
		});
	
	</script>

Advanced Example:

	<script>
	
	    $(document).ready(function() {
	
	         $('div.jGravity').live('click', function() {
	              $('body').jGravity({
	                   target: 'everything',
	                   ignoreClass: 'ignoreMe',
	                   weight: 25,
	                   depth: 5,
	                   drag: true
	          	});
	     	});
		});

	</script>

Also, don't be afraid to use multiple jGravity() class on multiple targets to effect them differently.

SETTINGS
========

target: Enter your target critera e.g. 'div, p, span', 'h2', 'div#specificDiv', or even 'everything' to target everything in the body. You can cover as many different targets as you like

ignoreClass: Specify if you would like to use an ignore class, and then specify the class in quotations, e.g. 'ignoreMe'

weight: Enter any  numerical  value that is greater than 1 to decide the weight of elements (25 is default), you can also use the strings 'heavy' or 'light' to quickly test effects

depth: Enter a numerical value that is greater than 1 to decide depth of gravity and how many elements it affects (1 is default). This is used to prevent targeting structural divs or other items which may break layout in jGravity

drag: Decide if users can drag elements which have been effected by jGravity. Only 'true' and 'false' are acceptable.

Example:

    target: 'everything'
    ignoreClass: 'ignoreMe'
    weight: 25
    depth: 5
    drag: true

Feel free to play with the above settings until you receive the desired effect.

DEMO
========

You can find a demo available here: http://tinybigideas.com/assets/demo/jquery-gravity/

CREDITS
========

jGravity would not be possible without the work of:

Mr. Doobs :: http://mrdoob.com/92/Google_Gravity

GravityScript :: http://gravityscript.googlecode.com/

Alex Arnell's inheritance.js :: http://code.google.com/p/inheritance/

Box2Djs :: http://box2d-js.sourceforge.net/

Thank you very much for your work on the above guys, I wouldn't have been able to make this work without you. If anyone if interested in more complex interactions with javascript physics engines, please check those guys out.
 
Hopefully that's all you need to know, so go ahead and download and have a play!

MORE
========

You can find more here: http://tinybigideas.com/plugins/jquery-gravity/

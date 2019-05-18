# "Hidden Link": SugarCube (v2.18)

## Summary

"Hidden Link" demonstrates how to create a 'hidden' link that is only revealed when the cursor passes over it.

Using CSS and JavaScript, a rule is created for transparent color and applied or removed through using jQuery's *[on()](http://api.jquery.com/on/)* function with 'mouseenter' and 'mouseleave' events.

The use of the *postdisplay* functionality is also used to run JavaScript after each passage is displayed.

## Twee Code

```
:: StoryTitle
SugarCube: Hidden Link

:: UserScript[script]
postdisplay['hidden-link-setup'] = function () {
	/*
		Hidden links that are always hidden:
			<span class="hidden">[[A hidden link]]</span>
	*/
	$('.hidden')
		.addClass('hidden');

	/*
		Hidden links that hide unless you're hovering over them:
			<span class="hides">[[A hidden link]]</span>
	*/
	$('.hides')
		.addClass('hidden')
		.on('mouseenter', function () {
			$(this).removeClass('hidden');
		})
		.on('mouseleave', function () {
			$(this).addClass('hidden');
		});

	/*
		Hidden links that reveal themselves when you hover over them:
			<span class="reveals">[[A hidden link]]</span>
	*/
	$('.reveals')
		.addClass('hidden')
		.one('mouseenter', function () {
			$(this).removeClass('hidden');
		});
};


:: UserStylesheet[stylesheet]
.hidden a {
	color: transparent;
}


:: Start
A hidden link that's always hidden: <span class="hidden">[[A hidden link]]</span>

A hidden link that hides unless you're hovering over it: <span class="hides">[[A hidden link]]</span>

A hidden link that reveals itself when you hover over it: <span class="reveals">[[A hidden link]]</span>

:: A hidden link
You found it!


```

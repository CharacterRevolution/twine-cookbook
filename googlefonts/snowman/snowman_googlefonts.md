# "Google Fonts": Snowman (v1.3)

## Summary

"Google Fonts" uses a [Google Font](https://fonts.google.com/) loaded via the CSS ```@import``` at-rule. A class style rule ("googleFont") is then created using the imported font-family and applied to a ```<div>``` element within a single passage.

Other Google Fonts could be imported and applied using the same method, creating new class or ID style rules to be applied for and across different HTML elements in the same way.

## Twee Code

```
:: StoryTitle
Snowman: Google Fonts

:: StoryStylesheet[stylesheet]
@import url('https://fonts.googleapis.com/css?family=Roboto');

.googleFont {
	font-family: 'Roboto', sans-serif;
}

:: Start
<div class="googleFont">This text is styled using a Google Font</div>

```

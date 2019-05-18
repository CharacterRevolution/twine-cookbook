# "Static Healthbars": SugarCube (v2.18)

## Summary

"Static Healthbars" demonstrates how to write HTML elements using variable values. In this example, [Attribute Directive](http://www.motoslave.net/sugarcube/2/docs/#markup-html-attribute-directive) markup is used to inject the current value of the *$heath* story variable into the &lt;progress&gt; and &lt;meter&gt; elements.

## Twee Code

```
:: StoryTitle
Static Healthbars for SugarCube

:: Start
<<set $health to 80>>

Show a healthbar using a Progress element:
<progress @value="$health" max="100"></progress>

Show a healthbar using a Meter element:
<meter @value="$health" min="0" max="100"></meter>


```

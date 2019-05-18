# "Deleting Variables": Snowman (v1.3)

## Summary

Through using the [Underscore template library](https://underscorejs.org/#template) available in Snowman, JavaScript can be used within passages without a &lt;script&gt; tag. The [*delete* operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete) can be used in JavaScript to remove a variable.

## Twee Code

```
:: StoryTitle
Snowman: Deleting Variables

:: UserScript[script]
window.story = {};

window.story.example = "an example!";

:: Start
What is the value of the property "example" of the object window.story? <%= window.story.example %>

[[Delete the value!]]

:: Delete the value!
<%

// Delete the variable
delete window.story.example;

%>

[[Test for value]]

:: Test for value
Does "example" still exist as part of the object window.story? <%= window.story.hasOwnProperty("example") %>

```

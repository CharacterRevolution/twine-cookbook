# "Lock and Key: Variable": SugarCube (v2.18)

<div class="alert information"><strong>Note: </strong>This recipe is affected by history changes in the story. Undoing or re-doing back to a passage containing this recipe has the potential to change its saved values.</div>

## Summary

"Lock and Key: Variable" demonstrates how to create the effect of picking up a key and unlocking a door. In this example, the key is a variable (*$key*) and is initially set to the value *false* in the Start passage.

When the link (created using a &lt;&lt;linkreplace&gt;&gt; macro) "Pick up the key" is clicked, *$key* is changed to the value *true* and the door link changes from its initial response of "Locked Door" to a link to the passage Exit.

## Twee Code

```
:: StoryTitle
Lock and Key: Variable in SugarCube

:: Start
<<set $key to false>>

Rooms:
[[Back Room]]
[[Front Room]]

:: Back Room
<<if $key is false>>
    Items:
    <<linkreplace "Pick up the key">><<set $key to true>>You have a key.<</linkreplace>>
<<else>>
    There is nothing here.
<</if>>

Rooms:
[[Front Room]]

:: Front Room
<<if $key is true>>
    [[Exit]]
<<else>>
    Locked Door
<</if>>

Rooms:
[[Back Room]]

:: Exit
You found the key and went through the door!

```

## See Also

[Setting and Showing Variables](../../settingandshowing/sugarcube/sugarcube_settingandshowing.md)

# "Programmatic Undo": SugarCube (v2.18)

## Summary

While SugarCube supports allowing the user to undo and redo moves, the "undo" operation can also be accessed through the [*&lt;&lt;back&gt;&gt;*](http://www.motoslave.net/sugarcube/2/docs/macros.html#macros-back) macro. Through its use, changes from the most current action can be "undone."

## Twee Code

```
:: StoryTitle
Programmatic Undo in SugarCube

:: Start
[[Enter the Darkness]]

:: Enter the Darkness
<<back "You are not ready! Go back!">>
```

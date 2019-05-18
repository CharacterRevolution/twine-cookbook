# "Date and Time": SugarCube (v2.18)

## Summary

"Date and Time" demonstrates how to use the JavaScirpt *[Date() ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)* functionality in SugarCube.

## Twee Code

```
:: StoryTitle
Date and Time in SugarCube

:: Start
<<print "The current time (in milliseconds since January 1, 1970 00:00:00 UTC) is " + Date.now()>>

<<set $date to new Date()>>
The current month is <<print $date.getMonth() >>.
The current day is <<print $date.getDay() >>.
The current hour is <<print $date.getHours() >>.
The current minute is <<print $date.getMinutes() >>.
The current fullyear is <<print $date.getFullYear() >>.

<<set $originalDate to new Date("October 20, 2018")>>
<<set $timeDifference to Date.now() - $originalDate>>
It has been $timeDifference milliseconds since October 20, 2018.

```

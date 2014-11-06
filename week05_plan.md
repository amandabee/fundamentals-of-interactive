# Week 10
Thursday Nov 6 / Monday Nov 17

## Discussion
Check in on pace -- how are we holding up so far?

Big lingering questions?

Good examples to work from:
<http://freegreentea.info/talks/2014/Ravitch/#/>
<http://freegreentea.info/talks/2014/JohnJay/#/3>


## Building out a quiz

There are a lot of ways in which this is a little clunky, but our goal is to play with writing for a news quiz and get one up and working. In a couple of weeks, we'll look at how to use CSS to beautify our Slideshows. The same principles will work here. For now, though, focus on the text. 

We're going to play a bit with Tabletop.js -- if you don't know it, [Source has a nice write up](http://source.opennews.org/en-US/articles/ultralight-cmses/) and Mike Ball has [another](http://www.mikeball.us/blog/using-google-spreadsheets-and-tabletop-js-as-a-web-application-back-end). The easiest way to work with this quiz script is to use a Google Spreadsheet as the backend, but you could, in theory, hand-code the JSON yourself. 

You don't actually need to use a Google Spreadsheet. You could use JSON. But for now, we're going the spreadsheet route.

We're going to use Mother Jones' [quiz framework](https://github.com/motherjones/newsquiz) to make a super basic quiz. 

You can vew [the data behind this quiz](https://docs.google.com/spreadsheet/ccc?key=0AqaPuVjW5_0OdEJpRVV2UVBndThRaHNyM1NGbk5ZblE&usp=sharing) at a URL different from he one provieded on the sample quiz. [Sample Quiz](http://digitalstorage.journalism.cuny.edu/amandahickman/newsgames/quiz/)

Walk through:

1: View the source of my demo quiz. Let's talk about what it says, especially local URLs vs the CDN.

2: Download the zip file <https://github.com/amandabee/newsquiz> and open it, let's look at the contents. 

** open index.html in text wrangler; look over the files it calling on. Which are coming from elsewhere? Which are local? 
** Look at your folders. What all do you have here? 
** Look at the two Newsquiz.js files -- what does Minify do?

I pulled a lot of things out of the original Mother Jones repository that certainly belong there if we're going to contribute to the code base, but if we're just going to use their work and give nothing back ... we don't need those extra files. 

## Exercise
Everyone pick your favorite stat out of [Stats and the City](http://mycrains.crainsnewyork.com/stats-and-the-city/boroughs) and we'll make a quiz about the city.

## Data/chart pitches
+ Finding data
+ Charting it

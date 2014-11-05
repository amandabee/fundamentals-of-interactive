## Quiz
*Pitch Week 4, Due Week 6*

## Tool

Mother Jones' [quiz framework](https://github.com/motherjones/newsquiz) 

## Technical Skills

+ Making an HTML Template (Story 1)
+ Basic Bootstrap (Story 1)
+ FTP and File Management (Story 1)
+ Embedding a local script on your page 


## Examples of the Form 

NY Times has a series called "Well Quiz" -- From [The Well Quiz](http://well.blogs.nytimes.com/category/the-well-quiz/), 
[Can You Read People’s Emotions?](http://well.blogs.nytimes.com/2013/10/03/well-quiz-the-mind-behind-the-eyes/) and [Well Flu](http://well.blogs.nytimes.com/2013/02/13/the-well-flu-quiz/)

[Popes](http://www.nytimes.com/interactive/2013/03/18/world/pope-quotes.html) 

[Presidential Fibs](http://ralphvacca.org/fibber/game/index.html)

From Craft II on [Bloomberg's Legacy](http://bloomberglegacy.nycitynewsservice.com/bloombergs-new-york-city-take-the-quiz/)

### Considerations

A newsquiz should move the story along. Don't just ding people for getting the answer wrong, tell them why it is wrong -- give them a little something to go on as they try again (and let them try again). And don't just reward people for getting the answer right -- tell them *why* it is the right answer. We're not here to grade your knowledge of the story, we're trying to make you think this story is interesting. 


## Hands-On

We're going to use Mother Jones' [quiz framework](https://github.com/motherjones/newsquiz) to make a super basic quiz. 

My starting point: <http://digitalstorage.journalism.cuny.edu/amandahickman/newsgames/quiz/>

We're going to play a bit with Tabletop.js -- if you don't know it, [Source has a nice write up](http://source.opennews.org/en-US/articles/ultralight-cmses/) and Mike Ball has [another](http://www.mikeball.us/blog/using-google-spreadsheets-and-tabletop-js-as-a-web-application-back-end). The easiest way to work with this quiz script is to use a Google Spreadsheet as the backend, but you could, in theory, hand-code the JSON yourself. 

And we're going to use a little jQuery. We're actually just going to pull in an external js file for jQuery [we're not going to host it ourselves, though](https://encosia.com/3-reasons-why-you-should-let-google-host-jquery-for-you/)

## Exercise
Everyone pick your favorite stat out of [Stats and the City](http://mycrains.crainsnewyork.com/stats-and-the-city/boroughs) and we'll make a quiz about the city.

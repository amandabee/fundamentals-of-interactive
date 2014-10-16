# Week 7 Plan

## Welcome, HTML troubleshooting
What was hard in putting the pitches together? 

###Pitches
+ [Lisa Brown, Cranberry Bog](http://digitalstorage.journalism.cuny.edu/lisa.brown/fundamental/week6.html)
+ [Ryan Wallerson, World Series](http://digitalstorage.journalism.cuny.edu/ryanwallerson/fundamentals/weeksix.html)
+ [Danni Santana, First Reformed Church of Astoria](http://digitalstorage.journalism.cuny.edu/dannisantana/coding/weeksix.html)
+ [Rania Berrada, Mott Haven at the Peoples Climate March](digitalstorage.journalism.cuny.edu/raniaberrada/Fundamentals/week6.html)
+ [Maura Ewing, Prison Bus](http://digitalstorage.journalism.cuny.edu/maura.ewing/public_html/fundamentals/week6.html)
+ [Annamarya Scaccia](http://digitalstorage.journalism.cuny.edu/annamarya.scaccia/week6.html)
+ [Luke Tress](http://digitalstorage.journalism.cuny.edu/luketress/week6.html)
+ [Brooke Williams](http://digitalstorage.journalism.cuny.edu/brooke.williams/fundamentals/week6.html)

Notes: your first draft is due next week. 

Edit the page title -- it should probably match the headline, though I'll take "Slideshow Draft" too. 

Follow instructions: week6.html is not the same as weeksix.html

Make the categories bold (eg. **Proposed Headline:**)

## Adding a Carousel

Work on "bootstrap_slideshow.html"

Adding an anchored link, first.

DOM, ids

## Maps and Mapping

What makes a map work as a story? 

http://jour72312.tumblr.com/tagged/maps

Don't just map population centers:
https://xkcd.com/1138/

+ WNYC [Sandy Flooding](http://project.wnyc.org/flooding-sandy-new/#12.00/40.7378/-74.07020)
+ ProPublica [Government Lends to Rebuild in Flood Zones](http://projects.propublica.org/sandy-sba/)

+ NPR [Zoom In On Oklahoma Tornado Damage](http://apps.npr.org/moore-oklahoma-tornado-damage/)

+ <http://www.wnyc.org/story/304422-new-york-remade-city-more-desirable-ever-also-too-expensive-many/>

+ [map as navigation](http://www.telegraph.co.uk/news/worldnews/asia/japan/9134487/Graphic-Aftermath-of-Japan-earthquake-and-tsunami-and-Fukushima.html)

## Pivot Tables to Summarize Data
You're going to wind up needing this for your map. 

Department of Environmental Conservation [data on gas wells](http://www.dec.ny.gov/energy/1603.html) in New York State.

How many wells are there per county? 

1. Start with `Data > Pivot Table Report` -- look at the cells Excel proposes to use. Does that include all of your data?
2. Add Row -- Use "COUNTY" for the rows. You should see a list of county names. 
3. Add Value -- Use "API_WELLNO" for now. 
4. Check the formula -- should excel `count` values or `sum` them? Or find an `average`? 

And there you have it. More things to play with:

* Try adding "SLANT" as a Column -- horizontal (as opposed to vertical) wells are particularly controversial. Are there any concentrations of horizontal wells?
* How would you work out how much money each county is collecting in permit fees?
* Can you see any trends in the average permit fee in each county? 

## Lab
Work on your slideshow. Get a placeholder version up and running. 

----

**Discussion:** Who has ideas for stories down the line? Are they interesting? What would make them interesting. You should be looking ahead!  

Maps and mapping -- how to make a map that tells a story. 

**Hands on:** 

1) Pivot tables to summarize data, HTML and FTP Review

**Homework:** Post the first draft of your slidshow on Digital Storage (name it "slideshow_draft.html"); Post a map pitch on Digital Storage (name it "map_pitch.html"); Use pivot tables to summarize 311 call data. 


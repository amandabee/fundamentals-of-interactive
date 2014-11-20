---
title     : Building a Chart
layout    : post
category  : hands-on
tagline   : Using Highcharts
tags      : [week11, review, charts, highcharts]

---

{% include JB/setup %}

**Step One: get organized**. You're going to need a few windows open. You might want to close other windows so you can focus.

+ the [Highcharts Demo](http://www.highcharts.com/demo/) page in a browser (we'll start with a basic line chart)   
+ our [sample data on Bronx graduation rates](https://raw.github.com/amandabee/cunyjdata/master/assignments/graduation_outcomes.csv) in a text editor or spreadsheet program   
+ your text editor (if you don't have one, try [Sublime](http://www.sublimetext.com/) or [Text Wrangler](http://www.barebones.com/products/TextWrangler/), or if you're feeling fancy and want free and open source software, try [Emacs](http://emacsformacosx.com/) or [Vim](http://macvim.org/OSX/index.php))   
+ [Mr Data Converter](http://shancarter.com/data_converter/) in a browser   

+ Our HighCharts [template is super helpful](assets/highcharts/highcharts_demo.html)

## Troubleshooting Highcharts

Many of you have figured out that you can embed a JSFiddle. But ... embedding Fiddles is fiddly. Instead of learnning how to do that, let's stick to learning how to put a chart on our own page. 

+ Did you place a `<div..>…</div>` on the page where you want the chart to appear?
+ Does your `<div>` have a descriptive, one word id? `id="container"` is not descriptive. `id="time_to_leak"` is.
+ Is your Highcharts Function looking for the right id?  
`$(function () {$('#oscar_night').highcharts({` is looking for a div with `id="oscar_night"` 
+ Is your jquery call above your function?
+ Is your highcharts call below your function?






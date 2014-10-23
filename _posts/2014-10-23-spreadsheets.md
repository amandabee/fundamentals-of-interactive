---
title     : Spreadsheet Skills
layout    : post
category  : hands-on
tagline   : Using spreadsheet functions to get what you need. 
tags      : [week08, review, excel, spreadsheets]

---

{% include JB/setup %}

More tips at <https://github.com/amandabee/cunyjdata/wiki/Tip-Sheet:-Spreadsheets>

A lot of you are dealing with data you had to create a pivot table to generate. Once you have your pivot table, you should ...

1. Save your data as a *spreadsheet* file -- an XLS or ODS. That will retain all the tabs and pivot table functionality. 
2. Flip to the tab that has the pivot table you actually want to work with. Use "Save As..." to save the data as a `.csv`
3. Close the file. Really. Just close it. Close everything you aren't working on while you're at it.
4. Re-open the csv. And try locating it with the finder and using "open with..." to open it in TextWrangler. If it seems wonky, close it and open it again, but this time read all the dialogs you see and try to figure out what they're trying to communicate. Look over what is and isn't checked and make sure that all makes sense. 

And one more thing: a number of you are encountering a common problem. That `WHERE us_states.state = bls_fatality_2011.state` clause in our query works because both tables have a column where the state of California is listed as "California" -- CartoDB's database can look for the word that matches. But what if your data doesn't match? What if your data has districts described like "Bronx 03" but your [Community District shapefile](http://www.nyc.gov/html/dcp/html/bytes/districts_download_metadata.shtml#bcd) has three digit `borocd` codes instead?

And what if you *looked* at the metadata and it didn't really help you understand what was going on? What to do then?

There are a bunch of ways to solve this problem, but I'm going to walk through just one. The first thing you need to know: the `borocd` is a three digit code, and the first digit is the boro code:

1: Manhattan
2: Bronx
3: Brooklyn
4: Queens
5: Staten Island

The second and third digits are the CD. So 314 is Brooklyn CD 14. In your spreadsheet, you're going to do the following:

0. Clean up your data. Cut out any extra rows that are hanging out at the top. Make sure you followed the instructions for saving a pivot table and reopening it as a `.csv` above. 

1. Select the column of values like "Bronx 04" and "Staten Island 01", and use `edit > find and replace ..." to replace "Staten Island" with "Staten_Island" (you'll see why in a moment).

2. Create a new, empty column next to the column where the CDs are listed. 

3. Select the whole CD column by clicking on the letter above the first data row. 

4. Use `Data > Text to Columns` to split it in two, using spaces as the delimiter. If you skipped step 1, you'll make a mess of things because you'll wind up with `Staten`, `Island`, `01` which isn't what you want. You should now have a column of boro names and a column of CD numbers. If you don't, let me know what you do have!

5. Click in any cell, to make sure that you don't have a subset of cells selected. Use `Data > Sort ...` to sort your table by borough. 

6. Add another empty column, title it "boro code" and fill it in with numbers. You already know how to pull down a single value -- alphabetically, Brooklyn is first, so type a 3 at the top of the column and then pull it down until you hit the Bronx. Bronx is 2. Repeat. When you're done you should have a column of boro codes. 


7. Your "CD" column probably contains some two digit numbers and some one digit numbers. You're going to use the [=TEXT()](https://help.libreoffice.org/Calc/Text_Functions#TEXT) function to ensure that it is all one digit. You could also use number formats. Create yet another blank column, call it "borocd" and find a row where the CD needs some left hand padding. In the adjacent blank cell, type `=` and then tap the cell that contains your CD. It should populate the blank cell with a cell reference. `=M13` or something. Column M, Row 13. Hit return and you'll see that when you aren't editing the cell it just displays the value. Now you need to enter a real formula. If `M13` is the cell that contains the CD number, your formula is going to be this: `=TEXT(M13, "00")` -- hit return and see what happens. You should see that the function has added zero padding to the left of any one digit number. This function, with `"00"` as the second argument, forces all your numbers to two digits by padding them with left-hand zeros as needed. If you're kind of thrilled by this, try seeing what `"0000"` does. 

8. Now we're going to nest functions. We need to string together two things: the boro code and the two digit CD code. If your boro codes are in column N and your CD codes are in column M, your function is going to look about like this, at least on row 2: `=CONCATENATE(N2,TEXT(M2,"00"))` 

That should leave you with a column full of three digit borocd codes that match exactly what you've got in your shapefile. So once you've uploaded your data to CartoDB you can merge it with your Borough shapefile with a query something like this:

	UPDATE mydata
	SET the_geom = nycd.the_geom
	FROM nycd
	WHERE nycd.borocd = mydata.borocd
	
	

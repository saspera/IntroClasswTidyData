# Geog/Envr 250, Day 1 Assignment

Hi class, 

I'm sorry I couldn't be there today but I'm up in Boston presenting some of my work on how deforestation & agricultural expansion in the Brazilian Cerrado may affect regional climate & the future of crop production in Brazil at the American Metereological Society Conference. (Did I assume we had another week of winter break before deciding to prsent at this conference? Yes, yes I did. I'm still not used to how short of a winter break we have here at UR.) But, you're in great hands with Dr. Lookingbill! And I'll be back for class on Wednesday.

You have three tasks to finish in class today, and one short assignment for Wednesday

#### Today
- [ ] Read through the syllabus on Blackboard
- [ ] Go through the assignment on keeping data tidy (see **Monday Assignment** section below) and submit it to Assignments>XXX
- [ ] Fill out [**_this_ short survey**](https://forms.gle/UASqkAGEi8dAfJvF6) 

#### For Wednesday
- [ ] Complete the **short** worksheet that Dr. Lookingbill will hand out, where we all remember how fun math is, which I'll collect at the beginning of class on Wednesday. 

## Monday Assignment
###### Adopted fromm DataCarpentry.org

#### You'll need
1. Microsoft Excel (freely available to all UR students)
2. Microsoft Word (to write up your answers which you'll submit to Blackboard at the end of the class period)
3. 'survey_data_spreadsheet.xlsx' which can be downloaded from Blackboard from Assignments>Day 1
   - These data are observations of a small mammal community in southern Arizona. It's part of a project studying the effects of rodents and ants on the plant community and this project has been running for more than 40 years. The rodents are sampled on a series of 24 plots, with different experimental manipulations controlling which rodents are allowed to access which plots. 
   - This is this simplified version of a real dataset that has been used in over 100 publications.
 

### Introduction
One of the major goals of this class is for everyone to leave here with a better understanding of how to collect data, different types of data, and how to ask questions and perform the approprioate statistical analyses on any dataset. So today, we're going to jump right into working with data and use the best practices and pitfall of data organization. If you organize your data in the most 'tidy, it makes data analyis (and science) so. much. easier. I don't think you'd believe me if I told you the amount of time (approimately my entire fourth year of graduate school) I've spent just organzing data, or 'data wrangling', before I could even begin to think about analyzing it. 
{science gif}
###### I could not find one 'science' gif with a lady, which was upsetting. 

Most researchers have their data in spreadhseets, so, that's where we'll start. Spreadsheets allow scientists to do a lot of things, like data entry, organzing data, subsetting and sorting data, (v. basic) statistics, and (v. basic) plotting. I say '(v. basic)' because spreadsheet-software like Excel is pretty limited in what it can do, and it's also easy to accidentlly apply the wrong formulas to adjacent cells - so for these - and reproducibility reasons - I like to do a majority of my statistics and figure making using other programs like R or Python.

That being said, Excel is still super useful for storing data, and also totally appropriate many of lab assignments for this class. So, we're going to use learn how to 'tidy' our data. *Good organization is the foundation of any research project.*

### Formatting data tables in Spreadsheets

The most common mistake made is treating spreadsheet programs like lab notebooks, that is, relying on context, notes in the margin, spatial layout of data and fields to convey information. As humans, we can (usually) interpret these things, but computers don’t view information the same way, and unless we explain to the computer what every single thing means (and that can be hard!), it will not be able to see how our data fits together.

Using the power of computers, we can manage and analyze data in much more effective and faster ways, but to use that power, we have to set up our data for the computer to be able to understand it (and computers are very literal).

This is why it’s extremely important to set up well-formatted tables from the outset - before you even start entering data from your very first preliminary experiment. *Data organization is the foundation of your research project.* It can make it easier or harder to work with your data throughout your analysis, so it’s worth thinking about when you’re doing your data entry or setting up your experiment. You can set things up in different ways in spreadsheets, but some of these choices can limit your ability to work with the data in other programs or have the you-of-6-months-from-now or your collaborator work with the data.

### Keep track of your analyses. 

When you’re working with spreadsheets, during data clean up or analyses, it’s very easy to end up with a spreadsheet that looks very different from the one you started with. In order to be able to reproduce your analyses or figure out what you did when Reviewer #3 asks for a different analysis, you should create a new file with your cleaned or analyzed data. Don’t modify the original dataset, or you will never know where you started!

keep track of the steps you took in your clean up or analysis. You should track these steps as you would any step in an experiment. We recommend that you do this in a plain text file stored in the same folder as the data file. (Do not do what I usually do, and have 4 different files and have to try and remember what they were 6 months after you last touched it, "survey_data_og.xlsx", "survey_data_final_for_real.xlsx", "survey_data_this_is_really_the_last_one.xlsx", "survey_data_actual_real_final_but_really.xlsx")

### Structuring data in spreadsheets
The cardinal rule of spreadsheet programs for data is to keep it ['tidy.'](https://www.jstatsoft.org/article/view/v059i10)

1. Put all your variables (the thing you're measuring, like 'weight' or 'temperature') in columns.
2. Put each observation in its own row.
3. Dont combine multiple pieces of information in one cell. 
4. Leave the raw data raw - don't touch that original data.
5. Save the cleaned dataset. 

For instance, we have data from a survey of small mammals in a desert ecosystem. Different people have gone to the field and entered data into a spreadsheet. They keep track of things like species, plot, weight, sex and date collected.

If they were to keep track of the data like this

the problem is that species and sex are in the same field. So, if they wanted to look at all of one species or look at different weight distributions by sex, it would be hard to do this using this data setup. If instead we put sex and species in different columns, you can see that it would be much easier.

The rule of thumb, when setting up a datasheet, is columns = variables, rows = observations, cells = data (values).
{image 2}

So, instead we should have:
{image 3}

```diff 
+ Exercise Part 1
1. Download the spreadsheet (survey_data_spreadsheet.xlsx) from Assignments>Day 1
2. Open the data in Excel.
3. You will see that there are two tabs. 
Two field assistants conducted the surveys, once in 2013 and one in 2014, and they both kept track of the datain their own way. 
Now it's 2015 (imaginary time travel) and you're the person in charge of this project, and you want to be able to start analyzing the data.

! In your Word document answer the questions below. 
!And like in our future in-class assignemnts, you can work with the people around you on this assignment:
Q1. Identify what's wrong with this spreadsheet. 
Q2. Write some of the steps you would need to take to clean up the 2013 and 2014 tabs, and to put them together in one spreadsheet. 
```

### Common Spreadsheet Errors
#### Skim this section to see how many of the common spreadsheet errors you identified. 
There are a few potential errors to be on the lookout for in your own data as well as data from collaborators or the Internet. If you are aware of the errors and the possible negative effect on downstream data analysis and result interpretation, it might motivate yourself and your project members to try and avoid them. Making small changes to the way you format your data in spreadsheets can have a great impact on efficiency and reliability when it comes to data cleaning and analysis.

#### Using multiple tables
A common strategy is creating multiple data tables within one spreadsheet. This confuses the computer, so don’t do this! When you create multiple tables within one spreadsheet, you’re drawing false associations between things for the computer, which sees each row as an observation. You’re also potentially using the same field name in multiple places, which will make it harder to clean your data up into a usable form. The example below depicts the problem:

{image 4}

In the example above, the computer will see (for example) row 4 and assume that all columns A-AF refer to the same sample. This row actually represents four distinct samples (sample 1 for each of four different collection dates - May 29th, June 12th, June 19th, and June 26th), as well as some calculated summary statistics (an average (avr) and standard error of measurement (SEM)) for two of those samples. Other rows are similarly problematic.

#### Using multiple tabs
But what about workbook tabs? That seems like an easy way to organize data, right? Well, yes and no. When you create extra tabs, you fail to allow the computer to see connections in the data that are there (you have to introduce spreadsheet application-specific functions or scripting to ensure this connection). Say, for instance, you make a separate tab for each day you take a measurement.

This isn’t good practice for two reasons: 1) you are more likely to accidentally add inconsistencies to your data if each time you take a measurement, you start recording data in a new tab, and 2) even if you manage to prevent all inconsistencies from creeping in, you will add an extra step for yourself before you analyze the data because you will have to combine these data into a single datatable. You will have to explicitly tell the computer how to combine tabs - and if the tabs are inconsistently formatted, you might even have to do it manually.

The next time you’re entering data, and you go to create another tab or table, ask yourself if you could avoid adding this tab by adding another column to your original spreadsheet. We used multiple tabs in our example of a messy data file, but now you’ve seen how you can reorganize your data to consolidate across tabs.

Your data sheet might get very long over the course of the experiment. This makes it harder to enter data if you can’t see your headers at the top of the spreadsheet. But don’t repeat your header row. These can easily get mixed into the data, leading to problems down the road.

Instead you can [freeze](https://support.office.com/en-us/article/freeze-panes-to-lock-the-first-row-or-column-in-excel-for-mac-b8eb717e-9d3e-4354-8c02-d779a4b404b2?redirectSourcePath=%252fen-us%252farticle%252fFreeze-column-headings-for-easy-scrolling-57ccce0c-cf85-4725-9579-c5d13106ca6a&ui=en-US&rs=en-US&ad=US) the column headers so that they remain visible even when you have a spreadsheet with many rows.

#### Not filling in zeros
It might be that when you’re measuring something, it’s usually a zero, say the number of times a rabbit is observed in the survey. Why bother writing in the number zero in that column, when it’s mostly zeros?

However, there’s a difference between a zero and a blank cell in a spreadsheet. To the computer, a zero is actually data. You measured or counted it. A blank cell means that it wasn’t measured and the computer will interpret it as an unknown value (otherwise known as a null value).

The spreadsheets or statistical programs will likely mis-interpret blank cells that you intend to be zeros. By not entering the value of your observation, you are telling your computer to represent that data as unknown or missing (null). This can cause problems with subsequent calculations or analyses. For example, the average of a set of numbers which includes a single null value is always null (because the computer can’t guess the value of the missing observations). Because of this, it’s very important to record zeros as zeros and truly missing data as nulls.

#### Using problematic null values
**Example:** using -999 or other numerical values (or zero) to represent missing data.
**Solutions:**
There are a few reasons why null values get represented differently within a dataset. Sometimes confusing null values are automatically recorded from the measuring device. If that’s the case, there’s not much you can do, but it can be addressed in data cleaning with a tool like OpenRefine before analysis. Other times different null values are used to convey different reasons why the data isn’t there. This is important information to capture, but is in effect using one column to capture two pieces of information. Like for using formatting to convey information it would be good here to create a new column like ‘data_missing’ and use that column to capture the different reasons.

Whatever the reason, it’s a problem if unknown or missing data is recorded as -999, 999, or 0. Many statistical programs will not recognize that these are intended to represent missing (null) values. How these values are interpreted will depend on the software you use to analyze your data. It is essential to use a clearly defined and consistent null indicator. Blanks (most applications) and NA (for R) are good choices. White et al, 2013, explain good choices for indicating null values for different software applications in their article: Nine simple ways to make it easier to (re)use your data. Ideas in Ecology and Evolution.
{image 5} 

#### Using formatting to convey information
**Example:** highlighting cells, rows or columns that should be excluded from an analysis, leaving blank rows to indicate separations in data.
{image 6} 
**Solution:** create a new field to encode which data should be excluded.
{image 7}

#### Placing or units in cells
Just put it in the column title. So of having a 'Temperature' field, and then, in the next three cells, having your entries be 45F, 42F, 53F; have a 'Temperature (deg F)' field, and then, your next three cells would be, 45, 42, and 53. 

#### Entering more than one piece of information in a cell
**Example:** You find one male, and one female of the same species. You enter this as 1M, 1F.
**Solution:** Don’t include more than one piece of information in a cell. This will limit the ways in which you can analyze your data. If you need both these measurements, design your data sheet to include this information. For example, include one column for number of individuals and a separate column for sex.

#### Using spaces (or other special characteris) in field names
Choose descriptive field names, but be careful not to include spaces, numbers, or special characters of any kind. Spaces can be misinterpreted by parsers that use whitespace as delimiters and some programs don’t like field names that are text strings that start with numbers.

Underscores are a good alternative to spaces. Consider writing names in camel case (like this: ExampleFileName) to improve readability. Remember that abbreviations that make sense at the moment may not be so obvious in 6 months, but don’t overdo it with names that are excessively long. Including the units in the field names avoids confusion and enables others to readily interpret your fields.

{image 8}

#### Including notes/metadata in the data table. 
**Example:** You add a legend at the top or bottom of your data table explaining column meaning, units, exceptions, etc.

**Solution:** Recording data about your data (“metadata”) is essential. You may be on v. close terms with your dataset while you are collecting and analysing it, but the chances that you will still remember that the variable “sglmemgp” means single member of group, for example, or the exact algorithm you used to transform a variable or create a derived one, after a few months, a year, or more are slim.

As well, there are many reasons other people may want to examine or use your data - to understand your findings, to verify your findings, to review your submitted publication, to replicate your results, to design a similar study, or even to archive your data for access and re-use by others. While digital data by definition are machine-readable, understanding their meaning is a job for human beings. The importance of documenting your data during the collection and analysis phase of your research cannot be overestimated, especially if your research is going to be part of the scholarly record.

However, metadata should not be contained in the data file itself. Unlike a table in a paper or a supplemental file, metadata (in the form of legends) should not be included in a data file since this information is not data, and including it can disrupt how computer programs interpret your data file. Rather, metadata should be stored as a separate file in the same directory as your data file, preferably in plain text format with a name that clearly associates it with your data file. Because metadata files are free text format, they also allow you to encode comments, units, information about how null values are encoded, etc. that are important to document but can disrupt the formatting of your data file. 

*Basically. Store all your notes in a seperate text file.*

**Phew, what a fun reference! Let's move on.**

### Dealing. With. Dates.
Dates in spreadsheets are stored in a single column. While this seems the most natural way to record dates, it actually is not best practice. A spreadsheet application will display the dates in a seemingly correct way (to a human observer) but how it actually handles and stores the dates may be problematic.

In particular, please remember that functions that are valid for a given spreadsheet program are usually guaranteed to be compatible only within the same family of products. If you will later need to export the data and need to conserve the timestamps, you are better off handling them using one of the solutions discussed below. (Jan 13, 2019 in Excel speak is actually stored as, "43478" - the number of days after January 1, 1900. Because. Sure.)

Additionally, Excel can turn things that aren’t dates into dates, for example names or identifiers like MAR1, DEC1, OCT4. So if you’re avoiding the date format overall, it’s easier to identify these issues.

```
+ Exercise Part 2
1. In the 'dates' tab of your spreadsheet, you have the data from 2014 plot 3.  
   There's a 'Date collected' column. 
2. Extract month, day, and year from the dates to new columns. 
   For this we can use the built in Excel functions '=Year()', '=Month()', '=Day()'
   (Make sure the new column is formatted as number and not as a date.)
3. Does the year say 2019? That's because Excel is dumb. Even though you want the year to be 2014,
   your spreadsheet automatically interpretetted it as 2019, the year you entered the data.
   Type 2014 into the first year cell, and then put the mouse over the lower, right-hand
   corner of the cell until a tiny, black, plus sign appears, and drag that value down.
```
It is much safer to store dates with YEAR, MONTH, DAY in separate columns or as YEAR and DAY-OF-YEAR in separate columns.

Note: Excel is unable to parse dates from before 1899-12-31, and will thus leave these untouched. If you’re mixing historic data from before and after this date, Excel will translate only the post-1900 dates into its internal format, thus resulting in mixed data. If you’re working with historic data, be extremely careful with your dates!

Excel also entertains a second date system, the 1904 date system, as the default in Excel for Macintosh. Because, again, sure. This system will assign a different serial number than the 1900 date system. Because of this, dates must be checked for accuracy when exporting data from Excel - and even when just switching data from PCs to Macs (look for dates that are ~4 years off).















# Data-Visualization-Racing-Bar-Graph-with-Cricket-Data
Racing Bar Graph is one of the most interactive and dynamic visualization. In this, you will see how to get the cricket's updated data and creating so many visualizations. You'll also learn a bit of cleaning using Python's Pandas and Tableau.

Top 10 Male ODI Batsmen of Each Calendar Year by Score

Abstract

Cricket is the most favorite game in a few countries, e.g. Australia, India, England, Pakistan, West Indies, and New Zealand. The first One Day International match was played in 1971. This visualization project aims to show the top 10 batsmen who scored highest in a calendar year from 1971 to August 2019 and also tells which two teams played the first match, which year was the highest number of runs scored and by whom, and who scored the first thousand runs in a calendar year.
A racing bar graph is created that answers all the questions addressed. In 1971, the first ODI was played between Australia and England. The third team, West Indies, played its first ODI in 1973. The English Batsman DI Gower was the first cricketer to score a thousand runs in a calendar year. SR Tendulkar, an Indian Batsman, had set a benchmark of one thousand eight hundred ninety-four runs, in 1999, which is still unbroken.
	
1. Dataset

Once the project topic is decided, I went through various websites, viz. cricbuzz.com, cricket.com.au, and cricheroes.com, but I got the data of cricketers by country from espncricinfo.com. Initially, I gathered the data and made a separate excel file for each country. After creating 12 separate Excel sheets, I realized it’s not going to help to visualize what I exactly want to show as the data is completely unstructured. Then I googled and found the dataset from Kaggle [1] which was provided by espncricinfo.com.
The dataset is of 17 MB and seems to be structured with 171,969 number of rows and 29 number of columns. The different data types present are: 
1.	temporal: Innings Date
2.	Spatial: Country, Ground, Opposition
3.	Ordinal: Innings
4.	Nominal: Innings Player
5.	Interval: Innings Runs Scored Buckets, Innings Wickets Taken Buckets
6.	Ratio: Innings Runs Scored Num, Innings Minutes Batted, Innings Balls Faced, Innings Boundary Fours, Innings Boundary Sixes, Innings Batting Strike Rate, 50’s, 100’s, Innings Overs Bowled, Innings Maidens Bowled, Innings Runs Conceded, Innings Wickets Taken, 4 Wickets, 5 Wickets, 10 Wickets, Innings Economy Rate
7.	Boolean: Innings Batted Flag, Innings Not Out Flag, Innings Bowled Flag
8.	Hybrid: Innings Runs Scored – Since it includes both ratio and Boolean as it says the number of runs a batsman scored and whether he was not-out or he got out.
There are two aspects of big data in this dataset, the first volume, as there are 4,987,101 records available and the second one is velocity, because for 1971 there were only 44 rows, for 1972 it became 132, for 1973 it was 220 and for 2019 it increased to 4818 number of rows which is almost 110 times the first year, i.e. 1971.

2. Data Exploration, Processing, Cleaning and/or Integration

The dataset contains 4,987,101 records. The exploratory analysis is done using MINITAB and is shown below:
 
Explanation:
•	N is the number of non-empty rows
•	N* is the number of empty rows
•	CumN is the total number of rows
•	Percent is the percentage of available non-empty rows
•	Mean is the average value of the variables and SE Mean is the standard error of the mean
•	StDev is the standard deviation and Variance is the measure of the spread of each column
•	Q1 and Q3 are first and third quartile, Median is the middle value and Skewness is the measure of asymmetry.
Processing and Cleaning:
In order to show the top 10 batsmen by score each year from different countries, I need the name of the players, countries, flag-images of the country, and the total score in each year from 1971 to 2019. The source file has the date given in the column which is transposed to row using Tableau. The original CSV file has a number of NULL values, dashes, and strings in the ratio data type like DNB and TDNB. All such values have been replaced with zero using Pandas. An ipynb file has been attached that contains code for cleaning. The two cleaned CSV files have also been attached.

3. Visualization

Choice of Chart:
I have chosen a racing bar graph because I have to show the top 10 batsmen of each calendar year with their cumulative score in the year. A racing bar graph is preferred over a static bar graph because the static bar graph will limit the visualization to either top 10 batsmen of a year or the top batsman of each year. The bar graph will overcome this limitation.

Design Choices:
 

1.	Color – The color of the bars has been given based on the color of the team jersey in One Day International. The yellow color is chosen for Australia as the jersey color is yellow for them. Similarly, the sky-blue color is for India, red is for England, black is for New Zealand, lavender is for Zimbabwe, olive green is for Bangladesh, emerald green is for Ireland, dark green is for Pakistan, Persian blue is for Afghanistan, maroon is for West Indies, and royal blue is for Sri Lanka. The gray color has been used for the year.
2.	Shapes: There is a circular image within each bar which is the flag of each country participating.
3.	Marks: The vertical lines, that change the number written over them (in the video), are the marks that initially show the nearest tens of the score and then changes to the nearest hundreds that have been achieved in that particular year.
4.	Layout and Structure: The players’ names have been placed on the y-axis that keeps changing based on the number of runs and years. The x-axis has the number of runs and it changes based on the year. This means the player name depends upon the number of runs and years while the number of runs depends upon the years. There are legends that show the different countries with their jersey color. The right bottom is the year that is independent. The spacing between the two bars is 10 pixels.
5.	Font and Labels: The font used here is Source Sans Pro. The labeling is done for the names, scores of the batsman in a year and the countries.
6.	Animation: A racing bar graph has been created and the video file has been attached. The 10 different bars show the top 10 scorers of the calendar year being the topmost bar for the highest and bottommost for the lowest. In 1971, there are only yellow and red color bars available which show that these are the two countries who played their first One Day International. DI Gower was the first person to score more than 1000 runs in a calendar year in 1983.

 


In 1999, SR Tendulkar scored 1894 runs, which is still unbroken.
 

List of Tools or Libraries Used:
1.	Python: Pandas (a Python library) has been used to clean the file to remove the string and null values from the original file and derived file.
2.	Tableau: It is a visualization tool used to derive a new file where the years have been placed in columns.
3.	MINITAB: It is a data analysis tool used to do exploratory analysis.
4.	Flourish: An online website that is used to create a racing bar graph.

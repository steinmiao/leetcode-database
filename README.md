[TOC]

# README

## data source

You can get data in this [Google Sheet](https://docs.google.com/spreadsheets/d/1eGwwn8xsSjpNDwin2GyUEVs-omLqx1yirNhhHABpv30/edit#gid=357381750). The source of data is [UN Data](http://data.un.org/Data.aspx?q=fertility+rate&d=PopDiv&f=variableID%3a54). In the website you can download the data that you need and then upload it to the Google Sheet.

## How-to



### create a line chart

+ Upload the file you downloaed from UN Data website, then create a pivot table for it. the row is year, and the column is the country or area.
+ Insert a line chart. What should be paid attention to is x-axis is years and series are countries.

### as a picture

+ When you get the line chart, you can save it as an image. When you get the image path, you can insert it into the web page.

### as an iframe

+ click the 'Publish chart...' and you can choose the 'Embed' way to publish.
+ copy the code into the web page and then get the line chart as an \<iframe>

### using the Google Charts library

+ you can get the example of line chart in the Google Charts library, which are  very useful.
+ code location
  + you can put the javescript code \<script> in \<head> or \<body>.
+ add data
  + you can use the google.visualization.DataTable to create a data variable. and use the functions addColumn and addRows to add actual data. 

```javascript
var data = new google.visualization.DataTable();
data.addColumn('string', 'Years');
data.addColumn('number', 'Afghanistan');
data.addRows([
        ['1990-1995',  7.482],
      ]);
```

+ draw line chart
  + you can use google.charts.Line to create a chart variable, and by using document.getElementById to specify the div id.
  + then use draw function to draw the chart.

```javascript
var chart = new google.charts.Line(document.getElementById('linechart_material'));
chart.draw(data, google.charts.Line.convertOptions(options));
```



### web page 

+ I created a index.html file and inserted 4 \<div> in \<body>, which included explanation of the dataset and provenance and 3 charts.
+ the first div is fixed so the information can be viewed when you see all 3 charts.



## Why line chart?



Because the data contains time and different countries, the line chart can show the variation trend of different countries separately. What's more, you can also compare different countries' information. Therefore, I only use the line chart to show the data.

### 







# leetcode-database

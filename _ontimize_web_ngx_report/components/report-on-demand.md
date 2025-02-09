---
title: "Report on-demand"
permalink: /report/components/report-on-demand/overview
---
## Introduction

The module **Ontimize Web Report on-demand** allow the final users of the applications developed with Ontimize to define, view and store reports from any table available in the application.

This visual tool will allow users to define parameters of the report such as:

1.- Title and subtitle

2.- Orientation (vertical or horizontal)

3.- Style (draw grid, row numbers, column names, background on odd rows, hide group details, group in page and first group in page)

4.- Columns to print (allowing to order them and select for each column a title, a width and an alignment)

5.- Order by (allows sorting of report rows)

6.- Groups (allow grouping by columns)

7.- Functions (allows to perform functions on numerical values ​​(maximum, minimum, sum and average) and the total function)

8.- Preferences (allows to save a configuration, apply an existing one or update it)

>**NOTE:** Remember to complete the steps you need to perform on your backend server to complete the report on-demand configuration following this [link](https://ontimize.github.io/ontimize-boot/basics/reports/report-on-demand){:target="_blank"}

## Menu option

![Report on demand menu option]({{ "/images/report/menuOption.PNG" | absolute_url }}){: .comp-example-img}

## Basic example

This basic example shows a report with four columns, title and subtitle

![Report on-demand example ]({{ "/images/report/basicReportOnDemand.PNG" | absolute_url }}){: .comp-example-img}

## Grouping example

This example shows a report with four columns, grouped by one of them (customer type) and ordered by its name. In addition, a style with a background was added in the odd rows.

![Report on-demand grouping example]({{ "/images/report/reportGrouped.PNG" | absolute_url }}){: .comp-example-img}

## Aggregate functions example

This example shows a report with four columns, performing sum and average operations on two of them and showing the total number of rows. A style with row numbers and with a grid in the cells was also added

![Report on-demand aggregate functions example ]({{ "/images/report/reportNumericFunctions.PNG" | absolute_url }}){: .comp-example-img}

## Save and load configuration

The example shows the dialog to save a configuration of a report

![Report on-demand save configuration ]({{ "/images/report/saveConfiguration.PNG" | absolute_url }}){: .comp-example-img}


The example shows the dialog to select a previously stored configuration and perform a faster report

![Report on-demand load configuration ]({{ "/images/report/loadConfiguration.PNG" | absolute_url }}){: .comp-example-img}
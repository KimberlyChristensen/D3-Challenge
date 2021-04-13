# D3 Times

This project involved creating a JavaScript file and incorporating D3 elements, to reflect the relationship between rates of income, poverty, age, obesity, smoking, and access to healthcare, by state.  The data is from the 2014 ACS (American Community Survey) 1-year estimates, as reported by the [US Census Bureau](https://data.census.gov/cedsci/).

The project includes an index file for the html code, a css file, and the app.js JavaScript file. The visualization is run through the `python -m http.server`; which hosts the page at `localhost:8000` in the web browser (to avoid a CORS error).

### Scatter Plot

The project includes creation of a scatter plot to represent the relationship between two of the data variables, starting with `Obesity vs. Poverty`.

The scatter plot created represents each state with circle elements. This graphic was coded in the `app.js` file and pulls the data from `data.csv` by using the `d3.csv` function. 

The axes and labels were adjusted to align to the left and bottom of the chart.

### Additional Interactivity

In addition to the `Obesity vs. Poverty` view, a user can select a different X Axis (Poverty, Income, or Age) and/or a different Y Axis (Obesity, Smoking Rate, and Lack of Healthcare).  When a new value is selected (clicked), the chart updates to reflect the selected data.

The code includes transitions for the circles' locations and the range of the axes.

### Incorporation of d3-tips
The project incorporates d3-tips using the `d3-tip.js` plugin developed by [Justin Palmer](https://github.com/Caged).  These tips allow the user to see the data points represented by each circle, including the state and values (e.g. Obesity % and In Poverty %).
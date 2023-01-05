# Create budgeting/personal finance calendar heatmaps of spending over the year 

## Motivation
One of my hobbies include analyzing personal finance metrics and finding trends in my personal spending data throughout the year. I use a custom budgeting spreadsheet on Google Sheets to track every expense on everyday of the year. This tool is to help me visualize my spending habits, how often I spend money, streaks of spending, and amount spent per day.

## How to use

I found calmap in a [blog](https://pythonhosted.org/calmap/) and wanted to try it out. The notebook takes in the excel file that I downloaded from GSheets, reads in the summary sheets using a fixed range, concatenate each month's dataframe, and create a sum column from the categories. This is then simply fed into calmap to create a heatmap.

## Example 

The inputs are Google Sheets that look like the picture below. One for each month. This is the summary view of the month whereas the daily recorded transactions are on another sheet. 

![Budget Template](budget_template.png?raw=true "Title")

After exporting the workbook and reading in each summary sheet using pandas dataframes, I concatenated them and created a simple dataset to feed the heatmap. 

Example Heatmap 1 - Spend or No Spend for each day of the year 

![Binary Heatmap](spend_binary.png?raw=true "Binary")

Example Heatmap 2 - Heapmap with a gradient for amount spent based on a range

![Gradient Heatmap](spend_0_500.png?raw=true "0_500")
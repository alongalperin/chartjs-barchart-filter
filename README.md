I want to share with you a small adjustment I made for my project with the bar chart in Chart.JS library.  
  
The result I wanted to achieve was to be able to filter specific bars from the chart.  
  
This is the original use with the legend that comes with ChartJS:  
Link:
<img src="images/1.gif" width="500" height="350" />
  
The result I wanted:  
Link: https://jsfiddle.net/ze7xwnLv/
<img src="images/2.gif" width="500" height="350" />
  
I uploaded here example files.  

Explanation regarding the solution:
A. First I get all the data to sit in global variables.  
We have 4 lists:
1. Data- list of the data "the numbers"
2. Labels- list of labels for X-axis labels
3. Colors- list of colors, the bars getting their colors according to this list.
4. isHidden- list of boolean, each boolean represent if the bar is hidden or not. The array first initialized with all 'false', because all the bars are shown at the begining.

```
let globalLabels = ['January', 'February', 'March', 'April', 'May', 'June', 'July']

const numberOfBars = globalLabels.length

let globalColors = ['#9ACD32', '#1E90FF', '#F08080', '#7B68EE', '#808000', '#2F4F4F', '	#F08080']

let globalData = [10, 20, 15, 18,5, 7, 25]

let globalHidden = []
for (let i = 0; i < numberOfBars; i += 1) {
	globalHidden.push(false)
}
```

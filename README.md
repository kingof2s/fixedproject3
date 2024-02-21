<h1>Design Overview</h1>
For our dataset, we wanted to see if there was any correlation between a country's median population age and the age of its leader. Since the two variables are both quantitative, we decided that a scatterplot would be the best way to show a correlation (if any).

<br>
We have around 173 data points, so labelling all of them individually at once would be extremely confusing, so we decided to add interaction by creating a mouseover tooltip that shows the details of each country. 

<br>
We thought the graph was initially quite boring and undescriptive, so we decided to create a color scheme based around the country regions to help viewers identify "trends" within regions. After adding the colors,
we realized we could make the visualization even more interesting and interactive by letting the viewers filter data points by region. 

<br>
We had some other ideas that we scrapped along the way. The first one was that of adding interactive trendlines; when we took a look at the data, we realized that there really wasn't a major trend, as median_age and leader_age appeared to have little correlation. We thought it would be more misleading to add a meaningless trend line, so we scrapped the idea.

<h1>Development process:</h1>

David - I created the scatterplot visualization 
in App.svelte and setup the interaction functionality. I'd say I spent around 10 hours 
on this, but the majority of the time was trying to figure out how to use d3 and integrate 
it with the github. After fixing technical errors and looking through d3 and svelte 
documentation and videos, creating the visualization and interaction itself took 
considerably shorter.

Dhilan - I used Python requests and BeautifulSoup4 to webscrape the country leader data from various websites and compiled it into a csv file. Then, I added upon David's code by reformatting the HTML aspect of it, as well as adding QoL (Quality of Life) features such as: 
* Moving the legends to the right hand side instead of underneath
* Greying out the filtered out regions, and un-greying them when the filter is removed.
* Move the tooltip to dynamically follow the cursor position, instead of as a static text box 
* Add a custom search box that filters dots based on country name

The web scraping and the QoL part both took about 4 hours, though I'm already familiar with web scraping so most of it is just figuring out how to parse the website HTML. The QoL part was more memory-intensive for my brain since I had to look up and try out a lot of new things.
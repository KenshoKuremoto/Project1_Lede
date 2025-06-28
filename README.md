# Project01
This is project-01 for the Lede Program.  
Link to the project-01:https://kenshokuremoto.github.io/Project1_Lede/

GitHub repository for data:https://github.com/KenshoKuremoto/Lede_Proect1_CCI

## Title
**Too Flawed to Save, or Too Hasty to Scrap?**  
Why Japan Killed Its 70-Year-Old Rice Index — and Whether the Numbers Justified It

## Aim
I'm a political journalist from Japan, so I wanted to explore a hot topic in Japanese politics. Right now, there’s a major public issue: the price of rice, our national staple, has skyrocketed to an unprecedented level.  
To tackle this, a political "prince" was appointed as the Minister of Agriculture. One of his boldest moves was announcing the abolishment of a 70-year-old government metric called the “Crop Condition Index,” saying it no longer reflected reality.  
This decision has sparked debate. Was the index truly outdated, or was it scrapped too hastily? I wanted to investigate this by analyzing 35 years of publicly available data to see whether the metric actually failed to reflect reality.  
On the technical side, I set goals to become proficient in visualization tools like Datawrapper and Flourish, and to learn how to build scroll-based storytelling content. I believe I successfully met both objectives.

## Findings
Within the scope of the public data analyzed, I found that the Crop Condition Index correlated reasonably well with harvest volume and price until around 2010. After that, it no longer aligned with those indicators.  
This matches both the minister’s reasoning for abolishing the index and the impressions of those in the field.  
On the technical side, I significantly improved my skills with Datawrapper and Flourish, and gained a solid understanding of their respective strengths and weaknesses.  
I also achieved one of my key goals in the Lede Program: building a full scroll-based storytelling page from scratch using HTML. More on that in the next section.

## Data Collection Process
I gathered three types of data:

1. **Rice Production Data**  
   Japan's official statistics database, [e-Stat](https://www.e-stat.go.jp/en), offers a long-term dataset on rice production.  
   I downloaded 70 years of data on the Crop Condition Index, harvest volume, and cultivated area.  
   [Crop Condition Index dataset](https://www.e-stat.go.jp/stat-search/files?page=1&layout=datalist&toukei=00500215&tstat=000001013427&cycle=7&year=20240&month=0&tclass1=000001032288&tclass2=000001032753&tclass3=000001226221&tclass4val=0)

2. **Consumer Price Index (CPI)**  
   I obtained both annual and monthly CPI data from [e-Stat](https://www.e-stat.go.jp/en).  
   I used annual data until 2024 and merged it with monthly data for 2025.  
   [CPI dataset](https://www.e-stat.go.jp/stat-search/files?page=1&layout=datalist&toukei=00200573&tstat=000001150147&cycle=1&year=20250&month=12040605&tclass1=000001150149&result_back=1&tclass2val=0)

3. **Recent Rice Price Trends**  
   Japan’s Ministry of Agriculture has a special page called  
   ["Current Rice Distribution Situation"](https://www.maff.go.jp/j/syouan/keikaku/soukatu/r6_kome_ryutu.html#hanbai).  
   Unfortunately, it only provides PDF charts, so I manually extracted average prices (overall, branded, and stockpiled rice) from the graphs and converted them into Excel.

## Data Analysis Process

### ① Pandas
Using Jupyter Notebook and Pandas, I explored the data through the following steps:

- **Three-variable time series**: CCI and cultivated area (line), harvest volume (bar)  
- **Two-variable scatter plots**: CCI vs cultivated area and harvest volume  
- **Merged time series**: annual CPI + monthly CPI in one graph  
- **Basic scatter plot**: CPI vs CCI  
- **Enhanced scatter plot**: CPI vs CCI with harvest volume as bubble size  

After several iterations, the two most effective visuals were:

- A combined line-bar chart showing CCI and harvest volume  
- A bubble chart plotting CPI vs CCI, with harvest volume represented by bubble size  

Final visualizations were created in Datawrapper and Flourish.

### ② Datawrapper
In Datawrapper, I created:

- A line graph showing CPI trends for key commodities  
- A line graph showing recent rice price trends  

While it doesn't support multi-variable plotting, it allows detailed annotations, line emphasis, and SVG export for Illustrator—making it well-suited for these charts.

### ③ Flourish
In Flourish, I created:

- A combined line-bar chart showing CCI and harvest volume  
- A bubble chart showing CPI vs CCI with bubble size as harvest volume  

Although I had limited prior experience, this project helped me fully grasp how Flourish works.  
It has fewer annotation features and limited map options (especially in Asia), but it excels at combining multiple variables in a single graphic.

## New Skills and Growth

Although I had only one month of experience, I saw real growth in the following areas:

### ① Pandas (Python)
I learned to efficiently analyze CSV/Excel data and generate custom charts.  
Pandas allows for visualizations that neither Excel nor Flourish/Datawrapper can handle—such as three-variable graphs.  
It’s now one of my most valuable tools.

### ② Datawrapper / Flourish
I now use both tools with a clear sense of their strengths and purposes.

### ③ Adobe Illustrator
Though I previously relied on PowerPoint for most design tasks, I gained foundational Illustrator skills through this project.  
There are still moments where I think “this would be easier in PowerPoint,” but I now understand Illustrator's unique capabilities.

### ④ HTML / CSS
Thanks to [Soma’s template](https://jsoma.github.io/page-templates/scrolly-images/index.html), I was able to recreate a scrollytelling experience.  
Since iframe-based charts don’t allow internal animation, I stacked several charts with the same layout and triggered transitions via scroll.  
This allowed for dynamic, text-responsive graphics.

And one more important thing: I became best friends with ChatGPT.

## Future Work
This project was created to consolidate everything I learned in the first month of the Lede Program. I don’t plan to expand it further.  
However, the skills I gained here will absolutely be applied in my next project.  
Next, I plan to use Mapbox to explore storytelling through interactive maps.

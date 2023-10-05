# Data512-HW1
Zachary Bowyer  
10/4/2023  
University Of Washington  
Data 512  

# Goal of the project
The goal of this project is to provide myself with practice on how to create reproducible research.  
This means adhering to a guideline of documentation, storage, and data generation practices outlined in http://www.practicereproducibleresearch.org/core-chapters/3-basic.html.  

Beyond the high-level goal, the specific task of this project is to construct, analyze, and publish a   dataset of monthly article traffic for a select set of pages from English Wikipedia from July 1, 2015   through September 30, 2023. Again, the purpose of the assignment is to develop and follow best practices for open scientific research. 

# License of source data
By using the Wikimedia REST API present in this code, you agree to Wikimedia's Terms of Use and Privacy  
 Policy. Unless otherwise specified in the endpoint documentation below, content accessed via this API  
  is licensed under the CC-BY-SA 3.0 and GFDL licenses, and you irrevocably agree to release   
  modifications or additions made through this API under these licenses. See https://www.mediawiki.org/  
  wiki/REST_API for background and details.  

# License of part of the software
Some code, which is properly referenced in it's respective location  
was developed by Dr. David W. McDonald for use in DATA 512, a course in the UW MS Data Science degree 
  program. This code is provided under the [Creative Commons](https://creativecommons.org) [CC-BY   
  license](https://creativecommons.org/licenses/by/4.0/). Revision 1.2 - August 14, 2023. Some of the  
  original code made be modified, however it still falls under the Creative Commons license.  
  
# Link to Wikimedia Foundation REST API terms of use:
https://www.mediawiki.org/wiki/API:REST_API#Terms_and_conditions  

# Link to Wikimedia API documentation
https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews  
https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end  

# All files and descriptions: 
/Data/academy_monthly_cumulative_201501-202309 - JSON file storing mobile+desktop article viewcounts for each month    
/Data/academy_monthly_desktop-202309 - JSON file storing desktop article viewcounts for each month  
/Data/academy_monthly_mobile_201501-202309 - JSON file storing mobile article viewcounts for each month    
/Data/ArticleNames.csv - CSV file storing the name and url of 1359 wikipedia articles     
/Results/FewestMonths.png - Time series graph of the top 10 articles with the fewest amount of recorded months for both desktop and mobile     
/Results/MinMaxAverages.png - Time series graph of the articles that have the highest and lowest average monthly viewership for both desktop and mobile.    
/Results/PeakViewership.png - Timeseries graphs of the top 10 articles that have the highest peak viewership for both desktop and mobile.   
/Src/CreateDatasets.ipynb - Jupyter notebook where data from ArticlesNames.csv is used combined with the wikimedia API to store monthly viewership results into the the json files located in the Data directory.    
/Src/VisualAnalysis.ipynb - Jupyter notebook where JSON file data is used to create the visualizations found in the Results directory.     
/Src/wp_article_views_example.ipynb - Jupyter notebook used as a template to use the wikimedia API.      
.gitingore - File used to exclude files from version control.     
README.md - This file, used for documentation and explanability.     
LICENSE - License file.     

# Notes for researchers
1. Data must be URI encoded when sent to the Wikimedia API. For example the character '/' should be encoded as '%2F'.  
2. Some months for articles have a viewership value of 0. In my case I included them in analysis, but it's ultimately up to you if you want them removed.  
3. Some of the code for the use of the Wikimedia API is under the creative commons license.  
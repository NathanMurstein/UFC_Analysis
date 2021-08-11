# UFC_Analysis

View main code and content in UFC_Analysis-NM.ipynb

If you wish to run the code yourself, I have added supporting files to the folder:

    1.	Run all imports at the top of the notebook 
    2.	I highly recommend not running SECTIONS 1.1 and 1.2 since they involve scraping and wrangling data that can take hours. When I ran
        them, I saved all the data into a pickle which is accessed on cell 8 where it says ‘START HERE’. Download ufc_master.pickle and start
        at cell 8. However, if you do want to run the previous cells, here is how:
        a.	Run second cell to read in ufc_master data (you may have to change the path):
            i.	Download dataset here: https://www.kaggle.com/mdabbert/ultimate-ufc-dataset
        b.	Scrape from Tapology.com at your own risk - this takes a long time and got me temporarily banned from their website. I should have
            automated pauses between page clicks.
        c.	Run cell 4 to read in supplementary data (you may have to change the path):
            i.	Download dataset here if needed: https://www.kaggle.com/calmdownkarm/ufcdataset
        d.	Run all subsequent cells
    3.	Now you should be able to run all subsequent cells in the notebook.
        a.	If you run into a GraphViz error when plotting the decision trees, download the package form here (https://graphviz.org/download/) and it should work.

Project Information:

Research Questions:
1.	Does “home field advantage” really exist in the UFC, and is the effect of fighting closer to one’s home city statistically significant?
2.	Do fight stance and attack volume affect the long-term success of a UFC fighter over their career?
3.	How accurately can a machine learning model predict the outcome of a UFC fight based on the aforementioned factors?

Motivation:
Predicting UFC fight outcomes and analyzing the underlying factors could be useful to both fighters and bettors. For fighters, understanding
what successful fighters statistically look like can help them design training programs, and predicting fight outcomes can help them accept 
favorable matchups. For bettors, predicting fight outcomes can help them place bets that will yield the highest possible success rate.

Dataset:
I will use the ‘Ultimate UFC Dataset’ from Kaggle. The dataset can be found at https://www.kaggle.com/mdabbert/ultimate-ufc-dataset/code. 
To calculate distance between home city and fight location, I scraped data from tapology.com using Selenium to automate searches, 
however I overused the site (I should have built in delays in queries) and my IP address was banned, so I had to combine the location 
data with this dataset: https://www.kaggle.com/calmdownkarm/ufcdataset . Combined, I was only missing location data for roughly 5% of rows.  

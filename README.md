# MICROSOFT MOVIE WORLD PROJECT

Student Name : Faithtesy Leo

PROJECT OVERVIEW

Microsoft has announced that they would like to get into the movie industry. They will be creating a studio, however they have no knowledge of the movie industry. Our goal is to collect, clean, and analyze movie data from a variety of sources so that we can provide recommendations to Microsoft that will allow them to be successful in the movie industry.

EXPLORATION OF DATA

The data that was used for this step can be found in the link below:

http://localhost:8888/edit/tn.movie_budgets.csv

http://localhost:8888/edit/tn.title.basics.csv

During the analysis, i looked into the question below which would help Microsoft be successful in the movie industry.

ANALYSIS QUESTION:
1.Which movies generate the highest profits and how much money should be spent for the budget to ensure success.
2.What genres of movies are majorly produced and whats their relation to the profit

QUESTION ONE
To answer this question and provide a recommendation we'll make use of a budgets dataframe called movie_budgets.csv. Our analysis will require that we use the data to calculate profit and profit margin whhich we will further access to determine the most profitable movies.
I calculatded the profit of the movies and added a column to the budget dataframe by finding the difference between the production budget and worldwide gross 
new_budgets_dataframe['Profit'] = new_budgets_dataframe['worldwide_gross'] - new_budgets_dataframe['Production_budget']

``new_budgets_dataframe['Profit_Margin'] = (new_budgets_dataframef['worldwide_gross'] - 
                                   new_budgets_dataframe['production_budget'])/new_budgets_dataframe['worldwide_gross']``
``new_budgets_dataframe['Profit_Margin'] = (new_budgets_dataframe['worldwide_gross'] - 
                                    new_budgets_dataframe['production_budget'])/new_budgets_dataframe['worldwide_gross']``
                                    
I further explored the 20 most profitable movies to understand their way of budgetting while also considering the outliers.

findings:
       The 20 top most successful movies have a median profit margin of 86.05% with a median budget of $200,000,000.
       
Further to this, i filtered data that had more than 75% profit margin and a budget of more than 21000000 in order to investigate the trends in regards to the budget and profit margin.
       
Recommendation: I recommend that microsoft should put a budget of 50,000,000 which corresponds to a 81.93 percent profit margin.

QUESTION TWO

What genres of movies are majorly produced and whats their relation to the profit
in order to answer tthis question , i looked into the median net profit and profit margin for every movie genre after grouping by genre.
i ddnt use the mean due to the possibility of outliers within the data.
lastly, i look at the percent of net profit by genre. THis steps will help microsoft to decide on how to budget in regards to the different genres as it will potray the profitability of evry genre.

Question 2 recommendation: I recommend that Microsoft should focus their efforts on the top 6 most profitable movie genres: Adventure, Action, Comedy, Drama, Sci-Fi and Animation.  

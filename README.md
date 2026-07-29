# ai_classification_of_nyt_bestsellers

Readme

This repo contains the data behind my project “Have we reached peak romance?” which explores the prominence of romance titles on the New York Times best seller list.

The finished writeup can be found here:

This project was created as part of the Lede Program run by Jonathan Soma at Columbia Journalism School. My personal intention was to create an individual project to become more familiar with Jeremy B. Merrill’s template for AI analysis which was taught as part of the program.

The repo is split into two sub-repos: “docs” and “analysis.” Docs contains the html for the above linked article. 

“Analysis” contains the following Notebooks:

data_gathering.ipynb: The code I used to query the New York Times' API to gather the list of print and e-book fiction best sellers for every week between Jan. 2016 and the end of June 2026. The code includes calls for older data, but this time frame is the only data that was ultimately analysed. This Notebook feeds data into the “raw_data” folder.

data_merging.ipynb: Uses pandas to clean and merge the data gathered into a data set of titles that the AI model would analyse. This involved removing missing values, filtering by date, and filtering for unique data. This Notebook fed data into the “raw_data” and “data_for_analysis” folders.

data_classification_ai_genre.ipynb: This adapts Jeremy B. Merrill’s template for AI Text Classification and Quantitative Evaluation. In it I use the GPT 5.4 Mini AI to classify the 2,137 unique titles in this data set as romance or non-romance novels based on their listed title and description. I refined my prompt to improve the model’s accuracy when compared to a handcoded sample of 100 titles. The accuracy rate of the prompt used for this analysis was 97%, based on this handcoded sample. The Notebook feeds data into the “data_for_analysis” folder.

data_analysis.ipynb: This Notebook maps the AI classification given to each book onto the wider best seller data from the past decade. It then analyses the data based on time, author, and title variables to establish any trends in the genre’s popularity. The Notebook feeds data into the “chart_data” folder to create graphics for the final document.

Limitations 
I did this analysis to learn AI classification for data journalism. There are many features that could be improved in future attempts. 
* Classification of books as purely romance or non-romance novels does not allow for more nuanced categories like romantasy to be quantified, and can result in debateable categorisations.
* While the model has an accuracy rate of 97 percent, this is based on a small handcoded sample which should be increased in size in future projects.


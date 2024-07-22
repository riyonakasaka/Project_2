# Project02
This is project-02 for the lede program.
<br>
Link to the project-02 (https://riyonakasaka.github.io/Project_2/)

## Title
Analysis of Prime Minister Kishida's Domestic Dining Engagements
<br>
Exploring Prime Minister Kishida's Administration: October 5, 2021 to July 9, 2024

## Aim
In Japan, the Prime Minister's activities are meticulously recorded down to the minute. 
This analysis focuses on Prime Minister Kishida's domestic dining engagements to provide insights into his trends and patterns.

## Findings
During periods of reduced dining engagements, correlations were found with factors such as increased COVID-19 infection rates, the Prime Minister's health status, and political scandals within the Prime Minister's party.　Detailed analysis of the individuals frequently dining with the Prime Minister provided deeper insights into his associations and contributed to a better understanding of his activities.

## Data Collection Process
1.Scraped Prime Minister's activities from Nikkei Shimbun and used MeCab to count the nouns.

2.Scraped Nikkei Shimbun's "Prime Minister's Activities" Website:
All articles from the "Prime Minister's Activities" section on the Nikkei Shimbun website were scraped to collect comprehensive data(https://www.nikkei.com/topics/22041100).

3.Tokyo Metropolitan Government Data:
Data on the number of COVID-19 infections from January 2020 to May 2023 was collected from official announcements and publications by the Tokyo Metropolitan Government(https://catalog.data.metro.tokyo.lg.jp/dataset/t000055d0000000397).

4.The Cabinet approval ratings were obtained from this link(https://vdata.nikkei.com/newsgraphics/cabinet-approval-rating/).

## Data Analysis Process
1-1.Data Cleaning from Nikkei Shimbun's "Prime Minister's Activities" Website(scrapping.ipynb): Scraped data from the Nikkei Shimbun's "Prime Minister's Activities" website required cleaning due to formatting issues and extraneous characters. Specifically, I filtered articles containing the keyword '会食' (dining engagements in Japanese) and extracted relevant text.

1-2.Classification of Dining Engagements(lunchdinner.ipynb): I classified the dining engagements into 'Lunch Meetings' and 'Dinner Meetings'. Lunch meetings typically occur between 11:00 and 13:00, so I divided the data into rows containing keywords '11時', '12時', '13時' (indicating lunchtime) and those that did not. Total counts were calculated for each category.()


1-3.Japanese Text Analysis using MeCab(mecab.ipynb): I utilized MeCab for Japanese text analysis on the cleaned DataFrame from step 1-1. MeCab was installed to count the occurrences of nouns within the DataFrame. Prior to counting, preprocessing involved filtering to ensure accurate counting of the same individuals despite variations in title, first name, and last name segmentation by MeCab.

2.Visualization of Tokyo Metropolitan Open Data(130001_tokyo_covid19_patients_per_report_date.csv): Tokyo Metropolitan open data, saved in CSV format, was graphically represented to illustrate relevant trends or patterns.

## New Skills and Growth

1.Scraping from Multiple Pages:　I developed a new skill in scraping multiple pages, which was not covered in our coursework. This allowed me to efficiently gather comprehensive data from diverse sources for this project.

2.Japanese Text Analysis with MeCab: I installed and employed MeCab for Japanese text analysis, which played a crucial role in conducting the analysis for this project. This tool enabled accurate parsing and counting of Japanese text elements, enhancing the depth of our findings.

3.Created a Scrollable Chart and Customizing Colors in Flourish.

## Future Work
1.Alternative Tool for Japanese Text Analysis: While MeCab was effective, its fine segmentation necessitated considerable preprocessing time for filtering. In future Japanese text analysis, I intend to explore alternative tools that can simplify this process and improve efficiency.

2.Enhanced Mapping of Dining Engagements: This project primarily focused on analyzing the frequency of dining engagements, timing, and participants. For future endeavors, I plan to create detailed maps illustrating specific restaurants visited, frequency of visits, and accompanying individuals. This visualization will offer a more comprehensive and insightful view of dining patterns during the analyzed period.

3.Improving Data Cleaning for Prime Minister's Activities: The cleaning process for the Prime Minister's activities data remains incomplete. Moving forward, I aim to further refine this process to create a more diverse and analytically robust DataFrame. This will enable a broader range of analyses and enhance the overall quality of insights derived from the data.

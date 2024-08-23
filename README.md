# Web_Scraping
Here, it is required to scrape some details regarding journals from given link (https://journals.sagepub.com/toc/JMX/current) such as title, authors and affiliations, first published date, DOI, abstract.
There is total number of 9 journals listed in the page, including title, authors, first published date. However, for details such as full abstract and DOI one has to follow the hyperlink of title.
My approach,
1. Getting access to website.
Due to the security system preventing bots from scraping the page, I've experimented with several approaches, including using different user-agents, Selenium, and inspecting request headers directly in the web browser. I was able to solve the issue by utilizing Zenrows with a customized api-key. 
2. Parsing the page with beautifulsoup.
3. Finding the class in which all journals are listed, which is ‘table-of-content’.
4. Extract all the hyperlinks of each article.
5. Now we just need to loop over each link and extract relevant details in each page.
6. All the details such as title, authors, first published date, DOI, abstract details are 
extracted with relevant tags, property, class, role to uniquely find the exact detail.
7. With each loop update all these in the dictionary.
8. Convert the dictionary to dataframe using pandas.
9. Download csv from dataframe using to_csv

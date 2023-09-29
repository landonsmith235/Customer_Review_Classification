![alt text](https://github.com/landonsmith235/Customer_Review_Classification/blob/fcc6833573fb3339df475dc4ccbe9b44c75a97ed/Images/title_slide.jpg)

## **Overview**
A common practice performed by restaurant management is analyzing customer reviews posted on websites like OpenTable and Yelp in order to gain insights into how to improve the operation of their business. Customer reviews have the potential to offer feedback to restaurant management on a wide variety of topics, such as quality of food and service, ambience, and countless others. According to the 2022 Local Consumer Review Survey, 98% of consumers look at restaurant/cafe reviews before deciding where to eat, meaning restaurants have a vested interest in improving their operations to improve the reviews they receive online, thereby increasing customer traffic. However, a large portion of the reviews restaurant management accesses online are far too vague to be actionable by restaurant management due to the reviews lacking specificity. The monotonous task of sifting through reviews that lack constructive content is time intensive for restaurant management and by extension, detracts from the overall productivity of the business. The goal of this project is to create a machine learning model that can parse customer reviews to automate the process of identifying actionable customer reviews, empowering restaurant management with a tool to analyze their customers' reviews with far more time efficiency.

## **Technologies Utilized** 
OpenAI API

Python Libraries
* pandas
* numpy
* bs4 (BeautifulSoup)
* selenium
* time
* openai
* matplotlib
* seaborn
* sklearn
* tensorflow
* keras
* re (Regular Expression)
* wordcloud
* gensim (Latent Dirichlet Allocation Model)
* nltk
  
## **Relevant Repository Contents & Descriptions**

### **Presentation.pptx**
This file is a Microsoft PowerPoint presentation that provides an overview of the methodologies utilized throughout the project. 

### **Report.docx**
This file is a Microsoft Word document that serves as a more granular explanation of the methodologies discussed in the aforementioned PowerPoint presentation.

### **Code.ipynb**
This file contains all of the code utilized to perform the following tasks:
* Web Scraping Customer Reviews from OpenTable and Yelp
* Data Cleaning for Reviews
* Review Actionability Classification using gpt-3.5-turbo LLM via OpenAI API
* Custom Machine Learning Model Creation (Logistic Regression, Random Forest, Deep Neural Network)
* Latent Dirichlet Allocation (LDA) NLP Framework for Review Grouping
  
### **Datasets Folder**
This folder contains two datasets created within our Code.ipynb file referenced above. The first dataset, titled Classified Review Dataset.csv, was created by feeding each web scraped review to the OpenAI API and asking the gpt-3.5-turbo LLM to classify the review as either a 0 (actionable) or a 1 (not actionable). Our second dataset, titled Identical Actionabilty Dataset.csv, was created after we discovered classification stochasticity present between the models responses despite theprompt and supplied review being identical. In an attempt to ensure greater label confidence, we consolidated 1,000 reviews where the gpt-3.5-turbo LLM had classified the review the same way five times in a row into the Identical Actionabilty Dataset. This process is further outlined in the report and PowerPoint slides. 

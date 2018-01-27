# AI-Law-Minicourse-HW
## notes
### Step 1 - Data Collecion & Preparation
Import all necessary packages from anaconda into the python kernel.
Creating a list of Supreme Court cases. The code creates a link to the repository which has all the Supreme Court cases.
Next, it assigns a variable: they are adding to root_url the link and the year so that they have all the URLs for each year.
Beautiful_soup_grabber is a method to make it easier to handle the data. The code is creating methods to go through data: method to run through all the documents on the website.
Next step is defining a method for each year within the range you've requested and convert result object into a loop that runs through all the data and it helps to collect the data. To "year_getter" you define a year you wish to search.
Panda is used to convert data to a table structure. This step is collacting data to a table form.
Next steps relates to testing the code and the result to see how it works and what it looks like. Converting the test results.

### Step 2 - Data Collection & Preparation
Code imports the necessary packages into the python kernel. 
pd.read_pickle("supcourt_yearlist.pickle"). Framework that is used to put data in other shape. Reads the data which was imported.
Code is splitting the dataframe into three dataframes. 
Collecting the data?
The code is putting data (ie. different supreme court cases) into different pickles. 
Then code is putting the result together "full_project = pd.concat([test2_df, test3_df, test_df]) #putting it all together" by combining previous steps. 
Then code is displaying the outcome.
Lastly saving the data by preprocessing it "full_proj_preproc.pickle"

### Step 3 - Data Processin
Code to install spacy.
Code imports the installed packages.
Code is creating a list for stop words i.e. high frequency words that are wanted to filter out. 
Defining homespun wordlist: code is setting a stoplist an defining the words. 
Code is adding all stoplist words together and creating a stoplist which is used for this code. Tokenizing the text. Next step is to clean the words by applying stoplist.

### Step 4 - Topic Modeling Method Testing
The method "modeler" runs a modell and then prints out the topwords with the method "print_top_words" to show the results.

It tests the methods LDA, NMF and LSA and adjusts some features within.
NMF proofed to be the best fit for this task because it allows do differentiate different fields of law and not just "law" and "not law" like LSA.

### Step 5 - Topic Model Application to Data
Model is run against the entire dataframe to get the different topics. 
The result are then used to create a document-score for each topic. 
The next step creates a dictionary to look up topics.
This dictionary is used to look up the words for each topics.
In last step the code is arranging the data to a vizual form.

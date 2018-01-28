# AI-Law-Minicourse-HW
## notes
### Step 1 - Data Collecion & Preparation
Firstly, the code is importing all necessary packages from anaconda into the python kernel.
The Code creates a list of Supreme Court cases. The code creates a link to the repository which has all the Supreme Court cases.
Next, it assigns the URL of the repository of Supreme court ruling opinions to the variable: they are adding to root_url the link and the year so that they have all the URLs for each year.
Beautiful_soup_grabber is a method to make it easier to handle the data. 
Next, the software creates a one-dimensional array "years" with the URLs of the years to explore. The Methode "Beautiful_soup_grabber" pulls the data from a given website into a nested data structure. The Methode "year_getter" then usese "beautiful_soup_grabber" and the array "years" in a loop to get the data for every document in the repository. The result is a data_frame table. A new variable is then filled with the results from "year_getter".
Next steps relates to testing the code and the result to see how it works and what it looks like. Converting the test results.

### Step 2 - Data Collection & Preparation
Code imports the necessary packages into the python kernel. 
"pd.read_pickle("supcourt_yearlist.pickle")" is a framework that is used to put data in other shape. The code reads in the output from the previous step and splits it up to prevent caselaw from blocking your ip for "spaming".

The method "supcourtdescr" collects the case details from URLs with a loop. 
The code is putting data (ie. different supreme court cases) into different pickles. 
Then code is putting the result together "full_project = pd.concat([test2_df, test3_df, test_df]) #putting it all together" by combining previous steps. In other words, all cases are added to the table.
Then code is displaying the outcome.
Lastly saving the data in a pickel file and preprocessing it "full_proj_preproc.pickle"

### Step 3 - Data Processing
Code to install spacy and imports the installed packages. This step cleans the data from unnecessary or "harmful" wrods with spacy.
Code is creating a list for stop words i.e. high frequency words that are wanted to filter out such as common stop wrods, statenames, parties' names.
Defining homespun wordlist: code is setting a stoplist an defining the words. 
All lists are then combined to the list "STOPLIST": the code is adding all stoplist words together and creating a stoplist which is used for this code. Tokenizing the text. Next step is to clean the words by applying stoplist.
In the end, the results are saved in a pickle file.

### Step 4 - Topic Modeling Method Testing
The method "modeler" runs a modell and then prints out the topwords with the methode "print_top_words" to show the results. It tests the following methods: LDA, NMF and LSA. NMF proofed to be the best fit for this task because it allows do differentiate different fields of law and not just "law" and "not law" like LSA.

### Step 5 - Topic Model Application to Data
Model is run against the entire dataframe to get the different topics. 
The result are then used to create a document-score for each topic. The higher the number of each topic's document-score means that it is more likely in that category.
The next step creates a dictionary to look up the top words for each topic.
This dictionary is used to look up these words in each item.
In last step the code is arranging the data to a visual form: the number of cases for each topic and year is put in a visual graphic form.

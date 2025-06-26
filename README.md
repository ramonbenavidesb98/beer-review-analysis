==============================================
Uncovering Consumer Preferences Through Beer Review Analytics
==============================================

DESCRIPTION
-----------
Welcome to our Beer Review Analysis project! 

This user guide provides instructions on how to set up and run the code contained in the `cse6242_project_code.ipynb` Jupyter notebook. 

Our project aims to uncover consumer preferences in the craft beer market by analyzing a dataset of 1.5 million beer reviews. Through this analysis, we aim to identify key factors influencing consumer choices, segment consumers based on preferences, investigate geographical influences, and provide actionable insights for breweries, marketers, and beer enthusiasts.

Data Source Description
The dataset used in this analysis includes several features capturing various aspects of beer reviews

The original dataset can be found under the following link:
https://www.kaggle.com/datasets/rdoume/beerreviews

We then used the Google Places API to enrich the original dataset with latitude and longitude coordinates for each brewery. We used the kagglehub Python package to programmatically download the dataset within the notebook:

import kagglehub

Download latest version of the dataset
path = kagglehub.dataset_download("rdoume/beerreviews")

Dataset variables description:

Brewery_id - Unique identifier for the brewery.
Brewery_name - Name of the brewery.
Review_time - Timestamp of the review in Unix time format.
Review_overall - Overall rating given by the reviewer.
Review_aroma - Rating for the aroma of the beer.
Review_appearance - Rating for the appearance of the beer.
Review_profilename - Profile name of the reviewer.
Beer_style - Style of the beer being reviewed.
Review_palate - Rating for the palate of the beer.
Review_taste - Rating for the taste of the beer.
Beer_name - Beer name.
Beer_abv - Alcohol By Volume (ABV) of the beer.
Beer_beerid - Unique identifier for the beer.
Latitude - Latitude coordinate of the brewery obtained through the Google Places API.
Longitude - Longitude coordinate of the brewery obtained through the Google Places API.

Process for Obtaining Geographic Coordinates (Latitude and Longitude):

To obtain geographic coordinates for breweries, we utilized the Google Places API within a Google Cloud Platform project. After obtaining an API key, we queried the API with a unique list of brewery names from our dataset. Each query to the Place Search endpoint returned the latitude and longitude coordinates for the corresponding brewery. We then merged this coordinate data with our original beer reviews dataset based on brewery names, creating a comprehensive dataset that combines review details with geographic locations. This integration enables spatial analysis, allowing us to explore patterns such as regional preferences and the influence of location on beer ratings.

The following two Python scripts files were generated and used to obtain both the Latitude and Longitute coordinates:


*Upon execution, the script provides feedback on the number of unique breweries lacking coordinates and confirms the successful save of the updated dataset.

FILE 1- google_api.ipynb:
This python script was designed to fetch geographical coordinates (latitude and longitude) for a list of unique brewery names from a dataset. 

The process involved the following steps:

*Setup and Library Import: Initializes the Google Maps client using a provided API key and imports necessary libraries like Pandas and Google Maps.
*Data Loading and Unique Brewery Extraction: Loads a CSV file containing beer reviews and extracts unique brewery names, saving them to a new CSV file.
*Data Chunking: Reads the CSV file of unique brewery names and splits it into smaller chunks, saving each chunk as a separate CSV file for batch processing.
*Coordinate Fetching Function: Defines a function to fetch latitude and longitude coordinates for a given brewery name using the Google Maps Places API.
*Batch Processing: Processes each chunk of brewery names to fetch coordinates, respecting the Google Maps API request limits (90 requests per minute in this script). 
Note: For this script we used a valid Google Maps API key with billing enabled due to the usage of the Places API for fetching coordinates.

FILE 2 - combine_chunks.ipynb: 
This Python script was designed to enhance the 'beer_reviews.csv' dataset by adding latitude and longitude coordinates to breweries. 

The process involved the following steps:

*Data Loading: The original dataset is loaded into a DataFrame named original_df.
*Data Copy: A copy of the original dataset is made and stored in updated_df.
*Chunk Integration: Twelve chunk files, each containing brewery coordinates, are combined into a single DataFrame combined_chunks_df.
*Coordinate Verification: The script identifies breweries without coordinates and counts the unique number of such breweries.
*Data Merging: The combined chunk DataFrame is merged with the copy of the original dataset based on the 'brewery_name' column.
*Data Saving: The updated dataset, now with added coordinates, is saved as 'beer_reviews_with_coordinates.csv'.

Both the combine_chunks.ipynb and google_api.ipynb notebooks can be run using the libraries listed below.

INSTALLATION
------------
Before running the code, ensure you have Python installed on your system. If not, you can download and install Python from [python.org](https://www.python.org/downloads/).

To set up the required Python libraries for this project, follow these steps:

1. Open your terminal or command prompt.

2. Navigate to the directory containing the `cse6242_project_code.ipynb` file.

3. To run the code, you will need to install the following libraries:

- pandas
- matplotlib
- seaborn
- numpy
- plotly
- scikit-learn 

4. If you have pip installed, you can install the required packages by running:

```bash 

pip install pandas matplotlib seaborn numpy plotly scikit-learn

5. If you do not have pip installed, you can manually download and install the required libraries from their official websites or use package managers like conda or apt.

For Anaconda environments:
conda install pandas matplotlib seaborn numpy plotly scikit-learn


EXECUTION
---------
To run the project and execute the code in the `cse6242_project_code.ipynb` notebook, follow these steps:

1. Launch Jupyter Notebook or Jupyter Lab by executing the following command in your terminal or command prompt: jupyter notebook or jupyter lab

2. In the Jupyter interface, navigate to the directory containing the `cse6242_project_code.ipynb` file and click on it to open the notebook.

3. Once the notebook is open, you can run the cells sequentially by clicking on each cell and pressing `Shift + Enter` or clicking the "Run" button in the toolbar.

The notebook contains detailed explanations and comments to guide you through each step of the analysis. By following these instructions, you'll be able to replicate the analysis and explore the insights derived from the craft beer review dataset.


TABLEAU INTERACTIVE DASHBOARD
-----------------------------
1. Download the dataset enhanced with geographical coordinates from this link:
[Brewery Data Link](https://www.dropbox.com/scl/fi/e6w6tyeh9ya030ovtla6g/beer_reviews_with_coordinates.csv?rlkey=p59f9axioxvthu8k63a1o8wlm&dl=1)

2. Place the dataset in the same location as the Tableau file (Tableau_Dashboard_File.twb)

3. Open the Tableau file and if the dataset is in the same location, you should be able to use the interactive Dashboard under the Cluster Analysis tab.


-- Cheers for diving into our beer review analytics project! We hope you find the insights as refreshing as a cold brew on a hot day. Whether you're a beer aficionado, a data enthusiast, or just curious about what the data reveals, we appreciate your interest. If you have any questions, feedback, or just want to chat about beer and data, please don't hesitate to reach out. Enjoy exploring and discovering the fascinating world of beer through analytics! --

Happy analyzing and sipping responsibly!

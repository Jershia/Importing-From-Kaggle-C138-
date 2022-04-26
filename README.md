# Importing-From-Kaggle-C138-

* *In Colab, if we want to run terminal commands, we have to add an exclamation mark “!” before all the commands. Install Kaggle using pip.**!pip install kaggle**.*
* *Go to kaggle’s website and login to Kaggle. We want to generate credentials to be able to use their API. Click on the top right corner of the screen and select “My
Account”.*
* *Scroll down to the API section and click Create New API Token.*
* *Upload the json file that is automatically downloaded into Google Colab:*
* *Run the following commands in your Colab to make sure there are no permission errors.*
* *Now to download the data, click on the 3 dots here on kaggle, which contains TMDB’s data for 5000 movies.*
* *Paste the command in google colab. Do not forget the exclamation mark “!” before the command.*
* *Run the “!ls” command.*
* *We have it in .zip format. Unzip it with the !unzip command and cross check with the !ls command.*
* *Load the CSV files and Pandas DataFrame and print the head of both the files.*
* *Merge the 2 datasets into one dataframe.*

## Code is Given
* *Code for uploading json file*
````
from google.colab import files
files.upload()
````
* *Code for preventing permission errors*
````
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
````
* *Code for unzipping the file*
````
!unzip tmdb-movie-metadata.zip
````
* *Code to merge data*
````
df1.columns = ['id','tittle','cast','crew']
df2= df2.merge(df1,on='id')
````
## New Terms
  * *.**Demographic Filtering**- They offer generalized recommendations to every user, based on movie popularity and/or genre. The System recommends the
same movies to users with similar demographic features. Since each user is different , this approach is considered to be too simple. The basic idea behind
this system is that movies that are more popular and critically acclaimed will have a higher probability of being liked by the average audience.*
  * *.**Content Based Filtering**- They suggest similar items based on a particular item. This system uses item metadata, such as genre, director, description,
actors, etc. for movies, to make these recommendations. The general idea behind these recommender systems is that if a person likes a particular item,he or she will also like an item that is similar to it.*
  * *.**Collaborative Filtering**- This system matches persons with similar interests and provides recommendations based on this matching. Collaborative filters do not require item metadata like its content-based counterparts.*
  * *mkdir - make new directory*
  * *cp - copy*
  * *chmod - to prevent permission errors*
  * *ls - list*

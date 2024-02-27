# YOUTUBE-DATA-HARVESTING-AND-WAREHOUSING-USING-STREAMLIT

## OVERVIEW OF PROJECT :

This Project aims to develop a user friendly  Streamlit application tht utilises the Googlle API to extract information from a You Tube channel , storing it in a Mongodb database,whereas migrating it to SQL and enable the user to view data in the Streamlit app.

## TECHNONLICAL TECHNIQUES:

* API Integrstion 
* Data Management using Mongodb and SQL
* Usage of Streamlit 
* Python scripting

## INSTALLATION :

We need to Install certain packages .They are as follows,

* !pip install google-api-python-client
* !python -m pip install "pymongo[srv]"
* pip install pandas

## RETRIEVING DATA :

  The project utilises the Google API to retrieve comprehensive data from Youtube Channels.The data includes information about chanels, videos and comments. but interaction with Google API ,we collect data and merge it into json file.The retrived data stored in Mongodb.

## MIGRATING TO SQL :

  The application allows users to migrate data from MongoDB to a SQL data warehouse. Users can choose which channel's data to migrate. To ensure compatibility with a structured format, the data is cleansed using the powerful pandas library. Following data cleaning, the information is segregated into separate tables, including channels, playlists, videos, and comments, utilizing SQL queries.

## SETUP:

  * FIRST STEP:
    As a first step, establish a connection to YouTube to fetch all the required details for the project and this can be achieved by using YouTube API key.

 * SECOND STEP:
     Once the connection is established to the YouTube we can start getting the channel information such as Name, ID, Subscribers Count, View Count, Total videos, Description of the channel and the playlist ID from any particular channel. With repeating the same process, we can fetch the details such as Video Ids, Video Information’s, Comment Info & Playlist Info. Also everything needs to be created as a function, so that we can get the details of multiple channels.

  * THIRD STEP:
       As a next step, establish a connection to mongo dB and create a Database with a collection. Now push all the data (Channel information,  Video Information & comment information)   store it as the document for the collection created.Establish a connection to SQL and create a table in SQL for the channel information available in the mongo dB with the respected columns.By using Pandas with Data Frame concept, retrieve all the data of Channel information from Mongo db and push it to sql to store it in the table created for Channel information.
Repeat the same process to store all the data’s like  Video information and Comment information from mongodb to sql using pandas.Create all this as a function, to make sure, we can insert multiple channel data to mongo dB and can fetch that data to store it in sql.

   * FOURTH STEP :
       As a final step, design the Streamlit application by using the inbuilt functions available for the libraries which we imported as streamlit. Once it is designed, then create a search bar to enter the channel details with a button which will collect and store all the data in Mongodb.With all the data’s transferred to mongodb, create a button to migrate all the data’s to SQL and to display all the data in form of tables (channels, videos, playlist, comments). Lastly With the given 10 Queries, create an if condition for all the questions to provide us with the expected output in the streamlit application.

    

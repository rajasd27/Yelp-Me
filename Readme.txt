{\rtf1\ansi\ansicpg1252\cocoartf1671\cocoasubrtf200
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\froman\fcharset0 TimesNewRomanPSMT;}
{\colortbl;\red255\green255\blue255;\red26\green26\blue26;\red255\green255\blue255;\red16\green60\blue192;
}
{\*\expandedcolortbl;;\cssrgb\c13333\c13333\c13333;\cssrgb\c100000\c100000\c100000;\cssrgb\c6667\c33333\c80000;
}
\margl1440\margr1440\vieww33400\viewh18460\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs28 \cf0 *********************************** CONFIGURATION ***********************************\
\
== API Accounts ==\
\
In order to use the Yelp Me application, a user must have registered an account with the Mapbox API.  The steps to create a mapbox account and generate the access tokens is given below.   \
\
https://www.mapbox.com/help/how-access-tokens-work/#mapbox-account\
\
Now copy the access token to the OAuth_Keys.json file.\
\
\
== Authentication File ==\
\
Once account is setup with the MapBox API services, the access tokens will need to be stored in JSON format in a file called OAuth_Keys.json.  This file is placed in the same directory as the YelpMe.py. A sample file containing dummy keys currently exists in the YelpMe zip file. The file must contain the following key value pairs all at the initial level in the JSON file.\
\
    KEY         VALUE\
    Token       Mapbox API access token\
\
\
== Data Subdirectory ==\
\
The data sub-directory must be located in the directory where the python code resides. This folder, contains files about businesses (restaurants) and business review (restaurants reviews) for different businesses across the United States in JSON format. Along with this, the data contains other JSON files which include the state and city latitude and longitude, cuisine file and food file.\
\
******************************** Running the Code ********************************\
\
== Install Dependencies ==\
\cf2 \expnd0\expndtw0\kerning0
\
\pard\pardeftab720\li2880\fi-2880\partightenfactor0

\f1 \cf2 \cb3 \'a0\'a0\'a0\'a0\'a0\'a0\'a0\'a0\'a0\'a0\'a0
\f0 i.
\f1 \'a0\'a0\'a0\'a0 
\f0 pip install dash==0.31.1\'a0 # The core dash backend\cb1 \

\f1 \cb3 \'a0\'a0\'a0\'a0\'a0\'a0    
\f0 ii.
\f1 \'a0\'a0\'a0\'a0 
\f0 pip install dash-html-components==0.13.2\'a0 # HTML components\cb1 \

\f1 \cb3 \'a0\'a0\'a0\'a0\'a0\'a0\'a0\'a0  
\f0 iii.
\f1 \'a0\'a0\'a0\'a0 
\f0 pip install dash-core-components==0.38.1\'a0 # Supercharged components\cb1 \
        
\f1 \cb3  
\f0 iv.
\f1 \'a0\'a0\'a0\'a0 
\f0 pip install dash-table==3.1.7\'a0 # Interactive DataTable component\cb1 \

\f1 \cb3 \'a0\'a0\'a0\'a0\'a0\'a0\'a0\'a0\'a0\'a0
\f0 v.
\f1 \'a0\'a0\'a0\'a0 
\f0 pip install dash-table-experiments==0.6.0\cb1 \
\pard\pardeftab720\partightenfactor0
\cf2 \cb3 \
Find the Documentation here: {\field{\*\fldinst{HYPERLINK "https://dash.plot.ly/"}}{\fldrslt \cf4 \ul \ulc4 https://dash.plot.ly/}}\cb1 \
\cb3 \'a0\cb1 \
\cb3 1.
\f1 \'a0\'a0\'a0\'a0\'a0 
\f0 Plotly- Install plotly-python from PyPI using: pip install plotly\
        Run the following code in python - \
		import Plotly\
		Plotly.tools.set_credentials_file(username=\'91Your Username\'92, api_key=\'91Your API key\'92)\
\cb1 \
\cb3 Find the Documentation here: {\field{\*\fldinst{HYPERLINK "https://plot.ly/python/getting-started/"}}{\fldrslt \cf4 \ul \ulc4 https://plot.ly/python/getting-started/}}\cb1 \
\cb3 \'a0\cb1 \
\cb3 2.
\f1 \'a0\'a0\'a0\'a0\'a0 
\f0 TextBlob- Install TextBlob-python from PyPI using: \'a0pip install -U textblob\cb1 \
\cb3 Find the Documentation here: {\field{\*\fldinst{HYPERLINK "https://textblob.readthedocs.io/en/dev/"}}{\fldrslt \cf4 \ul \ulc4 https://textblob.readthedocs.io/en/dev/}}\cf0 \cb1 \kerning1\expnd0\expndtw0 \
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0
\cf0 \
=====================\
After all of the configuration steps have been completed, the Yelp Me application is ready to be run.  In order to start the application, open your terminal and run the following command - \
\
python YelpMe.py\
\
The output of this command will be as follows -  \
\
Running on http://127.0.0.1:8050/ \
Debugger PIN: 269-419-746 \
 * Serving Flask app \'93YelpMe\'94 (lazy loading) \
 * Environment: production \
   WARNING: Do not use the development server in a production environment. \
   Use a production WSGI server instead. \
 * Debug mode: on \
\
Running on http://127.0.0.1:8050/ \
Debugger PIN: 330-499-856\
\
Enter the url mentioned after "Running On" on your browser and the application is started.\
\
*********************************** Limitations ***********************************\
\
== Mapbox API ==\
\
The location map provided by the MapBox API does not take the correct latitude and longitude values when the map is zoomed out to the maximum level during initialization. }
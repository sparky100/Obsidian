
# Speed Bot 

The speed bot makes use of a number of different components. 

- The Here API, is used to provide access to real time traffic data [[Traffic Using Here]]
- The API request is made using a python script.
- The Python script can be created either as
	- a Local function and use CRONTAB or  
	- a Google function with Google Scheduler  


The Python script uses a number of different modules

- [requests](https://docs.python-requests.org/en/latest/)- simplifies the request to the Here API 
- [datetime](https://docs.python.org/3/library/datetime.html) - enables conversion of date like strings returned by the API request to datetime objects  
- [dateutil](https://dateutil.readthedocs.io/en/stable/)  - converts datetime objects between time zones
- [tweepy](https://www.tweepy.org/) - authenticates access to twitter and allows Tweets to be sent 

## Python code
- Import modules
- Set up keys for Here API
- Make Here API request
- Define road segments of interest as a dictionary
- Iterate through Flow data 
- Identify where speed exceeds a defined value for targeted roads
	- Convert recorded time in UTC to BST
	- Tweet 

Local solution
Modules are imported using PIP and import statements included in code

GOogle solution
Modules are imported by including in requirements.txt  file
**MoodParser**

This is a tool to parse a file of JSON that is pulled from Moodtrack Diary, since it doesn't provide exports.
It then creates a .dsv file (tab delimited) of the creation timestamp, the mood, the star rating, 
and the number I put in the description. 

You need to first get the URL and code of your diary, which you can get from sharing your diary to an email. You 
need to put both the URL and the code into the moodparser.properties file, for which I have provided the 
template for you to fill in with your info. Just remove the _template part of the filename and you'll be good to go, 
provided that the properties file is in the same directory as your script.

Command to run: 
python moodparser.py *start_date* *end_date*

*start_date* and *end_date* are both in the format of MM-DD-YYY

**Latest addition**
I removed the AUTH token part of the properties and replaced with the code that's provided by the Moodtrack Diary app
when you choose to share the diary. Now everything the user needs to provide for MoodParser to work is provided 
directly by the app. The MoodParser program now finds the token through the requests library as well. I also 
abstracted out some of the logic into functions to make the program look a little cleaner.  

**Note**: This tool is definitely still in progress as right now I'm running the script to generate multiple tab 
delimited files and then pulling data from them into Excel sheets to make graphs.

**Goal of project** 
My hope is to get this tool to the point where it has a GUI of some sort, can handle multiple users, and also has the 
ability to generate reports/graphs instead of writing everything to files that need to be handled manually.



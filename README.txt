*********************************************************************
***	    README - Email Header CSV Parser - RFC5822            ***
***								  ***
*** Python 3.4 or later must be installed for this program to run!***
***								  ***
*********************************************************************
------------------------------------------------------------------------
**************************** Description *******************************
------------------------------------------------------------------------

EmailHeaderParser.py is a program which parses email header data into a 
structured file format (CSV). The program also creates two addtional files, 
one which includes a log which will detail errors which occur and the other 
provides statistics on how many 'Received:' traces have been parsed and 
how many rows of data are inside the CSV file. 

EmailHeaderParser.py parses the following email headers to CSV - 

'From:', 'To:', 'Reply-To:', 'In-Reply-To:', 'Resent-From:', 'Resent-Date:',
'Resent-Message-ID', 'Subject:', 'Date:', 'Message-ID:', 'References:', 
'Return-Path:', 'Received:', 'Received-SPF:', 'User-Agent:', 'Content-Type:'.

This is Version 1.0. There are already improvements which can be made to this 
program and these will be included in the next release (v1.1). This includes: 

	- More detailed logging and recommendations on how to resolve these
	  issues.
	- The 'Received:' feild will be futher seperated to clearly identify
	  the routes the email has took over the internet. 
	- Accuracy will also be improved in the next release, aiming to 
	  reliably acheive above 95%. 
	- User specified parsing, in which the user will select which email
	  header fields they would like to be parsed. 

------------------------------------------------------------------------
************************ Python modules used ***************************
------------------------------------------------------------------------
	csv
	email
	os
	time
	re
	ipaddress
	logging
	glob

------------------------------------------------------------------------
*********** Instructions on how to run EmailHeaderParser.py ************
------------------------------------------------------------------------
Microsoft Windows: 
	1. Copy Email Header CSV Parser source file [EmailHeaderParser.py] 
        to the directory which holds all the emails you wish to be parsed.
	
        2. Open File Explorer and navigate to that same directory.
	
        3. While holding down SHIFT, right-click your mouse on the white space 
        avoiding selecting any of the files.
	
        4. Select "Open Command Window Here".
	
        5. Run the program by typing [python EmailHeaderParser.py] and 
        follow the instructions via the Command Prompt.
	
        6. The resulting [CSV File], [Log File] and [Statistics File] 
        will be available in the same directory once the program has completed. 

MacOS:
	1. Copy Email Header CSV Parser source file [EmailHeaderParser.py] 
        to the directory which holds all the emails you wish to be parsed.
	
        2. Open Terminal and navigate to that same directory 
        - e.g. cd /Users/*User Name*/*Directory Location*/
	
        3. Run the program by typing [python3 EmailHeaderParser.py] 
        and follow the instructions via the Terminal.
	
        4. The resulting [CSV File], [Log File] and [Statistics File] 
        will be available in the same directory once the program has completed. 

Linux:
	1. Copy Email Header CSV Parser source file [EmailHeaderParser.py] 
        to the directory which holds all the emails you wish to be parsed.
	
        2. Open Terminal and navigate to that same directory
        - e.g. cd /Users/*User Name*/*Directory Location*/
	
        3. Run the program by typing [python3 EmailHeaderParser.py] 
        and follow the instructions via the Terminal.
	
        4. The resulting [CSV File], [Log File] and [Statistics File] 
        will be available in the same directory once the program has completed. 

------------------------------------------------------------------------
******************************* HELP ***********************************
------------------------------------------------------------------------
1. EmailHeaderParser.py will ask for the directory location for the email files. 
   Please follow the same directory naming convention as stated previously.
   
   Directory location command varies depending on the operating system. Below
   are the directory paths needed to get to your documents folder. 
   
   Microsoft Windows - the root directory path to My Documents is: [C:\Users\*User*\Documents\]
   MacOS - the root directory path to Documents is: [/Users/*User*/Documents/]
   Linux - the root directory path to Documents is: [/home/*User*/]
   
   Tip - *User* is commonly your username. 

2. Input options for speed and logging level use single digits to identify your option. 
   Please follow the instrucutions from the console when running the program.

2. Python (Version 3.4 and Later) must be installed for this program to operate. 
   This may need to be re-installed if errors occur when trying to run the program.

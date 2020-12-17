# covid-19_audio_assistant
COVID-19 has drastically changed the way of human living in 2020. We have to stay cautious, careful and follow the standard operating procedures to stop the spread of the disease. There are travel restrictions for different countries. We might want to know the number of cases in different countries. Our goal is to easily help the users know the number of COVID cases in each country. Our project is designed in such a way that we can ask the bot the number of cases in a country and the bot will reply us the number of cases. To achieve this, we will extract data from a website that updates the number of cases in each country. We will use the microphone and speech recognition libraries to listen to the user. Based on the query, the bot will match the country and reply us the number of cases in the country. This method could be helpful to know the cases and even used in AI speech assistants to answer the question precisely. 
In this project, we have used ParseHub for web scraping purpose. ParseHub is a powerful and free web scraper tool, which seamlessly perform data extraction from different websites. For substantial data mining, ParseHub includes several features like image file scraping, automatic IP rotation, scheduled runs and data accessibility in multiple forms including JSON and csv format. The first step of web scraping process is installing ParseHub application.
https://www.parsehub.com/docs/ref/api/v2/

The detailed web scraping process with ParseHub is as follows.
•	Open ParseHub and select the option for a new project. 
 
•	In the space provided for pasting the website URL, paste the link to the Worldometers website.	(https://www.worldometers.info/coronavirus/)
•	Click select the data that needs to be scraped from the website. It is possible to use the relative selection tool to connect different data. 
 
•	After selecting data, click 'Get Data' to retrieve it, after which the API key, Project token, and Run token is generated. These tokens are used while running the python code.
 
Implementation
1. Import the necessary libraries
2. Set up the speech engine
  Here, we convert text to speech. The speak function accepts the text as its argument and uses the pyttsx3 module to initialize the engine. runAndWait() function invokes        callbacks for engine notifications.
3. Set up a function for voice assistant
  Designed a function get_audio for the COVID-19 voice assistant to recognize and to accept human speech. Here, the microphone receives the human voice, and the recognizer identifies the voice to answer the query of human. The exception handling is included to handle the exception during the run time.
 4. To get updated information from the website
  When the console says, “Please speak. Listening…”, say “how many coronavirus cases in Canada,” The assistant would reply with the number of COVID19 cases across Canada. We can say, “update” and the assistant will update the values.
  5. To exit from running application
  To exit from the application, we need to input the “stop” command through the microphone.


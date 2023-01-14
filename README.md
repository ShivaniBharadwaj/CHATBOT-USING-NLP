# CHATBOT-USING-NLP

	PROBLEM STATEMENT
Design a chat bot that can greet us and can reply to the questions asked
After greetings, make the chatbot ask about some basic questions like what is the capital of India and then the chatbot makes a comment about your response.

A chatbot (conversational interface AI agent) is a computer program that can understand human language and converse with a user via a website or a messaging app

1 PREPARE THE DEPENDENCIES

In this step, you’ll set up a virtual environment and install the necessary dependencies. 
To get started with your chatbot project, create and activate a virtual environment, then 
1.1 Install chatterbot library
ChatterBot is a Python library built based on machine learning with an inbuilt conversational dialog flow and training engine. The bot created using this library will get trained automatically with the response it gets from the user.

1.2 Install spacy version 2.3.3
 Spacy is an open-source software library for advances natural language processing, and specifically designed for production use and helps to build applications that process understand large volumes of text. Also it can be used for information extraction.

1.3 Install pyttsx3 library
 pyttsx3 is a text-to-speech conversion library in Python. Unlike alternative libraries, it works offline and is compatible with both Python 2 and 3.


2 IMPORT CLASSES
Importing classes is the second step in the Python chatbot creation process. All you need to do is import five classes – tkinter, ChatBot from chatterbot, ListTrainer from chatterbot.trainers , pyttsx3 and os . To do this, you can execute the following command:
                  
          
3 CREATE AND TRAIN THE CHATTERBOT
This is the third step on creating chatbot in python. The chatbot we are creating will be an instance of the class “ChatBot.” After creating a new ChatterBot instance, we can train the bot to improve its performance.
Since we have to provide a list of responses, we can do it by specifying the lists of strings that can be later used to train your Python chatbot, and find the best match for each query. Here’s an example of responses we can train your chatbot using python to learn:
 
 3.1 Training of chatterbot with the help of responses.
We can also create and train the bot by writing an instance of “ListTrainer” and supplying it with a list of strings like so:
                     
3.2 Training of chatterbot with the help of instance ListTrainer.
 Now, our Python chatbot is ready to communicate. 

4 COMMUNICATE WITH THE PYTHON CHATBOT
To interact with our Python chatbot, we can use the. Get_response() function.
        
5 MAKING OUR CHAT BOT SPEAK
We can make our chatbot speak the answer for the question asked with the help of library pyttsx3 and by using the .speak() method of the library.
             
                                    


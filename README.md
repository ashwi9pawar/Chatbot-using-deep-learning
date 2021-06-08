# Chatbot-using-deep-learning
In this project a retrieval-based chatbot is made which uses predefined input patterns and responses. The chatbot will be trained on the dataset which contains categories (intents), pattern and responses. A special recurrent neural network (LSTM) is used to classify which category the user’s message belongs to and then a random response is given from the list of responses. 

## Steps to create a chatbot 

### 1. Import and load the data file
First, a file named train_chatbot.py is made. The necessary packages for chatbot are imported and the variables are initialised.
The data file is in JSON format so json package is used to parse the JSON file into Python.

### 2. Preprocess data
Tockenising is done on text data where the text is broken into small parts like words which are appended in a list. A list of classes are created for the tags.
Each word is lemmatized and duplicate words are removed from the list. Lemmatizing is the process of converting a word into its lemma form and then creating a 
pickle file to store the Python objects which ware used while predicting

### 3. Create training and testing data
The training data is created in which we provide the input and the output. Input is the pattern and output is the class our input pattern belongs to. But the computer doesn’t understand text so the text is converted into numbers.

### 4. Build the model
After training data is ready, a deep neural network is built that has 3 layers. The Keras sequential API is used for this. After training the model for 200 epochs, 100% accuracy is achievd on the model. The model is saved as ‘chatbot_model.h5’.

### 5. Predict the response (Graphical User Interface)
To predict the sentences and get a response from the user a new file ‘chatapp.py’ is created. The trained model is loaded and then a graphical user interface is used that predicts the response from the bot. The model tells us the class it belongs to, so some functions are implemented which will identify the class and then retrieve us a random response from the list of responses.The necessary packages are imported and the ‘words.pkl’ and ‘classes.pkl’ pickle files are loaded which were created when we trained our model. GUI is created with the help of Tkinter library.

### 6. Run the chatbot
There are two main files train_chatbot.py and chatapp.py. First we train the model using command in the terminal : python train_chatbot.py.
The to run the app we run the second file: python chatgui.py. The program opens GUI window in few seconds. With GUI we can easily chat with the bot.

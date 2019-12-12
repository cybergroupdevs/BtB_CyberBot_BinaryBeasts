# Cyber Bot

Install Python (preferrably version 3.6.8)
cmd -- pip install virtualenv

// Create virtual environment
>> Create a New Folder and in Command Prompt change the directory to that folder
cmd -- virtualenv env

// Activate virtual environment
cmd -- .\env\Scripts\activate

// Install necessary packages
cmd -- pip install deeppavlov (it will also install numpy, pandas and many more packages)
cmd -- pip install tensorflow==1.14

// Download the model (Approx size = 2.2 GB)
cmd -- python
python -- from deeppavlov import build_model, configs
python -- model = build_model(configs.squad.squad, download=True)

// Once the model is downloaded, test the model
python -- model(["James is a basketball player."],["Who is James"])

// Exiting the python environment
python -- exit()

// Reference it using a Rest Service
-- Activate the environment (if not)
cmd -- python -m deeppavlov riseapi PATH_TO_THE_FOLDER_YOU_CREATED\env\Lib\site-packages\deeppavlov\configs\squad\squad.json -d -p 9999
>> API will be hosted to localhost:9999. You can access it using "localhost:9999/docs".

>> We can make this API public using ngrok.

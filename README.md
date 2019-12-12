# Cyber Bot

## What is Cyber Bot?

Cyber Bot is the AI based chat bot that works on NLP (Natural Language Processing), that means an effective way for user to communicate to system without interference of any human being that ultimately results in flawless and quick performance.

## Setup Instructions:

**1) Install Python (preferrably version 3.6.8)**

**2) Download package to create Virtual Environment**

cmd -- *pip install virtualenv*

**3) Create virtual environment**

> Create a New Folder and in Command Prompt change the directory to that folder

cmd -- *virtualenv env*

**4) Activate virtual environment**

cmd -- *.\env\Scripts\activate*

**5) Install necessary packages**

cmd -- *pip install deeppavlov* (it will also install numpy, pandas and many more packages)

cmd -- *pip install tensorflow==1.14*

**6) Download the model (Approx size = 2.2 GB)**

cmd -- *python*

python -- *from deeppavlov import build_model, configs*

python -- *model = build_model(configs.squad.squad, download=True)*

**7) Once the model is downloaded, test the model**

python -- *model(["James is a basketball player."],["Who is James"])*

**8) Exiting the python environment**

python -- *exit()*

**9) Reference it using a Rest Service**

-- Activate the environment (if not)

cmd -- *python -m deeppavlov riseapi PATH_TO_THE_FOLDER_YOU_CREATED\env\Lib\site-packages\deeppavlov\configs\squad\squad.json -d -p 9999*

> API will be hosted to localhost:9999. You can access it using "localhost:9999/docs".

> We can make this API public using ngrok.

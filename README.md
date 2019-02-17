# Marathi MoodBot: Rasa chatbot example

The project was a quick implementation of chatbot using the tensforflow embeddings. Though the language mentioned in config file is English but words are in Marathi langauge but written in English.

## Prerequisites
Requires Python 3.6.x

## Installation
This will install all required packages 

`pip install rasa`

or alternatively you can do 

`pip install rasa_core`

`pip install rasa_nlu[tensorflow]`

The project was a quick implementation using the tensforflow embeddings

## Training
Train the natural language understanding using Rasa NLU
 
`python -m rasa_nlu.train -c config.yml --fixed_model_name current --data nlu.md --path models/ --project nlu`
 
Train the natural language understanding using Rasa NLU
 
`python -m rasa_core.train -s stories.md -d domain.yml -o models/dialogue`
 
## Running your Bot
Run your chatbot On cmdline
 
`python -m rasa_core.run -d models/dialogue -u models/nlu/current`

Over Web using custome channel

`python -m rasa_core.run --enable_api -d models/dialogue -u models/current/nlu --cors "*" --endpoints endpoints.yml --verbose`

## Evaluate NLU
Evaluates the nlu data

`python -m rasa_nlu.evaluate --model models/nlu/current --data nlu.md`

## Visualize 
visualize your stories as a graph

`python -m rasa_core.visualize -s stories.md -d domain.yml -o story_graph.html`

## Results
![Chatbot Snippet](https://github.com/Ajinkz/Marathi-MoodBot/blob/master/Marathi_moodbot.png)

## Acknowledgment

* [Souvik Ghosh](https://github.com/souvikg10/rasa_bot_example)
* [Jitesh Gaikwad](https://github.com/JiteshGaikwad/RASA-Chatbot-UI)

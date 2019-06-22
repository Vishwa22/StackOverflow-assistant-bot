# StackOverflow-assistant-bot
Constructing a dialogue chat bot, which will be able to:  answer programming-related questions (using StackOverflow dataset); chit-chat and simulate dialogue on all non programming-related questions.

This chatbot has been readied with the help of resources provided by Natural Language Processing course on Coursera. Please check the links below:

https://www.coursera.org/learn/language-processing

https://github.com/hse-aml/natural-language-processing

For instructions on the working of the bot please refer **Working_on_chatbot.pdf** provided in the repository.

### Key requirements to run this project:

* Google Colab account to train the models

* AWS account to host the chatbot

* Telegram account to instantiate the bot

* Docker installed in windows 8.1 to generate starspace embeddings

* Putty in Windows 8.1 (ssh to AWS linux machine) for transferring necessary python files and trained models to run bot on AWS linux machine.

**chatbot_project.ipynb** will produce following outputs:
* intent_recognizer.pkl � intent recognition model;
* tag_classifier.pkl � programming language classification model;
* tfidf_vectorizer.pkl � vectorizer used during training;
* thread_embeddings_by_tags � folder with thread embeddings, arranged by tags.

**Starspace_embeddings_Stackoverflow.ipynb** will produce the starspace embeddings using the specific dataset for our specific task i.e. stackoverflow post. Please follow the instructions in **Working_on_chatbot.pdf** to run starspace model on docker.
*  my_starspace_embeddings_0612.tsv

**utils.py** contains necessary helper functions

**dialogue_manager.py** contains the exact flow of how chatbot interacts with the user

**main_bot.py** is the python file you run on AWS with input as telegram token generated for our bot(on telegram)

All the output generated in the course of this project is saved in `output` folder

## Stakeholders

- Data Provider
- AI Creator
- AI Operator
- AI User
- Oversight Authority


## Objects

- Chatbot
- AI Model
- Training data
- Conversation
- Conversation Record
- Record Purpose
- Chatbot Goal
- Algorithm
- Juridiction

----

Relationships from Competency Questions

| Relationship | Question |
|--------------|----------|
| AI User, use, Chatbot | |
| AI Operator, operate, Chatbot | |
| Chatbot, use, AI Model | |
| AI Creator, create, AI Model | |
| AI Model, use data from, Training data | |
| Data Provider, provide, Training data | |
| Chatbot, is aware of, Sensitive user information | Will the chatbot be aware of a sensitive property of the user? |
| Chatbot, record, Conversation | Does the chatbot record the conversation?|
| Chatbot, create, Conversation Record | |
| Record, is for, Record Purpose | For what regulatory and non-regulatory purposes that the conversation is recorded for? |
| Record, is part of, Training data | Does the chatbot use the user's response to train the new model? |
| Chatbot, is type of, (Goal-oriented OR Free chat) | |
| Chatbot, goal is, Chatbot Goal | |
| Chatbot Goal, is essential public service, YES/NO | Does the service provided by the chatbot a public service or an essential service? |
| Training data, contain, Personal data | |
| Training data, contain, Conversation Record /| |
| AI model, created by algorithm, Algorithm | |
| AI Operator, operate in, Jurisdiction | |


### (from 29 Apr 2020 Supervision Notes)
```
App.feature ----[has]----> Permission
App.feature --[request]--> Permission
App.feature --[require]--> Permission
App.feature --[require]--> Software Library
App.feature --[require]--> Network connection
App.feature --[not has]--> Network connection permission
Data set X --[is]--> Synthetic data
Data set X --[contains]--> Personal data
Data set X --[contains]--> Incentive data
Data set X --[went through]--> De-identification method Y
Model X --[trained from]--> Data set Y
Organisation --[has access]--> Medical treatment information
Organisation --[under regulation of]--> Some regulation+jurisdiction
Organisation --[has to report the use of]--> Some person data
Organisation --[has power to make decision about]--> Some aspect of a person's life
Organisation --[share data with]--> Organisation
Organisation --[is a data controller of]--> App
Organisation X --[is a data processor of, for]--> Info, Organisation Y
```

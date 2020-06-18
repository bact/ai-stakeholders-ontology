## Competency Questions

Initial questions and some components inside a question.

- Does the chatbot record the conversation?
  - `Agent`: Chatbot
  - `Agent's Action`: Record
  - `Object`: Conversation
  
- For what regulatory and non-regulatory purposes that the conversation is recorded for?
  - `Agent`: Someone (implicit)
  - `Agent's Action`: Record
  - `Object`: Conversation
  - `Purpose of Action`: X
  - `Type of Purpose of Action`: Regulatory | Non-regulatory
  - Rationale: Justificatory
  - Theme: Accountability, Transparency and Explainability

- Does the chatbot use the user's response to train the new model?
  - = Does `User's reponse` in `Model's Input` ?
  - `Agent`: Chatbot
  - `Agent's Model`: Model
    - `Model's Input`: List of `Dataset`s
      - `Dataset`: `source`, `date`, `size`, `has_personal_data`, `has_sensitive_data`
      - `Preprocessing`: `normalization`, `masking`
    - `Model's Modelling Algorithm`: A
  - Theme: Accountability, Transparency and Explainability

- Can the AI provider alter the model of the chatbot?
  - Mentioned a stakeholder
- Can the AI user alter the model of the chatbot?
  - Mentioned a stakeholder

- Does the chatbot able to get information about the user more than what the user provided in the current conversation and previous conversation?
- The response that the chatbot delivers to the user is in its original form (a snippet from a webpage, a row from a database) or in an modified/aggregated form? (curator role vs editor role) Or the answer is from an inference? (creator role)
- What is the algorithm for the chatbot to choose an answer from possible candidates? Or the chatbot will not choose and instead display all the candidates to the user?
- In order to make reponse, which internal and external services that the chatbot needed to make a query (with information from the user, not necessary personal information) to? (There can be a regulatory difference. Internal/external, controller/processor.)
- Will the chatbot be aware of a sensitive property of the user?
- Does the chatbot use the same model for every user? (I’m thinking about negative discrimination)
- Which chatbots require user location in order to fulfil its function?
- Which chatbots may deliver different answers for different users asking the same question?
- For the same service that the chatbot provides, does the user have other channels as their options? (like phone, email, face-to-face over the counter, etc.)
- Can the chatbot decide by itself to make a reference / initiate a call to their counterpart human agent and transfer the conversation there?
- Within the user interface/conversational with the chatbot, can the user initiate a call to a human agent by themselves?
- Can a human agent make an intervention with or without user consent to the conversation between the user and the chatbot?
- Will the human agent see information in the conversation between the user and the chatbot?
- Does the service provided by the chatbot a public service or an essential service?
- What is the agreed service level for the service provided by the chatbot, according to regulations or contracts?

Suggestions for more questions

- Addressing: questions about the way the chatbot formulate the dialog - like intimacy, gender, addressing with first name, biases
- Discrimiation: accent, choice of words, that can reveal a category of people and lead to different treatments - does the chatbot make an inference of a person’s social/cultural category, does the chatbot take a different action based on the social/cultural category? --- Profiling questions)

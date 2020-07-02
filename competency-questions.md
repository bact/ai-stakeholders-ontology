## Competency Questions

Initial questions and some components inside a question.

**From this we should create hypothetical scenarios, so we ask these questions and get hypothetical answers. From these answers, we can start to build the concepts and relationships for the ontology.**

### Questions to identify stakeholders

- Who is AI Creator (organization/business function)? +
  - Who is Business Owner (who defines business goals and requirements) *
  - Who is Data Scientist (who uses data to train models to meet requirements) *
  - Who is Model Validator (who uses business goals, regulations, and best practices to test models) *
    - This can be further expanded. For example, based on I. D. Raji et al. 2020.
- Who is AI Operator (organization/function)? +
  - Who is AI Operations Engineer (who deploys and monitors models in running services) *
- Who is AI User? +
- Who is Data Provider? ++
- Who is Oversight Authority? ++
- Who are Associate Stakeholder? ++

An AI model will be created by an AI Creator and will be deployed as a service by AI Operator for the AI User to use. A Data Provider provides training and testing data to AI Creator.

**There can be a set of questions about roles each individual takes. In which that answer can be use to justify if one belongs to which type of stakeholders.**

(+ ) OECD

(++) D. Lewis, and PJ Wall, ‘The Role of Data Governance and Social Responsibility Standards in Ethical and Societal Considerations of Trustworthy AI’, 2019.

(* ) From J. Richards, D. Piorkowski, M. Hind, S. Houde, and A. Mojsilović, ‘A Methodology for Creating AI FactSheets’, arXiv:2006.13796 [cs], Jun. 2020, Accessed: Jul. 01, 2020. [Online]. Available: http://arxiv.org/abs/2006.13796.

I. D. Raji et al., ‘Closing the AI Accountability Gap: Defining an End-to-End Framework for Internal Algorithmic Auditing’, arXiv:2001.00973 [cs], Jan. 2020, Accessed: Feb. 07, 2020. [Online]. Available: http://arxiv.org/abs/2001.00973.


### Questions for Data Provider (provides data)

#### Training/Testing data

(from the perspective of the Data Provider, it just a dataset - the AI Creator will decide about the training/testin split)

- Transparency and Explainability
  - Can we tell where the training and testing data come from?
  - How the data is being collected? (methodology)
  - How the data is being annotated?
    - Annotation guideline URL?
- Privacy
  - Which methods that have been used to remove personally identifiable information from the dataset
- Cultural sensitivity
  - Balance (again, that can be up to the AI Creator to decide about the selection from the whole dataset)

### Questions for AI Creator (provides model)

#### Model (for inference)

- Transparency and Explainability
  - What is this model for?
  - What domain was it designed for?
  - e.g. Is this a domain specifi or general chatbot?
  - Can a user get an explanation of how the model makes its decision?
  - What are the model's inputs and outputs?
- Professional Responsibility
  - What are the model's performance metrics?
    - accuracy
    - bias
    - robustness
    - domain shift
  - Based on experience during the development, in what circumestances does the model perform poorly? (e.g. domain shift, specific kinds of input)

### Questions for AI Operator (provides service)

#### Input data

- Does the chatbot record the conversation?
  - `Agent`: Chatbot
  - `Agent's Action`: Record
  - `Object`: Conversation
  - To Whom?: Impacted individuals
  - Why?: Regulatory compliance; To improve service
  - What?: Conversation, which may contain personal data of the individual who directly interact with the system or personal data of someone else
  - When?: Everytime the end-user uses the system; Everytime the end-user gives the content to record
  - How?: Record to database

- For what regulatory and non-regulatory purposes that the conversation is recorded for?
  - `Agent`: Someone (implicit)
  - `Agent's Action`: Record
  - `Object`: Conversation
  - `Purpose of Action`: X
  - `Type of Purpose of Action`: Regulatory | Non-regulatory
  - Rationale: Justificatory
  - Theme: Accountability, Transparency and Explainability

- Does the chatbot able to get information about the user more than what the user provided in the current conversation and previous conversation?

- In order to make reponse, which internal and external services that the chatbot needed to make a query (with information from the user, not necessary personal information) to? (There can be a regulatory difference. Internal/external, controller/processor.)

- Will the chatbot be aware of a sensitive property of the user? (and may use that as additional input)

- Will chatbots require user location in order to fulfil its function?
  - This may relate to the AI Creator as well

#### Output data (predictions)

- The response that the chatbot delivers to the user is in its original form (a snippet from a webpage, a row from a database) or in an modified/aggregated form? (curator role vs editor role) Or the answer is from an inference? (creator role)

- What is the algorithm for the chatbot to choose an answer from possible candidates? Or the chatbot will not choose and instead display all the candidates to the user?

- Does the chatbot use the same model for every user? (I’m thinking about negative discrimination)

- Will chatbots may deliver different answers for different users asking the same question?

- Addressing: questions about the way the chatbot formulate the dialog - like intimacy, gender, addressing with first name, biases

- Discrimiation: accent, choice of words, that can reveal a category of people and lead to different treatments - does the chatbot make an inference of a person’s social/cultural category, does the chatbot take a different action based on the social/cultural category? --- Profiling questions)

#### Training/Testing data

- Does the chatbot use the user's response to train the new model?
  - = Does `User's reponse` in `Model's Input` ?
  - `Agent`: Chatbot
  - `Agent's Model`: Model
    - `Model's Input`: List of `Dataset`s
      - `Dataset`: `source`, `date`, `size`, `has_personal_data`, `has_sensitive_data`
      - `Preprocessing`: `normalization`, `masking`
    - `Model's Modelling Algorithm`: A
  - Theme: Accountability, Transparency and Explainability
  - Also involves AI Creator
    - **AI Operator will be a Data Provider to AI Creator**

#### Model

- Can the AI Provider alter the model of the chatbot?


### Questions for AI User 

- Can the chatbot decide by itself to make a reference / initiate a call to their counterpart human agent and transfer the conversation there?

- Within the user interface/conversational with the chatbot, can the user initiate a call to a human agent by themselves?

- For the same service that the chatbot provides, does the user have other channels as their options? (like phone, email, face-to-face over the counter, etc.)

- Can the AI User alter the model of the chatbot?

- Can a human agent make an intervention with or without user consent to the conversation between the user and the chatbot?

- Will the human agent see information in the conversation between the user and the chatbot?

- Does the service provided by the chatbot a public service or an essential service?

- What is the agreed service level for the service provided by the chatbot, according to regulations or contracts?


### Questions for Oversight Authority


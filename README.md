# 🤖 BOTFORGE: Agentic AI for Mental Health Support

A  agentic AI assistant that provides supportive and interactive mental wellness conversations based on Cognitive Behavioral Therapy (CBT) principles. Built using LangChain, Pinecone, and Gemini Chat model , google Drive Loader, it acts as a compassionate AI companion to help users discuss their mental health in a non-judgmental space and replaces the need to go to a Psychiatrist.

## 💡 Project Overview

BOTFORGE aims to reduce the accessibility barriers associated with traditional mental health care by offering a conversational agent that listens, understands, and guides users through their emotions using CBT-based techniques.

The system leverages multiple agents to simulate a therapeutic session that adapts to user inputs and dynamically retrieves relevant mental wellness strategies.

---

## 🧩 Key Components

### 🧠 Agentic Workflow

1. **Intake Agent**  
   - Initiates the session with predefined mental health intake questions.
   - Stores user responses for further context.

2. **Follow-up Agent**  
   - Analyzes user responses.
   - Crafts intelligent and compassionate follow-up questions in loop to understand deeply about user mental state.

3. **Advice Agent (RAG Pipeline)**  
   - Retrieves contextually relevant CBT therapy information or solution to user issue using a Pinecone vector store.
   - Generates suggestions using 3 Psychology based manuals.

---

## 📦 Dataset & Knowledge Base

- `intake_questions list`: Contains structured predefined set of questions to initiate mental health conversations :
    1. How would you describe your mood today on a scale of 1 to 10 (1 being very low, 10 being very high)?
    2. Have you been experiencing any significant changes in your sleep patterns recently (e.g., sleeping more or less than usual)?
    3. Have you noticed any changes in your appetite or eating habits lately?
    4. How would you rate your energy levels today? (Low, Medium, High)
    5. Can you describe any specific feelings or emotions you're currently experiencing?
- `cbt_manual.pdf`: A curated reference of CBT practices :
    1. comer abnormal psychology 8th edition
    2.  Research Methods in Psychology
    3.   The Body Keeps the Score.

---

## 🧪 Example Use Case

```plaintext
Bot:Hey! Please answer these so that I can help you:

1. How would you describe your mood today on a scale of 1 to 10 (1 being very low, 10 being very high)?
2. Have you been experiencing any significant changes in your sleep patterns recently (e.g., sleeping more or less than usual)?
3. Have you noticed any changes in your appetite or eating habits lately?
4. How would you rate your energy levels today? (Low, Medium, High)
5. Can you describe any specific feelings or emotions you're currently experiencing?

User: 1 → 3  
      2 → sleeping less  
      3 → yes  
      4 → low  
      5 → sadness

Bot: Okay, thank you for sharing that. I understand you're feeling quite low today. To get a better understanding of what might be contributing to this, could you answer a few more questions?

1. Can you tell me more about the changes in your appetite? Are you eating more or less than usual, and do you have any specific cravings or aversions?

2. What do you think is causing you to sleep less? Are you having trouble falling asleep, staying asleep, or waking up too early?

3. Can you identify any specific events, situations, or thoughts that seem to trigger or worsen your feelings of sadness?

4. How long have you been feeling this way?

5. Are there any activities or people that usually help you feel better, and have you tried engaging with them recently?
User: ............


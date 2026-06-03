# Multi-Agent-Orchestration-Health-care-Project
# Overview

This project demonstrates a real-world implementation of Master Agent Orchestration using Salesforce Agentforce.

The solution is designed for the healthcare industry, where a single Master Orchestration Agent intelligently manages and coordinates multiple specialized healthcare agents. Instead of requiring users to interact with different agents individually, the Master Agent understands the user's intent, determines the most appropriate agent to handle the request, passes the required context and parameters, and returns a unified response.

#  Project showcases:

Multi-Agent Architecture
Agent-to-Agent Communication
Context Passing Between Agents
Intelligent Intent Detection
Dynamic Agent Routing
Retrieval-Augmented Generation (RAG)
Salesforce Agentforce
Embedded Messaging Integration
Healthcare Industry Use Cases
NLP-Based Response Enhancement
Business Problem

Healthcare organizations often need to support different types of patient requests, such as:

Health-related questions
Symptom analysis
Medicine information
Appointment scheduling
Doctor recommendations
Medical concerns
Risk assessments
Patient guidance

Traditionally, each function would require a separate application or support process.

This project solves that challenge by using a centralized Master Orchestration Agent that automatically routes conversations to the most relevant specialized healthcare agent.

# Used Agentforce Service Agents
<img width="988" height="294" alt="image" src="https://github.com/user-attachments/assets/42f70695-b430-4693-a2b7-ef668cd1d767" />

# Architecture

<img width="1366" height="543" alt="image" src="https://github.com/user-attachments/assets/95b2e204-3a8e-4a28-a947-85aa340cc489" />
<img width="1366" height="449" alt="image" src="https://github.com/user-attachments/assets/9309e990-146a-4767-b36b-4b76163976c2" />

 # How Master Agent Orchestration Works
 # Step 1: User Query

The user starts a conversation through the healthcare portal using Embedded Messaging.

Example:

I feel chest pain. What should I do?
# Step 2: Intent Understanding

The Master Orchestration Agent analyzes the user query using LLM capabilities.

It identifies:

User Intent
Required Agent
Relevant Context
Required Parameters

Example:

{
  "symptom": "chest pain",
  "intent": "health_assistance"
}
# Step 3: Agent Selection

The Master Agent determines which specialized healthcare agent should handle the request.

Example:

Intent Detected:
Health Assistance

Selected Agent:
Health Assistant AI
Step 4: Context Passing

The Master Agent forwards the user query, context, and extracted parameters to the selected child agent.

Example:

{
  "symptom": "chest pain",
  "patientQuery": "I feel chest pain. What should I do?"
}

This demonstrates Agent-to-Agent Context Passing.

# Step 5: Child Agent Processing

The selected child agent performs its specialized work using:

Agent Topics
Agent Actions
Prompt Instructions
Knowledge Articles
Data Library Resources
RAG Architecture

The child agent generates a response based on its domain expertise.

# Step 6: Response Returned to Master Agent

After completing its task, the child agent sends the response back to the Master Orchestration Agent.

The Master Agent:

Validates the response
Applies NLP enhancements
Formats the response
Generates a user-friendly answer
# Step 7: Final User Response

The enhanced response is returned to the user through the messaging channel.

User → Master Agent → Child Agent
             ↓
      Context Passing
             ↓
      Child Processing
             ↓
      Response Returned
             ↓
      NLP Enhancement
             ↓
          User



# Final Conversation Demonstrations 

Case 1 . if user query "I want to see the adherence of Patient Aarav Sharma and also booked the appointment with Dr. Priya Menon for date 03 June for time 3 Am " then agent route to first Adherence ai and then Appointment Booking Ai .

<img width="703" height="584" alt="image" src="https://github.com/user-attachments/assets/13909b3b-51b8-446e-9f7c-9e508b80ec4f" />



Case 2. If user have some medical query and also best doctor recommendation  and ask for doctor appointment so agent will answer like that .


<img width="1111" height="510" alt="image" src="https://github.com/user-attachments/assets/0051d82b-25c1-4d85-9286-0049a5cf44ca" />


Case 3. Use this Master agent on your experience cloud  or external site agent bot and it will answer all questiion by routing the agent directlly throught site.

<img width="937" height="574" alt="image" src="https://github.com/user-attachments/assets/73736066-4748-4e86-b0d5-80b3c73f15bd" />

Case 4. This agent also connected to Data cloud Calculated insights so this runs every hour and refine the patient to high possibly disease category and also divide thier into segment and trigger the data activation and insure future high risk possibility prediction

<img width="876" height="496" alt="image" src="https://github.com/user-attachments/assets/14fe1c2a-7b2f-4f05-9f1f-3f107a175af6" />


# Core Features

### 1. Healthcare Query Assistance

The platform provides intelligent healthcare assistance by answering user questions related to diseases, symptoms, allergies, medications, treatments, and general health concerns. The Health Assistant Agent uses Retrieval-Augmented Generation (RAG) with the Agentforce Data Library to deliver context-aware and relevant healthcare information.

### 2. Doctor Recommendation Engine

Based on the symptoms or medical concerns shared by the user, the system automatically identifies the most suitable medical specialization and recommends appropriate doctors. This helps patients quickly connect with healthcare professionals who are best suited to address their condition.

### 3. Medicine Guidance and Recommendations

The solution assists users with medicine-related queries by providing general medication information, explaining medicine usage, and suggesting commonly used over-the-counter medicines when appropriate. Responses are generated using trusted healthcare knowledge sources connected to the agent.

### 4. Prescription and Treatment Information

Users can ask questions related to prescriptions, treatment plans, medication schedules, and general medicine concerns. The agent simplifies complex medical information and provides easy-to-understand guidance while encouraging consultation with healthcare professionals when necessary.

### 5. Doctor Search and Availability Management

Patients can search for doctors based on specialization and view available healthcare professionals through a conversational interface. The system helps users discover the right doctor without manually browsing multiple records or schedules.

### 6. Patient Appointment Management

The platform allows patients to view all their scheduled appointments, access appointment details, and manage upcoming healthcare visits directly through the AI-powered interface.

### 7. Doctor Appointment Visibility

Healthcare providers can view their booked appointments and manage patient schedules efficiently. This feature helps doctors monitor daily appointments and maintain organized scheduling information.

### 8. Appointment Booking and Cancellation

The system supports appointment creation, modification, and cancellation between patients and doctors. Built-in scheduling validation prevents overlapping appointments and ensures accurate appointment management across the healthcare network.

### 9. Medication Adherence Tracking

The Medication Adherence Agent continuously monitors patient medicine-tracking records and analyzes adherence behavior. By evaluating treatment history and medication patterns, the system determines whether a patient is following prescribed treatment plans.

### 10. AI-Powered Medication Reminder and Risk Awareness

When a patient misses prescribed medication, the platform automatically evaluates the disease, treatment plan, and medicine details. It then generates personalized reminders explaining why the medication is important and what health risks may arise if treatment is not followed consistently.

### 11. High-Risk Patient Identification

Using Salesforce Data Cloud Calculated Insights, the platform identifies patients who may be at higher risk based on disease history, adherence patterns, and behavioral indicators. This allows healthcare organizations to proactively monitor vulnerable patients and prioritize care efforts.

### 12. Predictive Risk Segmentation

The solution leverages pre-calculated risk models and patient segmentation to classify individuals into different risk categories. These insights help healthcare teams implement preventive care strategies and improve long-term patient outcomes.

### 13. Agent-to-Agent Communication

The project demonstrates real Agentforce Agent-to-Agent communication, where specialized healthcare agents collaborate to complete complex requests. The Master Agent coordinates interactions and ensures information flows correctly between participating agents.

### 14. Context Passing and Intelligent Orchestration

A Master Orchestration Agent acts as the central coordinator of the system. It understands user intent, selects the most appropriate healthcare agent, passes relevant context and parameters, receives responses from child agents, and delivers a unified response back to the user.

### 15. External MCP Pharmacy Integration

The platform integrates with an external MCP server to access pharmacy and medicine availability information. This enables healthcare agents to retrieve real-time medicine data and extend capabilities beyond the Salesforce ecosystem.

# Conclusion

This project demonstrates a complete Healthcare Multi-Agent Orchestration solution built on Salesforce Agentforce. It combines a Master Orchestration Agent, Agent-to-Agent communication, intelligent context passing, Retrieval-Augmented Generation (RAG), Salesforce Data Cloud, Calculated Insights, patient risk segmentation, medication adherence automation, appointment management, and external MCP integrations to solve real healthcare business challenges.

Through this project, I gained hands-on experience in designing multi-agent architectures, implementing orchestration patterns, building AI-powered healthcare workflows, integrating external services, leveraging predictive insights, and creating scalable Agentforce solutions that automate patient engagement and healthcare operations.

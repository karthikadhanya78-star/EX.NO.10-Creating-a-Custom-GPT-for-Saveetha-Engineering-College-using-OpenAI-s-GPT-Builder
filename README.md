# EX.NO.10-Creating-a-Custom-GPT-for-Saveetha-Engineering-College-using-OpenAI-s-GPT-Builder
## AIM
To understand the concept of a Custom GPT and to design, build, configure, and publish a Custom GPT chatbot for Saveetha Engineering College (www.saveetha.ac.in) using OpenAI's GPT Builder, so that it can answer student and visitor questions about the college's courses, admissions, fees, facilities, and placements.
## WHAT IS A CUSTOM GPT?
A Custom GPT is a personalised version of ChatGPT that can be built without writing any code. It is created by giving the GPT Builder three things: a name, a set of Instructions that describe how it should behave, and (optionally) reference files called Knowledge that it reads before answering. Once published, the Custom GPT behaves like a specialised chatbot — for example, a “Saveetha Engineering College Assistant” that always answers using the college's own information instead of general internet knowledge.
### TOOLS REQUIRED
•	Web browser – Google Chrome or Microsoft Edge
•	A ChatGPT account with a Plus, Team, Enterprise, or Edu subscription (the GPT Builder is not available on the free plan)
•	OpenAI's GPT Builder – built into ChatGPT, opened from chatgpt.com/create
•	Reference material about Saveetha Engineering College, collected from www.saveetha.ac.in (About, Courses, Admission, Placement, and Contact pages)
•	MS Word / Google Docs – to organise the collected information into clean Knowledge files (PDF/DOCX) before uploading
•	(Optional) Canva or the built-in DALL·E image generator – to design a profile picture/logo for the GPT

# THEORY
1. CUSTOM GPT

A Custom GPT is a specially configured version of ChatGPT designed for a specific purpose.

Instead of giving the same instructions repeatedly in every conversation, the required behaviour and task can be configured in the GPT.

A Custom GPT may include:

Name
Description
Instructions
Conversation starters
Knowledge files
Recommended model
Capabilities
Apps or Actions, depending on the configuration

These components help define what the GPT should do and how it should respond.

2. GPT BUILDER

The GPT Builder is used to create and configure a Custom GPT.

According to the current OpenAI documentation, GPT creation and publishing depend on account and workspace eligibility. New GPT creation is currently available in eligible Business, Enterprise, and Edu workspaces when permissions allow it; personal accounts cannot create new GPTs.

An eligible user can generally configure the GPT by defining:

Purpose
   ↓
Instructions
   ↓
Knowledge
   ↓
Conversation Starters
   ↓
Capabilities
   ↓
Testing
   ↓
Custom GPT
3. SAVEETHA ENGINEERING COLLEGE CUSTOM GPT

The purpose of this Custom GPT is to act as a simple AI assistant for students.

The GPT can be configured to provide information related to:

College information
Departments
Courses
Academic programs
Laboratories
Student activities
Events
Projects
General academic queries
Basic campus-related information

The information provided by the GPT should depend on the knowledge files and instructions configured by the GPT creator.

4. INSTRUCTIONS

Instructions are one of the most important components of a Custom GPT.

They define:

What the GPT should do.
How it should respond.
The language and tone it should use.
The structure of its answers.
The information it should prioritize.
The tasks it should avoid.

OpenAI recommends using clear and concrete instructions, especially for multi-step workflows.

Example Instructions
You are an AI assistant designed to help students of
Saveetha Engineering College.

Provide clear, accurate, and student-friendly responses.

Use the uploaded knowledge files as the primary source for
college-specific information.

If the requested information is not available in the knowledge
files, clearly inform the user.

Use headings and bullet points when appropriate.

Provide answers in simple and understandable language.
5. KNOWLEDGE BASE

Knowledge allows a Custom GPT to use information from uploaded files during a conversation.

For a college-based Custom GPT, suitable knowledge files may include:

College handbook
Department information
Course information
Academic regulations
Student guidelines
Laboratory manuals
Event information
Frequently asked questions

Knowledge files act as reference material for the GPT, while instructions define the behaviour of the GPT.

The working process can be represented as:

User Query
     ↓
Custom GPT
     ↓
Search Relevant Knowledge
     ↓
Process Instructions
     ↓
Generate Response
     ↓
Display Answer
6. CONVERSATION STARTERS

Conversation starters are example questions displayed to users when they begin interacting with a Custom GPT.

Examples for the Saveetha Engineering College GPT may include:

Tell me about the available departments.
Provide information about the ECE department.
What academic information is available?
Help me understand the college guidelines.

Conversation starters help users understand the purpose and functionality of the Custom GPT.

7. CAPABILITIES

Capabilities extend the functionality of a Custom GPT.

Depending on the available configuration, capabilities may include:

Web search
Image generation
Data analysis
Other supported tools and integrations

These capabilities can allow the GPT to perform tasks beyond normal text generation. Available capabilities depend on the account, workspace configuration, permissions, and region.

For a basic college information assistant, the main requirement may simply be:

Clear Instructions
+
College Knowledge Files
+
Student Queries
8. WORKING PRINCIPLE

The Custom GPT works by combining user input with its configured instructions and available knowledge.

The general process is:

Step 1: User Query

The student enters a question.

Example:

Tell me about the Electronics and Communication Engineering department.
Step 2: Query Processing

The Custom GPT analyzes the question to understand the user's request.

Step 3: Instruction Processing

The GPT follows its predefined instructions regarding:

Response style
Language
Format
Information source
Step 4: Knowledge Retrieval

The GPT uses relevant uploaded knowledge files when answering college-specific questions.

Step 5: Response Generation

The AI processes the available information and generates a response.

Step 6: Response Display

The final answer is displayed to the student.

# BLOCK DIAGRAM

CUSTOM GPT FOR SAVEETHA ENGINEERING COLLEGE
```
┌──────────────────────────┐
│        STUDENT           │
│          USER            │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│       USER QUERY         │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│     CUSTOM GPT SYSTEM    │
└────────────┬─────────────┘
             ↓
     ┌───────┴────────┐
     ↓                ↓
┌──────────────┐ ┌───────────────┐
│ INSTRUCTIONS │ │   KNOWLEDGE   │
│              │ │     FILES     │
└──────┬───────┘ └───────┬───────┘
       └────────┬────────┘
                ↓
┌──────────────────────────┐
│   AI PROCESSING MODEL    │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│    RESPONSE GENERATOR    │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│   COLLEGE INFORMATION    │
│      AND ASSISTANCE      │
└──────────────────────────┘
```


## PROCEDURE

### Step 1: Collecting College Information (Knowledge Preparation)
Before building the GPT, gather accurate information about Saveetha Engineering College from its official website www.saveetha.ac.in. Visit and note down content from pages such as About Us, Departments/Courses Offered, Admission Procedure, Fee Structure, Placements, Facilities, and Contact Details. Paste this content into a Word document and save it as a PDF. This file becomes the “Knowledge” for the GPT, so that it answers only with correct, college-specific information instead of guessing.

### Step 2: Signing in to ChatGPT
Open a web browser and go to chatgpt.com. Sign in using an existing OpenAI account, or create a new one. Make sure the account is upgraded to a ChatGPT Plus, Team, Enterprise, or Edu plan, since the GPT Builder is a paid-plan feature and is not available on the free version.

### Step 3: Opening the GPT Builder
On the left sidebar, click “Explore GPTs” and then click the “+ Create” button (or go directly to chatgpt.com/create). This opens the GPT Builder, which has two tabs: Create and Configure.

### Step 4: Building the GPT Conversationally (Create Tab)
In the Create tab, type a plain-English description of the required GPT in the message box, for example:
“Create a GPT for Saveetha Engineering College that answers questions about admissions, courses, fees, placements, and campus facilities in a friendly and professional tone.”
The Builder chats back and automatically suggests a name, a short description, and a profile picture for the GPT based on this description.

### Step 5: Fine-Tuning with the Configure Tab
Switch to the Configure tab for full manual control over the GPT, and fill in the following fields:
•	Name: e.g., “Saveetha Engineering College Assistant”
•	Description: a one-line summary, e.g., “Your guide to admissions, courses, fees, and placements at Saveetha Engineering College.”
•	Instructions: a detailed system prompt describing the GPT's role, tone, and rules (see the sample instructions given later in this report).
•	Conversation starters: four sample questions users can click to begin the chat, for example:
1.	What B.Tech courses does Saveetha Engineering College offer?
2.	How do I apply for admission?
3.	What is the placement record of the college?
4.	Where is the campus located?

### Step 6: Uploading Knowledge Files
In the Knowledge section of the Configure tab, click “Upload files” and add the PDF/DOCX file prepared in Step 1. This lets the GPT search and quote from the actual college content instead of guessing, which keeps its answers accurate and trustworthy. As a best practice, upload 2 to 5 well-organised files rather than many small ones, since retrieval accuracy drops once too many files are added.

### Step 7: Enabling Capabilities
In the Capabilities section, select the tools the GPT is allowed to use:
•	Web Browsing – to fetch live information if the uploaded knowledge file becomes outdated
•	Code Interpreter & Data Analysis – not usually needed for a college-information bot, so it can be left off
•	Image Generation (DALL·E) – optional, for generating a campus or course-related illustration
For a simple college-information GPT, enabling Web Browsing along with the uploaded Knowledge is generally enough.

### Step 8: Setting Up Actions (Optional, Advanced)
Actions allow the GPT to call an external API — for example, to check live seat availability or fetch the latest fee notification from a college server. This requires an API endpoint and an OpenAPI schema, so it is optional for a basic informational GPT and can be skipped by beginners.

### Step 9: Testing the GPT
Use the Preview panel on the right side of the Builder to chat with the GPT before publishing it. Ask sample questions such as “What courses are offered?” or “How do I apply for admission?” and check whether the answers are correct, polite, and based on the uploaded knowledge. If any answer is wrong or incomplete, edit the Instructions or Knowledge files and test again until the responses are accurate.

### Step 10: Publishing and Sharing
Click the “Create” (or “Save”) button in the top-right corner of the Builder. Choose who can access the GPT:
•	Only me – for personal testing
•	Anyone with the link – to share with students and faculty of the department
•	GPT Store (Public) – to make the GPT visible to all ChatGPT users
Click “Publish”/“Update” to finish. Copy the generated link and share it with students through the college portal, WhatsApp group, or LMS.

### SAMPLE INSTRUCTIONS (SYSTEM PROMPT) FOR THE GPT
<br><img width="587" height="151" alt="image" src="https://github.com/user-attachments/assets/cd378cba-9488-4cc9-9974-99a44f3695f8" /></br>

## SAMPLE OUTPUT SCREEN
The screen below shows a sample conversation with the published “Saveetha Engineering College Assistant” Custom GPT, illustrating how it answers a student's admission query using the uploaded knowledge files.
</br><img width="545" height="385" alt="image" src="https://github.com/user-attachments/assets/677bee25-a510-48db-824d-4dbb5795d610" /></br>

APPLICATIONS

A Custom GPT for Saveetha Engineering College can be useful for:

Student Assistance

Students can ask common questions and receive automated assistance.

Academic Support

The GPT can help explain academic information available in its knowledge source.

Information Retrieval

Students can obtain information from uploaded college documents.

Frequently Asked Questions

Common questions can be handled automatically.

Department Assistance

Separate knowledge and instructions can be configured to provide department-specific information.

Event Information

The GPT can provide information about college events if relevant information is included in its knowledge files.

Learning Support

It can assist students in understanding topics and accessing available academic information.

# ADVANTAGES
Provides quick assistance.
Gives consistent responses.
Reduces repetitive questions.
Can use uploaded college knowledge.
Provides a user-friendly interface.
Can be customized for a specific institution.
Can be improved by updating instructions.
Can support different academic tasks.
Helps students access information easily.
Can be tested and refined before wider use.

# LIMITATIONS
The quality of responses depends on the provided instructions.
Incorrect or incomplete knowledge files can affect responses.
College information must be updated regularly.
The GPT may not contain information that has not been provided.
Some questions may require assistance from college staff.
Capabilities depend on account and workspace permissions.
A Custom GPT should not be treated as the official source for information unless its knowledge is properly maintained and approved.

# FUTURE ENHANCEMENTS

The system can be improved by adding:

Updated college knowledge files.
Department-specific assistants.
Multilingual support.
Event information.
Academic calendar information.
Student FAQ support.
Personalized academic assistance.
Data analysis capabilities.
Integration with approved external systems where permitted.

## OUTPUT
A working Custom GPT named “Saveetha Engineering College Assistant” is created and published. When a user asks questions like “What courses does Saveetha offer?” or “How can I apply for B.Tech admission?”, the GPT replies with accurate information drawn from the uploaded college knowledge files, in a friendly and professional tone.

## RESULT
Thus, a Custom GPT chatbot for Saveetha Engineering College was successfully designed, configured with knowledge files and instructions, tested, and published using OpenAI's GPT
Builder.

## CONCLUSION

### In conclusion, building a Custom GPT shows how modern generative AI tools let anyone — even without programming knowledge — create a specialised, organisation-branded chatbot in a few simple steps. By combining clear instructions, focused knowledge files, and the right capabilities, Saveetha Engineering College can offer students and visitors instant, accurate answers to their questions, saving time for both the institution and its users.


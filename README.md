# aipi561 ADHD Guardian 🤖
AHDH Guardian is a web application specifically designed to support professionals and students with ADHD. It aims to mitigate executive function challenges by providing AI-driven task decomposition, prioritization assistance, and positive reinforcement.

## Motivation:
As someone with ADHD myself, along with an estimated 4-5% of adults worldwide with ADHD (approximately 366 million people), initiating and completing tasks can feel like hitting an invisible barrier. This executive function challenge involves difficulties with: 
* Planning and organizing work
* Sequencing steps in logical order
* Prioritizing competing demands
* Overcoming the mental inertia required to simply start
  
## Solution:
ADHD Guardian acts as a non-judgmental, supportive co-pilot specifically designed to help neurodivergent individuals navigate executive function hurdles. 

The application leverages Azure OpenAI (GPT-4o) through an AI persona named "Em" to:

Decompose Overwhelm: Users input a task or objective they find daunting
Generate Actionable Steps: Em breaks the task down into 3-5 small, concrete, achievable first steps
Provide Sincere Encouragement: Crucially, Em offers brief, gentle understanding focused only on starting the very first step—validating the difficulty without judgment
The goal is not to replace planning tools but to provide the scaffolding and dopamine boost needed to overcome initiation paralysis and build momentum.

## Timeline
* Week 1: Ideation. Problem/motivation + solution description + Timeline
* Week 2: Architecture/Component Diagram
* Week 3: Frontend application (Flask, HTML, and Tailwind CSS)
* Week 4: Use Azure OpenAI to breakdown user-inputted tasks and device action steps
* Week 5: Auth (Secure login via Azure AD)
* Week 6: Deployment and CI/CD


## Week 2 UPDATE

### Architecture Diagrams

* Overall Architecture:
![image](https://github.com/user-attachments/assets/c54ef0b0-5a9a-4188-9154-0e425791c133)
* Component Breakdown
<img width="822" alt="image" src="https://github.com/user-attachments/assets/eb0d34ee-5a15-4d10-a006-b0275257a2d2" />


* Task Decomposition Flow:
<img width="822" alt="image" src="https://github.com/user-attachments/assets/30389517-c46e-4b31-9dc5-7310d0472d1b" />


## Week 3 & 4 UPDATE

### Developed the front end and backend locally


Create and activate a virtual environment:

# Windows
python -m venv venv
.\venv\Scripts\activate

# macOS/Linux
python -m venv venv
source venv/bin/activate
Install dependencies:

pip install -r requirements.txt
Configure your .env file:

# Azure OpenAI
AZURE_OPENAI_ENDPOINT="YOUR_AZURE_OPENAI_ENDPOINT"
AZURE_OPENAI_KEY="YOUR_AZURE_OPENAI_KEY"
AZURE_OPENAI_DEPLOYMENT_NAME="YOUR_MODEL_DEPLOYMENT_NAME"

# Azure AD App Registration
CLIENT_ID="YOUR_APP_REGISTRATION_CLIENT_ID"
CLIENT_SECRET="YOUR_APP_REGISTRATION_CLIENT_SECRET_VALUE"
AUTHORITY="https://login.microsoftonline.com/common" # Or your specific tenant
REDIRECT_PATH="/getAToken"
SCOPE="User.Read Calendars.Read Tasks.Read email" # Required scopes

# Flask Session
SECRET_KEY="generate-a-strong-random-secret-key-here"
Run the application:

flask run --port 5001
Access the application at http://localhost:5001

## Week 5 UPDATE

Deployed the Application and recorded final project video: https://youtu.be/mtn1pZkRc00




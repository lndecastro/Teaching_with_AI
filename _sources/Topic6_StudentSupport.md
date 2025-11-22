
# 6. Student Support  
_Promoting academic success and well-being_

This phase focuses on using generative AI to enhance the support structures available to learners, fostering inclusivity, personalization, and early intervention. This includes using AI to supplement office hours with FAQs, offering guidance on assignments and study strategies, monitoring student success through data, providing AI-curated resources like study guides, encouraging peer collaboration, and exploring the use of AI tutors. This stage includes:

1. Provide Office Hours and Timely Responses to Inquiries
2. Offer Guidance on Assignments and Study Strategies
3. Monitor Student Success
4. Provide AI-Curated Resources (e.g., Study Guides, Tutoring Suggestions)
5. Encourage Peer Collaboration and Support Networks

## 6.1 Provide Office Hours and Timely Responses to Inquiries

**Task:** 
In addition to your office hours, use generative AI to supplement your availability and provide consistent, supportive responses to common student queries (FAQ).

### Tool 1: General LLMs (e.g. ChatGPT, Copilot, Gemini, Grok, etc.)
Upload your course material and prompt the LLMs to generate an FAQ.

*Instructional Prompt*
```
Read the attached PDF file(s) and generate a structured FAQ section that summarizes the key aspects of the material. 
Ensure each FAQ includes a clear question and a concise, informative answer, and group the FAQs into thematic categories.
```

### Tool 2: Perplexity
Create a *Space* with your course material and prompt the LLMs to generate an FAQ. Use the same *instructional prompt* presented above.

### Tool 3: NotebookLM
Create a *Notebook* with your course material and use button **FAQ** to generate the FAQ. 

**Sample illustration** Inbox of AI-generated response examples, labeled by type.

## 6.2 Offer Guidance on Assignments and Study Strategies

**Task**
Use AI to offer personalized academic coaching or scaffolded support on deliverables.

*Zero-Shot Prompt*
```
Provide five examples of how generative AI can help faculty learners in a course about AI pedagogy better understand and complete their assignments. Include study strategies and task breakdowns.
```

**Sample illustration** Flowchart: Assignment → AI Feedback → Strategy Suggestion → Revision

## 6.3 Monitor Student Success

**Task:**
Use engagement data or AI-generated insights to detect patterns that indicate a need for support.

*Chain-of-Thought Prompt: Tasking the LLM with the Table Design*
```
I want to design a table to collect student information in a course. The goal is to use the data to calculate a "Student Success Score." 

1. Propose a matrix with at least 5 student variables (e.g., attendance, assignment completion, quiz scores, engagement, self-assessments).
2. For each variable, define:
   - Data type (numeric, categorical)
   - Measurement method
   - Weight or influence on success

3. Propose a formula to compute a success score from these variables (e.g., weighted average or custom equation).
4. Explain how this score can be used to monitor or support students throughout the course.
5. Save this matrix as a table in XLSX, CSV, or Google Spreadsheet format.
```

*Instructional Prompt: Guiding the LLM with a Pre-Specified Score Matrix*
```
# Prompt to Design a Student Success Score Matrix

Please provide the following details to create a matrix or table for collecting student information and calculating a success score. The matrix should include relevant student data points, and a success score will be calculated using a weighted equation. Use a clear, structured table format, and ensure the success score equation is included with explanations of each component.

## Student Information to Collect
[List the data points you want to collect for each student. Examples include:
- Student Name: [Text input, e.g., John Doe]
- Attendance Rate: [Percentage, e.g., 95%]
- Assignment Completion Rate: [Percentage, e.g., 90%]
- Quiz Average Score: [Percentage, e.g., 85%]
- Discussion Participation: [Number of posts, e.g., 5]
- Time Spent on LMS: [Hours per week, e.g., 10 hours]
Add or modify data points as needed.]

## Table Structure
[Design a table to collect the data. Example structure:
| Student Name | Attendance Rate (%) | Assignment Completion Rate (%) | Quiz Average Score (%) | Discussion Participation (Posts) | Time Spent on LMS (Hours/Week) | Success Score |
|--------------|---------------------|-------------------------------|-----------------------|---------------------------------|-------------------------------|---------------|
| [Name 1]     | [Percentage]        | [Percentage]                  | [Percentage]          | [Number]                        | [Hours]                       | [TBD]         |
| [Name 2]     | [Percentage]        | [Percentage]                  | [Percentage]          | [Number]                        | [Hours]                       | [TBD]         |
Ensure the table includes a column for the Success Score, which will be calculated.]

## Success Score Equation
[Define the equation to calculate the Success Score. Here is an example equation with weights assigned to each data point:
Success Score = (0.2 * Attendance Rate) + (0.3 * Assignment Completion Rate) + (0.3 * Quiz Average Score) + (0.1 * Normalized Discussion Participation) + (0.1 * Normalized Time Spent on LMS)

- **Weights Explanation**:
  - Attendance Rate (20%): Reflects engagement and consistency.
  - Assignment Completion Rate (30%): Measures task completion, a key indicator of effort.
  - Quiz Average Score (30%): Assesses academic performance.
  - Discussion Participation (10%): Gauges interaction (normalized to a 0-100 scale, e.g., max posts = 10, so 5 posts = 50%).
  - Time Spent on LMS (10%): Indicates resource usage (normalized to a 0-100 scale, e.g., max expected hours = 20, so 10 hours = 50%).

- **Normalization**:
  - Normalize Discussion Participation: (Student Posts / Max Expected Posts) * 100
  - Normalize Time Spent on LMS: (Student Hours / Max Expected Hours) * 100

Modify weights or add/remove components as needed.]

## Additional Notes
- Ensure all percentages are on a 0-100 scale for consistency.
- The Success Score should range from 0 to 100, with higher scores indicating greater likelihood of success.
- Include a brief explanation of how to interpret the score (e.g., “Scores above 80 indicate strong performance, 60-80 suggest moderate success with room for improvement, below 60 indicate a need for intervention”).

## Output 
[Generate the final table and equation in a clear format, e.g.:
**Student Success Score Matrix**

| Student Name | Attendance Rate (%) | Assignment Completion Rate (%) | Quiz Average Score (%) | Discussion Participation (Posts) | Time Spent on LMS (Hours/Week) | Success Score |
|--------------|---------------------|-------------------------------|-----------------------|---------------------------------|-------------------------------|---------------|
| John Doe     | 95                  | 90                            | 85                    | 5                               | 10                            | [Calculated]  |
| Jane Smith   | 80                  | 70                            | 65                    | 3                               | 8                             | [Calculated]  |

**Success Score Equation**  
Success Score = (0.2 * Attendance Rate) + (0.3 * Assignment Completion Rate) + (0.3 * Quiz Average Score) + (0.1 * Normalized Discussion Participation) + (0.1 * Normalized Time Spent on LMS)

**Interpretation**  
- Above 80: Strong performance  
- 60-80: Moderate success, room for improvement  
- Below 60: Needs intervention  
]

**Output file and graphs**
- Save the generated table in an xlsx or csv spreadsheet file.
- Generate a bar graph for each student with the values in each criteria normalized in the 0-100 interval. The success score bar should have different colors for each of the three interpretations.
```

**Sample illustration** Early alert system diagram with AI dashboard and action paths.

## 6.4 Provide AI-Curated Resources (e.g., Study Guides, Tutoring Suggestions)

**Task:**
Curate and generate personalized learning resources using GenAI.

*Instructional Prompt*
```
Create a custom study guide using generative AI for learners struggling with [the ethical use of AI in education]. Include summaries, definitions, discussion questions, and one quiz.
```

**Sample illustration** Sample study guide layout with AI-generated components.

## 6.5 Encourage Peer Collaboration and Support Networks

**Task:**
Design AI-assisted prompts and activities that build peer learning environments.

**Use Case 1: Initiating Collaboration & Group Formation**
Help students find common ground, form groups, and define initial collaborative tasks.

*Role-Based Prompt*
```
Act as a matchmaker. Given the following student responses about their biggest challenges in [Course Topic] and their areas of interest, suggest 3-5 potential peer learning groups. For each group, briefly explain the common thread that connects them and suggest an initial discussion topic.
Student 1: [Input: 'Struggles with [Course Topic], interested in [Topic].']
Student 2: [Input: 'Finds [Course Topic] confusing, good at explaining [Topic].']
Student 3: [Input: 'Wants to apply [Course Topic] to real-world cases, enjoys problem-solving.']
```

**Use Case 2: Collaborative Icebreaker & Goal Setting**
Help students to feel comfortable with one another, the instructor, and the learning environment.

*Instructional Prompt*
```
Generate an icebreaker activity for a new peer learning group in [Course Name]. The activity should encourage members to share a personal learning goal for the upcoming module and one strength they bring to the group. After the icebreaker, provide 3 guiding questions for them to collaboratively define their group's learning objectives for the week.
```
**Use Case 3: Scenario-Based Team Formation**
Help students to build teams under a specific context (scenario).

*Instructional Prompt*
```
You are designing a collaborative project for [Course Name] focusing on [Specific Topic]. Create 3-4 diverse roles within a team (e.g., 'Researcher,' 'Synthesizer,' 'Presenter,' 'Critique Editor'). For each role, describe the primary responsibilities and the type of skills that would be best suited for it. Then, generate a short 'team charter' template that groups can fill out to define their internal roles and communication norms.
```

**Use Case 4: Fostering Support Networks & Reflection**
Encourage students to offer and seek help, reflect on the benefits of collaboration, and build a sense of community.

*Role-Based Prompt*
```
Imagine you are a student struggling with [Specific Skill/Concept]. Write 3 different ways to ask for help from a peer or a peer learning group, varying the level of detail or formality. Ensure the prompts are empathetic and clear about the challenge.
```

**Sample illustration** Collaboration map showing peers, prompts, and AI facilitation layers.

## 6.6 Introduce AI Tutors

**Task:**
Explore the use of AI assistants in dynamic, real-world contexts using **Google AI Studio** with the **Stream function** enabled. The focus is on teaching AI to interact with **your environment** through a **background camera** or **screen capture**. This powerful setup brings AI into your personal or digital workspace, enhancing observation, navigation, and learning experience.

### Tools & Setup

- **Platform**: Google AI Studio
- **Key Feature**: Stream
- **Capabilities Used**:
  - Background Camera
  - Screen Capture
  - Real-Time AI Interaction

> Ensure the **Stream** function is enabled and permissions for camera and screen sharing are granted.

**Use Case 1:** Interacting with the Physical Environment

*Scenario*: The participant activates their **background camera** and points it toward their environment (e.g., desk, classroom, lab, objects).

*Instructional + Role-Based Interaction (**Voice Prompt**)*
```
Observe my environment and describe what you see. Focus on identifying objects and their likely purpose or function. Then suggest one or two ideas for organizing or improving this workspace for productivity.
```

*Alternative **Voice Prompt** (Educational Context):*
```
Act as a tutor. I am pointing my camera at an object. Explain what you are seeing.
[SELECT THE OBJECT OR CONTEXT]
```

**What students learn**:
- How to direct the AI’s visual attention
- How to formulate prompts to extract meaningful insights from real-time observations

**Use Case 2:** Navigating the Digital Workspace

*Scenario*: The participant shares their **screen** (e.g., browser, application, workspace, spreadsheet), and the AI assistant provides support.

*Chain-of-Thought + Instructional **Voice Prompt***
```
Watch my screen as I navigate my email inbox. Help me:
1. Identify unread messages and group them by priority
2. Draft responses to the top three messages
3. Create a task list based on action items in the emails
```

*Instructional **Voice Prompt***
```
I am going to open a website I am unfamiliar with. As I explore, please explain what each section seems to do, and guide me to locate the help center and pricing information.
```




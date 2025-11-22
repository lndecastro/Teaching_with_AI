
# 7. Assessment and Feedback  
_Measuring learning and guiding improvement_

This step integrates previously designed assignments and rubrics with generative AI to enhance assessment strategies and feedback mechanisms. You will learn how to conduct assessments using existing assignment types with AI support, generate rubric-based constructive feedback, use AI-assisted self- and peer-assessment, and leverage AI for tasks like feedback generation, grading, and originality verification. The section also explores various AI tools and techniques for these tasks. The session covers the following topics:

1. Conduct Assessments Using Existing Assignment Types
2. Generate Rubric-Based, Constructive Feedback
3. Use AI-Assisted Self- and Peer-Assessment
4. Use AI for Feedback, Grading, and Originality Verification

## 7.1 Conduct Assessments Using Existing Assignment Types

**Task:**
Leverage previously developed assignments (quizzes, case studies, and projects) and embed generative AI to support delivery and evaluation.

*Instructional Prompt*
```
For each of the following assignments describe how generative AI can support their administration and analysis. Include one example prompt or tool for each assignment type. [Attach your assignments]
```

**Sample illustration** Matrix: Assignment Type × GenAI Support (e.g., quiz auto-grading, case analysis generation, project feedback).

## 7.2 Generate Rubric-Based, Constructive Feedback

**Task:**
Use the rubrics created earlier (Topic 4) to automate high-quality feedback using generative AI.

*Role-Based Prompt*
```
You are an AI tutor grading a student’s AI-enhanced case study or teaching project. Based on this rubric (1. Pedagogical Soundness, 2. AI Integration, 3. Clarity of design), provide constructive feedback for each criterion and suggest improvements. [Attach the student's assignments]
```

**Sample illustration** Rubric feedback table: Criteria | Score | AI-generated Feedback

## 7.3 Use AI-Assisted Self- and Peer-Assessment

**Task:**
Integrate reflection and peer review workflows supported by AI-generated guiding questions.

*Few-Shot Prompt*
```
Examples of peer review prompts:
1. Evaluate how effectively AI was integrated into your peer’s lesson design.
2. Suggest one way to improve ethical considerations in the use of AI.

Now generate a guided self-assessment checklist and three peer review prompts using the project rubric.
```

**Sample illustration** Checklist and review form interface with AI question generation icons.

## 7.4 Use AI for Feedback, Grading, and Originality Verification

**Task:**
Automate parts of the grading process while maintaining instructor oversight.

**Use Case 1: Finding Tools Available in the Literature**

*Zero-Shot Prompt*
```
List and briefly explain 3 tools that can be used to:
- Auto-grade AI-generated quiz responses
- Generate rubric-based feedback for student case studies
- Detect AI-generated plagiarism in teaching project submissions
Include benefits and limitations for each.
```

**Use Case 2: Auto-grade AI-generated Quiz Responses**

*Role-Based Prompt*
```
You are an expert educator, specifically an experienced grader for [Subject Name] at the [Grade Level]. Your task is to evaluate a student's answer to a quiz question.

Here is the quiz question:
[Quiz Question Text]

Here is the expected correct answer (or key concepts to be included):
[Expected Answer / Key Concepts / Rubric for scoring specific elements]

Here is the student's response:
[Student's Response Text]

Evaluate the student's response based on the following criteria and provide a score out of 5, along with a brief justification.
- **Accuracy:** How factually correct is the student's response?
- **Completeness:** Does the response cover all the essential points from the expected answer?
- **Clarity:** Is the response easy to understand and well-articulated?

Provide your output in the following JSON format:
{
  "score": [0-5 integer],
  "justification": "Explain reasoning for the score based on accuracy, completeness, and clarity."
}
```

**Use Case 3: Generate Rubric-Based Feedback for Student Case Studies**

*Role-Based Prompt with Embedded Instructional Prompts*
```
You are an expert academic evaluator for [Subject Name], specializing in providing detailed, rubric-based feedback for student case study analyses.

Here is the case study prompt/assignment description:
[Case Study Prompt/Assignment Description Text]

Here is the student's case study submission:
[Student's Full Case Study Submission Text]

Here is the grading rubric:
[Detailed Rubric - Paste the full rubric here. Include criteria, performance levels (e.g., Excellent, Good, Developing, Beginning), and their descriptions.]

Your task is to:
1.  **Evaluate the student's submission against each criterion in the rubric.**
2.  **Assign a performance level/score for each criterion based on the rubric's descriptors.**
3.  **Generate specific, actionable feedback for each criterion, explaining *why* the student received that score and providing concrete suggestions for improvement.**
4.  **Provide an overall summary of strengths and areas for development.**
5.  **Calculate the total score based on the rubric's point values.**

Provide your output in a structured format, similar to a feedback report:

## Feedback Report for Case Study Analysis

**Student Name:** [Leave Blank / Student ID if known]
**Assignment:** Case Study Analysis: [Case Study Title]

### Rubric Evaluation:

**Criterion 1: [Criterion Name from Rubric]**
* **Score/Level:** [e.g., 4/5 - "Good" / "Developing"]
* **Feedback:** [Specific feedback relating student's submission to this criterion's descriptors. Explain what they did well and where they could improve, using examples from their text if possible.]

**Criterion 2: [Criterion Name from Rubric]**
* **Score/Level:** [e.g., 3/5 - "Developing"]
* **Feedback:** [Specific feedback]

... (Repeat for all criteria) ...

### Overall Summary:
**Strengths:**
[Summarize overall strengths based on the feedback above.]

**Areas for Development:**
[Summarize overall areas for improvement based on the feedback above.]

**Total Score:** [Calculated Total Score] / [Maximum Possible Score]
```

**Use Case 4: Detect AI-generated Plagiarism in Teaching Project Submissions**
> **Note:** Detecting AI-generated plagiarism with a general LLM is a trickier and less reliable task than dedicated tools like Turnitin or GPTZero. While an LLM can analyze text for patterns, it lacks the specific training and sophisticated algorithms of specialized detectors. It's best used as a signal for human review, not as a definitive judgment.

*Role_based Prompt*
```
You are an expert text analyst specializing in identifying characteristics of human-written versus AI-generated content. You understand that AI-generated text often exhibits patterns like:
- High predictability (low perplexity)
- Uniform sentence structure and vocabulary
- Lack of distinct personal voice or anecdotes
- Repetitive phrasing or transition words (e.g., "deep dive", "furthermore," "in conclusion," "however")
- Grammatically perfect but bland language
- Potential factual inaccuracies or "hallucinations" if the AI wasn't grounded in specific sources.

Here is a student's project submission:
[Student's Project Submission Text]

Analyze the text and provide an assessment of whether it exhibits characteristics commonly associated with AI-generated content. Do NOT make a definitive judgment, but highlight specific elements that *suggest* it might be AI-generated, or that it appears to be human-written.

Focus your analysis on:
1.  **Perplexity and Burstiness:** Does the text feel highly predictable, or does it have natural variations in sentence length and complexity?
2.  **Voice and Personality:** Is there a distinct student voice, personal reflection, or anecdotal evidence?
3.  **Vocabulary and Structure:** Is the language overly formal or repetitive? Are sentence structures varied?
4.  **Content Nuance:** Does the content demonstrate deep understanding, critical thinking, and original insights, or does it feel generic and surface-level?

Provide your analysis in a clear, bulleted list, followed by an overall assessment.

**Example of Analysis Format:**

-   **Perplexity/Burstiness:** [Comment on predictability/variation]
-   **Voice/Personality:** [Comment on presence/absence of unique voice]
-   **Vocabulary/Structure:** [Comment on word choice and sentence construction]
-   **Content Nuance:** [Comment on depth of understanding and originality]

**Overall Assessment:** [Summarize likelihood of AI generation based on observations, e.g., "The text exhibits several characteristics consistent with AI generation, such as...", or "The text appears to be human-written, showing a distinct voice and varied sentence structures."]
```

> **Note:** To make these gradings more streamlined in standard LLMs, it is possible to create a **Project** in ChatGPT/Claude, a **Space** in Perplexity, or a **Gem** in Gemini. These are organizational features (as of 2024–2025) that allow you to create persistent, goal-oriented workspaces inside the tools. They are designed for more structured, long-term, or collaborative work with the AI.

**Use Case 5: Using a Single Prompt to Perform the Three Gradings (Essay, Case Study, and Project)**

*Role-Based Prompt with Embedded Instructional Prompts*
```
# Prompt to Grade Essays

You are an educational assistant tasked with grading essays. Perform the following tasks for a course on 'Teaching and Learning with AI', using student submissions. The tasks are: auto-grading quiz responses, generating rubric-based feedback for student case studies, and detecting AI-generated plagiarism in teaching project submissions. Follow the instructions for each task, ensuring consistency, accuracy, and actionable feedback.

## Task 1: Auto-Grade Quiz Responses
**Objective**: Grade quiz responses, including those potentially generated by AI, using a provided rubric.
**Inputs**:
- Quiz Question: [e.g., "How can AI support the 'Analyze' level of Bloom’s Taxonomy in a classroom?"]
- Sample Responses: [e.g., Response 1: "AI can generate case studies for students to break down data patterns."; Response 2: "AI helps with analyzing stuff."]
- Rubric:
  - Content Accuracy (50%): Correctness of concepts.
  - Clarity (30%): Logical flow and readability.
  - Completeness (20%): Addresses all parts of the question.

**Instructions**:
1. Evaluate each response against the rubric.
2. Assign a score (0-100) with a breakdown (e.g., Content: 40/50, Clarity: 20/30, Completeness: 15/20).
3. Provide 1-2 sentences of feedback with improvement suggestions.
4. Return results in a table format:
   | Response | Content Accuracy (50) | Clarity (30) | Completeness (20) | Total Score (100) | Feedback |

## Task 2: Generate Rubric-Based Feedback for Student Case Studies
**Objective**: Provide detailed feedback on a case study submission using a rubric.
**Inputs**:
- Case Study Submission: [e.g., "I used an AI chatbot to teach students about computational complexity. It asked questions and gave feedback. Students found it helpful."]
- Rubric:
  - Relevance (40%): Alignment with course topics (e.g., computational complexity, AI pedagogy).
  - Depth of Analysis (30%): Insight into AI application in teaching.
  - Presentation (20%): Clarity and structure.
  - Innovation (10%): Creative use of AI tools.

**Instructions**:
1. Assess the submission against each rubric criterion, assigning scores out of 100 for each (e.g., Relevance: 60/100).
2. Calculate a total score as a weighted average.
3. Provide 2-3 sentences of feedback, including strengths, weaknesses, and suggestions.
4. Format the output as a table with scores and feedback:
   | Criterion | Score (out of 100) | Feedback |
   | Total Score | [Calculated] |

## Task 3: Detect AI-Generated Plagiarism in Teaching Project Submissions
**Objective**: Identify potential AI-generated content in project submissions.
**Inputs**:
- Project Submission: [e.g., "The application of AI in education enhances student engagement through personalized learning pathways. AI systems adapt content delivery based on individual performance metrics."]
- Detection Criteria: Look for signs of AI generation (e.g., overly polished phrasing, generic language, lack of personal voice, uniform structure).

**Instructions**:
1. Analyze the submission for signs of AI generation.
2. Assign a confidence score (0-100%) indicating the likelihood of AI generation.
3. Provide 1-2 sentences explaining your assessment and suggest next steps if plagiarism is suspected.
4. Return results in a table format:
   | Submission | Confidence Score (AI-Generated) | Assessment and Next Steps |

## Additional Notes
- Use course context where applicable.
- Ensure feedback is constructive and aligned with educational goals (e.g., improving student understanding of the topic).
- For Task 3, if the confidence score is high (>70%), recommend actions like requesting a revision or draft history by a specific date.
- Identify performance trends and misconceptions across students.
- Summarize this data to prepare a follow-up review session.
```

### Tools 1: Cograder.com or EssayGrader.ai (Essay Grading)
Cograder.com and EssayGrader.ai are AI tools designed to grade essays and help teachers to provide quality feedback in less time.

**Use Case 6:** To learn how Cograder or EssaGrader work try them by selecting the *Fill in with sample* in CoGrader (or copying this sample into EssayGrader) and analyze the output.

**Use Case 7:** If you have the case study delivered by a student, import or create the rubric into one of the tools to assess the assignment.

### Tool 2: SciSpace

**Use Case 8:** Using function *AI Detector* input the text or upload the PDF file with the content to be checked for originality.

**Sample illustration:** Infographic of tools and risks (AI grading vs. human review).

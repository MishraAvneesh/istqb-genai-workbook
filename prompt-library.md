# 📚 My CT-GenAI Prompt Library

> Add your best prompts here as you complete each chapter project. By exam day, this becomes your personal study reference.

---

## Chapter 1 — GenAI Foundations

### Prompt: Login Page Test Cases (6-part structure)
**Technique:** Zero-shot with structured format  
**Use when:** Quick test case generation for simple features

```
Role: You are a senior software QA engineer.
Context: We are testing a simple login page with username, password, and Login button.
Instruction: Generate 8 test cases.
Constraints: Include 2 negative cases and 1 boundary value test.
Output Format: Table — Test ID | Name | Steps | Expected Result
```

**My notes:** *(add what you observed when running this)*

---

## Chapter 2 — Prompt Engineering

### Prompt: Acceptance Criteria (Few-shot)
**Technique:** Few-shot prompting  
**Use when:** Generating Gherkin acceptance criteria from user stories

```
Role: You are a QA engineer writing Gherkin acceptance criteria.
Context: [Your app context here]

Examples:
User Story: "User can apply discount code"
AC: Given a valid code exists / When entered at checkout / Then discount applied

Instruction: Write AC for: [Your user story here]
Constraints: Include at least one negative scenario.
Output Format: Gherkin (Given/When/Then)
```

**My notes:** *(add what you observed)*

### Prompt: Prompt Chaining — Test Design Pipeline
**Technique:** Prompt chaining  
**Use when:** Breaking down complex user stories into test assets step by step

```
Step 1: "Extract all testable conditions from this user story: [paste story]"
Step 2 (feed Step 1 output): "Generate test cases for each condition above."
Step 3 (feed Step 2 output): "Flag the top 3 highest priority test cases and explain why."
```

**My notes:** *(add what you observed)*

### Prompt: Meta Prompt Request
**Technique:** Meta prompting  
**Use when:** You're not sure how to write a good prompt for a new task

```
Write me the best possible structured prompt (using Role, Context, Instruction, 
Input Data, Constraints, Output Format) to generate synthetic test data for 
[your feature] that covers edge cases without exposing real PII.
```

**My notes:** *(add what the AI gave you)*

---

## Chapter 3 — Managing Risks

### Prompt: Hallucination Trigger (for learning)
**Use when:** Demonstrating to others what hallucinations look like

```
Vague (triggers hallucination):
"Generate test cases for the XYZ banking app."

Improved (reduces hallucination):
Role: You are a QA engineer.
Context: The banking app has ONLY: [list features]
Instruction: Generate test cases for ONLY the features above.
Constraints: Do NOT add test cases for features not listed.
```

**My observation:** *(what did the LLM invent that wasn't in the spec?)*

### Prompt: Synthetic Test Data
**Use when:** Generating safe, PII-free test data

```
Generate synthetic test data for a user registration form. 
The data must look realistic but use completely fictitious names, 
emails, and phone numbers. Do NOT use real PII patterns.
Format: 10 rows as CSV with columns: Name, Email, Phone, DOB
```

**My notes:**

---

## Chapter 4 — LLM Infrastructure

### Prompt: LLM Agent Simulation
**Technique:** Chain-of-thought / Agent-style  
**Use when:** Simulating how an LLM-powered test agent would operate

```
Role: You are an LLM-powered test agent.
Context: You have been given a new user story to process.
User Story: [paste story]

Instruction: Work through these steps:
STEP 1: Identify all testable conditions.
STEP 2: Generate test cases for each condition.
STEP 3: Flag highest priority test cases.
STEP 4: Recommend which to automate.

Constraints: Think through each step before proceeding. Show your reasoning.
Output Format: Use headers for each STEP.
```

**My notes:** *(how did the agent reasoning look? Did it plan before acting?)*

---

## Chapter 5 — Deployment & Strategy

### Prompt: Strategy Critique
**Use when:** Reviewing a GenAI testing strategy for gaps

```
Review the following GenAI testing strategy document. 
Identify any gaps based on ISTQB CT-GenAI best practices.
Pay special attention to: shadow AI risks, LLM selection criteria, 
data privacy, compliance standards, and adoption phase.
Suggest specific improvements for each gap found.

[Paste your strategy here]
```

**My strategy doc:** *(paste your completed strategy here or link to it)*

---

## My Key Observations (fill in as you go)

| Observation | Chapter |
|-------------|---------|
| | Ch 1 |
| | Ch 2 |
| | Ch 3 |
| | Ch 4 |
| | Ch 5 |

---

*Last updated: [add date]*  
*Exam date target: [add your target date]*

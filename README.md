# GSAT Article Grader Prompts

AI-powered evaluation prompts that simulate **official Taiwan GSAT Writing graders** — one for English Writing, one for Mandarin Writing. Each prompt evaluates a student's essay according to the official scoring standards and returns detailed feedback, error corrections, and a full-marks revised version.

---

## 📌 Overview

This repository contains two grading prompts:

| File | Subject | Max Score |
|---|---|---:|
| `GSAT English Article Grader Prompt.md` | English Writing | 20 |
| `GSAT Mandarin Article Grader Prompt.md` | Mandarin Writing | 25 |

Both prompts turn the AI into an official GSAT examiner that:

- Scores the essay category-by-category with justification
- Produces a complete error-correction table
- Rewrites the essay as a full-marks model version
- Gives concrete suggestions for improving future writing

---

# 🤖 Recommended AI Models

These prompts work with most modern chat-based AI models, but grading quality depends heavily on the model's reasoning ability, context length, and (for the Mandarin grader) fluency in written Mandarin. 

The table below lists the top-performing models across three major US AI corporations (**Anthropic, PBC**, **OpenAI, Inc.**, and **Google LLC**), alongside standout global reasoning engines from **DeepSeek Inc.** and **Alibaba Group**.

| Provider / Company | Model | Tier | Best Suited For & Why |
|---|---|---|---|
| **Anthropic, PBC** | **Claude Sonnet 5** | Mid-Tier (Speed & Balance) | **Everyday grading & routine feedback.** Extremely strong balance of instruction-following, formatting stability, and natural, fluid prose. |
| **Anthropic, PBC** | **Claude Opus 4.8** | Frontier (High Reasoning) | **The gold standard for Mandarin (Type A & B) essays.** Outstanding, natural mastery of Traditional Mandarin literary devices, idioms, and deep critical reasoning. |
| **OpenAI, Inc.** | **GPT-5.5** | Mid-Tier (Speed & Balance) | **Fast, highly descriptive English grading.** The primary modern workhorse for structured feedback, generating pristine Markdown tables and precise grammar corrections. |
| **OpenAI, Inc.** | **OpenAI o3-mini** | Frontier (Fast Reasoning) | **Rapid analytical evaluation.** Ideal for scanning English grammatical structures in real time, pinpointing subtle run-on sentences and punctuation slips. |
| **OpenAI, Inc.** | **GPT-5.5 Pro / Extended** | Frontier (High Reasoning) | **Deep diagnostic evaluation.** Excels at dissecting highly complex arguments, checking student premises in analytical essays before issuing a final score. |
| **Google LLC** | **Gemini 3.5 Flash** | Lightweight (High Speed) | **Near-instant, classroom-paced feedback.** Perfect for rapid, high-speed, and cost-effective checking of simpler English writing assignments. |
| **Google LLC** | **Gemini 3.1 Pro** | Mid-Tier (Speed & Balance) | **Large batch grading or extensive reference materials.** Outstanding for Mandarin Type B essays accompanied by multiple long source articles, thanks to its exceptional context handling. |
| **Google LLC** | **Gemini 3.5 Pro** *(Preview)* | Frontier (High Reasoning) | **Advanced dual-language grading.** Brings specialized "Deep Think" reasoning to the table, analyzing complex structural decisions in both English and Mandarin. |
| **DeepSeek Inc.** | **DeepSeek-R1** | Frontier (High Reasoning) | **Rigorous, systematic rubric evaluation.** Uses its internal reasoning traces to methodically break down each grading category step-by-step before printing a final score. |
| **DeepSeek Inc.** | **DeepSeek-V3** | Mid-Tier (Speed & Balance) | **Cost-effective bulk grading.** Highly capable at parsing complex, multi-tiered instructions and generating robust error-correction tables. |
| **Alibaba Group** | **Qwen3.7 Max** | Frontier (High Reasoning) | **Excellent native-level Traditional Mandarin syntax.** Optimized for localized Taiwanese phrasing, idiom structures, and the unique stylistic demands of Mandarin writing (國寫). |

### 💡 Quick Tips for Choosing Your Model
- **For the English Grader:** Standard mid-tier models like **Claude Sonnet 5** or **GPT-5.5** provide incredibly natural, encouraging, and accurate linguistic feedback.
- **For the Mandarin Grader:** Always prioritize high-reasoning engines with strong Traditional Mandarin fluency such as **Claude Opus 4.8**, **DeepSeek-R1**, or **Qwen3.7 Max**. They are far better at judging the subtle emotional depth of Reflective Essays and the logical rigor of Analytical Essays.
- **For Batch Grading:** If you are feeding multiple essays at once or uploading long reading passages alongside student work, use **Gemini 3.1 Pro** to ensure you do not hit memory or token limits.

---

# 🚀 How to Use

## Step 1 — Copy the Prompt

Copy the complete grader prompt for the subject you need:
- `GSAT English Article Grader Prompt.md` for English essays
- `GSAT Mandarin Article Grader Prompt.md` for Mandarin essays

## Step 2 — Provide the Essay

Paste the student's essay after the prompt.

Example:
```
[Prompt]
[Student Essay]
```

For the Mandarin grader, also indicate (or let the AI determine) whether the essay is:
- **Type A: Reflective Essay (情意題)**
- **Type B: Analytical Essay (知性題)**

## Step 3 — Receive Evaluation

The AI will return:

- Score report
- Detailed feedback
- Error correction table
- Revised full-marks essay
- Improvement advice

---

# 🤖 Recommended AI Models

These prompts work with any capable chatbot, but grading quality (especially for the Mandarin Writing prompt, which requires strong Traditional Mandarin and idiom comprehension) varies by model. Recommended options:

| Model | Provider | Notes |
|---|---|---|
| **Claude (Sonnet / Opus)** | Anthropic | Strong instruction-following for long rubrics; reliably produces well-structured tables; good bilingual (English/Mandarin) performance |
| **ChatGPT (GPT-5 / GPT-4o class)** | OpenAI | Widely available, strong general writing feedback; good for English essays |
| **Gemini (2.5 Pro / Flash)** | Google | Good Traditional Mandarin support; useful if you're already in the Google ecosystem (Docs/Drive integration) |
| **DeepSeek** | DeepSeek | Strong Mandarin-language reasoning at low cost; a solid alternative for the Mandarin grader |
| **Qwen** | Alibaba | Another strong option for Traditional/Simplified Mandarin grading tasks |

### Tips for choosing a model
- **For the English grader:** most mainstream models (Claude, ChatGPT, Gemini) perform well; pick whichever you already have access to.
- **For the Mandarin grader:** prefer a model with strong Traditional Mandarin fluency and idiom recognition — Claude, Gemini, DeepSeek, and Qwen tend to handle this better than English-centric models.
- **For long essays or batch grading:** use a model/plan with a larger context window (e.g. Claude, Gemini 1.5/2.5 Pro, GPT-4o/5) to avoid truncation.
- Always double-check scores against a human teacher's judgment — no model is a substitute for official GSAT grading.

---

# 📊 Scoring Systems

## English Writing (20 points)

| Category | Maximum Score |
|---|---:|
| Content | 5 |
| Organization | 5 |
| Grammar & Sentence Structure | 5 |
| Vocabulary & Spelling | 5 |
| **Total** | **20** |

## Mandarin Writing (25 points)

| Category | Maximum Score |
|---|---:|
| Content and Development | 10 |
| Use and Understanding of Source Materials | 5 |
| Organization and Structure | 5 |
| Language Expression | 5 |
| **Total** | **25** |

---

# 📝 English Writing — Evaluation Criteria

## 1. Content (5 points)
Evaluates whether the main idea is clear, whether the essay answers the prompt, and whether supporting details are relevant and well-developed.

| Score | Description |
|---|---|
| 5–4 | Clear topic with complete and detailed support |
| 3 | Topic is present but insufficiently developed |
| 2–1 | Topic unclear or details mostly irrelevant |
| 0 | Off-topic or blank |

## 2. Organization (5 points)
Evaluates introduction/body/conclusion structure, logical flow, and use of transitions.

| Score | Description |
|---|---|
| 5–4 | Clear structure and effective transitions |
| 3 | Some organization problems |
| 2–1 | Weak coherence and unclear structure |
| 0 | No meaningful organization |

## 3. Grammar & Sentence Structure (5 points)
Evaluates grammar accuracy, sentence variety, sentence construction, and punctuation.

| Score | Description |
|---|---|
| 5–4 | Few errors, varied sentence structures |
| 3 | Some errors but meaning remains clear |
| 2–1 | Frequent errors affecting readability |
| 0 | Meaning is unclear due to severe errors |

## 4. Vocabulary & Spelling (5 points)
Evaluates word choice, vocabulary range, spelling, and capitalization.

| Score | Description |
|---|---|
| 5–4 | Accurate and appropriate vocabulary |
| 3 | Simple vocabulary or occasional misuse |
| 2–1 | Frequent vocabulary/spelling problems |
| 0 | Only isolated words or copied phrases |

---

# 📝 Mandarin Writing — Evaluation Criteria

The grader first classifies the essay as **Reflective (情意題)** or **Analytical (知性題)**, since expectations differ slightly for each.

## 1. Content and Development (10 points)
Evaluates understanding of the prompt, clarity and depth of the central idea, and quality of supporting reasoning or reflection.
- **Reflective essays**: sincerity of emotion, transformation of experience into reflection, evidence of growth or self-awareness.
- **Analytical essays**: accuracy of analysis, logic of argument, independent/critical thinking.

| Grade | Description |
|---|---|
| A (Excellent) | Insightful, well-supported, deeply reflective/analytical |
| B (Good) | Clear but lacks depth or originality |
| C (Needs Improvement) | Superficial, repetitive, or off-topic; reflective essays merely narrate events, analytical essays merely restate information |

## 2. Use and Understanding of Source Materials (5 points)
Evaluates how well the essay integrates and interprets any provided reference material rather than copying it.

| Grade | Description |
|---|---|
| A | Correctly integrates all materials with original interpretation |
| B | Uses some materials correctly but connections are underdeveloped |
| C | Misinterprets, copies, or mechanically inserts materials |

## 3. Organization and Structure (5 points)
Evaluates introduction/body/conclusion structure, paragraph logic, and transitions.

| Grade | Description |
|---|---|
| A | Clear structure, coherent progression, effective transitions |
| B | Understandable structure with minor issues |
| C | Unclear or disorganized, poor readability |

## 4. Language Expression (5 points)
Evaluates vocabulary precision, sentence fluency and variety, rhetorical technique, and punctuation.

| Grade | Description |
|---|---|
| A | Precise, fluent, strong command of written Mandarin |
| B | Generally clear with minor wording/punctuation issues |
| C | Frequent problems that impede clarity |

---

# 📄 Output Structure

Both graders produce the same five sections, adapted to their scoring scale.

## A. Score Summary
A table with Category, Score Awarded, Maximum Score, and Justification (the Mandarin grader also includes a Grade A/B/C column).

## B. Detailed Feedback
Explains why each score was assigned, the essay's strengths, and areas needing improvement. The Mandarin grader also compares the essay against a high-scoring reference response.

## C. Error Correction Table
Every language error is identified.

**English format:**

| Original | Corrected | Error Type | Explanation |
|-|-|-|-|
| He go to school | He goes to school | Grammar | Third-person singular requires -s |

**Mandarin format:**

| Original Sentence | Incorrect Word or Phrase | Corrected Version | Error Type | Explanation |
|-|-|-|-|-|

Checks include grammar/word usage, sentence structure, vocabulary/character errors, misused idioms, punctuation, and (for Mandarin) logical inconsistencies and misuse of source materials.

## D. Revised Essay (Full-Marks Version)
The AI rewrites the essay while:
- Preserving the student's original ideas and perspective
- Improving organization, vocabulary, and grammar/fluency
- Producing a response that would plausibly earn full marks (20/20 or 25/25)

## E. Improvement Suggestions
Three specific, practical strategies for improving future GSAT writing performance.

---

# 🎯 Recommended Use Cases

## Students
- Practicing GSAT English or Mandarin writing
- Understanding official scoring standards
- Identifying repeated mistakes
- Improving essay structure and depth of reflection/analysis

## Teachers
- Providing consistent, rubric-aligned feedback
- Creating writing exercises and model answers
- Demonstrating high-scoring examples in both languages

## Writing Programs
Can be integrated into:
- AI writing assistants
- School learning platforms
- Essay feedback systems

---

# ⚠️ Limitations

These AI graders are designed to simulate GSAT evaluation but do not replace official scoring.

Scores may differ from actual GSAT graders because:
- Human graders may interpret ideas differently
- Creativity and style can influence judgment
- Real exam scoring involves professional moderation

Use the feedback as a learning tool rather than an official result.

---

# 📌 Prompt Design Principles

Both prompts follow these principles:

✅ Evaluate before correcting
✅ Follow official GSAT scoring standards
✅ Provide transparent deductions
✅ Identify every language error
✅ Preserve original student ideas
✅ Encourage improvement rather than only grading

---

# 📜 License

This project is released for educational purposes.

You may modify and use these prompts for:
- Personal learning
- Classroom teaching
- Educational software development

Please retain attribution when redistributing.

---

# ⭐ Contributing

Suggestions and improvements are welcome, including:
- Better GSAT scoring calibration (English or Mandarin)
- More example essays for either subject
- Teacher feedback
- Prompt optimization

Feel free to open an issue or submit a pull request.

---

Good luck!

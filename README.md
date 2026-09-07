# Daily Exercises

This repository contains the **daily exercises and assignments** for learning how to design and develop **LaTeX templates for Graduation Theses and Academic Presentations**.

The exercises are designed to help you gradually develop your understanding of **LaTeX, document structure, modular document design, formatting, template development, and collaborative Git-based workflows**.

The ultimate goal is to apply these concepts to the development of reusable and maintainable templates for:

* **Graduation Thesis**
* **Academic Presentation**

## Language & AI Usage
### Language Requirement

**All answers must be written in English.**

You are expected to develop your ability to understand and communicate technical concepts in English. Do not submit answers in Vietnamese.

### AI Usage

You may use AI tools to help you answer the exercises. However, you are responsible for understanding everything you submit.

If you use AI to write or improve your answer, make sure you understand what the answer means, why it is written that way, and how it relates to the question.

You may be asked to explain or answer questions about your own submission during the review process. If you cannot explain what you submitted, the answer may be considered incomplete even if the written response appears correct.

AI should be used as a learning and writing assistant, not as a replacement for your own understanding.

### Writing Without AI

You are also encouraged to write your answers yourself without using AI.

If you understand the technical content but are unsure about English grammar, wording, vocabulary, or how to express an idea naturally, you may contact the instructor via Messenger for help with English expression.

For example, you can ask for help with:

- Choosing the appropriate technical term
- Correcting grammar
- Improving sentence structure
- Finding a more natural English expression
- Understanding the difference between similar English words

The purpose of this support is to help you express your own understanding in English, not to replace your thinking or answer the exercise for you.

## Daily Exercise Updates

A new exercise will be added to the repository **each day** under the corresponding `day-xx` section.

Before starting each new exercise, **remember to pull the latest changes from the `main` branch** to make sure you have the most up-to-date exercise.

For example:

```bash
git checkout hauvq
git pull origin main
```

Then complete the new exercise and submit it following the submission guidelines above.

> [!IMPORTANT]
> **Remember to pull the latest changes from `main` before starting each day's exercise.**

## Submission Guidelines

### 1. Answer the Questions

Each exercise is provided as a Markdown (`.md`) file containing the questions and answer templates.

For each question, you will find a placeholder: `<!-- Your answer here -->`

Replace **only** this placeholder with your answer.

For example:

```md
**Q1.** What is a LaTeX document class?

**A1.** <!-- Your answer here -->
```

Your submission should become:

```md
**Q1.** What is a LaTeX document class?

**A1.** A document class defines the overall structure and layout of a LaTeX document.
```

### 2. Do Not Modify the Questions

**Do not modify, remove, reorder, or rewrite the questions.**

You should only replace: `<!-- Your answer here -->` with your answer.

The questions are tracked through GitHub, so changes to the original questions can be identified.

### 3. Submit on Your Branch

**Do not push your assignment directly to `main`.**

Submit your assignment through your assigned branch: `hauvq`.

Your work should follow this workflow:

```text
main
  │
  └── hauvq
       │
       └── Your assignment
```

Push your changes to `hauvq` and submit them for review through GitHub.

### 4. Commit Message

Use the following **Conventional Commit** format when submitting an assignment:

```text
feat(day-0x): submit assignment
```

For example:

```bash
git add .
git commit -m "feat(day-01): submit assignment"
git push origin hauvq
```

For Day 02:

```bash
git commit -m "feat(day-02): submit assignment"
```

For Day 03:

```bash
git commit -m "feat(day-03): submit assignment"
```

Replace `0x` with the appropriate day number.

## Assignment Review

Your submission will be reviewed on GitHub.

If your assignment does not meet the requirements, you will receive a **Request Changes** review.

You should then:

1. Read the review comments.
2. Correct your assignment.
3. Commit the changes to the **same branch**.
4. Push the changes to GitHub.
5. Wait for another review.

This process will continue until your assignment satisfies the requirements.

```text
Submit
  ↓
Review
  ↓
┌──────────────────────┐
│ Meets requirements?  │
└──────────────────────┘
       ↓          ↓
      Yes         No
       ↓          ↓
   Approved    Request Changes
                    ↓
                 Fix & Push
                    ↓
                  Review
```

## Important Rules

> [!IMPORTANT]
> **Do not push directly to `main`.**

> [!IMPORTANT]
> **Do not modify the questions.** Only replace the `<!-- Your answer here -->` placeholders with your answers.

> [!IMPORTANT]
> **Use the required commit message format:**
>
> ```text
> feat(day-0x): submit assignment
> ```

### Quick Checklist

Before submitting, make sure that:

* [ ] I answered all required questions.
* [ ] I only replaced `<!-- Your answer here -->`.
* [ ] I did not modify the original questions.
* [ ] I did not push directly to `main`.
* [ ] I submitted my work on the `hauvq` branch.
* [ ] I used the correct Conventional Commit message.
* [ ] My Markdown file is properly formatted.
* [ ] I reviewed my answers before submitting.

## Repository Workflow

```text
Clone Repository
       ↓
Read the Daily Exercise
       ↓
Research / Learn
       ↓
Answer the Questions
       ↓
Replace <!-- Your answer here -->
       ↓
Check Your Markdown
       ↓
Commit
       ↓
Push to hauvq
       ↓
GitHub Review
       ↓
┌───────────────────┐
│ Request Changes?  │
└───────────────────┘
       ↓
      Yes
       ↓
Fix & Push Again
       ↓
     Review
       ↓
    Approved
```

## Learning Objective

The exercises are not only intended to test your understanding of LaTeX syntax. They are designed to help you develop the knowledge and design principles required to build **clean, modular, reusable, maintainable, and collaborative LaTeX templates** for academic documents.

By the end of the exercises, you should be able to apply these principles to your own:

* **Graduation Thesis template**
* **Academic Presentation template**
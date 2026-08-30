# Assignment – Prompting Patterns

---

# Q1. Conceptual Understanding

## Explain the difference between Zero-shot, Few-shot, and Chain-of-Thought prompting in your own words. Provide one professional use case for each pattern.

## Zero-shot Prompting

### Definition

Zero-shot prompting means giving the AI a task **without providing any examples**. The AI relies on its pre-trained knowledge to understand and complete the task.

### Characteristics

- No examples are provided.
- Best for simple and straightforward tasks.
- Fast and easy to write.
- Suitable when the required output format is clear.

### Professional Use Case

A customer support executive wants to translate a product description into another language.

**Example Prompt**

```text
Translate the following product description into French.

"Our smartwatch offers 7-day battery life and heart rate monitoring."
```

---

## Few-shot Prompting

### Definition

Few-shot prompting provides the AI with **a few examples** before asking it to perform the task. The examples help the AI understand the expected format, tone, or pattern.

### Characteristics

- Includes example input-output pairs.
- Produces more consistent results.
- Useful when a specific output format is required.

### Professional Use Case

An e-commerce company wants AI to classify customer reviews consistently.

**Example Prompt**

```text
Review: Excellent product and fast delivery.
Sentiment: Positive

Review: Very poor quality.
Sentiment: Negative

Review: Packaging was okay.
Sentiment:
```

---

## Chain-of-Thought (CoT) Prompting

### Definition

Chain-of-Thought prompting asks the AI to **reason through a problem step by step** before giving the final answer.

### Characteristics

- Encourages logical reasoning.
- Improves accuracy.
- Best for complex or multi-step problems.
- Makes the reasoning process easier to verify.

### Professional Use Case

A financial analyst asks AI to calculate investment returns while explaining each calculation step.

**Example Prompt**

```text
Calculate the total profit from an investment.

Think step by step and explain each calculation before giving the final answer.
```

---

# Summary

| Pattern          | Description            | Best Use Case                                  |
| ---------------- | ---------------------- | ---------------------------------------------- |
| Zero-shot        | No examples            | Translation, summarization, simple Q&A         |
| Few-shot         | Uses examples          | Classification, formatting, sentiment analysis |
| Chain-of-Thought | Step-by-step reasoning | Math, logic, planning, debugging               |

---

# Q2. Pattern Identification

Identify the prompting pattern used in each example.

---

### a)

```text
Translate the word "apple" into Spanish.
```

### Answer

**Pattern:** Zero-shot Prompting

**Reason:**

The AI is given a direct instruction without any examples.

---

### b)

```text
Review: Excellent quality → Positive

Review: Bad service → Negative

Review: Average taste → ?
```

### Answer

**Pattern:** Few-shot Prompting

**Reason:**

The AI learns from the provided examples before classifying the final review.

---

### c)

```text
If a train travels 60 km in 1 hour,

how long will it take to travel 180 km?

Think step by step.
```

### Answer

**Pattern:** Chain-of-Thought Prompting

**Reason:**

The phrase **"Think step by step"** instructs the AI to reason before answering.

---

# Q3. Prompt Rewriting

## Task

Classify emails into:

- Work
- Personal
- Spam

---

## Zero-shot Prompt

```text
Classify the following email into one of these categories:

- Work
- Personal
- Spam

Email:

"Congratulations! You have won a free vacation. Click here to claim your prize."

Return only the category.
```

---

## Few-shot Prompt

```text
Classify emails into:

- Work
- Personal
- Spam

Example 1

Email:

"Please attend tomorrow's project meeting at 10 AM."

Category:

Work

--------------------

Example 2

Email:

"Happy Birthday! Looking forward to celebrating with you."

Category:

Personal

--------------------

Example 3

Email:

"You have won ₹10,00,000! Click the link below immediately."

Category:

Spam

--------------------

Now classify:

Email:

"Our quarterly sales report is ready for review."

Category:
```

---

# Q4. Chain-of-Thought Application

## Problem

A shopkeeper buys 50 pens.

Each pen costs ₹12.

He sells each pen for ₹15.

Find the total profit.

---

## Prompt

```text
Solve the following problem step by step.

First calculate the total buying cost.

Then calculate the total selling price.

Finally calculate the profit.

Explain every step before giving the final answer.

Problem:

A shopkeeper buys 50 pens.

Each pen costs ₹12.

He sells each pen for ₹15.

What is the total profit?
```

---

## Expected Step-by-Step Reasoning

### Step 1

Buying Cost

```text
50 × 12 = ₹600
```

---

### Step 2

Selling Price

```text
50 × 15 = ₹750
```

---

### Step 3

Profit

```text
₹750 − ₹600 = ₹150
```

---

### Final Answer

```text
Total Profit = ₹150
```

---

# Q5. Case Study – Choosing the Right Pattern

## Task 1

Generate a quick translation of a marketing slogan into French.

### Best Pattern

**Zero-shot Prompting**

### Justification

Translation is a straightforward task that does not require examples or reasoning. Modern AI models are already trained on multiple languages and can perform translations accurately with a simple instruction.

---

## Task 2

Categorize 100 product reviews as:

- Positive
- Negative
- Neutral

### Best Pattern

**Few-shot Prompting**

### Justification

Providing a few labeled examples helps the AI understand the expected classification style and ensures consistent labeling across a large number of reviews.

---

## Task 3

Solve a multi-step logic problem about customer segmentation.

### Best Pattern

**Chain-of-Thought Prompting**

### Justification

Customer segmentation often involves multiple conditions, calculations, and reasoning steps. Chain-of-Thought prompting encourages the AI to analyze each condition systematically before arriving at the final answer, improving both accuracy and transparency.

---

# Final Summary

| Task                                        | Recommended Pattern | Reason                                                  |
| ------------------------------------------- | ------------------- | ------------------------------------------------------- |
| Translate a marketing slogan                | Zero-shot           | Simple, direct task requiring no examples               |
| Categorize 100 product reviews              | Few-shot            | Examples improve consistency and accuracy               |
| Solve a customer segmentation logic problem | Chain-of-Thought    | Requires structured reasoning and step-by-step analysis |

---

# Key Takeaways

- **Zero-shot Prompting** is ideal for simple tasks where the AI already has sufficient knowledge.
- **Few-shot Prompting** improves consistency by teaching the AI through examples before asking it to perform the task.
- **Chain-of-Thought Prompting** is best for complex problems that require logical reasoning, calculations, or multiple decision-making steps.
- Choosing the appropriate prompting pattern based on the task leads to more accurate, reliable, and efficient AI responses.

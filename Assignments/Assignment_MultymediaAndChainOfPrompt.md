# Assignment – Multimodal Prompting & Prompt Chaining

---

# Q1. Conceptual Understanding

## a) What is Multimodal Prompting?

**Answer:**

Multimodal prompting is a technique where AI is provided with **multiple types of input**, such as text, images, audio, video, PDFs, or charts, to better understand the context and generate more accurate responses. Instead of relying only on text, the AI combines information from different sources to produce a richer and more relevant output.

### Example

**Input:**

- **Text:** "Analyze this sales dashboard and summarize the key findings."
- **Image:** Sales dashboard screenshot.

**Output:**

- Sales increased by 15% in Q2.
- Customer retention improved by 8%.
- Revenue declined slightly in Q4 due to seasonal demand.

### Professional Use Case

**Business Intelligence**

A financial analyst uploads a dashboard containing charts and asks AI to identify revenue trends, risks, and business opportunities for an executive meeting.

---

## b) What is Prompt Chaining?

**Answer:**

Prompt chaining is the process of breaking a complex task into multiple smaller prompts, where the output of one prompt becomes the input for the next. This structured workflow improves accuracy, logical reasoning, and overall output quality.

### Example

**Task:** Create a business report.

**Step 1**

Summarize the report.

↓

**Step 2**

Identify business challenges.

↓

**Step 3**

Recommend solutions.

↓

**Final Output**

A complete business report with actionable recommendations.

### Professional Use Case

**Consulting**

A management consultant first summarizes client survey data, then extracts key business insights, and finally generates strategic recommendations for executives.

---

# Q2. Multimodal Prompt Design

### Scenario

You have:

- 📈 A line chart showing quarterly sales data for 2023.
- 📝 A text instruction.

### Multimodal Prompt

> **Act as a Business Analyst. Analyze the uploaded quarterly sales line chart for 2023.**
>
> Your tasks are:
>
> 1. Identify the overall sales trend across all four quarters.
> 2. Highlight one potential business risk based on the observed trend.
> 3. Recommend one practical growth strategy to improve future sales.
>
> Present your response using the following format:
>
> - **Sales Trend**
> - **Business Risk**
> - **Growth Strategy**
>
> Keep the explanation concise and suitable for an executive audience.

### Why This is Multimodal

- **Image Input:** Quarterly sales chart.
- **Text Input:** Analysis instructions.
- **AI combines both inputs** to produce an informed response.

---

# Q3. Chaining Workflow Exercise

## Goal

Generate a client-ready report from raw survey data.

### Step 1 – Survey Summary

**Prompt**

> Analyze the provided survey responses and summarize the overall findings in no more than 250 words. Highlight major customer opinions, satisfaction levels, and recurring feedback.

↓

### Step 2 – Business Insights

**Prompt**

> Using the survey summary, identify the top three customer insights and explain how each insight impacts the business.

↓

### Step 3 – Recommendations

**Prompt**

> Based on the identified customer insights, recommend three actionable business strategies. Include expected benefits and implementation priorities.

↓

### Final Output

A client-ready report containing:

1. Executive Summary
2. Customer Insights
3. Business Recommendations

### Why Prompt Chaining?

Each prompt builds upon the previous response, making the workflow more structured, accurate, and easier to validate.

---

# Q4. Combining Multimodal + Chaining

## Scenario

You have:

- 🖼️ Product advertisement image.
- 📊 Spreadsheet containing campaign performance metrics.

### Step 1 – Multimodal Analysis

**Prompt**

> Analyze the uploaded product advertisement image together with the campaign performance spreadsheet. Identify the key marketing message, evaluate campaign performance, and summarize three important observations.

↓

### Step 2 – Executive Insights

**Prompt**

> Based on the marketing analysis, identify the strongest campaign success, one weakness, and one opportunity for improvement. Keep the explanation suitable for senior executives.

↓

### Step 3 – Presentation Draft

**Prompt**

> Convert the executive insights into three concise PowerPoint bullet points suitable for a board meeting presentation.

### Example Output

- Campaign achieved a 20% increase in customer engagement.
- Conversion rates dropped among first-time users, indicating optimization opportunities.
- Increase investment in high-performing digital advertising channels.

### Why Use Both?

- **Multimodal Prompting** combines the image and spreadsheet for richer context.
- **Prompt Chaining** transforms the analysis into executive-ready presentation content through sequential steps.

---

# Q5. Strategy Selection – Applied Scenario

| Scenario                                                                | Strategy       | Justification                                                                                                                                                              |
| ----------------------------------------------------------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **a) Explaining a complex biology diagram to high school students.**    | **Multimodal** | The AI must interpret a visual biology diagram and combine it with text instructions to explain the concepts in simple language.                                           |
| **b) Generating a financial dashboard summary with visualized trends.** | **Both**       | Multimodal prompting is needed to analyze charts and dashboards, while prompt chaining helps convert the analysis into structured executive summaries and recommendations. |
| **c) Drafting a legal case brief from multiple long documents.**        | **Chaining**   | Since the task involves processing large text documents, breaking the work into stages (summarization → issue identification → case brief) improves clarity and accuracy.  |
| **d) Creating social media captions for a set of product images.**      | **Multimodal** | AI must understand the visual content of the product images and generate engaging captions tailored to the marketing objective.                                            |

---

# Summary

### ✅ Multimodal Prompting

- Combines different input types such as text, images, audio, PDFs, and charts.
- Helps AI understand richer context.
- Best suited for visual analysis, image understanding, dashboards, diagrams, and multimedia tasks.

### ✅ Prompt Chaining

- Breaks complex tasks into smaller, sequential prompts.
- Improves reasoning, organization, and output quality.
- Best suited for reports, research, document summarization, software development, and decision-making workflows.

### ✅ Combining Both

Using **Multimodal Prompting** and **Prompt Chaining** together enables AI to process diverse inputs and produce structured, high-quality outputs. This combination is especially valuable in business intelligence, healthcare, education, marketing, consulting, and enterprise AI applications, where both rich context and step-by-step reasoning are essential.

# Voice-bot
# 🏦 AI Loan Against Property (LAP) Qualification Voice Assistant

An AI-powered **Voice Assistant for preliminary Loan Against Property (LAP) qualification**. The assistant conducts a natural conversation with existing customers, verifies basic eligibility criteria, collects required information, handles customer questions, and identifies whether the customer should proceed to a senior loan expert.

> **Note:** This system performs only preliminary qualification. It does **not** make final loan approval or lending decisions.

---

## 📌 Project Overview

The **AI Loan Against Property Qualification Voice Assistant** is designed to automate the initial customer screening process for a pre-approved LAP offer of up to **₹75 Lakhs**.

Instead of requiring a customer service representative to manually ask every eligibility question, the AI assistant:

* Greets and verifies the customer
* Presents the pre-approved LAP offer
* Detects existing loans or EMI-reduction requests
* Collects property and financial information
* Validates eligibility rules in real time
* Handles out-of-order information naturally
* Responds to customer questions during the conversation
* Disqualifies ineligible applications politely
* Forwards eligible customers to a senior loan expert

---

## 🎯 Key Objective

The primary objective is to create a **conversational, rule-based preliminary qualification system** that reduces manual screening effort while providing customers with a simple and natural voice-based experience.

### Offer

**Loan Against Property (LAP)**
Maximum pre-approved offer: **₹75,00,000 (₹75 Lakhs)**

---

## 🔄 Conversation Flow

```text
Customer Call
     │
     ▼
Customer Verification
     │
     ▼
LAP Offer Presentation
     │
     ▼
Existing Loan / EMI Check
     │
     ├── Yes ──► Loan Transfer Specialist
     │
     └── No
          │
          ▼
     Property Type
          │
          ▼
     Ownership Status
          │
          ▼
     Original Documents
          │
          ▼
     Desired Loan Amount
          │
          ▼
     Occupation & Income Mode
          │
          ▼
     Property Market Value
          │
          ▼
     Repayment Tenure
          │
          ▼
   Eligibility Validation
       │          │
       ▼          ▼
  Eligible     Ineligible
       │          │
       ▼          ▼
 Senior Loan   Polite
   Expert     Rejection
```

---

## ✅ Eligibility Criteria

The assistant evaluates the following preliminary criteria.

| Parameter             | Eligibility Rule                    |
| --------------------- | ----------------------------------- |
| Property Type         | Residential, Commercial, Industrial |
| Agricultural Property | ❌ Not eligible                      |
| Ownership             | Sole or Joint                       |
| Original Documents    | Must be available                   |
| Maximum Loan Amount   | ₹75 Lakhs                           |
| Occupation            | Salaried or Self-Employed           |
| Income Mode           | Bank Transfer / Cheque              |
| Cash Income           | ❌ Not eligible                      |
| Property Value        | Estimated market value is recorded  |
| Repayment Tenure      | 3–15 years                          |

---

## 🧠 Intelligent Conversation Handling

### 1. Out-of-Order Information

The assistant can understand multiple pieces of information provided in a single response.

**Example:**

> "I have a residential house worth ₹1 crore and it is jointly owned."

The system captures:

```text
Property Type   → Residential
Market Value   → ₹1 Crore
Ownership      → Joint
```

It does not ask the customer for the same information again.

---

### 2. Existing Loan Detection

If the customer mentions an existing loan on the property or wants to reduce an existing EMI, the assistant immediately routes the request to the appropriate specialist.

```text
Customer
   ↓
Existing Loan Detected
   ↓
Loan Transfer Specialist
```

The assistant does not continue the normal eligibility questionnaire.

---

### 3. Automatic Disqualification

The assistant immediately stops the qualification process when a mandatory eligibility rule is violated.

Examples include:

* Agricultural property
* Original documents unavailable
* Cash-based income
* Repayment tenure below 3 years
* Repayment tenure above 15 years

This prevents unnecessary questions after an application has already become ineligible.

---

### 4. Loan Amount Handling

If a customer requests an amount above ₹75 Lakhs, the assistant explains the offer limit and asks whether they would like to proceed with the maximum available amount.

```text
Requested Amount > ₹75 Lakhs
          ↓
Explain Maximum Limit
          ↓
Customer Decision
       ↙       ↘
     Yes        No
      ↓          ↓
₹75 Lakhs    End Call
```

---

## 🗂️ Information Collected

During the conversation, the assistant maintains an internal state for:

```text
Verification Status
Property Type
Ownership
Document Availability
Desired Loan Amount
Occupation
Income Mode
Property Market Value
Repayment Tenure
```

The assistant uses this state to determine the **next missing question** instead of repeating questions already answered.

---

## 🎙️ Voice Assistant Behavior

The assistant is designed to communicate in a:

* Natural manner
* Professional tone
* Clear and concise style
* Customer-friendly manner
* Advisory tone
* Empathetic manner

The assistant generally keeps responses to **1–3 conversational sentences** before asking the next required question.

---

## 🛡️ Important Business Rules

### Maximum Loan Amount

```text
Maximum = ₹75,00,000
```

Requests above this amount are handled according to the offer rules.

### Property Types

```text
Residential  → ✅
Commercial   → ✅
Industrial   → ✅
Agricultural → ❌
```

### Income Mode

```text
Bank / Cheque → ✅
Cash          → ❌
```

### Tenure

```text
3 years ≤ Tenure ≤ 15 years
```

---

## 🔀 Exception Handling

The assistant supports several conversational edge cases.

### Customer is Busy

The assistant:

1. Asks for a preferred callback date/time
2. Records the callback information
3. Thanks the customer
4. Ends the call

### Customer Asks a Question

The assistant answers briefly using the available product information and then returns to the qualification process.

### Customer Provides Multiple Answers

All available eligibility information is extracted and stored before determining the next question.

### Customer Gives an Invalid Answer

The assistant explains the specific eligibility issue and terminates the qualification process politely.

---

## 🏁 Final Qualification

Only after **all required eligibility criteria have been collected and validated** does the assistant proceed with the senior-expert handoff.

Example outcome:

> The customer meets all preliminary eligibility criteria and their profile can be forwarded to a Senior Loan Expert for further processing.

The senior expert handles final details such as:

* Interest rates
* Customized terms
* Final loan assessment
* Processing requirements
* Final approval

---

## 🔐 Important Disclaimer

This AI assistant is a **preliminary qualification system** and should not be considered a final lending decision engine.

It does not independently approve or reject loans based on creditworthiness. Its purpose is to collect preliminary information and apply predefined qualification rules before forwarding eligible profiles to a human loan expert.

---

## 💡 Key Features

* 🎙️ Voice-based customer interaction
* 🤖 AI-powered conversational qualification
* 🏠 Loan Against Property screening
* 🔄 Existing loan / EMI detection
* 🧠 Context-aware conversation
* 📋 Sequential eligibility checking
* 🔀 Out-of-order information extraction
* ⚡ Real-time rule validation
* ❌ Immediate disqualification handling
* 👨‍💼 Senior expert handoff
* 💬 Natural customer interaction
* 🔐 Preliminary qualification only

---

## 🛠️ Technology

The implementation can be integrated with:

* **AI / LLM** – Natural language understanding and reasoning
* **Voice AI** – Speech-to-text and text-to-speech
* **Prompt Engineering** – Conversation and business-rule control
* **RAG** – Product-specific information retrieval
* **API Integration** – Customer and loan-related services
* **Workflow Automation** – Qualification and handoff workflows

> Update this section with the exact technologies used in your implementation.

---

## 📁 Suggested Project Structure

```text
loan-qualification-voice-assistant/
│
├── README.md
├── prompts/
│   └── loan_qualification_prompt.txt
│
├── workflows/
│   └── qualification_workflow.json
│
├── docs/
│   └── conversation-flow.md
│
├── assets/
│   └── architecture.png
│
└── .gitignore
```

---

## 🚀 Future Enhancements

* Integration with CRM systems
* Automated callback scheduling
* Customer profile lookup
* Multilingual voice support
* Real-time CRM updates
* Call analytics and reporting
* Conversation history
* Advanced fraud and document checks
* Human-agent dashboard
* Automated lead scoring

---

## 👩‍💻 Project Highlights

This project demonstrates practical implementation of:

**AI + Voice Automation + Prompt Engineering + RAG + Business Rule Validation + Conversational AI**

It focuses on transforming a traditional manual customer qualification process into an automated conversational workflow while keeping the final lending decision with a human expert.

---

## 📄 License

This project is intended for educational, demonstration, and prototype purposes.

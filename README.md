# PhishCheck

*A senior-friendly phishing awareness tool*

## Overview

**PhishCheck** is a web-based tool that helps users identify potential phishing emails by highlighting common warning signs and explaining *why* those elements may be risky. The goal is not to declare emails “safe” or “unsafe,” but to support safer decision-making—especially for users who may hesitate to ask for help or fear being a burden.

This project was designed as part of an **AI UX portfolio** with a strong emphasis on ethical safeguards, explainability, and user trust calibration.

---

## Problem Statement

Phishing remains one of the most common causes of fraud and account compromise. While many users—particularly seniors—would benefit from a second pair of eyes, they may avoid asking for help due to:

* fear of being a burden,
* a desire to remain self-reliant,
* or lack of immediate access to a trusted person.

At the same time, overly confident or opaque AI tools can unintentionally increase harm by encouraging users to defer judgment entirely.

---

## Design Goals

* **Explainability over authority**
  Users should understand *why* something is flagged.
* **Assist, don’t decide**
  The tool supports judgment without claiming certainty.
* **Calm, non-alarmist language**
  Reduce panic; encourage verification.
* **Consistent safety nudges**
  Reinforce best practices regardless of outcome.

---

## Target Users

* **Primary:** Older adults (65+) who use email regularly but lack confidence in identifying scams.
* **Secondary:** Any non-technical or moderately technical user who wants a second pair of eyes on a suspicious email.

While the UI and language are optimized for seniors, the tool is intentionally accessible to a broader audience.

---

## How It Works (v1)

1. User pastes the body of an email into the tool.
2. The server analyzes the text using a **rule-based detection system**.
3. Potential red flags are:

   * highlighted directly in the email text,
   * labeled in plain language,
   * expandable with short explanations and recommended next steps.
4. The tool returns one of three qualitative outcomes:

   * **No obvious red flags found**
   * **Be cautious — verify before acting**
   * **Something looks phishy — do not click or reply**

> At no point does the tool claim an email is “safe.”

---

## Why Rule-Based (Not AI-First)

For the initial version, the tool intentionally avoids a black-box AI classifier.

**Reasons:**

* Rule-based systems are more transparent and teach pattern recognition.
* They reduce the risk of false confidence.
* They allow users to learn *how* scams work, not just receive a verdict.

AI is considered a future enhancement for:

* improving explanation clarity,
* accessibility support,
* and user-initiated clarification—not automated decision-making.

---

## Ethical Safeguards

* No percentage-based “risk scores”
* No “clean” or “safe” labels
* Persistent disclaimer: *“This is a helper, not a guarantee.”*
* Repeated guidance to verify requests involving:

  * money,
  * passwords or codes,
  * urgent action,
  * remote access.
* Email content is processed in memory and not stored by default.

---

## Tech Stack

* **Frontend:** HTML, CSS, JavaScript
* **Backend:** Node.js + Express
* **Architecture:**
  Client submits email text → server analyzes → structured results returned
* **Deployment:** Designed for lightweight hosting and iterative expansion

---

## Status & Next Steps

This project is under active development and testing.

Planned improvements:

* Optional email header analysis (v2)
* AI-assisted explanation rewriting (non-authoritative)
* Structured usability testing with older adults
* Accessibility enhancements (font scaling, screen readers)

---

## Disclaimer

This tool does not guarantee that an email is safe or unsafe. Scammers frequently change tactics. If an email requests money, passwords, codes, or urgent action, users are encouraged to verify through a trusted source or contact an IT professional or trusted individual.

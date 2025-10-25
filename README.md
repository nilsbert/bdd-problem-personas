# 🧩 BDD Problem Personas

<img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Problems%20Personas%20-%20Title.png?raw=true" width="600"/>

Repository for **BDD Problem Personas** — a toolkit for integrating personas into Behavior-Driven Development (BDD) to uncover error paths, negative scenarios, and edge cases.  
This repo includes **cards**, **manuals**, **examples**, **images**, and **translations**, all organized for clarity and collaboration.  

⚠️ **Note:** The project is under **active development** — the card design and layout may still change.  

---

## 🎯 What Is This?

**Problem Personas** are character cards that help agile teams think beyond the *happy path*.  
Each persona represents a behavior pattern or weakness that could cause errors, expose system flaws, or reveal hidden requirements.  

By role-playing these personas in backlog refinement, BDD workshops, or exploratory testing, teams discover risks earlier and strengthen product quality.

👉 Try the **[Problem Persona BDD Copilot](https://chatgpt.com/g/g-68d1bc47e300819196a0b009c97ef095-problem-persona-bdd-copilot)** – a Custom GPT that automatically generates persona-driven BDD scenarios.

Explore all cards here → **[Cards Folder on GitHub](https://github.com/nilsbert/bdd-problem-personas/tree/main/Cards)**

---

## 🃏 Example Cards  

| | |
|:--:|:--:|
| <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/01%20-%20Thorsten%20Tester.png?raw=true" width="200"/> | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/02%20-%20Compliance%20Clara.png?raw=true" width="200"/> |
| <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/03%20-%20Accessibility%20Alex.png?raw=true" width="200"/> | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/04%20-%20Always-Right%20Aya.png?raw=true" width="200"/> |
| <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/05%20-%20Consistent%20Connie.png?raw=true" width="200"/> | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/06%20-%20Poolside%20Phil.png?raw=true" width="200"/> |
| <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/07%20-%20Cleanup%20Carl.png?raw=true" width="200"/> | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/08%20-%20Nils%20Newby.png?raw=true" width="200"/> |
| <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/09%20-%20Confused%20Conrad.png?raw=true" width="200"/> | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/10%20-%20Third-Party%20Theo.png?raw=true" width="200"/> |
| <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/11%20-%20Chaos%20Claus.png?raw=true" width="200"/> | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/12%20-%20Malicious%20Max.png?raw=true" width="200"/> |

➡️ View the full collection: **[All Cards Folder](https://github.com/nilsbert/bdd-problem-personas/tree/main/Cards)**  

---

## 🚀 How to Use  

1. Pick one or more personas during backlog refinement, BDD scenario writing, or exploratory testing.  
2. Ask: *“What would this persona do with our feature?”*  
3. Write scenarios (Gherkin or user stories) to reflect their perspective.  
4. Discuss, refine, and add them to your acceptance criteria or test suite.  

**Example:**  

```gherkin
Scenario: Accessibility Alex tries to use keyboard navigation
  Given the login page is open
  When Alex navigates using only the keyboard
  Then all interactive elements are reachable
  And focus order follows logical reading order

# BDD Problem Personas

<img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Pre-Mortem%20Personas.png?raw=true" width="150"/>

Repository for **BDD Problem Personas** content — modular rules, player manual, examples, images, player aids, and translations.  
Organized for clarity and collaboration with templates, consistent style, and versioned releases.  
A single source of truth for players, playtesters, and editors.  

⚠️ **Note:** This repository is currently in **active development**.  
The **design of the cards is not final** and may change over time.  

---

## 🎯 What Is This?

Problem Personas are **character cards** you can use in Behavior-Driven Development (BDD) to discover error paths and negative scenarios.  
Instead of only testing the *happy path*, these personas encourage teams to explore real-world failure modes, risks, and edge cases.

Each card represents a persona that may cause or expose a problem in your system.  
By role-playing these personas during backlog refinement or BDD workshops, teams can uncover hidden requirements and improve quality.

👉 You can also try the **[Problem Persona BDD Copilot](https://chatgpt.com/g/g-68d1bc47e300819196a0b009c97ef095-problem-persona-bdd-copilot)** — a Custom GPT that automatically generates persona-driven BDD scenarios.

---

## 🖼️ Example Cards

| Persona | Card |
|---------|------|
| Accessibility Alex | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Accessibility%20Alex.png?raw=true" width="150"/> |
| Always-Right Aya | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Always-Right%20Aya.png?raw=true" width="150"/> |
| Chaos Claus | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Chaos%20Claus.png?raw=true" width="150"/> |
| Cleanup Carl | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Cleanup%20Carl.png?raw=true" width="150"/> |
| Compliance Clara | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Compliance%20Clara.png?raw=true" width="150"/> |
| Confused Conrad | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Confused%20Conrad.png?raw=true" width="150"/> |
| Malicious Max | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Malicious%20Max.png?raw=true" width="150"/> |
| Nils Newby | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Nils%20Newby.png?raw=true" width="150"/> |
| Poolside Phil | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Poolside%20Phil.png?raw=true" width="150"/> |
| Third-Party Theo | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Third-Party%20Theo.png?raw=true" width="150"/> |
| Thorsten Tester | <img src="https://github.com/nilsbert/bdd-problem-personas/blob/main/Cards/Thorsten%20Tester.png?raw=true" width="150"/> |


---

## 🚀 How to Use

1. Pick one or more personas during backlog refinement, BDD scenario writing, or exploratory testing.  
2. Ask: *“What would this persona do with our feature?”*  
3. Write scenarios (Gherkin or user stories) that cover those edge cases.  
4. Add them to your test suite.

Example:

```gherkin
Scenario: Accessibility Alex tries to use keyboard navigation
  Given the login page is open
  When Alex navigates using only the keyboard
  Then all interactive elements are reachable
  And focus order follows logical reading order

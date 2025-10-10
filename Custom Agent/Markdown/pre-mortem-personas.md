# Pre-Mortem Personas Knowledge Base

---

## Thorsten Tester

![Thorsten Tester](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/01-ThorstenTester-removebg-preview.png) – *The Button Smasher*  
**Quote:**  
“If there’s a button, I’ll press it.”  

**Profile:**  
- **Age:** 50  
- **Role/Background:** Senior Test Manager with a passion for exploratory testing  
- **Motivation:** Uncover flaws before customers do  
- **Behavior Style:** Systematic but chaotic, ignores “intended use”  

**Description:**  
Relentlessly tests boundaries with odd inputs, rapid clicks, and illogical workflows. Uncovers validation gaps and missing error handling.  

**Risk Tags:**  
- Validation, Reliability, Data Integrity, Robustness  

**Typical Behavior:**  
- Ignores instructions, tries odd paths  
- Repeats actions rapidly  
- Mixes valid, invalid, and extreme values  

**Detailed Problems:**  
- **Input Validation:** `0`, negatives, strings in numeric fields, extreme numbers, emojis, SQL injection  
- **Dates:** Nonexistent days (30 Feb), past/far-future dates  
- **Workflows:** Skips mandatory steps, double-submits forms, uses multiple tabs  
- **Files:** Wrong type, oversized, corrupted, renamed executables  
- **System Use:** Refreshes mid-action, logs out during save, deep-links into hidden features  

**Example Tests:**  
- Given 30 Feb is selected → Then system blocks submission with clear error.  
- Given Thorsten double-clicks “Buy” → Then only one order is created.  

---

## Compliance Clara

![Compliance Clara](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/02-ComplianceClara-removebg-preview.png) – *The Guardian*  
**Quote:**  
“Shine safely, or don’t shine at all.”  

**Profile:**  
- **Age:** 42  
- **Role/Background:** Compliance officer, QA consultant  
- **Motivation:** Protect against legal/regulatory risks  
- **Behavior Style:** Cautious, documentation-driven  

**Description:**  
Ensures GDPR, auditability, and standards are respected. Reveals blind spots in compliance and non-functional requirements.  

**Risk Tags:**  
- Compliance, Security, Auditability  

**Typical Behavior:**  
- Double-checks every regulation  
- Reviews change logs meticulously  
- Demands evidence for safe defaults  

**Detailed Problems:**  
- Data exports without anonymization  
- Missing audit trail entries  
- Retention rules violated (e.g., data never deleted)  
- Weak password policies  
- Unencrypted sensitive fields  

**Example Tests:**  
- Given user requests data deletion → Then audit log shows deletion event.  
- Given password length < 8 → Then system rejects with policy error.  

---

## Accessibility Alex

![Accessibility Alex](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/03-AccessibilityAlex-removebg-preview.png) – *The Inclusive Designer*  
**Quote:**  
“If everyone can’t use it, no one can.”  

**Profile:**  
- **Age:** 31  
- **Role/Background:** Accessibility tester & advocate  
- **Motivation:** Equal access for all users  
- **Behavior Style:** Uses assistive tech, validates WCAG standards  

**Description:**  
Highlights accessibility gaps with screen readers, keyboard navigation, and color contrasts. Ensures inclusivity is built-in.  

**Risk Tags:**  
- Accessibility, Usability, Compliance  

**Typical Behavior:**  
- Tests with NVDA/VoiceOver  
- Navigates without mouse  
- Checks captions, labels, ARIA tags

**Detailed Problems:**  
- Buttons unlabeled for screen readers  
- Non-focusable elements  
- Insufficient color contrast (light grey text)  
- Videos without captions  
- Dynamic content not announced  

**Example Tests:**  
- Given Alex uses keyboard only → Then focus order matches visual order.  
- Given a video plays → Then captions are displayed.  

---

## Always-Right Aya

![Always-Right Aya](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/04-Always-RightAya-removebg-preview.png) – *The Edge-Case Enforcer*  
**Quote:**  
“If it happened once, it must be prevented forever.”  

**Profile:**  
- **Age:** 28  
- **Role/Background:** QA engineer specializing in edge cases  
- **Motivation:** Prevent every rare failure  
- **Behavior Style:** Persistent, detail-obsessed  

**Description:**  
Pushes systems with unusual but valid inputs. Protects against subtle, overlooked risks.  

**Risk Tags:**  
- Validation, Data Integrity, Robustness  

**Typical Behavior:**  
- Finds hidden workflows  
- Insists on handling every rare case  
- Pushes system rules to extremes  

**Detailed Problems:**  
- Boundary values (0, max int, 2,147,483,647)  
- Leap years, daylight saving time  
- Names with diacritics (Ø, Ç, Ł)  
- Unicode edge cases (emojis in names)  
- Nested optional workflows  

**Example Tests:**  
- Given birthdate 29 Feb 2000 → Then accepted.  
- Given birthdate 29 Feb 1900 → Then rejected.  

---

## Poolside Phil

![Poolside Phil](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/05-PoolsidePhil-removebg-preview.png) – *The Workation Surfer*  
**Quote:**  
“Wi-Fi’s weak, I’ll try again later.”  

**Profile:**  
- **Age:** 29  
- **Role/Background:** Digital nomad, freelancer  
- **Motivation:** Stay productive despite poor connectivity  
- **Behavior Style:** Relaxed but careless under lag  

**Description:**  
Shows resilience gaps in sync, retry, and offline handling.  

**Risk Tags:**  
- Reliability, Data Integrity, UX  

**Typical Behavior:**  
- Uses unstable networks  
- Refreshes during loading  
- Retries actions repeatedly  

**Detailed Problems:**  
- Upload stalls at 60%  
- Duplicate creation from retry  
- Offline cache not synced correctly
- Timeouts with no user feedback  

**Example Tests:**  
- Given connection drops mid-upload → Then resume from last chunk.  
- Given Phil retries → Then duplicates are prevented.  

---

## Cleanup Carl

![Cleanup Carl](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/06-CleanupCarl-removebg-preview.png) – *The Fixer*  
**Quote:**  
“I don’t make the mess, but I clean it up.”  

**Profile:**  
- **Age:** 40  
- **Role/Background:** IT admin, data steward  
- **Motivation:** Keep system usable by fixing others’ mistakes  
- **Behavior Style:** Works backend, needs rollback/audit tools  

**Description:**  
Represents admins dealing with bad or inconsistent data. Surfaces the need for strong operability.  

**Risk Tags:**  
- Data Integrity, Maintainability  

**Typical Behavior:**  
- Manually cleans databases
- Resolves duplicates  
- Repairs failed imports  

**Detailed Problems:**
- He has no access to the data, nobody can fix it just in time
- Duplicate records from retries  
- Inconsistent states between systems  
- Wrong permissions causing access chaos  
- No rollback options → forced manual fixes  

**Example Tests:**  
- Ist there an Admin Interface for him
- Can he access the data directly

---

## Nils Newby

![Nils Newby](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/07-NilsNewby-removebg-preview.png) – *The Insecure Beginner*  
**Quote:**  
“I’m not sure if I’m doing this right… but I’ll try anyway.”  

**Profile:**  
- **Age:** 23  
- **Role/Background:** Junior employee, learning system  
- **Motivation:** Get work done but unsure of process  
- **Behavior Style:** Hesitant, prone to mistakes  

**Description:**  
Exposes learnability and UX weaknesses. Makes repeated simple errors.  

**Risk Tags:**  
- Usability, Learnability  

**Typical Behavior:**  
- Ignores help text  
- Misunderstands mandatory fields  
- Re-enters data multiple times
- Has to navigate back and forth in processes to change data

**Detailed Problems:**  
- Leaves fields blank by mistake  
- Confuses tooltips/help messages  
- Deletes/overwrites wrong records  
- Navigates wrong workflow repeatedly  

**Example Tests:**  
- Given Nils leaves a required field empty → Then error highlights field.  
- Given Nils retries → Then system prevents duplicate entry.

---

## Confused Conrad

![Confused Conrad](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/08-Confused_Conrad-removebg-preview.png) – *The Panic Clicker*  
**Quote:**  
“If I click enough, something will work!”  

**Profile:**  
- **Age:** 55  
- **Role/Background:** Stressed office worker  
- **Motivation:** Fix issues quickly, even irrationally  
- **Behavior Style:** Rapid, random clicks under pressure  

**Description:**  
Tests system stability under erratic user behavior.  

**Risk Tags:**  
- Reliability, Stability, UX  

**Typical Behavior:**  
- Rapid clicks  
- Opens/closes windows quickly  
- Restarts mid-process  

**Detailed Problems:**  
- Double submits causing duplicates  
- Cancels processes halfway  
- Overlaps workflows by clicking too fast  
- Exits system without saving  

**Example Tests:**  
- Given Conrad double-clicks → Then only one transaction recorded.  
- Given Conrad closes window mid-save → Then rollback ensures integrity.  

---

## Third-Party Theo

![Third-Party Theo](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/09-Third-Party_Theo-removebg-preview.png) – *The Flaky Partner*  
**Quote:**  
“Our API works… most of the time.”  

**Profile:**  
- **Age:** 37  
- **Role/Background:** Integration partner API provider  
- **Motivation:** Provide service, but unreliable and inconsistent  
- **Behavior Style:** Unpredictable, undocumented changes  

**Description:**  
Represents unreliable external dependencies. Surfaces fragile integrations.  

**Risk Tags:**  
- Availability, Integration, Data Quality  

**Typical Behavior:**  
- Sends delayed responses  
- Changes schemas without warning  
- Returns invalid data  

**Detailed Problems:**  
- API times out at random  
- Data contracts broken (missing fields)  
- Inconsistent formats (JSON one day, XML the next)  
- Service unavailable with no error  

**Example Tests:**  
- Given API returns null → Then system handles gracefully.  
- Given schema changes → Then system rejects with error.  

---

## Chaos Claus

![Chaos Claus](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/10-ChaosClaus-removebg-preview.png) – *The Misconfigured Admin*  
**Quote:**  
“Nobody trained me, so I’ll just do it.”  

**Profile:**  
- **Age:** 45  
- **Role/Background:** Well-meaning but untrained IT admin  
- **Motivation:** “Get it done,” even without knowledge  
- **Behavior Style:** Independent, careless, undocumented  

**Description:**  
Causes chaos via misconfiguration and lack of documentation.  

**Risk Tags:**  
- Reliability, Operability  

**Typical Behavior:**  
- Changes settings without testing  
- Forgets to document changes  
- Overwrites configs directly  

**Detailed Problems:**  
- Breaks deployment config
- Accidentally deletes permissions  
- Corrupts DB settings  
- Leaves undocumented “fixes”  

**Example Tests:**  
- Given Claus changes DB schema → Then system should warn about a corriupt schema
- Given config is invalid → Then deployment blocked with error.  

---

## Malicious Max

![Malicious Max](https://raw.githubusercontent.com/nilsbert/bdd-problem-personas/main/Images/PortraitsWithTransparentBackground/11-Malicious_Max-removebg-preview.png) – *The Saboteur*  
**Quote:**  
“If it can be broken, I’ll break it.”  

**Profile:**  
- **Age:** 38  
- **Role/Background:** Ex-employee turned hacker  
- **Motivation:** Exploit weaknesses for revenge/profit  
- **Behavior Style:** Deliberate, malicious, clever  

**Description:**  
Represents hostile actors. Tests system resilience under intentional abuse.  

**Risk Tags:**  
- Security, Data Integrity, Availability  

**Typical Behavior:**  
- Injects malicious code  
- Explores hidden APIs  
- Pushes system into failure  

**Detailed Problems:**  
- SQL injection in forms  
- Malicious file uploads  
- Token forgery in APIs  
- Directly calling backend methods  
- Brute force logins  

**Example Tests:**  
- Given Max injects SQL → Then system rejects input safely.  
- Given Max uploads `.exe` renamed to `.jpg` → Then upload blocked.  

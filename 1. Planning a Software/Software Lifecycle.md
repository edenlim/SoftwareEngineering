# Software Development Lifecycle
## Phases
SDLC is split into 6 distinct phases
1. Anforderungserhebung/Requirements (Lastenheft):
    - The Requirements phase consists the creation of the ***Lastenheft*** (What the Clients want) from the Client side.
    - The ***Pflichtenheft*** (How the Agency will solve it) will be created as the technical blueprint
2. Analysis/Planning (Pflichtenheft)
    - Creating Functional Models using ***UML Activity*** or ***UML Use Case*** Diagrams
3. Design
    - Bridging the Analysis and Implementation phase with ***UML Class*** or ***UML Sequence*** Diagrams
4. Implementation
    - Programming in specific languages
5. Testing
    - Verifying the correctness of the software relative to the requirements
6. Maintenance
    - Bug Fixing and Version maintenance

## Traversal between Phases

Traversal between phases are called **Models**

- Waterfall Model
- Incremental Iterative Model
- V-Model
- Scrum (Part of Project Management)
- Kanban (Part of Project Management)

### Waterfall Model
A Classic sequential Model, where each phase must be completed before the next begins.

**Phases**: Uses the generic SDLC Phase (Requirement, Analysis, Design, Implementation, Test, Maintenance)

#### Pros
- **Simplicity**: Very easy to manage; every phase has specific deliverables and a review process.

- **Disciplined**: High level of documentation and clear milestones.

- **Predictable**: Works well for small projects where requirements are fixed and well-understood.

#### Cons
- **Rigidity**: Changing requirements later is extremely expensive and difficult.

- **Late Testing**: A working version of the software isn't seen until the very end.

- **Risk**: If a requirement was misunderstood at the start, the entire project might fail, but you only realize it during the final delivery.

### Incremental Iterative Model
A sequential Model that breaks project into smaller, repeated increments. Each increment has its own lifecycle
- Each increment adds a core feature (v1, v1.1, v1.2,...)

**Phases**: The lifecycle of each increment is only the 2nd - 5th phase (Analysis, Design, Implementation, Testing). The first step and last step will only be conducted once; The first step at the start of the project , and the last step after finishing the whole project

#### Pros
- **Early Value**: The customer gets a usable (though incomplete) product very early.

- **Flexibility**: It is easy to change direction or add new features after any iteration.

- **Risk Mitigation**: Errors in requirements are caught early through frequent customer feedback.

#### Cons
- **Management Complexity**: Requires a highly skilled team and constant communication.

- **Scope Creep**: Without strict management, the project can keep growing forever because "it's easy to change."

- **System Architecture**: Constant changes can sometimes lead to "spaghetti" code if the architecture isn't refactored properly.

### Waterfall Model
The "V" shape represents two wings:
- Left Wing (Down): Decomposition and definition (Requirements $\rightarrow$ System Design $\rightarrow$ Architecture $\rightarrow$ Module Design).
- Right Wing (Up): Integration and verification (Unit Testing $\rightarrow$ Integration Testing $\rightarrow$ System Testing $\rightarrow$ Acceptance Testing).
- Bottom of the V: The actual implementation (Coding).

#### Pros
- **Quality Focused**: Testing is planned early (during the design phase), leading to fewer bugs.
- **Clear Structure**: Every "step down" has a corresponding "step up" for verification.
- **Reliability**: Excellent for safety-critical industries (medical, automotive).

#### Cons
- **Inflexible**: Like Waterfall, it struggles with changing requirements.
- **Heavyweight**: High documentation overhead can slow down smaller teams.
- **Late Prototype**: The customer still doesn't see a working product until late in the cycle.


# Lastenheft and Pflichtenheft
## Structure
### Chapter Structure
In Lastenheft and Pflichtenheft, they must follow the following structure:
0. Metadata to chapters
1. Visionen und Ziele (Visions and Goals)
    - What the system should achieve and why it exists.
    - Vision: Long term goal
    - Ziel: Concrete measurable objective
2. Rahmenbedingungen (Framework Conditions)
    - Constraints and rules the system must follow (technical, legal, organizational).
3. Kontext und Überblick (Context and Overview)
    - How the system fits into its environment and interacts with users or other systems.
4. Funktionale Anforderungen (Functional Requirements)
    - What are the concreten requirements the system must perform (features and behaviors).
5. Qualitätsanforderungen (Quality Requirements): How well the system must perform.
    - Functional Safety/Security: Protecting data, such that only authorized users can see it.
        - Security: Encrypted Transfer (e.g HTTPS)
        - Authorization: Requiring login
        - Access Rights: Assigning roles
    - Benutzbarkeit: The User Experience of the System
        - Self-Explainatory: Intuitive design without needing explaination
        - Learnability: How complex it is to learn
    - Effizienz: Performance and resources
        - Time: How fast the system works
        - Resources: How much resources the system consumes
    - Zuverlässigkeit: Systems should remain stable and not crash when error occurs.
        - Failure rate: Frequency of failure during normal operations.
        - Fault tolerance: System still provides a level of performances despite errors
        - Recoverability: How fast and easily system can recover data upon error
    - Wartbarkeit: Code should be easily maintained in the future
        - Analyzability: How easy to find bug
        - Changeability: How easy to add or remove features
        - Testability: How easy to validate System is working
    - Portabilität
        - Instability: How easy to install system in targetted hardware
        - Adaptability: How easy system can be adapted into new OS environmanet
        - Replaceability: How easy to use this system in the place of another system in the same environment
6. Abnahmekriteria (ONLY FOR PFLICHTENHEFT)
    - Includes which function is allowed for which roles/view
    - Includes 
6. Glossary (ONLY FOR LASTENHEFT)
    - Defines Roles/User views

To remember:
- Vz RKFQ: Very-Zippy Robots Keeps Firmware Quality
- FB-ez-WP: FaceBook EaZy WorkPlace

#### Metadata
The first chapter introduces the metadata of the (Pflichten)heft.

- Voreinstellung (Default settings). Default settings are written in *Cursive*
- Settings: All options are wrapped in curly braces.

### Anforderung (Requirement) ID Naming Convention
#### Summary
1. In both Heften, each Chapter has a specific ID indicator.
2. Each requirement's ID must use the ID indicator of the chapter it belongs to.
3. Each requirement ID is numbered in increments of `10`.
    - Subpoints can and should be added in increments of `1`.
4. All ID must be enclosed in a single Slash `/`
5. Lastenheft will append `L` in front of the Chapter ID Indicator
6. Mapping of ID in Pflichtenheft will be done with `PflichtenheftID(LastenheftID)`
---
#### Chapter Annotation
- Vision: `V`
- Ziele: `Z`
- Rahmenbedingungen: `R`
- Kontext/Überblick: `K`
- Funktionale Anforderung: `F`
- Quality:
    - Functional Safety/Security: `QF`
    - Benutzbarkeit: `QB`
    - Effizienz: `QE`
    - Zuverlässigkeit: `QZ`
    - Wartbarkeit: `QW`
    - Portabilität: `QP`
#### Example
- **Lastenheft**
    - `/LF10/`: The system must allow the user to search for our products by name and sort by availability, price, alphabetically and recency.
- **Pflichtenheft**
    - `/F10/ (/LF10/)`: The system must provide the user with a clear searchbar, where products can be searched via text-input. The result must display a list view that can be sorted via a dropdown menu based on the following criteria:
        - Availability: Filter out non-available product
        - Price: Ascending/Descending
        - Alphabetical: A-Z or Z-A
        - Recency: Date added, Ascending/Descending
    - `/F11/`: If no products match the search criteria, the system must display the message 'No results found' and offer a button to reset all filters."
    - `/F12/`: The search results must be paginated, displaying a maximum of 25 products per page, with 'Next' and 'Previous' navigation buttons."
---
#### Description

In both Heften, there exists the 5 aforementioned chapters. 

The Lastenheft will, within each chapter, describe several points (requirements) that it would like to accomplish. These Requirements will have its own ID.

The Pflichtenheft will, within each chapter, describes the features it implemented. It will map on to the Lastenheft ID similar to "Foreign Keys", indicating that the feature is a direct solution to that particular Requirement.

## Lastenheft (Target Specifications)

1. Visionen und Ziele (Visions and Goals): Answers why the customer is buying the software (e.g., to open new business fields, increase efficiency). It does not answer what the product can do.

2. Rahmenbedingungen (Framework Conditions): Answers where the application runs and who uses it. This is critical for determining usability and IT security requirements.

3. Kontext und Überblick (Context and Overview): Defines interfaces (Schnittstellen) to other systems.

4. Funktionale Anforderungen (Functional Requirements): Specifies core features. Rule: Naming must consist of a noun and a verb in the infinitive (e.g., "Maintain vehicle data" / Fahrzeugdaten pflegen).

5. Qualitätsanforderungen (Quality Requirements): Defines required accuracy, fault tolerance, learnability, response times, changeability, etc. These are often rated in a matrix (very good, good, normal, not relevant).

6. Glossary (Glossar): Defines system-specific terms and synonyms to prevent misunderstandings.

Key Success Factors: Requirements must be complete but not duplicated. Naming must be clear. Everything must trace back to the original business goals.

### Language
**Should**: Used for general vision or desired features
**Must**: Critical Business Logic


## Pflichtenheft (Technical Specifications)

Definition: A Lastenheft refined with technical approaches (Basically Lastenheft but with Verfeinung and Erweiterung). It is the legally binding, detailed description of the service to be delivered. It answers what is being realized and with what technical tools.

1. Visionen und Ziele (Visions and Goals): Mapped directly from the Lastenheft.

2. Rahmenbedingungen (Framework Conditions): Expanded to include the physical environment, operating times, required target hardware/software, and development hardware/software.

3. Kontext und Überblick (Context and Overview): Expanded to include specific hardware interfaces.

4. Funktionale Anforderungen (Functional Requirements): Refined with system logic (e.g., specific functionalities depending on user permissions).

5. Qualitätsanforderungen (Quality Requirements): Expanded to include strict metrics and a Roles and Rights (Rollen und Rechte) matrix mapping specific functions to specific user types (e.g., Clerk -> F10, F30).

6. Acceptance Criteria (Abnahmekriterien): Specific, testable scenarios. Example: "A user of Role X logs into the application, then..."

7. Subsystem Structure (Subsystemstruktur): Optional breakdown showing which features arrive in which version (Version 1.0, 2.0, 3.0) for iterative development.

### Language
Pflichtenheft predominantly uses the word **Must**, due to its legal and binding status. The following are examples:

**Standard Language**
- The system **must** allow `[user]` to `[action]`.
- If `[condition]` then the system **must** `[action]`. 
    - Else If `[condition]` then the system **must** `[action]`
    - Else the system **must** `[action]`.

**Data Types**
- The system **must** ...: `[Data Types]`
    - The system must allow the user to sort the result **alphabetically, numerically, pricewise**.

**Performance**
- The system **must** be able to `[Task]` in `[Metric] && [Value]`
    - The system must be able to **process** all searches in **5** **Seconds**.

### 6. Abnahmekriterien
Specifically targetting **Functional Requirements**.
- Must be testable (Yes/No result)
- Every criterion must link back to a specific function ID



## Lastenheft vs. Pflichtenheft
In German software engineering standards (like DIN 69901), these two documents form the foundation of project planning. They operate as a "Problem vs. Solution" pair.

---
Lastenheft (The "What" and "Why")

Author: The Customer (Auftraggeber).

Focus: The business problem.

Content: It is written in plain, non-technical language. It explains what the business needs to achieve and what features the users require to do their jobs. The customer does not care about the programming language or database used here.

---
Pflichtenheft (The "How" and "With What")

Author: The Contractor / Developer (Auftragnehmer).

Focus: The technical solution.

Content: It translates the Lastenheft into a technical blueprint. It dictates exactly how the system will be built, specifying databases, hardware limitations, precise security logic, and exact test scenarios for project handover. Once signed, it is a legally binding contract defining the scope of work.

---

# Analysis

- Strukturierte Analyse (SA)
• fachliche Modellierung der Anforderungen für prozedurale Sprachen
- Objektorientierte Analyse (OOA)
• fachliche Modellierung der Anforderungen mittels UML für objektorientierte Sprachen
- Datenanalyse
• fachliche Modellierung der Daten z.B. mittels ERM
# Design
- Beschreibung: Brücke zwischen Analyse und Programmierung
    
- Strukturiertes Design (SD)
    - technische, plattformabhängige Modellierung auf Basis der Strukturierten Analyse für prozedurale Sprachen
- Objektorientiertes Design (OOD)
    - technische, plattformabhängige Modellierung mittels UML für objektorientierte Sprachen
- Datenbankdesign
    - Umsetzung eines ERM in ein relationales Datenbankmodell

# Implementation
Structured Programming
- use C
OOP
- use Java
Database
- use SQL 
# Testing
 E.Denert, Software-Engineering, Springer, 1991:
"der überprüfbare und jederzeit wiederholbare Nachweis
der Korrektheit eines Softwarebausteines relativ zu vorher
festgelegten Anforderungen"
# Maintenance
auch Betrieb und Wartung
➢ Ziele
• Unkomplizierte Inbetriebnahme
• Störungsfreier Betrieb
• Geregelte Fehlerbehebung
➢ Tools
• zur Versionsverwaltung:.
- Testversion
- Produktivversion
• zur geregelten Verwaltung und Behebung von Fehlern
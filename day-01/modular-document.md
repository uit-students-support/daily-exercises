Based on your research and understanding, answer the following question:

**Q1.**
What is a modular document in LaTeX?

**A1.**
A modular document in LaTeX is a project organization method that breaks a massive document into multiple independent `.tex` files, linking them together through a central master file that contains all formatting configurations.

**Q2.**
Why should a large document be divided into multiple files?

**A2.**
A large LaTeX document should be divided into multiple files to improve modularity, organization, maintainability, and collaboration. Each chapter or logical section can be stored in a separate `.tex` file and incorporated into a main document using commands such as `\input` or `\include`. This structure makes it easier to locate and modify specific parts, debug compilation errors, collaborate on different sections, and selectively compile parts of a large document during development. For large projects, this modular approach also helps keep the main document concise and separates document structure, configuration, and content.

**Q3.**
When designing a modular LaTeX document, the structure should not only be divided into multiple files but should also be easy to understand, maintain, extend, collaborate on, and debug. Consider the following 6 criteria when evaluating a modular LaTeX document and its source code. For each sub-criterion below, provide one example that follows the criterion and one example that does not follow the criterion.

**Main Evaluation Criteria**

| Criterion           | Description                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Modularity**      | How well the document is divided into independent and logically organized components.                                           |
| **Readability**     | How easily another person can understand the document structure and read the LaTeX source code.                                 |
| **Maintainability** | How easily the document can be modified, updated, or corrected without causing unnecessary changes elsewhere.                   |
| **Scalability**     | How well the document structure can accommodate growth, such as adding new chapters, sections, figures, tables, or appendices.  |
| **Collaboration**   | How easily multiple people can work on different parts of the document while minimizing conflicts and unnecessary dependencies. |
| **Debugging**       | How easily errors can be identified, isolated, traced, and fixed within the document structure.                                 |

---

**Sub-Criteria**

**1. Modularity**

| Sub-criterion              | Description                                                                                                                               |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Component separation**   | Major components of the thesis are separated into appropriate files or modules.                                                           |
| **Single responsibility**  | Each file or module has a clear and specific purpose instead of handling unrelated content.                                               |
| **Logical grouping**       | Related files and resources are grouped together in meaningful folders or modules.                                                        |
| **Separation of concerns** | Different responsibilities, such as document configuration, thesis content, figures, tables, and references, are appropriately separated. |

**2. Readability**

| Sub-criterion                    | Description                                                                                                          |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Meaningful naming**            | Files, folders, labels, commands, and other identifiers have clear and descriptive names.                            |
| **Clear hierarchy**              | The file and folder structure clearly reflects the hierarchy of the thesis.                                          |
| **Structural simplicity**        | The project avoids unnecessary files, folders, nesting, or structural complexity.                                    |
| **Consistency**                  | The same organizational and coding conventions are followed throughout the project.                                  |
| **Code formatting & simplicity** | LaTeX source code uses consistent indentation, spacing, line breaks, and a simple coding style that is easy to read. |
| **Comments & documentation**     | Important or non-obvious code, configurations, and project conventions are documented when necessary.                |

**3. Maintainability**

| Sub-criterion                 | Description                                                                                                   |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **Change isolation**          | Changes to one component can be made without unnecessarily modifying other components.                        |
| **Centralized configuration** | Shared settings, formatting rules, commands, and configurations are defined in appropriate central locations. |
| **Low duplication**           | Repeated content, commands, or configurations are minimized and reused where appropriate.                     |
| **Dependency management**     | Dependencies between files, modules, packages, and configurations are clear and appropriately managed.        |

**4. Scalability**

| Sub-criterion             | Description                                                                                             |
| ------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Easy extension**        | New chapters, sections, appendices, or other components can be added without major restructuring.       |
| **Stable structure**      | The overall project structure remains understandable as the thesis becomes larger.                      |
| **Resource organization** | Figures, tables, references, appendices, and other resources can be added and organized systematically. |
| **Consistent growth**     | The same organizational rules and conventions can continue to be applied as the project grows.          |

**5. Collaboration**

| Sub-criterion                    | Description                                                                                          |
| -------------------------------- | ---------------------------------------------------------------------------------------------------- |
| **Work separation**              | Different contributors can work on different components of the thesis.                               |
| **Conflict reduction**           | The structure minimizes situations where multiple contributors need to modify the same file or code. |
| **Independent editing**          | Contributors can modify their assigned components without unnecessarily affecting other components.  |
| **Shared configuration control** | Shared settings and configuration files are clearly identified and managed carefully.                |

**6. Debugging**

| Sub-criterion               | Description                                                                                                    |
| --------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Error localization**      | It is possible to identify which file or component is responsible for an error.                                |
| **Module isolation**        | Individual modules can be examined, tested, or temporarily isolated when troubleshooting.                      |
| **Dependency traceability** | It is possible to understand which files, commands, or configurations are related to the error.                |
| **Failure containment**     | An error in one component does not unnecessarily make the entire project difficult to inspect or troubleshoot. |

**A3.**
The examples assume a thesis project with the following structure:

```text
thesis/
├── main.tex
├── preamble.tex
├── references.bib
│
├── chapters/
│   ├── introduction.tex
│   ├── literature-review.tex
│   ├── methodology.tex
│   ├── experiments.tex
│   └── conclusion.tex
│
├── figures/
│   ├── architecture/
│   └── experiments/
│
├── tables/
│
└── appendices/
    └── additional-results.tex
```

---

### Modularity

Modularity describes how well the document is divided into independent and logically organized components.

**Component Separation**

**Example that follows the criterion**

Each major chapter is stored in a separate `.tex` file:

```text
chapters/
├── introduction.tex
├── literature-review.tex
├── methodology.tex
├── experiments.tex
└── conclusion.tex
```

The main document then assembles these components:

```latex
\include{chapters/introduction}
\include{chapters/literature-review}
\include{chapters/methodology}
\include{chapters/experiments}
\include{chapters/conclusion}
```

**Example that does not follow the criterion**

All chapters are written directly inside one large `main.tex` file:

```text
main.tex
```

The file contains the introduction, literature review, methodology, experiments, conclusion, and appendices.

This makes the document difficult to navigate and modify as it becomes larger.

---

**Single Responsibility**

**Example that follows the criterion**

The file:

```text
chapters/methodology.tex
```

contains only the content of the methodology chapter.

**Example that does not follow the criterion**

The file:

```text
chapters/methodology.tex
```

contains:

* methodology content,
* package configuration,
* bibliography configuration,
* conclusion content,
* appendix content.

The file therefore has multiple unrelated responsibilities.

---

**Logical Grouping**

**Example that follows the criterion**

Architecture-related figures are grouped together:

```text
figures/
└── architecture/
    ├── system-architecture.pdf
    └── network-architecture.pdf
```

Experiment-related figures are stored separately:

```text
figures/
└── experiments/
    ├── experiment-01.pdf
    └── experiment-02.pdf
```

**Example that does not follow the criterion**

All resources are placed randomly in the project root:

```text
thesis/
├── system-architecture.pdf
├── experiment-01.pdf
├── methodology.tex
├── network-architecture.pdf
├── chapter2.tex
└── result-final.pdf
```

There is no clear grouping of related resources.

---

**Separation of Concerns**

**Example that follows the criterion**

Different responsibilities are separated:

```text
preamble.tex       → document configuration
chapters/          → thesis content
figures/           → figures
tables/            → tables
references.bib     → bibliography
appendices/        → appendices
```

**Example that does not follow the criterion**

A chapter file contains both thesis content and unrelated configuration:

```latex
% methodology.tex

\usepackage{graphicx}
\usepackage{amsmath}

\section{Methodology}

...

\bibliographystyle{plain}
```

Configuration and content are unnecessarily mixed together.

---

### Readability

**Meaningful Naming**

**Example that follows the criterion**

```text
literature-review.tex
system-architecture.pdf
experimental-results.tex
```

A descriptive label can also be used:

```latex
\label{fig:system-architecture}
```

**Example that does not follow the criterion**

```text
ch2.tex
final2.pdf
abc.tex
new_new_final.tex
```

and:

```latex
\label{fig:x}
```

These names provide little information about their purpose.

---

**Clear Hierarchy**

**Example that follows the criterion**

```text
chapters/
├── introduction.tex
├── background/
│   ├── networking.tex
│   └── kubernetes.tex
└── methodology/
    ├── system-design.tex
    └── experiments.tex
```

The folder structure communicates the relationship between chapters and their components.

**Example that does not follow the criterion**

```text
a/
├── x.tex
└── b/
    └── test/
        └── final.tex
```

The hierarchy does not communicate the structure of the thesis.

---

**Structural Simplicity**

**Example that follows the criterion**

A thesis with five major chapters uses a simple structure:

```text
chapters/
├── introduction.tex
├── background.tex
├── methodology.tex
├── results.tex
└── conclusion.tex
```

**Example that does not follow the criterion**

Every paragraph is placed in a separate file:

```text
chapters/
└── methodology/
    └── section-1/
        └── subsection-1/
            └── paragraph-1/
                └── paragraph.tex
```

This introduces unnecessary complexity.

---

**Consistency**

**Example that follows the criterion**

All chapter files use lowercase kebab-case:

```text
introduction.tex
literature-review.tex
system-design.tex
experimental-results.tex
```

**Example that does not follow the criterion**

The project uses inconsistent naming conventions:

```text
Introduction.tex
literature_review.tex
SystemDesign.tex
chapter4-FINAL.tex
RESULTS_new.tex
```

---

**Code Formatting and Simplicity**

**Example that follows the criterion**

```latex
\section{Experimental Setup}

The experiment consists of three components:

\begin{itemize}
    \item Client
    \item Server
    \item Database
\end{itemize}
```

**Example that does not follow the criterion**

```latex
\section{Experimental Setup}
The experiment consists of three components:
\begin{itemize}\item Client
\item Server
\item Database\end{itemize}
```

Although both examples may compile, the first is easier to read and maintain.

---

**Comments and Documentation**

**Example that follows the criterion**

```latex
% This command defines the notation used
% for system load throughout the thesis.
\newcommand{\Load}{L_i}
```

The comment explains the purpose of a non-obvious command.

**Example that does not follow the criterion**

```latex
\newcommand{\Load}{L_i}
```

The command is important but its purpose is not documented.

---

### Maintainability

**Change Isolation**

**Example that follows the criterion**

To modify the methodology chapter, only this file needs to be changed:

```text
chapters/methodology.tex
```

**Example that does not follow the criterion**

A small change to the methodology requires modifications to:

```text
main.tex
preamble.tex
methodology.tex
results.tex
conclusion.tex
```

This indicates strong coupling between components.

---

**Centralized Configuration**

**Example that follows the criterion**

Shared configuration is placed in `preamble.tex`:

```latex
\usepackage{graphicx}
\usepackage{amsmath}
\usepackage{booktabs}

\newcommand{\EKS}{Amazon Elastic Kubernetes Service (EKS)}
```

**Example that does not follow the criterion**

Each chapter independently defines shared packages and commands:

```latex
% methodology.tex
\usepackage{graphicx}

% experiments.tex
\usepackage{graphicx}

% results.tex
\usepackage{graphicx}
```

This creates unnecessary duplication.

---

**Low Duplication**

**Example that follows the criterion**

A frequently used term is defined once:

```latex
\newcommand{\EKS}{Amazon Elastic Kubernetes Service (EKS)}
```

It can then be reused:

```latex
\EKS
```

**Example that does not follow the criterion**

The full expression is repeatedly written and manually formatted throughout many files:

```latex
Amazon Elastic Kubernetes Service (EKS)
```

If the formatting or terminology changes, many files may need to be modified.

---

**Dependency Management**

**Example that follows the criterion**

The dependency structure is straightforward:

```text
main.tex
├── preamble.tex
├── chapters/introduction.tex
├── chapters/methodology.tex
└── chapters/results.tex
```

The main document assembles the independent content modules.

**Example that does not follow the criterion**

`results.tex` depends on commands defined inside `methodology.tex`, while `methodology.tex` also depends on definitions from `results.tex`.

```text
methodology.tex
       ↕
results.tex
```

This creates hidden or circular dependencies.

---

### Scalability

**Easy Extension**

**Example that follows the criterion**

To add a new chapter:

```text
chapters/future-work.tex
```

Then add:

```latex
\include{chapters/future-work}
```

to `main.tex`.

**Example that does not follow the criterion**

Adding one chapter requires restructuring the existing `main.tex` because all existing content is tightly coupled inside one large source file.

---

**Stable Structure**

**Example that follows the criterion**

The project grows while preserving the same structure:

```text
chapters/
├── introduction.tex
├── background.tex
├── methodology.tex
├── implementation.tex
├── experiments.tex
├── results.tex
├── discussion.tex
└── conclusion.tex
```

**Example that does not follow the criterion**

The project gradually becomes:

```text
chapter2-final.tex
chapter2-final-new.tex
newchapter.tex
result-final2.tex
old/
stuff/
test/
backup/
```

The structure becomes increasingly difficult to understand.

---

**Resource Organization**

**Example that follows the criterion**

```text
figures/
├── architecture/
└── experiments/

tables/
├── datasets/
└── results/

appendices/
└── additional-results.tex

references.bib
```

**Example that does not follow the criterion**

```text
image1.png
image-final.png
table.tex
result2.png
appendix-final.tex
reference-new.bib
figure-new-final.png
```

All resources are mixed together without a systematic organization.

---

**Consistent Growth**

**Example that follows the criterion**

Existing files:

```text
chapters/methodology.tex
chapters/experiments.tex
```

A new chapter follows the same convention:

```text
chapters/discussion.tex
```

**Example that does not follow the criterion**

The project initially uses:

```text
chapter-1.tex
chapter-2.tex
```

but later introduces:

```text
Chapter3Final.tex
chapter_4_new.tex
FINAL-chapter5.tex
```

The naming convention becomes inconsistent.

---

### Collaboration

**Work Separation**

**Example that follows the criterion**

```text
Contributor A → introduction.tex
Contributor B → methodology.tex
Contributor C → experiments.tex
```

Each contributor works primarily on a different module.

**Example that does not follow the criterion**

All contributors must edit:

```text
main.tex
```

because the entire thesis is stored in one file.

---

**Conflict Reduction**

**Example that follows the criterion**

```text
Alice → chapters/methodology.tex
Bob   → chapters/experiments.tex
```

Because the contributors work on different files, the probability of Git merge conflicts is reduced.

**Example that does not follow the criterion**

```text
Alice → main.tex
Bob   → main.tex
```

Both contributors modify the same large file, increasing the likelihood of merge conflicts.

---

**Independent Editing**

**Example that follows the criterion**

A contributor can modify:

```text
chapters/experiments.tex
```

without modifying:

```text
chapters/introduction.tex
```

**Example that does not follow the criterion**

Changing one experiment subsection requires modifying a shared file containing the introduction, methodology, experiments, and conclusion.

---

**Shared Configuration Control**

**Example that follows the criterion**

The project has a central configuration file:

```text
preamble.tex
```

The team knows that changes to this file may affect the entire thesis.

**Example that does not follow the criterion**

Each contributor independently modifies global formatting or package configuration inside their own chapter.

This can result in inconsistent document behavior and formatting.

---

### Debugging

**Error Localization**

**Example that follows the criterion**

A LaTeX error is reported in:

```text
chapters/methodology.tex
```

The developer can immediately inspect the methodology module.

**Example that does not follow the criterion**

A 5,000-line `main.tex` contains the entire thesis. An error occurs somewhere in the file, requiring a large amount of searching to locate the problem.

---

**Module Isolation**

**Example that follows the criterion**

The project uses:

```latex
\include{chapters/introduction}
\include{chapters/methodology}
\include{chapters/results}
```

During development, a specific module can be selected using:

```latex
\includeonly{chapters/methodology}
```

This allows the developer to focus on one part of a large document.

**Example that does not follow the criterion**

All content is embedded directly into one large `main.tex`, with no meaningful module boundaries that can be isolated during troubleshooting.

---

**Dependency Traceability**

**Example that follows the criterion**

If `results.tex` uses:

```latex
\systemname
```

and the command is defined in:

```text
preamble.tex
```

the dependency can be easily traced:

```text
results.tex
    ↓
\systemname
    ↓
preamble.tex
```

**Example that does not follow the criterion**

A command used in `results.tex` is defined inside another unrelated chapter file, such as `methodology.tex`.

The dependency is hidden and difficult to trace.

---

**Failure Containment**

**Example that follows the criterion**

A figure used only by the experiments chapter is invalid:

```text
figures/experiments/result-01.pdf
```

The developer can focus on the experiments module and the corresponding figure.

**Example that does not follow the criterion**

A global macro in a large `main.tex` file causes many subsequent compilation errors across unrelated chapters.

It becomes difficult to distinguish the original error from cascading errors.


**Q4.**
What is the difference between a `.cls` file and a `.sty` file in LaTeX? You may present your answer in a table format.

**A4.**

| Feature | `.cls` file | `.sty` file |
| :--- | :--- | :--- |
| **Core Purpose** | Defines the **overall structure and layout** of the document (the skeleton). | Provides **specific features, tools, or local formatting** overrides (the accessories). |
| **How to Load** | Loaded using the `\documentclass{filename}` command. | Loaded using the `\usepackage{filename}` command. |
| **Quantity Allowed** | You can only use **exactly one** `.cls` file per document. | You can use **multiple** (unlimited) `.sty` files in a single document. |
| **Placement** | Must be the very first command in your `.tex` file. | Placed in the preamble (between `\documentclass` and `\begin{document}`). |
| **Common Examples** | `article`, `report`, `book`, `beamer`, `ieeeconf` | `graphicx` (images), `amsmath` (math), `hyperref` (links) |
| **Analogy** | The architectural blueprint and foundation of a house. | The furniture, plumbing, and paint added to the house. |


**Q5.**
For the graduation thesis and academic presentation template, when would you use a `.cls` file, a `.sty` file, or neither? Your explanation should show how each choice supports or affects these 6 criteria above.

**A5.**
When structuring a graduation thesis or an academic presentation (like a Beamer slide deck), deciding where to place your configurations dictates the health of your LaTeX project. Here is how choosing a `.cls` file, a `.sty` file, or neither impacts your workflow across the six core criteria.

**Using Neither (Putting Everything in `main.tex`)**
This approach involves writing all custom commands, margin adjustments, and package imports directly in the preamble of your master file.

*   **Modularity:** **Poor.** Layout rules, custom macros, and actual content are all tangled in a single file. 
*   **Readability:** **Low.** Before reaching the actual introduction of your high-availability Raspberry Pi cluster deployment, you have to scroll through hundreds of lines of code.
*   **Maintainability:** **Low.** If you want to reuse a custom table format in a future presentation, you have to manually copy-paste the preamble.
*   **Scalability:** **Poor.** As the thesis grows to 50+ pages, managing a bloated master file becomes unwieldy.
*   **Collaboration:** **Risky.** If multiple authors are pushing changes via Git, modifying a monolithic preamble often leads to frustrating merge conflicts.
*   **Debugging:** **Difficult.** A missing bracket in a custom macro might throw an error that points to line 450, mixed right in with your text.

**Using a `.sty` File**
This involves moving your custom commands, specific packages, and local formatting rules into a separate file (e.g., `my_macros.sty`) and calling `\usepackage{my_macros}`.

*   **Modularity:** **High.** You separate specific features from the skeleton. You might have one `.sty` file for math macros and another for drawing network topologies.
*   **Readability:** **Excellent.** Your `main.tex` preamble is reduced to a few clean `\usepackage{}` lines.
*   **Maintainability:** **High.** If you need to adjust how experimental performance metrics (like response latencies or embedding model scores) are formatted across dozens of tables, you only change the macro once in the `.sty` file.
*   **Scalability:** **Excellent.** You can easily toggle features on or off by commenting out a single `\usepackage` line as the project expands.
*   **Collaboration:** **Smooth.** Teammates can write content in the `.tex` files without accidentally breaking your custom formatting rules, preventing Git conflicts.
*   **Debugging:** **Targeted.** If a custom equation syntax fails, LaTeX will indicate that the error originates inside `my_macros.sty`, isolating the logic bug from the text.

**Using a `.cls` File (Document Class)**
This involves writing or using a custom class (e.g., `my_university_thesis.cls`) to define the absolute foundational layout-like the 3cm/3.5cm margin rules, standard font sizes, and the exact title page structure. 

*   **Modularity:** **Absolute.** The `.cls` file handles the strict, unchangeable architectural rules, entirely independent of user features or content.
*   **Readability:** **Maximum.** The document author doesn't even see the complex layout code. They just write `\documentclass{my_university_thesis}` and start typing.
*   **Maintainability:** **Rigid but Secure.** It is harder to write and maintain a `.cls` file from scratch, but once created, it ensures total consistency. 
*   **Scalability:** **Perfect.** A well-designed `.cls` file will robustly handle a 5-page proposal or a 150-page graduation thesis with equal stability.
*   **Collaboration:** **Enforced.** It acts as a constraint. Collaborators cannot accidentally mess up the mandatory university formatting guidelines because the rules are locked away in the `.cls` file.
*   **Debugging:** **Categorized.** Structural layout errors (like wrong page numbering on the Front Matter) are isolated to the `.cls` file, while content errors are in the `.tex` files. 


**Q6.**
Design a directory tree for your own graduation thesis and academic presentation LaTeX projects.Your directory structure should be designed according to the 6 criteria discussed above. For each major directory or file, briefly explain its purpose and how your structure supports the 6 criteria. You may present your answer using a directory tree format. You may also research the topics of *Separation of Content and Presentation* and the *DRY (Don't Repeat Yourself)* principle to inform your design.

**A6.**
```text
graduation_project/
│
├── shared_assets/                  
│   ├── figures/
│   │   ├── raspberry_pi_cluster.png
│   │   └── wlan_architecture.pdf
│   ├── bibliography/
│   │   └── references.bib
│   └── styles/
│       ├── custom_macros.sty       
│       └── acronyms.tex            
│
├── thesis/                         
│   ├── main_thesis.tex             
│   ├── thesis_layout.cls           
│   ├── frontmatter/
│   │   ├── title_page.tex
│   │   ├── abstract.tex
│   │   └── acknowledgments.tex
│   ├── chapters/                   
│   │   ├── 01_introduction.tex
│   │   ├── 02_background.tex
│   │   ├── 03_methodology.tex
│   │   ├── 04_experimental_eval.tex 
│   │   └── 05_conclusion.tex
│   └── backmatter/
│       └── appendix_code.tex
│
└── presentation/                   
    ├── main_slides.tex             
    ├── slides_theme.sty            
    └── sections/                   
        ├── 01_problem_statement.tex
        ├── 02_system_architecture.tex
        └── 03_results.tex
```
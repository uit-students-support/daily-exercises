Based on your research and understanding, answer the following question:

**Q1.**
What is a modular document in LaTeX?

**A1.**
<!-- Your answer here -->

**Q2.**
Why should a large document be divided into multiple files?

**A2.**
<!-- Your answer here -->

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
<!-- Your answer here -->

**Q4.**
What is the difference between a `.cls` file and a `.sty` file in LaTeX? You may present your answer in a table format.

**A4.**
<!-- Your answer here -->

**Q5.**
For the graduation thesis and academic presentation template, when would you use a `.cls` file, a `.sty` file, or neither? Your explanation should show how each choice supports or affects these 6 criteria above.

**A5.**
<!-- Your answer here -->

**Q6.**
Design a directory tree for your own graduation thesis and academic presentation LaTeX projects.Your directory structure should be designed according to the 6 criteria discussed above. For each major directory or file, briefly explain its purpose and how your structure supports the 6 criteria. You may present your answer using a directory tree format. You may also research the topics of *Separation of Content and Presentation* and the *DRY (Don't Repeat Yourself)* principle to inform your design.

**A6.**
<!-- Your answer here -->
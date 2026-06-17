# Academic Program Transfer Planner

## Introduction

This project was created for the Introduction to Artificial Intelligence midterm assignment.

The purpose of the application is to help students who want to transfer from one academic program to another. It shows which completed courses from the current program may correspond to courses in the new program.

The current program used in this project is Computer Engineering.

---

## Main Features

The website includes:

* A table containing all courses.
* Information about whether each course has been passed.
* A menu for selecting a target program.
* A transfer button.
* An equivalency table that contains only completed courses.

---

## Technologies

This project was developed using:

* HTML
* CSS
* JavaScript

Everything is contained in a single HTML file.

---

## How the Equivalency Works

When the user presses the Transfer button, the program checks the list of courses.

Courses marked with "Yes" are considered completed and are included in the equivalency table.

Courses marked with "No" are ignored.

For each completed course, the program tries to find a similar course in the selected program. If no suitable match exists, the application displays "N/A".

Some examples are:

| Course                           | Equivalent Course     |
| -------------------------------- | --------------------- |
| Calculus I                       | Calculus I            |
| Calculus II                      | Calculus II           |
| Computer Organization            | Computer Architecture |
| Scripting Languages              | Programming Languages |
| Introduction to Modern Thought I | N/A                   |

---

## File Structure

```text
index.html
README.md
```

The HTML file contains the structure of the page, the CSS styles, and the JavaScript code.

---

## Future Improvements

Currently, the equivalencies are based on manually defined rules. In the future, this process could be automated.

One possible solution would be to compare the syllabi of academic programs automatically.

A possible algorithm would be:

1. Load the syllabi of both programs.
2. Extract course descriptions and learning outcomes.
3. Use artificial intelligence and natural language processing to analyze the contents.
4. Measure the similarity between courses.
5. Determine equivalent courses automatically.
6. Generate the transfer table.

This approach could make the results more accurate and reduce manual work.

Other improvements could include:

* Support for more programs.
* Better user interface.
* Search and filtering.
* Exporting results to PDF.
* Saving transfer results.

---

## Conclusion

This project provides a simple way to compare completed courses and estimate how they may transfer to another academic program.

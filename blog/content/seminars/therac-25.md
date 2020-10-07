---
title: "Seminar: Week 4 - Software Disasters: Therac-25"
date: 2020-10-07T12:00:45+11:00

categories: ["Seminars"]
hiddenFromHomePage: false
postMetaInFooter: false

flowchartDiagrams:
  enable: false
  options: ""

sequenceDiagrams: 
  enable: false
  options: ""

---

# Therac-25

* Medical Linear Accelerator
* Mechanical restrictions were removed in favour of software control
  * Originally restricted operability from the Therac-20 and Therac-6
* Programmed by one person
  * Minimal testing
  * Software designed without consideration of error handling
  * Software was not reviewed

1985 - Overdose of 100x the intended amount

* Software Issue
  * Race condition
  * If the operator entered inputs too fast, the list of configurations will be malformed
  * Issue wasn't discovered earlier as it required the operator to be proficient

* As a result of previous successful machines, the AECL believed in the safety.

<!-- * Ethical Issues
  * Saved money
  * Faster turnaround -->

---

## Blame??

* Developers
* AECL (Business)
* Operator
* FDA (Regulators)

---

# How much is a human life worth?

* This isn't the right question to ask
* **What's the purpose of the product** - to save humans

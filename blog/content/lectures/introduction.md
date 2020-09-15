---
title: "Lecture: Introduction to Management and Ethics"
date: 2020-09-15T13:00:00+10:00

categories: ["Lectures"]
hiddenFromHomePage: false
postMetaInFooter: false

flowchartDiagrams:
  enable: false
  options: ""

sequenceDiagrams: 
  enable: false
  options: ""

---

# Management and Ethics

* Software Project Management
* Professional Issues and Ethics

# Ethics

Ethics is about what you ***should*** do, NOT what **to** do.

* Based on rules/principles/duties/rights/obligations
* Based on consequences

---

# Ethics in Action

* UNSW job losses
* Would you take a 20% pay cut so that other staff members will keep their jobs
* Will you follow through with your decision?

---

# Why Do Software Projects Fail?

* Unclear requirements
* Overly optimistic / unrealistic schedules
* Lack of user input
* Lack of executive sponsorship and support
* Turnover and layoffs

---

* Lack of adoption

## Ariane 5 - Rocket failure

* Software exception
* Wrong data sent to the onboard computer
* Large correction for attitude deviation (artificial horizon)
* Rocket disintegrated after 39 seconds

---

There were redundant hardware and software in place, however the bug was existent on both systems (since they are identical). This caused some software trace to be considered as flight data - which caused an invalid response.

---

**Code Analysis**

* After an review of the code, it was concluded that some variables could have led to the software exception. However some of these variables were not protected by design - as they had a large margin of safety, and/or should never reach that code path.

* Redundant/unnecessary code was also being executed.

* The Ariane 5 rocket used the same Inertial Reference System as the Ariane 4 rocket.  
However the Ariane 5 had different (physical) parameters than the Ariane 4. This issue is known as a **reuse specification error**

> #WorksOnMy<s>Machine</s>Rocket

## Takeaways

* Duplication of components is only useful for handling hardware faults
* Software reuse must be handled with consideration of the new environment

---

# What is Good Quality Software

* It works
* It works well
* It always works (well)
* It works everywhere
* Easy to maintain
* Easy to test
* :)

---

Successful projects often have clear requirements, realistic budgets and schedules, proper planning, and constructive feedback.

---

* Functional vs Non-Functional Requirements
  * Functional - Features
  * Non-Functional - The experience

* Brooks' Law
  * Adding people to a late software project makes it later
  * "Bathtub Curve"
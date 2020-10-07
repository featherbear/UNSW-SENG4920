---
title: "Seminar: Week 4 - Software Disasters: Uber Autonomous Car Crash"
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

# Uber Autonomous Car Crash

* Jaywalker on a street with a bicycle
  * Black clothes
  * No reflectors on their bicycle
* The automated driving system (ADS) detected the lady 5.6 seconds before the crash
  * Did not accurately classify the jaywalker as a pedestrian
  * Unknown <-> Pedestrian <-> Cyclist
    * ???
    * Car kept recalculating
* The driver of the car was on her phone, and not fully paying attention to the road
* There were software issues previously reported by other Uber employees
  * Incidents were ignored and logs were left unreviewed for weeks
* During testing, Uber
  * Removed sudden emergency braking
  * Reduced the number of supervisors in the test vehicles

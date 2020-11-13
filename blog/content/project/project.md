---
title: "Project: Splitify"
date: 2020-11-13T05:11:08+11:00

categories: ["Project"]

hiddenFromHomePage: false
postMetaInFooter: false

flowchartDiagrams:
  enable: false
  options: ""

sequenceDiagrams: 
  enable: false
  options: ""

---

* [Web Application](https://splitify.github.io/)
* [Source Code](https://github.com/Splitify/splitify)
* [GitHub Organisation](https://github.com/splitify/)
* [Project Diary](https://featherbear.cc/UNSW-SENG4920-diary/)
* [Initial Project Pitch](https://splitify.github.io/initial-project-pitch)
* [Branding Resources](https://splitify.github.io/branding/)

---

![](https://splitify.github.io/branding/textmark/textmark@72.png)

After 7 weeks of toiling and staring at my Webpack instance taking its time "Compiling", and eslint shouting bad things in red at me - We're done!

For the group project, my team settled upon a Spotify playlist manager application, dubbed "Splitify". 
It's in no way polished or feature rich, and there's a lot that I would have done, but given that this was done in 7 weeks, amongst other courses to study for - it's "adequate".

Now that the assignment has been submitted, if I were to clean up the code, there would be many improvements that I'd want to make.

* Removing the callback hell and just having a single `onUpdate` callback that listeners could attach to
* Optimising functions
* Using ES6 syntax for more things
* Use something other than React. _Svelte anyone?_

# Jumping In Too Early

Early into the project, I wanted to get started with the infrastructural design of the components, such as the data structures, and how data would be passed around the components (on a design level). Something like Redux or MobX - but before I knew it, my other team members had already pushed out code, and we were locked into that design structure.

I could definitely see artifacts of bad code designs coming up, but it was difficult to revert due to everyone pushing out code. Merge conflicts would arise, and people didn't carefully consider what to merge during conflict resolution, leading to even more problems.

For example, take the [`dashboard.tsx`](https://github.com/Splitify/splitify/blob/master/src/routes/pages/dashboard.tsx) file - which was the main view inside the application. It's **fat**.

# React

It wouldn't be an Andrew post if I didn't post about my gripe about React.  
It's great. It's used everywhere. It's advanced. It's built by the overlords at Facebook.  

But it's so freaking massive.  

![](Snipaste_2020-11-14_00-15-15.png)

<h1>SO MANY THINGS</h1>

Sure, you don't need to do a `npm install` / `yarn` every time you launch the development server; so you only have to wait a few minutes during the initial package installation. Webpack did like to take its sweet time when I tried to develop the project on my Windows machine... I'm not too sure why that was the case.

---

React offers a great amount of flexibility when it comes to writing your code.  

> `useState` is a funky subscriber based value store for updating data and bubbling events to other components.  
Their `useCallback` and `useEffect` hooks are great to conditional execute code, and `useMemo` is a nice touch to amortise renders of the same component.  
And `useContext` is a great way to pass data between elements without having to pass down props every component you go.  
`createRef` is pretty neat if dealing with DOM-based functionality.

I did however, find myself question my knowledge (and sanity) when it came to forcibly re-rendering components. This occurred when storing values in an objet that was passed into a component. Since I'm not modifying the object address (which the prop is sensitive to), an update inside the memory pointed to by the address wouldn't trigger a re-render.

I wrote this sort of code twice during this project

```tsx
const [refreshDrilldown, __setRefreshDrilldown] = useState(false)
const refresh = () => __setRefreshDrilldown(r => !r);
```

It's a function `refresh` that updates a value store `refreshDrilldown`.  
Any component who I pass and set up `refreshDrilldown` as a prop can then be re-rendered when `refresh()` is called.

But is this the right way to do it? I have no clue.

---

# Presentation

I was a bit shocked when my team decided not to create (even a simple) presentation our initial project pitch, so I decided to [do it myself](https://splitify.github.io/initial-project-pitch). Safe to say, it was a good decision, as every other team that pitched had a presentation.  

It would have made our team look unprepared and unorgansised.

That did indeed was how I felt during the development of this project.  
No one in my group had much experience with developing with React.  
I seemed to be the most proficient at it - [and I don't even like React!](https://featherbear.cc/blog/post/react/).

One of the members in my team also asked what a pull request was

---

# Contribution and Timeline

[[Full statistics page]](./contrib.html)

<iframe src="contrib.html" width="100%" height="500px"></iframe>

Shout out to Team Member 1 who did their 20% of work, and also for being responsive online!

I didn't any time to touch the project for the first few weeks, as I was busy with other work commitments. But from the end of Week 5, I had time available to dedicate to working on the project

However, the rest of the team also seemed to not have done much either during that time. I would have hoped to see some progress during my absence, having already done a lot with creating the [branding resources](https://splitify.github.io/branding/) - logo, textmark, colour scheme, even a build chain to generate different qualities of those images, as well as website to view all of them. 

Okay to be fair - it was over the top, and was just me being extra. But I had also created the [project pitch presentation](https://splitify.github.io/initial-project-pitch), during the wee hours of the morning when I should have been asleep to prepare for the actual project pitch. We should all have been working on that presentation, not just me.

|Planned|Actual|
|:---:|:---:|
|![](timeline-planned.png)|![](timeline-actual.png)|

Slow development also meant delayed tasks, as you can see by the delayed tasks (red).  
I really wanted to finish everything by the start of Week 9, as I knew that I'd be busy with other things in Week 9. However, not enough progress was done by the start of Week 8 - and I knew that it wouldn't be possible to finish early.

If you know me, I ***hate*** last-minute work.

But.. ahhahaha.. Here we are, submitting 6 seconds before it is due.  

At least I could automate the submission :')  

![](submission.png)


---

But, we got there in the end. It's over and I'm glad.

Here's a nice screenshot of the project's git activity :)

![](Snipaste_2020-11-14_00-20-22.png)

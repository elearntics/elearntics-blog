---
title: How to use e-journal
description: Learn how to create a file system that will help you finish online courses.
---

## What's e-journal?

e-journal is a file system inspired by [Bullet Journal](http://bulletjournal.com/) that is meant to **engage** and **motivate** yourself to finish online courses.

> Though it does require a notebook, Bullet Journal® is actually a methodology. It's designed to help you organize your what while you remain aware of your why. The goal of the Bullet Journal is to help its practitioners (bullet journalists) live intentional lives, ones that are productive and meaningful.

![Bullet Journal Example](/images/bullet_journal_example.jpg)
*[Image from Pinterest](https://www.pinterest.es/pin/358458451581999051/)*

### How it works?

You'll make use of gamification techniques that will help you to be awared of the course scope, track your progress, continue your lessons and take value of the different exams and exercises any course could have.

> Note: This system is not intended to work for everyone, but it's worth to give it a try.

You can use an empty notebook, blank papers or your favourite writing software to start with your e-journal setup. You can use this [Google Drive Document](https://drive.google.com/open?id=13XBUZBkzjNjtcU51oIpfsF5HiPdik3Ua) as a boilerplate.

> Remember this guide is only a recommendation, you can adapt it to your own needs and personalize it as you wish.

## Creating the structure

This is the file structure you'll end up with:

```

|__ / COURSE
|____ / LESSONS
|________ / LESSON_1
|____________ / ACTIVITIES
|________________ Activity_1
|________________ Activity_2
|________________ Activity_n
|________________ Results_1
|________________ Results_2
|________________ Results_n
|____________ / EXERCISES
|________________ Exercise_1
|________________ Exercise_2
|________________ Exercise_n
|____________ Index
|____________ Concepts
|____________ Notes
|____________ Resources
|________ / LESSON_2
|________ / LESSON_n
|____ Calendar
|____ Stats
|____ Index

```

Let's dive into the different sections.

### 1. Create the `Index`

We usually tend to start with the first lesson of a course without having the whole perspective. Therefore, this should be the first step of the process of setting up your e-journal. It'll help you to know all the sections, exercises, activities, and in general all the content of the course.

```
Course Name

📅 Calendar
📈 Stats
📖 Lessons
  * 📝 Lesson 1: Lesson Name
  * 📝 Lesson 2: Lesson Name
  ...
  * 📝 Lesson n: Lesson Name
  ...
 
```

If you're using a writing software, you'll have to add links to the different directories where the content will be placed. However, in case you're using a notebook, you'll have to write the page number where each section starts. Don't worry, you don't need to do this at this stage.

### 2. Create the `Stats`

The stats should be the main **source of truth** of your **progress**. In this file, you should track everything you finish or accomplish. But in order to track it, you've to define it first and set all the activities as *unstarted*.

There're three different status: **unstarted**, **started** and **finished**. First of all, decide which symbol are you going to use for each status. It can be anything, even an emoji. They'll be your **stats legend**.

- Each **activity** must have as much "unstarted" symbols as exercises, resources to read or watch. Every time you start or finish an exercise or resource, replace it with the proper symbol.
- Each **lesson** must have as much "unstarted" symbols as activities. Every time you start or finish an activity, replace it with the proper symbol.
- Each **course** must have as much "unstarted" symbols as lessons. Every time you start or finish an lesson, replace it with the proper symbol.

This is very helpful to visualize your progress and encourage yourself to complete all the progress bars.

The following example is a three-lessons course. Each lesson has three activities. Usually, there'll be much more lessons, so you'll probably end up with a couple of sheets.

```
Stats

Legend
* 0: Unstarted
* *: Started
* X: Completed

COURSE X*0

LESSON 1 XXX
ACTIVITY 1 X
ACTIVITY 2 X
ACTIVITY 3 X

LESSON 2 XX*
ACTIVITY 1 X
ACTIVITY 2 X
ACTIVITY 3 X

LESSON 3 000
ACTIVITY 1 0
ACTIVITY 2 0
ACTIVITY 3 0

```

### 3. Create the `Calendar`

Everytime you **finish** an exercise, a lesson, an activity, or if you make any remarkable accomplishment, write it down in the `Calendar` file using the following format:

```
- DD/MM/YYYY

* I've finished lesson 1.
* I've finished the exercise "Exercise Title".

```

You can use this calendar as a TODO list with deadlines, but it's recommended to use it as a **tracker** of accomplishments. **It's more motivating seing tasks done rather than seeing tasks that have to be done.**

### 4. Creating the `Lessons`

If you're using a notebook, you can choose between these options:

1. Leave empty pages between each lesson and add all the index lessons at the beggining of the process, adding the page number of each lesson in the course index.

2. Create each lesson once you've finished the previous one.

The pros of the first option is that it'll help you to have a better perspective of the whole content. However, it could be hard to know in advance how much space you'd need for each one. Sometimes, lessons can have a very different length, or you could need more or less space depending on your previous knowledge. This decission is up to you :)

Each lesson section has its own `Index`, and it works as the course index.

```

Lesson 1: Lesson Name

📝 Activities [optional]
  * Activity Name
  * Results [optional]
* 🧠 Concepts
* ✏️ Exercises
  * Exercise Name
* 📌 Notes
* 🔗 Resources

```

- Activity:
*Not Mandatory*

> **Note:** Activity directories are **optional**. You can track quizzes, tests and other exercises in the `Exercise` file under the `Lesson` directory. The idea of Activities is to help you with tests and exams you can repeat several times, so you can save and track your errors and learn from them.

- Results:
*Not mandatory*

Write down all the attempt results of the activity **chronologically**. If the exercise consist of a test exam, try to add your both answers and the correct / wrong answers too for every attempt.

```

Result

- DD/MM/YYYY
1. Question

Answer

```

### Concepts:
*Mandatory*

Save all the useful concepts you learn in the `Concepts` file. A concept is something very **specific** whose meaning or content you want to **empathise**. It's recommended to write down all the concepts **alphabetically**.

```
Concepts

- Concept 1
Description

- Concept 2
Description

```
### Exercises:
*Not Mandatory*

Use the `Exercises` directory to keep the different exercises. Remember to keep them as **small** and **concise** as possible. This file is optional, only needed if the activity has any exercise or if you want to put in practice a concept you've learned.

### Notes:
*Not mandatory*

Empty space to write random notes. It doesn't follow any structure, feel free to add diagrams, drawings or anything you've the need to express.

### Resources:
*Not mandatory*

In the `Resources` file, keep a list with all the links you've used.
* Optionally, rank them with "points" or "stars" (for example, using `*`) from 1 to 5, where 5 is the maximum positive score you can give to rank a resource.
* Optionally, add a short description of the resource.

```

Resources

- Resource Name: https://examplelink.com/example_1 [*]
- Resource Name: https://examplelink.com/example_1 [* * * * *]
  * Resource Description.
* Resource Name(https://examplelink.com/example_2 [* *]

```

## Conclusions

That's all you need to know how to start using e-journal. If you've any question regarding how to implement this system, or any idea or suggestion you want to share with us, please do it! We'll be wiling to help and collaborate with you.

## Do you want more?

Would you be interested in an **e-journal notebook** or using it as an **app** for your smartphone / tablet / computer? If so, write us to [hello@elearntics.com](hello@elearntics.com)
# Features
- Individual page for assignments, lectures, course material, course schedule
- Auto generated Course schedule Page
- Auto generated course updates section (for each new lectures and assignments) + custom/manual announcements 
- Super lightweight 
- Highly customizable
- Ready to be used in Github Pages

## Change log
- Version 2.0
  - New Schedule page with more efficient use of space.
  - Gregorian calendar is now the default one (English Calendar).
  - Add customization option to home, assignments, lectures, and schedule pages.
  - Add support for themes (so you can modify website's look according to your school's brandings)!.
  - Move navigation menus to yaml which means it is now easier to add new pages.
  - Add more flexibility to lecture's links

# Demo
Checkout for a working demo at [kazemnejad.github.io/jekyll-course-website-template/](https://kazemnejad.github.io/jekyll-course-website-template/). You may also want to see this real-world example at [iust-deep-learning.github.io/972](https://iust-deep-learning.github.io/972/) or [iust-courses.github.io/ai97/](https://iust-courses.github.io/ai97/) (Please note the last two examples are using the older version).

# Some Screenshot
<p float="left">
<img src="https://raw.githubusercontent.com/kazemnejad/jekyll-course-website-template/master/_images/screenshots/screen_home.jpg" width="300">
<img src="https://raw.githubusercontent.com/kazemnejad/jekyll-course-website-template/master/_images/screenshots/screen_schedule.jpg" width="300">
<img src="https://raw.githubusercontent.com/kazemnejad/jekyll-course-website-template/master/_images/screenshots/screen_lecture.jpg" width="300">
</p>

<p float="left">
<img src="https://raw.githubusercontent.com/kazemnejad/jekyll-course-website-template/master/_images/screenshots/screen_assign.jpg" width="300">
<img src="https://raw.githubusercontent.com/kazemnejad/jekyll-course-website-template/master/_images/screenshots/screen_sample_assign.jpg" width="300">
<img src="https://raw.githubusercontent.com/kazemnejad/jekyll-course-website-template/master/_images/screenshots/screen_material.jpg" width="300">
</p>

# Acknowledgement 
This template is heavily based on [svmiller / course-website](https://github.com/svmiller/course-website).


# How to use
1. Install Jekyll ([Installation guide](https://jekyllrb.com/docs/installation/))
3. Install requirements:
   `gem install jekyll-jalali`
4. Watch your website while changing: `jekyll serve`
5. add your content, apply your changes.
6. build! `jekyll build -d path/to/your/output/dir`

# How to edit website
There are 6 types of content you can add to the website, each content category has its own template & its own subdirectory. if you follow the templates, All pages will be generated automatically for you including Announcements, Schedule, and Lectures.

## Lectures
If you want to add a new lecture, please create an empty file with `.md` postfix in `_lectures/` directory. fill it using below template:
```markdown
---
type: lecture
date: 20xx-xx-xxTx:xx:xx+4:30 
title: <Title of this lecture>

# optional
suggested_readings:
    - title: Readings 1
      url: http://example.com  # optional attribute 
    - title: Readings 2
      url: http://example2.com # optional attribute 

# optional
# please use /static_files/presentations directory to store slides
slides: /static_files/presentations/1-Introduction-Fa.pdf

# optional
# please use /static_files/notes directory to store notes
notes: /static_files/notes/notes_01.pdf

# optional
# please use /static_files/notes directory to store notes
thumbnail: /static_files/path/to/image.jpg

# optional
tldr: "What is AI? How does it impact our lives? The current state of the art."
  
# optional
# set it to true if you dont want to this lecture appear in the announcements section
hide_from_announcments: false
---
```

## Announcements
Use `_announcements/` directory to create new Announcement
```markdown
---
date: 20xx-xx-xxTx:xx:xx+4:30
---
<put a short announcement here, you can use all markdown features>
```

## Assignments 
Use `_assignments/` directory to create new Assignment
```markdown
---
type: assignment
date: 20xx-xx-xxTx:xx:xx+4:30
title: <Assignment title (e.x. Assignment #1>

# optinal
pdf: /static_files/assignments/assign_01.pdf

# optinal
solutions: /static_files/assignments/assign_01_solutions.pdf

# optional
attachment: /static_files/assignments/assign_01_attachment.zip

# optional
# set it to true if you don't want to this assignment appear in the announcements section
hide_from_announcments: false
---
```

## Dues & Deadlines
Use `_events/` directory to add new Deadline, use `type: due`
```markdown
---
type: due
date: 20xx-xx-xxTx:xx:xx+4:30
description: <Description of deadline (e.x. 'Assignment #1 due')>

# optional
# set it to true if you don't want to this event appear in the announcements section
hide_from_announcments: false
---
```

## Exams
Use `_events/` directory to add new Exam alert, use `type: exam`
```markdown
---
type: exam
date: 20xx-xx-xxTx:xx:xx+4:30
description: <Description of the exam (e.x. 'The midterm exam')>

# optional
# set it to true if you don't want to this event appear in the announcements section
hide_from_announcments: false
---
```

## Custom Events
Use `_events/` directory to add new Exam alert, use `type: exam`
```markdown
---
type: raw_event
name: <Event name>
date: 20xx-xx-xxTx:xx:xx+4:30
description: <Event description>

# optional
# if you want to hide time in Schedule, set this to true
hide_time: false

# optional
# set it to true if you don't want to this event appear in the announcements section
hide_from_announcments: false
---
<!-- you can create custom content using markdown. this section will be placed in "Course Materials (in schedule section)" -->
## Hello
this is a custom event with `code` 
```


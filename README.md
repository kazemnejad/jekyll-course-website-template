Development strategy
=======================================================

# How to build & contribute
1. clone repository `git clone https://github.com/iust-courses/iust-courses.github.io.git`
2. `cd iust-courses.github.io/developments/ai97`
3. install requirements:
   `gem install jekyll-jalali`
4. add your content, apply your changes.
4. build! `jekyll build -d ../../ai97/`
5. push your changes

# How to edit website
There are 6 types of content you can add to the website, each content category has its own template & its own subdirectory. if you use just use with these categories then All pages will be generated automatically for you including Announcements, Schedule, and Lectures.

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
### Acknowledgement 
This template is heavily based on [svmiller / course-website](https://github.com/svmiller/course-website) works.


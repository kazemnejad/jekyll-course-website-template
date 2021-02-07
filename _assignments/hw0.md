---
type: assignment
date: 2021-02-01T4:00:00-5:00
title: 'Assignment #0 - How to submit assignments?'
thumbnail: /static_files/assignments/hw0/thumbnail.png
due_event:
    type: due
    date: 2021-02-01T23:59:00-5:00
    description: 'Assignment #0 due'
hide_from_announcments: true
---

## How to submit assignments? (in general) 
For each assignment, you will be required to submit two packages unless specified otherwise:  your __code__ and your __webpage__:
### Submit code to Canvas
For every assignment you should create a `main.py` that can be used to run all your code for the assignment, and a `README.md` file that contains all required documentation. Place all source code used to generate your results, as well as any documentation required to use the code, in a folder named `andrewid_code_projX` where X is the hw number. Zip the whole folder and submit the zip to Canvas. Here is an example of your folder structure:
```angular2html
yye2_code_proj1.zip:
yye2_code_proj1/
    main.py
    README.md
    utils.py
    ....
```
### Submit your webpage to the class website
We will use [Andrew File System(AFS)](https://www.cmu.edu/computing/services/comm-collab/collaboration/afs/how-to/index.html) to store and display webpages. Here is a step by step tutorial: 
1. Place your website under folder `andrewid_web_projX` and zip it. Please make sure that your main report page is called `index.html` so browsers open it automatically.
1. Remote Copy. Use WinSCP or your favorite scp/ftp tool to copy all your files to your Andrew home directory `scp andrewid_web_projX.zip username@linux.andrew.cmu.edu:/home/username`, where `username` is your Andrew id.
1. Log in to a linux Andrew machine: `ssh username@linux.andrew.cmu.edu`
1. Get cs credentials: `aklog cs.cmu.edu`. 
     1. A tip for sanity check: type `tokens` to see your afs tokens; after running aklog you should see two lines, one for andrew and one for cs.
1. File Transfer.  Unzip your website and copy the folder to your project directory: `cp -r andrewid_web_projX/ /afs/cs.cmu.edu/academic/class/16726-s21-users/username/projectname/www/`. The folder structure should look like this:
```angular2html
# suppose your are at /afs/cs.cmu.edu/academic/class/16726-s21-users/username/projectname/www/
yye2_web_proj1/
    index.html
    data/...
yye2_web_proj2/
    index.html
``` 
Last step, test your page by visiting: `http://www.cs.cmu.edu/afs/cs.cmu.edu/academic/class/16726-f21-users/username/projectname/www/
`

__FAQs__
- Remember __NOT to use any absolute links__ to images etc, as these will not work online. __Only use relative links.__
-   Do not try using WinSCP or similar to copy directly from your laptop to your class project directory. You don't have the credentials (i.e. you can't run aklog cs.cmu.edu through WinSCP)
- Afs gets unhappy if your quota is full. Run `fs quota` to see the percent used; if it's close to 100 percent, delete things (java and matlab dumps, large tif's...) before trying the copy again.
- Your project directory is linked to your _Andrew_ id; if you use a CS computer (*.cs.cmu.edu), and run into trouble, try the instructions above, using an Andrew computer to hand in your work.
- If you have problems with images not appearing on your page, check that 1) filenames match your html files (e.g. .JPG vs .jpeg). 2) relative path is used from the correct root directory. 
- Please contact TA if there are problems. 
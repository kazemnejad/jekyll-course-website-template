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
yye2_code_proj1/
    main.py
    README.md
    utils.py
    ....
## zip the whold folder to yye2_code_proj1.zip:
```

### Submit your webpage to the class website
We will use [Andrew File System(AFS)](https://www.cmu.edu/computing/services/comm-collab/collaboration/afs/how-to/index.html) to store and display webpages. Here is a step by step tutorial: 
1. Place your website under folder `projX` and zip it. Please make sure that your main report page is called `index.html` so browsers open it automatically. X is the hw number.
1. Remote Copy. Use WinSCP or your favorite scp/ftp tool to copy all your files to your Andrew home directory `scp projX.zip username@linux.andrew.cmu.edu:/home/andrew_id/`.
1. Log in to a Unix Andrew machine: `ssh username@linux.andrew.cmu.edu`
1. File Transfer.  Unzip your website and copy the folder to your project directory: `cp -r projX/ /afs/andrew.cmu.edu/course/16/726/www/projects/andrew_id/projX`.
   The folder structure should look like this:
    ```angular2html
    # suppose you are at /afs/andrew.cmu.edu/course/16/726/www/projects/andrew_id/
    proj1/
        index.html
        data/...
    proj2/
        index.html
        data/...
    ```
1. Publish. The course website needs to be refreshed with your updated files. Do that by going [here](https://www.andrew.cmu.edu/server/publish.html), choosing web pages for a course, and inputing 16-726.
1. Last step, test your page by visiting: `http://www.andrew.cmu.edu/course/16-726/projects/andrew_id/projX/`.
`

__FAQs__
- Remember __NOT to use any absolute links__ to images etc, as these will not work online. __Only use relative links.__\
- Note that 16, 726 is connected by `-` in URL while your folder is `16/726/`     
-   Do not try using WinSCP or similar to copy directly from your laptop to your class project directory as you don't have the credentials.
- Afs gets unhappy if your quota is full. Run `fs quota` to see the percent used; if it's close to 100 percent, delete things (java and matlab dumps, large tif's...) before trying the copy again.
- Your project directory is linked to your _Andrew_ id; if you use a CS computer (*.cs.cmu.edu), and run into trouble, try the instructions above, using an Andrew computer to hand in your work.
- If you have problems with images not appearing on your page, check that 1) filenames match your html files (e.g. .JPG vs .jpeg). 2) relative path is used from the correct root directory. 
- Please contact TA if there are problems. 

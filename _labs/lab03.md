---
layout: lab
title: "Lab 03"
date: 2025-07-09
---
# Goal

In today's Lab session, we will:

- Continue working on Github collaboration.
- Clean the survery responses.
- Design the group website.

# I. Github Collaboration
- Go to <https://github.com/wonjun-seo/cosmos-data-analysis>.
- Follow the instructions in **Git Exercise**.

# II. Cleaning the Survey Responses
1. You can export the responses from your Google From as a CSV file.
2. **One person** from each group uploads the CSV file to `data/raw` directory in the group's data analysis Github repository (`main` branch).
3. Each member opens VS Code and open your group's data analysis directory.
4. **Pull** the `main` branch.
5. Each member creates a notebook named `data_cleaning_yourname.ipynb` inside the `notebooks` folder and works on cleaning the data individually. **Do not use Git during this step** (no commit or push)
6. After individual work is done, choose **one member's computer** to create the final version:
  - Create `data_cleaning.ipynb` in the `notebooks` folder.
  - Discuss and finalize the notebook together.
  - Save the cleaned dataset in the `data/cleaned` folder.
  - Create a new branch `cleaning`
  - Stage and commit `data_cleaning.ipynb` and the cleaned CSV file. (**Do not stage `data_cleaning_yourname.ipynb` file**)
  - Push the branch and create a pull request.
7. Other members review the pull request.
8. Once approved, merge the branch and each member will pull the `main` branch so that everyone has the updated files.

After pooling, compare `data_cleaning.ipynb` with your own `data_cleaning_yourname.ipynb` to see how your approach aligns with the group version.

# III. Design the Group Website
Although it's not the usual practice, for simplicity we will use the main branch exclusively to maintain your group website.
**Important**: To avoid conflicts, make sure only **one person edits and pushes changes at a time**.

### Update `README.md` file!

### Update the Home Profile Photo
  1. Upload a new photo to the `static` folder.
  2. In `hugo.yaml` file, update the `params: imageUrl` field to point to the new photo.

### Change the Website Title and Home Description
  1. Open `hugo.yaml` file.
  2. Modify the following fields:
     - `title`
     - `profileMode: title`
     - `profileMode: subtitle`
 
### Add a New Tab to Your Website:
  1. In `hugo.yaml`, add a new item to the `menu: main` field.
  2. In the `content` folder, create a new folder with an `_index.md` file inside. The folder name should match with the url in the `menu:main`.

### Make It Yours!
This website belongs to your group. Feel free to customize it!
Here are some ideas for content you can add:

- **Journal**: Write daily reflections or logs.
- **Activity**: Share night activities or field trip stories.
- **Photos**: Upload and display group photos.

Discuss with your team how you want to organize your website! If you plan to include a journal section, we recommend taking turns to write entries each day so that everyone contributes and the content stays up to date.

### Tips
- If you want to include a table in your Markdown, I highly recommend you use [this link](https://www.tablesgenerator.com/markdown_tables). 

- If you want to create a Markdown table from Python, follow these steps:
  1. Open your VS code.
  2. Open a new terminal.
  3. On the terminal, activate `cosmos` environment: `conda cosmos activate`.
  4. On the terminal, type `conda install tabulate` and proceed installation. (After installation, you don't have to repeat this anymore. Start from v.)
  5. On the `ipynb` file, create a data frame that you want to make it to a Markdown table. Let's say its variable name is `df`.
  6. On the `ipynb` file, run `print(df.to_markdown())`. Change `df` to your data frame variable.
  7. Use the printed output.

 - More tips to come!

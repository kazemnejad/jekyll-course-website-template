---
layout: lab
title: "Lab 04: Workflow and Plotly"
date: 2025-07-10
---
# Goal

In today's Lab session, we will:

- Discuss Git workflows for data analysis project.
- Create an interactive plot via [Plotly](https://plotly.com) and embed the plot to the website.

# I. Git workflows
So far, we've explored how to manage repositories using Git. Today, each group will design a custom Git workflow for their project.

There is **one important rule: You are NOT allowed to push directly to the main branch**.
Instead, any changes to the main branch must go through a separate branch and a pull request.

With this rule in mind—and using the workflow pipeline we discussed in the lecture—discuss the following questions with your group:

- When to create a new branch
- What types of work should be done within that branch
- When to merge the branch back into the main workflow

After your internal group discussion, each group will present their strategy to the class. Other groups will then provide feedback and suggestions.

Through this activity, each group is expected to gain a clearer understanding of the overall workflow of the project.

# 2. Plotly
From the mini project, each group has their own dataset containing county-wise income and AQI. With this dataset, we will create an interactive plot that can be embedded to the group website.
In this example, we use [Choropleth Maps](https://plotly.com/python/choropleth-maps/) in the package `plotly`.
Please find <a href ="https://github.com/wonjun-seo/cosmos/blob/master/static_files/labs/4/income_aqi.ipynb">this file</a>.

## Package installation
In your current `cosmos` environment, all the packages required for the lectures are pre-installed. However, you may need additional packages along your project, like `addfips` in this example.
If so, please search the package in [Conda-forge website](https://anaconda.org/conda-forge/) (If you can't find a package here, you can use `pip`. If you don't know how to use `pip`, please let me know).
There should be a command for installation. Please run the command on your terminal (either VS code terminal or system terminal) after activating `cosmos` environment.

**Example**
```zsh
# On terminal
conda activate cosmos
conda install conda-forge::addfips
```

After installation, you can load the package by the command `import`
```python
# On ipynb
import addfips
```

## Embedding HTML to website
1. Go to the website repository on Github.
2. Locate your file to `static/plotly/`.
3. Go to the markdown file you want to include the plot.
4. Type `<iframe src="/plotly/YOUR_FIGURE_NAME.html" width="100%" height="400px" style="border:none;"></iframe>`.
5. Commit changes.

## Zoom in?
If your data only contains counties in California, then it is not a good idea to show the whole map of the U.S. Check out <a href ="https://github.com/wonjun-seo/cosmos/blob/master/static_files/labs/4/income_aqi_BayArea.ipynb">this file</a>.


## Some notes
- The plot may not display well on mobile devices.
- If the HTML file is larger than 25MB, you cannot upload it via web browser. Please reach out to me.

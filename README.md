# Chaoss_19_Microtasks

## General Information
This is the repository containing the microtask submissions for CHAOSS GSOC 2019. The idea I want to work on is:
**[Idea #2: Implementing CHAOSS metrics with perceval](https://github.com/chaoss/wg-gmd/issues/81)**


## My contributions and participation in CHAOSS
I started contributing to CHAOSS halfway through January, 2019 and have made several contributions.  **To avoid crowding out important information** in the README, I've mentioned all my contributions in [contributions.md](./contributions.md).

 
  
## Microtasks
Click on the Binder badge to run the notebooks in this repo in real time  
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Polaris000/Chaoss_19_Microtasks/master) 

### Important Information
- **Project used: atom**

- **Data**  
Specifically, the repositories used were:   
    - [language-java](https://github.com/atom/language-java)  
    - [teletype](https://github.com/atom/teletype)    

- The data was fetched at: 
    - `2019-03-30 18:42:51` (Indian Standard Time)     
    - `2019-03-30 13:12:51` (UTC)  

### Some numbers (from the analysis in this notebook): 
**The total number of commits is**:   
    language-java: 336  
    teletype: 1102  
      
**The total number of issues is**:   
    language-java: 96  
    teletype: 300  
      
**The total number of pull-requests is**:       
    language-java: 99  
    teletype: 130  
  
**- Files:**    
    - 'atom.json' -- the data collected by perceval  
    - 'atom.csv' -- the result of writing data to csv for microtask 1 and 2  
    - 'atom_last_3_months.csv' -- csv output of microtask 4 and 5

### [Microtask0](./microtask0)  
- The aim of this microtask is to understand the basics of perceval.    
- Please click on the microtask heading to proceed to the microtask directory  

### [Microtask1](./microtask1)   
- The aim of this microtask is to analyse changes on a quarterly basis without using pandas.  
- Please click on the microtask heading to proceed to the microtask directory    

### [Microtask2](./microtask2)  
- The aim of this microtask is to analyse changes on a quarterly basis using pandas.  
- Please click on the microtask heading to proceed to the microtask directory  

### [Microtask4](./microtask4)  
- The aim of this microtask is to analyse changes for all repositories for the last 3 months using pure python. 
- The repositories are to be sorted based on the total number of items (commits, issues and pull requests) created in the last 3 months.
- Please click on the microtask heading to proceed to the microtask directory 

### [Microtask5](./microtask5)  
- The aim of this microtask is to analyse changes for all repositories for the last 3 months using pandas. 
- The repositories are to be sorted based on the total number of items (commits, issues and pull requests) created in the last 3 months.
- Please click on the microtask heading to proceed to the microtask directory.   

### [Microtask6](./microtask6)  
- The aim of this microtask is to perform an analysis of my choice using the data fetched by perceval. 
- I chose to perform an analysis regarding the issues from the data: number of open and closed issues, age of open issues etc.
- Please click on the microtask heading to proceed to the microtask directory.   

#### Optional Microtasks
### Microtask7  
- The aim of this microtask is to contribute to any grimoirelab tools.  
- Please check [contributions.md](./contributions.md) for all of my contributions.
  
### Microtask8  
- The aim of this microtask is to contribute to wg-gmd.    
- Please check the [wg-gmd section of contributions.md](./contributions.md#wg-gmd) for my contributions to wg-gmd. 
  
## About me  
- My name is **Aniruddha Karajgi**. I am in my **second year studying Bachelor of Engineering (B.E.) Computer Science** at  
Birla Institute of Technology and Science, Pilani, located in the state of Rajasthan, India. I was born in Mumbai, though my current place of residence is Hyderabad, India. 
- I have been programming in python for two years now. 
- At college, I am a **member of two technical clubs**, where I **work on backend development using Django** and **machine learning** (with python). I have **conducted a workshop** on the same. 
- During the summer after my freshman year at college, I **interned at CereLabs**, a startup working on deep learning applications, where I helped implement deep learning models (GANS), mainly by making data ready for the models and researching the effectiveness of those models. I also worked on cleaning and understanding open street map data, which was to be used for parsing addresses with NLP. I extensively used numpy, pandas and matplotlib during the internship.

## Using this repository
- Run `git clone https://github.com/Polaris000/Chaoss_19_Microtasks.git`  
- Install perceval  
    `pip3 install perceval`
- Navigate to the microtask of your interest, say, microtask0.   
    `cd microtask0`
- Start the `microtask0.ipynb` notebook with jupyter
- Set the variables to your preference (if you want to run it on some other data) in code cell #2

```python
github_url = "https://github.com/"  # the github url domain: used for generating repo_urls     
owner = "atom"   
repos_used = ["language-java", "teletype"]   
repo_urls = [github_url + owner + "/" + repo_used for repo_used in repos_used]    
auth_token = "" # Please enter your github token here   
file_name = owner + ".json"   # file to which perceval stores data (a ../ is   automatically added)  
```

- Next, uncomment the script in code cell #3 and run it. Rememeber that if you have `owner = "atom"` in the previous cell and you run the commented cell, the current data fetched by perceval will be overwritten.
- Of course, there is no such problem if you intend to use this script for a different owner. 
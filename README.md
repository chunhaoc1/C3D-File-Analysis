# C3D-File-Analysis
This program analyze C3D file in several method for Caren System research.



## Processing and Visualizing C3D Files Using Google Colab


## Authors:

**Xin Shen** - Master of Information Technology, University of Melbourne

xsshen2@student.unimelb.edu.au 

**Chun-Hao Chen** - Master of Information Systems, University of Melbourne

chunhaoc1@student.unimelb.edu.au 

**Songxiang Tang** - Master of Information Systems, University of Melbourne

songxiangt@student.unimelb.edu.au 

### Introduction

Motion capture data has always been an active area of research, with significant technological advancements over recent decades. However, researchers will still encounter barriers to collaborative work and remote access, primarily due to the limitations imposed by specific devices and software environments. This paper leverages cloud platforms, such as Google Colab and Google Drive, to establish an environment that facilitates remote analysis of C3D files.

This project aims to build upon the previous work of A User-Friendly Approach Using Google Cloab and Open-Source Python Packages, demonstrating that C3D files can be visualized and interpreted in Colab.

Previous work can be found at  [GitHub Page](https://github.com/etoshey/colabC3D).

### Our current goals are twofold:

Leverage publicly available C3D files.
Provide next steps for data analysis, including but not limited to kinematic and kinetic data such as marker positions, ground reaction forces (GRFs), gait events, and joint motion.
In this notebook, we present a framework that enables users with minimal or no data analysis or coding experience to upload a C3D file and perform data processing, visualization, and statistical analysis using Python libraries.

### Methodology

- Step1: Installing and Configuring Python Packages

Google Colab comes pre-installed with commonly used Python packages for data analysis, making them readily accessible to all users. The necessary packages for this notebook will be automatically loaded. Additionally, this notebook utilizes two external packages specifically designed to visualise and analyse C3D files: pyc3dtools and pygwalker. The ipywidgets package is also employed to create interactive widgets. These packages require the user to install them by running the installation code every time a new session starts.


- Step 2: Uploading and Import C3D File

This notebook provides two options for uploading C3D files: directly from Google Drive or manually upload from a local device. Google Colab offers seamless access to Google Drive, making direct import significantly faster than manual upload. However, users must grant this notebook permission to access their Google Drive during the active session. A manual upload portal is available for users who prefer not to use Google Drive or do not have their files stored there, allowing files to be selected and uploaded from the local directory.

There is another alternative of importing files from Google Drive without permitting access to the notebook; it only requires the user to set the file accessibility to ‘anyone with the link’. The steps are more complicated, and tutorials can be added to the scaffold in the future.


- Step 3: Viewing Datalog

Data processed in this notebook are stored in the Datalog section. Users can view a summary of all entries stored in the Datalog, enabling them to understand and check for errors.


- Step 4: Data Visualising

The notebook leverages Python's data visualization packages to plot and display time series data, such as Ground Reaction Force, Moment, and Acceleration. For datasets with many records within a short timeframe, users can zoom in and focus on a specific time window.


- Step 5: Event detection:

The notebook also includes a feature for detecting specific events, such as toe-off and heel strikes for both legs. A table summarizing the gait cycle (right/left foot), event (toe-off/heel-strike), and the corresponding time points will be displayed for the user. This data can also be exported as a CSV file. The CSV file will be temporarily stored in a cloud directory and must be manually downloaded to the local device; otherwise, it will be deleted after the session ends.

### Conclusion
The current version of this notebook provides fundamental analysis capabilities for C3D files. It is actively being developed, with more advanced features planned for future updates. At this stage, the notebook offers a reproducible data analysis pipeline that can be executed automatically and remotely. This tool enables researchers to perform their work on any computing device with internet access. Additionally, teams can collaborate effectively by sharing a copy of this notebook with colleagues. All necessary code for generating outputs is fully implemented, allowing even users with limited Python experience to reproduce the results. The primary goal of this project is to create a remotely accessible, collaborative environment with an open and reproducible coding framework.

### Future Work
The current code scaffold leverages pre-downloaded C3D files and performs data analysis. In the future, we aim to incorporate motion capture modules that can extract marker data from video or real-time filmed human motion, deriving a data file. The data file can be either C3D or in other format. The notebook will be adjusted so it can adapt data analysis to either file format. All processes will be accomplished using Google Clolab.


- [x] Data analysis notebook : Finding modules with Motion fields.
- [ ] Perturbation : Brainstorm ideas and elaborate on them to create a detailed profile.
      

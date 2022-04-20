# Starbucks Capstone Challenge

# Table of Contents
1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python.  The code should run with no issues using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

For this project, I was interested in using Starbucks datasets to study which offers have the best success rate and if there's a way to predict them. To answer this question, I've focused my research to answer the questions below:

1. What's the average age of Starbuck's customers?
2. What are the most successful offers?
3. What are the most successful offers for each age?
4. What are the most successful offers for each gender?
5. Can a Machine Learning model predict the customer behavior for a promotional offer?

## File Descriptions <a name="files"></a>

There is one notebook available (the other is localized in chinese) here to showcase work related to the above questions. The notebook is exploratory in searching through the data pertaining to the questions showcased by the notebook title. Markdown cells were used to assist in walking through the thought process for individual steps. 

The **data** folder contains the Datasets about the (customers) **profiles**, **transcripts**, and **portfolio** (about the offers) in **JSON** format.

- portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
- profile.json - demographic data for each customer
- transcript.json - records for transactions, offers received, offers viewed, and offers completed

Below is the schema and explanation of each variable in the files:

### portfolio.json

- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)

### profile.json

- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

### transcript.json

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record

## Results<a name="results"></a>

The main findings of the code can be found at the post available [here](https://medium.com/@martini.f/starbucks-capstone-challange-977811f882).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to Starbucks for the data. The Licensing for the data and other descriptive information was provided by **Udacity** as part of the course material, but feel free to use the code here as you would like!

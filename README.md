# Covid Case Counts and Mandates
Project for CSE 583: COVID, Mandates, etc.
[![Build Status](https://travis-ci.com/gabewiss/covid.svg?branch=main)](https://travis-ci.com/gabewiss/covid)
[![Coverage Status](https://coveralls.io/repos/github/gabewiss/covid/badge.svg?branch=main)](https://coveralls.io/github/gabewiss/covid?branch=main)


### Introduction

This is a softeware that takes the latest Covid-19 case counts data updated by _Center for Disease Control(CDC)_ and shows it with the Covid-19 related Mandates in the United States.
With this tool, we can see how effective a certain mandate is in terms of increased case counts.

Includes
1. A choropleth of USA to see the overview of monthly positive Covid-19 counts of each state.

2. Line graphs of states to compare (cases/100K).

### Team Members

* Zhaowen Guo
* Jee Hoon Han
* Oliver Li
* Gabriel Wisswaesser

### Example
* Choropleth of the United States

<img src="https://github.com/gabewiss/covid/blob/main/docs/example_figure/choropleth_example.png" width=85% height=85%>

<br>
<br>

* Line graphs of states with when certain mandates were implemented
<img src="https://github.com/gabewiss/covid/blob/main/docs/example_figure/linegraph_example.png" width=85% height=85%>


### Software dependencies
#### Python Packages
* Dash
* Dash_core_components
* Dash_html_components
* Dash.dependencies
* Pandas
* Plotly.express
* Plotly.graph_objects

### Installation
Instruction to run the softeware locally   

1. Clone the git repo: `git clone https://github.com/gabewiss/covid.git`
2. Go into `src` directory in the terminal
3. Run `covid.py` file
`python covid.py`
4. Visit http://127.0.0.1:8050/ in your web browser


### Directory Summary
We have _docs_ directory, where related articles, component design, and use cases can be located.

Then, we have _covid_ directory, where data, examples, and test codes can be located

### Directory Structure
```
covid
    ├── LICENSE
    ├── README.md
    ├── covid
    │   ├── __init__.py
    │   ├── data
    │   │   └── states_population.csv
    │   ├── environment.yml
    │   ├── examples
    │   │   └── example of choropleth and line graph.ipynb
    │   ├── src
    │   │   ├── __init__.py
    │   │   ├── count_processing.py
    │   │   ├── covid.py
    │   │   ├── data_check.py
    │   │   └── mandate_processing.py
    │   └── tests
    │       ├── __init__.py
    │       ├── test_count.py
    │       ├── test_covid.py
    │       └── test_mandate.py
    ├── docs
    │   ├── CSE583_ComponentDiagram.pdf
    │   ├── CSE583_UseCaseDiagram.pdf
    │   ├── CSE583_technical_review.pdf
    │   ├── SoftwareDesign.pdf
    │   ├── CSE583 presentation covid-mandate.mp4.zip
    │   ├── final_presentation.mp4
    │   ├── articles
    │   │   ├── mandate_face_covering.pdf
    │   │   └── mandate_social_distancing.pdf
    │   └── example_figure
    │       ├── choropleth_example.png
    │       └── linegraph_example.png
    ├── environment.yml
    └── setup.py
```

### Data Source
#### Covid-19 Case Counts
  - Covid-19 data repository held by [CDC](https://data.cdc.gov/Case-Surveillance/United-States-COVID-19-Cases-and-Deaths-by-State-o/9mfq-cb36)

#### Covid-19 State and County Policy
  - State and county orders held by [HealthData.gov](https://healthdata.gov/node/3281076/)

### Limitation
Although the softeware is designed to continuously update the data from the data source, the repository may not be continuously maintained beyond December 2020.
The population data is from December 2020, before the new census data.
The software is coded for the data of the year 2020. Once it's 2021, it might not properly represent the data.

# Analysis of Horizon 2020 energy projects directed to communities

## Subject of research:
The subject of the study is information on completed projects of the EC Horizon 2020 program (H2020), collected on the CORDIS service. 
The project archive is available in CSV and XLSX format at: https://data.europa.eu/data/datasets/cordish2020projects

The interest is in energy projects aimed at implementation in communities in the following two areas:
Carbon Zero - is a community activity that results in minimal (ideally zero) greenhouse gas emissions.
Positive Energy - Local energy generation exceeds the energy costs of the community

## Goals of the research:
1.	One of the goals of the research is to generalize the methods, approaches, solutions, etc. addressed to achieve the goals of Carbon Zero and Positive Energy. 
2.	To classify the resulting list of methods (in the form of a hierarchy) and evaluated numerically.
3.	Demonstrate application of data analysis and nature language processing method to the problem.

## The methodology of this study
The database contains information on 35,326 projects. Each record (one project) is divided into 19 fields. Of these fields, the following 7 fields will be of primary interest: status, title, startDate, endDate, totalCost, topics, objective.
1.	First, we try to weed out unfulfilled projects in the status field.
2.	We are trying to understand the possibility of filtering the necessary or vice versa - unnecessary projects in the field of topics.
3.	Using the objective field, we build a list of terms (1-, 2-, 3- and possibly 4-grams) and their frequency distribution (normal distribution and TF-IDF distribution). Here it´s important to expand the list of stop words
4.	The list of terms is going to be classified (as a two level categories). But here it is necessary to reasonably limit the number of categories of level 2. At this stage, it would be "manual" creative work. In the meantime, we get this kind of plate:

| Term |	Frequency |	Inverse document frequency|	Category 1 <br /> (upper layer)	| Category 2 <br /> (second layer) |
| :----: | :--------------------: | :------------------: | :--------------------------------: | :-------------------------------: |			

## Visualisation 
The version of visualisation tool with limited functionality available in ../notebook/03_simplified_dashboard.ipynb file
![newplot2](https://github.com/ohusiev/enercomm_h2020_categorisation/blob/1c8b19f40546a1e7d0ec7faf77e6c0dd09c3d25f/docs/newplot1.png)

---

This is the GitHub repository of the code developed for the analyses in:

O. Husiev, O. Ukar Arrien, and M. Enciso-Santocildes, ‘What does Horizon 2020 contribute to? Analysing and visualising the community practices of Europe’s largest research and innovation programme’, Energy Research & Social Science, vol. 95, p. 102879, Jan. 2023, [doi: 10.1016/j.erss.2022.102879](https://doi.org/10.1016/j.erss.2022.102879).

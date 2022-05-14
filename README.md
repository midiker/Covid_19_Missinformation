# Covid_19_Missinformation
Navanti Group
COVID-19 Sentiment Analysis & Visualization


## Executive Summary

For our Practicum Project at The George Washington University, we were sponsored by our client, Navanti Group, to produce a real-time sentiment analysis and tracking dashboard, which will aggregate and display COVID-19 misinformation transfer into the “mainstream”. To carry out the analysis, we elected to use social media posts from the Twitter and Gettr platforms as a proxy for public opinion on the subject. Throughout the course of the semester, we met regularly with our client to refine the project scope, provide updates on the progress of the project, and incorporate feedback on our efforts. The final dashboard product is a result of those efforts and the analysis therein, which provides actionable insights and recommendations based on the reality that COVID-19 misinformation is in fact having an impact on mainstream media content.
	To conduct our analysis, we first developed a scope for the information to collect. Overall, content remained limited to users located within the United States. First, definitions were drafted and approved by Navanti to compartmentalize the types of information to be harvested. Second, specific user accounts were researched and selected to represent the primary definition categories we had drafted. Third, ancillary requirements were developed to eliminate redundancies in the information, such as controlling for employer accounts where a user worked, which could lead to duplication of content. The project scope also required a fair representation of accounts across the political spectrum, along with a category to designate specific politicians currently holding political office.
	Following completion of the dashboard, which includes five unique visualizations and automated interval-based updating, preliminary results show a marked association between mainstream sources and “fringe-like” post content. By viewing the K-means algorithm results in particular, one finds a clear clustering of all users along the upper regions of the y-axis, which represents a low “mainstream-like”, high “fringe-like” volume of content. While the project scope is limited, these findings encourage further analysis and a broader look into both the causal factors of these phenomena and mitigation strategies for COVID-19 misinformation. In addition, the project authors recommend further extrapolation of the methodology to analyze misinformation on social media as a broad phenomenon.


## Problem Statement
COVID-19 misinformation has spread widely in the mainstream public sphere. Navanti seeks to monitor “fringe” COVID-19 misinformation transformation into “mainstream” assertions across mainstream and non-mainstream sources. This monitoring will assess the inflection point of fringe information absorption into the mainstream. Navanti desires to undertake an intellectual excercise through the use of a living dashboard with COVID-19 sentiment analysis. This will facilitate the monitoring of key misinformation life cycles across mainstream and non-mainstream sources, with scientific sources serving as the anchoring “truth” by which relative levels of misinformation can be measured.

## Hypothesis
The prevalence of COVID-19 misinformation is influencing mainstream public opinion in unprecedented ways. Fringe information that might previously have been rejected on scientific grounds is finding acceptance among large populations of people, and even among subject matter experts. To prove or disprove this hypothesis, we conduct analysis of COVID-19 themes using ongoing data streams. We then test our hypothesis through juxtaposition of fringe and mainstream media sources using scientific sources as a baseline. Finally, aim to view the analytics results through a data visualization pipeline, draw conclusions, and make actionable recommendations.

## Scope & Methodology
Conceptual Definitions
Misinformation - Information largely unsupported by or fundamentally contradicting facts derived from scientific research or empirical evidence.
Mainstream sources - institutional and news organizations that shape broad public opinion. These sources employ reasonable amounts of editorializing and opinion catering.
Fringe sources - Persons or news outlets primarily sharing information derived from personal opinion not grounded in fact. These sources regularly employ ideological rhetoric or persuasion aimed at converting or entrenching individuals’ personally held beliefs.
Scientific sources - United States federal government agencies with national public health as their primary mission. They strive to provide the most accurate information derived from empirical studies that employ the scientific method (i.e. the Centers for Disease Control and the National Institutes of Health).


## Media Segmentation
Defined source* sectors (see Appendix B for list of monitored accounts):
Scientific (anchor)
Mainstream
Fringe
Politician

## Information Bounding
Flag inherently political sources (i.e. holding political office)
Exclude redundancies between persons and their associated organizations/affiliates to control for magnification effects
Evaluate verified and unverified accounts to establish user scope
Media source definitions determine categorization
Overtly political sources are prioritized for fringe content harvesting
Exclusion of  policymakers without a prominent, established following
Flexibility to add source accounts over time, based on relevance and source definitions (“living” source list)

## Twitter & Gettr Post Data
Twitter: April 2022 onward
Gettr: May 2021 onward
Post attributes: Username, Date of Post/Tweet, Post/Tweet raw text

## Data Analytics
Tools & Methods
Twitter (Advanced Tier API) derived custom data extracts
Gettr open source API (GitHub) derived custom data extracts
AWS EC2 cloud computing for analytic processing power
SQLite Database framework for data storage
Data filtering & wrangling (Python)
Browser-hosted dashboard visualization server (Bokeh module)
Automated API querying capability for data ingest at regular intervals (via schedule module)




## Initial Tracked Themes
Covid-19
Words used for Covid-19 theme: covid, c@vid, pandemic, virus, disease, omicron, delta, SARS-CoV-2, variant, outbreak
Vaccines
Words used for Vaccines theme: vaccin, vax, jab, mrna, pfizer, biontech, moderna, J&J, Johnson & Johnson
Mandates
Words used for Mandates theme: mandate, mask mandate, vaccine mandate, vaccine card, passport, lockdown, quarantine, restriction
Alternative Treatments
Words used for Alternative treatment theme: vitamin, zinc, ivermectin
Health Organizations
Words used for Health Organizations theme: CDC, NIH, FDA, WHO
Conspiracies  
Words used for Conspiracies theme: bioweapon, lab
Origin
Words used for Origin theme: Wuhan

## Algorithms
K-means Clustering
Unsupervised machine learning outlier detection and contextualization of user posts
Sentiment Analysis 
Pre-defined algorithm to classify user posts by positive, negative, or neutral overall sentiment



Dashboard & Visualizations

db.png

Our dashboard consists of 5 visualizations, providing on-demand analysis of harvested social media content from Twitter and Gettr. Users are able to select from 5 distinct tabs, which segment the data by source type. There are also filters available to target specific themes in the data.


<p align="center"><img width=100% src="https://github.com/jishubasak/Dataxi-Science/blob/master/catalog/intro.png"></p>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![PyPI pyversions](https://img.shields.io/pypi/pyversions/ansicolortags.svg)](https://pypi.python.org/pypi/ansicolortags/)
![Build Status](https://travis-ci.org/anfederico/Clairvoyant.svg?branch=master)
![Dependencies](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://gitHub.com/jishubasak/eCResearch)
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://github.com/jishubasak)
[![Website shields.io](https://img.shields.io/website-up-down-green-red/http/shields.io.svg)](http://ecfullfill.com/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)


To access the full project either download and view Dataxi Science.html or access the jupyter notebook inside the Notebook folder 

<h1><font color='#FDB515'>Executive Summary</font></h1>

<div align='justify'>There are roughly 200 million taxi rides in New York City each year. Exploiting an understanding of taxi supply and demand could increase the efficiency of the city’s taxi system. In the New York city, people use taxi, specifically 'Yellow Taxi' in a frequency much higher than any other cities of US. Instead of booking a taxi by phone one day ahead of time, New York taxi drivers pick up passengers on street. The ability to predict taxi ridership could present valuable insights to city planners and taxi dispatchers in answering questions such as how to position cabs where they are most needed, how many taxis to dispatch, and how ridership varies over time.This mini project focuses on predicting the number of yellow taxi pickups given a one-hour time window and a location within New York City.
<br>
<br>
<ul>
    <li>After Data Analysis, I found out that Manhattan(Borough), JFK Airport and LaGuardia Airport are the most demanding place when it comes to both, Passenger Count and Total amount.</li>
    <li> Evenings are the busiest and mornings, specially around 5AM are silent when it comes to demand.</li>
    <li> Gradient Boosting Regressor out performs in predicting Passenger Demand and Total Gross revenue demand based on Date/Time and Pickup location.</li>
</div>
 
<h1><font color='#FDB515'>A. Introduction</font></h1>

<div align='justify'> 
    In New York City, taxicabs come in two varieties: yellow and green; they are widely recognizable symbols of the city. Taxis painted yellow (medallion taxis) are able to pick up passengers anywhere in the five boroughs.Taxicabs are operated by private companies and licensed by the New York City Taxi and Limousine Commission (TLC)
<br><br>
    The New York City Taxi and Limousine Commission (TLC), created in 1971, is the agency responsible for licensing and regulating New York City's Medallion (Yellow) taxi cabs,
    for-hire vehicles (community-based liveries, black cars and luxury limousines), commuter vans, and paratransit vehicles. The Commission's Board consists of nine members,
    eight of whom are unsalaried Commissioners. The salaried Chair/ Commissioner presides over regularly scheduled public commission meetings and is the head of the agency,
    which maintains a staff of approximately 600 TLC employees.
    Over 200,000 TLC licensees complete approximately 1,000,000 trips each day. To operate for hire, drivers must first undergo a background check, have a safe driving record,
    and complete 24 hours of driver training. TLC-licensed vehicles are inspected for safety and emissions at TLC's Woodside Inspection Facility.
</div>

<h1><font color='#FDB515'>B. Problem Statement</font></h1>

<div align='justify'> There are roughly 200 million taxi rides in New York City each year. Exploiting an understanding of taxi supply and demand could increase the efficiency of the city's taxi system. This mini project focuses on predicting the passenger demand and total gross revenue demand given a the given time (one-hour time window) and a location within New York City. In general this project aims to answer how can Data Science address the pitfall in demand of Medallion Taxi in New York City.
</div>

<h1><font color='#FDB515'>C. Methodology</font></h1>

The high-level workflow for NYC Yellow Taxi Demand prediction and analysis is as follows:

1. Data Description, Extraction and Storage
2. Data Cleaning and Feature Engineering
4. Data Analysis
5. Feature Engineering
6. Modelling


<h1><font color='#FDB515'>D. Conclusion and Future Work</font></h1>

Overall, our models for predicting Taxi Demand(Passenger Count) and Gross Revenue in New York City performed well. The Gradient Boosting regression model performed best, likely due to its unique ability to capture complex feature dependencies. The decision tree regression model performed fairly better than Random Forest and Simple Regression. Our results and error analysis for the most part supported our intuitions about the usefulness of our feature. 

We previously discussed about the historic demand of Medallion Taxis based on Time, Pickup Zones, Gross Revenue and types of trips. Knowing that there is a declination of Taxicabs in NYC in recent years due to Ride Hailing apps, the Medallion Taxi car owners and agencies have to rethink of different strategies to maintain their portion of market size. One of the most important aspect to strategy development is to analyze the demand and make data driven decisions in terms of determining where to position taxicabs, studying patterns in ridership, determining when to position the taxi cabs and finally the optimal days of working to maximize the capital.

Being said that, this research has few limitations with can be nullified if following robust areas are explored:
- Neural network regression: We may be able to achieve good results using a neural network regression, since neural networks can automatically tune and model feature interactions. Instead of manually determining which features to combine in order to capture feature interactions, we could let the learning algorithm perform this task. 
- K-means Clustering: In order to find non-obvious patterns across data points, we could use unsupervised learning to cluster our training set. The clustering algorithm could use features such as the number of bars and restaurants in a given zone, or distance to the nearest subway station. The cluster in which each data point falls could then serve as an additional feature for our regression models, thereby exploiting similar characteristics between different zones for learning.
- Adding additional features such as Weather Data, Rainfall Data, Amenities data(such as number of Restaurants, Bars, Hotels) which can be accessed through Open Street Maps in python should be taken into the consideration while training the models. Taxi companies could benefit from this in many ways such as, merging with few outlets, special discounts could be offered to customers and so on.
- The data can be augmented. I only considered 2017 dataset. However, other years can also be included(Historic data is available starting from 2009)

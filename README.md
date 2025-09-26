# Data Visualization Project: 2024 Boston Marathon Finisher Data Analysis

## Data

The data I propose to visualize for my project is the 2024 Boston Marathon finisher's data, along with weather data in all zip codes of the finishers. A few things that the finishers data includes is age, gender, finishing time, 1st half split, 2nd half split, and percent change. The weather data consists of zip code, high temp, low temp, and average temp.


## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * Which geographic regions produce the most consistent performers?
 * Does the difference between training weather and race day weather effect performance?
 * Which age groups produce the most consistent runners?
 * How can we differentiate between geographic regions or age of runners causing 1st and 2nd half differences?
 * How can we visually show geographic regions of runners along with the time data being analyzed?
 * How can we visualize as much data as we can in one interactive, user-friendly display?

## Sketches

These first three sketches show various ideas of different ways to analyze and visualize the Boston Marathon data. The top sketch is ideally the starting point for the final product of this project, an interactive map of the US showing different information about the runners from the different geographic regions. One idea, shown in this sketch, is the percent change from 1st half split to 2nd half split of each runner, grouped and labled by arbitrary geographic regions that would be determined by the zip codes of the runners. The next sketch is an idea for showing the weather data compared to finishing time. The idea here is that as the temperature you are training in differs more and more from the race day temperature, your finishing time will go up. The last sketch is an idea on how to show the relationship between people in different age groups and how consistent their races were, graphing the average percent change of each age group.

![IMG_7580](https://github.com/user-attachments/assets/23ed10a6-5701-4f76-888c-1aab1d092df8)


This next sketch is a more refined version of the top sketch in the previous image, with an improved key and group visualization style. This also contains an idea for an interactive piece to this visualization, where mousing over either states or regions could give you a pop up window of more information on this region. 

![IMG_7602](https://github.com/user-attachments/assets/8c686cfe-e05d-488c-8497-6d8c47bf06df)



## Prototypes

I’ve created a couple proof of concept visualizations of this data. The first is a bar chart that shows the 1st half vs. 2nd Half time percent change by age group, similar to the bottom sketch in the first image of the previous section.

<img width="962" height="501" alt="Screenshot 2025-09-25 at 8 50 06 PM" src="https://github.com/user-attachments/assets/38246bb7-a99d-4d04-b0d8-ec10f4a412db" />
(https://vizhub.com/bentrantanella/d63092c74a734142a920dc5007bd460a)

The second visualization is another bar chart, this time showing age group versus number of runners in them, along with a color key showing the average 1st half vs. 2nd Half time percent change as ranges.

<img width="959" height="504" alt="Screenshot 2025-09-25 at 8 49 54 PM" src="https://github.com/user-attachments/assets/1327a215-cad2-41fb-9a2c-3de7a47cef81" />
(https://vizhub.com/bentrantanella/6b795d3b69394c719913e02a315775d5)


## Open Questions

1. I'm not sure how to build a map of the US and apply data to it yet and don't know how hard it will be
2. I don't know if the questions I'm asking will reveal any meaningful trends in the data
3. I don't know whether the conclusions I will reach from the visualizations of the data can be taken as truth.

## Milestones
Starting week: 9/25 - 10/1  
Will be working on repository ReadMe throughout all weeks  
Week 1: Determine specific trends that I want to analyze and begin research on how to visually show the US map  
Week 2: Build rough visualizations of data to see whether the trends actually show up  
Week 3: Begin rough setup of what will be the final product  
Week 4-7: Continue working on base visualization of final product  
Week 8-10: Implement interactive components of visualization  
Week 11-13: Optimize visualization for user understanding through user tests and finalize project report in repository readme  

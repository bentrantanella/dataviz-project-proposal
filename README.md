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

## Rough Schedule
Starting week: 9/25 - 10/1  
Will be working on repository ReadMe throughout all weeks  
Week 1: Determine specific trends that I want to analyze and begin research on how to visually show the US map  
Week 2: Build rough visualizations of data to see whether the trends actually show up  
Week 3: Begin rough setup of what will be the final product  
Week 4-7: Continue working on base visualization of final product  
Week 8-10: Implement interactive components of visualization  
Week 11-13: Optimize visualization for user understanding through user tests and finalize project report in repository readme  

# Project Progress Milestones

## Progress 1: Creating the map

[Vizhub Link](https://vizhub.com/bentrantanella/457e358e65584b168877c9cf5ac1a889)

For the first progress milestone, the goal was the create the map of the US and figure out how to overlay some data on the map. The first challenge was dealing with the topojson and geojson data, and translating this to a map projection. Originally the idea was the display all 50 states and overlay points based on a translation of latitude and longitude to pixel position, however the decision was made to only focus on the lower 48 states in order to maintain the one uniform projection. Here is the first iteration of the map visual:

<img width="908" height="474" alt="Screenshot 2025-12-12 at 2 56 31 PM" src="https://github.com/user-attachments/assets/3783e122-ac40-4bd0-9370-74b10ee02a29" />

For this initial map visualalization, I plotted the center of each state with a red circle, then scaled the circle diameter based on the number of finishers from that state. I also added a small interactive piece, by turning a state green if the user hovers over it with their mouse (Texas in the above image). This was more of a building block for future iterations, as it did not rely on any data and was purly a proof of concept.

## Progress 2: Formatting

[Vizhub Link](https://vizhub.com/bentrantanella/7c403743079b43318aaa064de9811b11)

The main focus of this progress iteration was to begin to make the visual into something that is conveying user-understandable data. The major changes were adding a title, changing the background color and map color to reflect the Boston Marathon brand colors, and adding a small tool-tips mechanism. This just showed the user the name of the state they were currently hovering over, as well as the specific number of finishers from that state. Here is the 2nd iteration of the map visual:

<img width="961" height="501" alt="Screenshot 2025-12-12 at 3 08 42 PM" src="https://github.com/user-attachments/assets/23ec404e-3ed0-4ec2-8cca-0bcb5c8011af" />


This progress point was more about laying the foundation for future features to be implemented, as fixing the formatting allowed me to focus on the data more during the next steps. A lot was tinkered with during this phase, with the formatting you see above and the added tool tips being the features kept for the next iterations. One bug was encountered during this phase that needed to be fixed, as the map would load in with the desired yellow color, but then turn to grey and stay grey once the user moused over a state. However, this was any easy fix. It was also in this phase where I decided to base the scale of my vis on the fullscreen mode, rather than the smaller preview window, as it allowed me to spread out and communicate the data easier.

## Progress 3: Color

[Vizhub Link](https://vizhub.com/bentrantanella/30157fd3d6ac402d95ca570c0abad79f)

For this progress iteration, the goal was to incorporate color into the visualization in a meaningful way. To do this, I kept the yellow color scheme for the states, but turned it into a gradient relating to the relative number of finishers to other states. This allowed the visualtion to show the data in two different ways, targeting users who think in different ways visually. Also in this iteration I added more information to the hover tool tips. This now shows (from each state) total number of finishers, average finish time, average age of finishers, and the average difference between their first half split and their second half split. Here is the current map visual:

<img width="961" height="500" alt="Screenshot 2025-12-12 at 3 25 18 PM" src="https://github.com/user-attachments/assets/1fe12cef-35d9-415a-9623-cd2733555a4f" />


## Progress 4: Interactivity

[Vizhub Link](https://vizhub.com/bentrantanella/ff1f855c388f41ef96a21df52add30b9)

The next step to iterating my data visualtization closer to a finished product was to enhance the interactivity. To do this, I decided to add a clickable legend, which changed the data being viewed on the map. These option reflected what is being shown on the hover tool tips, but with the same color gradient style shading as before, with darker colors representing higher values. This interactivity allows the visual to display much more data in a concise and readable way, enhancing the project and begining to approach a more polished and usable final product. 

<img width="1204" height="900" alt="Screenshot 2025-12-12 at 3 29 23 PM" src="https://github.com/user-attachments/assets/d6193525-6aa1-43e2-b930-d95b173690dd" />

By again showing the same data in two different ways, my visualization is becoming much more enhanced and can cater to different learning styles of diffferent people. Some people like the raw numbers, so hovering over each state and getting those can be very helpful to them, but others prefer more intuative color grading to interpret the data, with the interactive legend now provides.

## Progress 5: Polishing

[Vizhub Link](https://vizhub.com/bentrantanella/e7187dc2bb6641798e4c3d80def6e956)

The goal of this progress step was to clear up any confusion a user may have when viewing my data visualization. I did this in two main ways. First, as recieved from peer feedback, since the data being shown wasn't being explained in it's entirety, I added a new text box with some Vis Notes. The goal with this was to provide a bit of context on what I was showing and to leave as little guessing or interpretation as possible for the user. So, I explained specifically what the circles mean, what the color gradient means, and finally what the 'Split Difference' was showing. I felt that the split difference explanation was the most needed, as for non-runners this may be a bit less intuative as to what it was meaning. Lastly, the other tweak I made to polish to Vis was the colors, making the diffrence in gradient as bit less harsh, since states like Massachusetts and California were dominating some categories and taking away from the aim of the color grading. 

<img width="1229" height="905" alt="Screenshot 2025-12-12 at 3 33 17 PM" src="https://github.com/user-attachments/assets/db549ec3-0375-4c64-b9db-f4d034d47be4" />

## Final Project

[Vizhub Link](https://vizhub.com/bentrantanella/8c16a528ddba42c0b0867f66f0f37115)

For the final product, I tested out various different formatting strategies, but ulimately landed on a similar one to what I have been working with. The major changes were an updated title formatting as well as another tweaking of the colors, finally nailing the color shading piece to most accurately represent the data while also being easily interpreted by the user. Overall, I was satisfied with how the project turned out, as at the beginning I did not know if overlaying data on a map in this way was a feasible project. A next step that I would have loved to take is to incorporate the weather data and elevation data of where the finishers were training, in order to see how those factors affected the finishers times. I learned a lot from this project and really enjoyed getting into the weeds of technical data visualtizion using d3.

<img width="1220" height="899" alt="Screenshot 2025-12-12 at 3 52 53 PM" src="https://github.com/user-attachments/assets/abcdf57b-9f79-4ccb-b7d9-3447766875cd" />


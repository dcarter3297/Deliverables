# Deliverables
Ctec 298 deliverables
Cell: A container where code is entered and executed in Jupyter Notebook.
Kernel: A computational engine that executes code in Jupyter Notebook.
Ipynb file: A text file that describes the contents of your notebook in JSON format.
JSON: JavaScript Object Notation is a file format that turns text into data objects.
Metadata: A place where one can put JSON-able information regarding your notebook, cell, or output.
Code cell: Contains code to be executed in the kernel and displays its output below. 
Markdown cell: contains text formatted using Markdown and displays its output in-place when it is run.




Police Stops
Diamond Carter
Ctec 298-101
INTRODUCTION

Mistreatment by the police has been an issue for black and brown citizens of America as far back as the 1900s. The issue that my team addressed was the “why” of this matter. Why were black and brown people profiled by police and if there was a greater amount of stops of black and brown citizens than others in the state of California in the cities of Stockton and San Diego. 

SUMMARY
	While researching for this topic my team and I compiled research questions on which we planned to answer using the data that we found. The research questions were: What is the relationship of the racial characteristics of those cities and the racial characteristics of those stopped by police? What is the age of those stopped by police in the city of San Diego vs the city of Stockton? Does race and age matter when drivers are stopped by police? Based on the research conducted, what is the outcome after a driver is stopped by police? With these research questions and the data that were provided with we used the following variables to assist in answering our questions : Age, race, sex, warning issued, citation issued, arrest made, reason for stop, and outcome. From our research we learned that mistreatment by the police in the state of California has been a recurring issue. Specifically black and brown citizens have always gotten the short end of the stick when it has to do with police stops, mistreatment, and profiling. We found that the majority of stops in the city of Stockton was of Black and Hispanics compared to San Diego the majority of stops were of Whites in Hispanics. Despite the demographics of San Diego, the numbers were higher for Hispanics pulled over than whites. Also the ages of those pulled over were higher in the 15-34 age range for hispanic drivers supporting the profiling of younger hispanic citizens. To combat and prevent any further police brutality and mistreatment we recommended that the governor of California check into the stops and see if anything unlawful is occuring. We also recommended that the governor request more information to be looked into when reviewing the stops. Lastly, we recommended that the governor collaborate with black and brown citizens and their communities to discuss and improve the relationships and perspectives on police brutality.

DESCRIPTION OF CTEC MATERIALS SUBMITTED
At the beginning of the 8 weeks, we were assigned the task to submit the files and assignments that we completed in CTEC 128. With 128 being a data science class, the materials and assignments we submitted would be a stepping stone for us to broaden our knowledge in CTEC 298. The first material that was submitted was our final research paper and powerpoint. These two go hand in hand and were used to explore a problem of police stops. In my group we used the state of California and the cities of Stockton and San Diego. We were tasked to research the issue of police stops in these cities and were there any racial disparities faced by the black and brown citizens of these two cities. The next materials that we were asked to submit was the actual data sets that we used to create our visualizations with. These were in the form of excel spreadsheets and were too large of files to email so a shared drive was created. The next material was the concept map that was created for the research paper. The concept map was a brainstorm of ideas of what categories we’d use to help explain our research. The categories that we used in our concept map were: Treatment, Police, Demographics, Location, and Vehicle. These 5 categories were all the best categories that we could come up with to assist in explaining and answering our research questions. The next material was our data codebook. The data codebook was an excel spreadsheet of the variables that we were going to be using, the type of variable, our plans to handle the missing and incorrect data and lastly the mean, median, mode, and range of the data. The last material that we were asked to submit was the visualizations that we created using excel. We were asked to submit these in order to give us something to base our next visualizations on. The visualizations helped put the data into an image so it would be easier to understand and comprehend. Also the excel visualizations were going to be used to create new visualizations using python. 
DESCRIPTION OF PLOT DELIVERABLES
The plots that I have created were once visualizations that were created in excel. With the knowledge that I gained in this class I was able to transform excel visualizations into plots in matplotlib using python. The original dataset that was used was the excel visualizations were the same datasets that I used for matplotlib plots. The datasets were already cleaned previously due to the fact that my group in CTEC 128 were assigned the same task of wrangling the data we were provided with. 

This plot shows the races of drivers pulled over in the city of Stockton, CA. 
import matplotlib.pyplot as plt 
  
# defining labels 
races = ['Asian/Pacific Islander', 'Black', 'Hispanic', 'Other/Unknown','White'] 
  
# portion covered by each label 
slices = [9, 26, 40, 4, 21] 
  
# color for each label 
colors = ['cyan', 'orange', 'grey', 'yellow','blue'] 
  
# plotting the pie chart 
plt.pie(slices, labels = races, colors=colors,  
        startangle=90, shadow = True, explode = (0, 0, 0.1, 0, 0), 
        radius = 1.2, autopct = '%1.1f%%') 
  
# plotting legend 
plt.legend() 
  
# showing the plot 
plt.show() 
 
 


This plot shows the races of drivers pulled over in the city of San Diego,CA.

import matplotlib.pyplot as plt 
  
# defining labels 
races = ['Asian/Pacific Islander', 'Black', 'Hispanic', 'Other/Unknown','White'] 
  
# portion covered by each label 
slices = [9, 11, 31, 7, 42] 
  
# color for each label 
colors = ['cyan', 'orange', 'grey', 'yellow','blue'] 
  
# plotting the pie chart 
plt.pie(slices, labels = races, colors=colors,  
        startangle=90, shadow = True, explode = (0, 0, 0.1, 0, 0), 
        radius = 1.2, autopct = '%1.1f%%') 
  
# plotting legend 
plt.legend() 
  
# showing the plot 
plt.show() 



This plot shows the number of drivers pulled over by age in the city of San Diego, CA


import matplotlib.pyplot as plt
  
# x-coordinates of left sides of bars 
left = [1, 2, 3, 4, 5 ,6, 7, 8, 9]
  
# heights of bars
height = [29890, 126819, 86248, 63512, 45167, 19536, 5639, 1394, 146]
  
# labels for bars
tick_label = ['11-20', '21-30', '31-40', '41-50', '51-60', '61-70', '71-80', '81-90', '91-100']
  
# plotting a bar chart
plt.bar(left, height, tick_label = tick_label,
        width = 0.8, color = ['blue'])
  
# naming the x-axis
plt.xlabel('Ages')
# naming the y-axis
plt.ylabel('Number of drivers pulled over')
# plot title
plt.title('Number of drivers pulled over by age in San Diego from 2014-2017')
  
# function to show the plot
plt.show()
 



This plot shows the number of drivers pulled over by age in the city of Stockton, CA.


import matplotlib.pyplot as plt
  
# x-coordinates of left sides of bars 
left = [1, 2, 3, 4, 5 ,6, 7, 8, 9]
  
# heights of bars
height = [4804, 9135, 5828, 3460, 1349, 362, 102, 11, 1]
  
# labels for bars
tick_label = ['11-20', '21-30', '31-40', '41-50', '51-60', '61-70', '71-80', '81-90', '91-100']
  
# plotting a bar chart
plt.bar(left, height, tick_label = tick_label,
        width = 0.8, color = ['green'])
  
# naming the x-axis
plt.xlabel('Ages')
# naming the y-axis
plt.ylabel('Number of drivers pulled over')
# plot title
plt.title('Number of drivers pulled over by age in Stockton from 2012-2016')
  
# function to show the plot
plt.show()
 


This plot shows the number of drivers pulled over by age and race in Stockton, CA.



%matplotlib inline
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
Age_range = {'Ages': ['15-24', '25-34', '35-44', '45-55'],
        'Asian_PacificIslander': [7090, 8831, 6819, 5658],
        'Black': [9645, 13805, 7803, 6972],
        'Hispanic': [28583, 35970, 23917, 18665],
        'Other_Unknown': [6044, 8402, 5543, 3938],
        'White': [29880, 45381, 29631, 28936]}
df = pd.DataFrame(Age_range, columns = ['Ages', 'Asian_PacificIslander', 'Black', 'Hispanic', 'Other_Unknown', 'White'])
df
# Setting the positions and width for the bars
pos = list(range(len(df['Asian_PacificIslander']))) 
width = 0.15 
    
# Plotting the bars
fig, ax = plt.subplots(figsize=(10,5))

# Create a bar with Asian_PacificIslander data,
# in position pos,
plt.bar(pos, 
        #using df['Asian_PacificIslander'] data,
        df['Asian_PacificIslander'], 
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='blue', 
        # with label the first value in Ages
        label=df['Ages'][0]) 

# Create a bar with Black data,
# in position pos + some width buffer,
plt.bar([p + width for p in pos], 
        #using df['Black'] data,
        df['Black'],
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='orange', 
        # with label the second value in Ages
        label=df['Ages'][1]) 

# Create a bar with Hispanic data,
# in position pos + some width buffer,
plt.bar([p + width*2 for p in pos], 
        #using df['Hispanic'] data,
        df['Hispanic'], 
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='grey', 
        # with label the third value in Ages
        label=df['Ages'][2]) 

# Create a bar with Other_Unknown data,
# in position pos + some width buffer,
plt.bar([p + width*3 for p in pos], 
        #using df['Other_Unknown'] data,
        df['Other_Unknown'], 
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='yellow', 
        # with label the fourth value in Ages
        label=df['Ages'][3]) 

# Create a bar with White data,
# in position pos + some width buffer,
plt.bar([p + width*4 for p in pos], 
        #using df['White'] data,
        df['White'], 
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='cyan', 
        # with label the fourth value in Ages
        label=df['Ages'][3]) 

# Set the y axis label
ax.set_ylabel('# of Stops')

# Set the chart's title
ax.set_title('Number of Stops by Race and Age in Stockton, CA 2012-1016')

# Set the position of the x ticks
ax.set_xticks([p + 1.5 * width for p in pos])

# Set the labels for the x ticks
ax.set_xticklabels(df['Ages'])

# Setting the x-axis and y-axis limits
plt.xlim(min(pos)-width, max(pos)+width*4)
plt.ylim([0, max(df['Asian_PacificIslander'] + df['Black'] + df['Hispanic'] + df['Other_Unknown'] +df['White'])] )

# Adding the legend and showing the plot
plt.legend(['Asian_PacificIslander', 'Black', 'Hispanic', 'Other_Unknown','White'], loc='upper left')
plt.grid()
plt.show()



This plot shows the number of drivers pulled over by age and race in San Diego, CA


%matplotlib inline
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
Age_range = {'Ages': ['15-24', '25-34', '35-44', '45-55'],
        'Asian_PacificIslander': [7090, 8831, 6819, 5658],
        'Black': [9645, 13805, 7803, 6972],
        'Hispanic': [28583, 35970, 23917, 18665],
        'Other_Unknown': [6044, 8402, 5543, 3938],
        'White': [29880, 45381, 29631, 28936]}
df = pd.DataFrame(Age_range, columns = ['Ages', 'Asian_PacificIslander', 'Black', 'Hispanic', 'Other_Unknown', 'White'])
df
# Setting the positions and width for the bars
pos = list(range(len(df['Asian_PacificIslander']))) 
width = 0.15 
    
# Plotting the bars
fig, ax = plt.subplots(figsize=(10,5))

# Create a bar with Asian_PacificIslander data,
# in position pos,
plt.bar(pos, 
        #using df['Asian_PacificIslander'] data,
        df['Asian_PacificIslander'], 
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='blue', 
        # with label the first value in Ages
        label=df['Ages'][0]) 

# Create a bar with Black data,
# in position pos + some width buffer,
plt.bar([p + width for p in pos], 
        #using df['Black'] data,
        df['Black'],
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='orange', 
        # with label the second value in Ages
        label=df['Ages'][1]) 

# Create a bar with Hispanic data,
# in position pos + some width buffer,
plt.bar([p + width*2 for p in pos], 
        #using df['Hispanic'] data,
        df['Hispanic'], 
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='grey', 
        # with label the third value in Ages
        label=df['Ages'][2]) 

# Create a bar with Other_Unknown data,
# in position pos + some width buffer,
plt.bar([p + width*3 for p in pos], 
        #using df['Other_Unknown'] data,
        df['Other_Unknown'], 
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='yellow', 
        # with label the fourth value in Ages
        label=df['Ages'][3]) 

# Create a bar with White data,
# in position pos + some width buffer,
plt.bar([p + width*4 for p in pos], 
        #using df['White'] data,
        df['White'], 
        # of width
        width, 
        # with alpha 0.5
        alpha=0.5, 
        # with color
        color='cyan', 
        # with label the fourth value in Ages
        label=df['Ages'][3]) 

# Set the y axis label
ax.set_ylabel('# of Stops')

# Set the chart's title
ax.set_title('Number of Stops by Race and Age in San Diego, CA 2014, 2017')

# Set the position of the x ticks
ax.set_xticks([p + 1.5 * width for p in pos])

# Set the labels for the x ticks
ax.set_xticklabels(df['Ages'])

# Setting the x-axis and y-axis limits
plt.xlim(min(pos)-width, max(pos)+width*4)
plt.ylim([0, max(df['Asian_PacificIslander'] + df['Black'] + df['Hispanic'] + df['Other_Unknown'] +df['White'])] )

# Adding the legend and showing the plot
plt.legend(['Asian_PacificIslander', 'Black', 'Hispanic', 'Other_Unknown','White'], loc='upper left')
plt.grid()
plt.show()


SUMMARY/CONCLUSION
In conclusion, the information that was taught was very helpful in teaching myself to use python, matplotlib, pandas, and online repositories in general. Also the assignments from CTEC 128 went hand in hand with the assignments that we’ve done in this class. This class was very informative and has aided me in learning new skills for my future.


Data files are too large, will be in shared drive.
Tutorials were completed as poerpoint presentations.. Will be added shared drive.

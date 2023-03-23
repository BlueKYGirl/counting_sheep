This README is a work in progress.

# Counting Sheep, Courting Sleep
## Using Python Data Analysis Tools to Find the Recipe for a Good Night's Sleep
### by Toni Moore
___

> We are such stuff as dreams are made on;       
>And our little life is rounded with a sleep.
>              
> -William Shakespeare
___
>It's me, hi, I'm the problem, it's me.
>
>-Taylor Swift
___

According to the National Sleep Foundation, more than one-third of adults aren't getting the recommended 7-9 hours of sleep per night. 

According to my clock, my Apple Watch,  and everyone who has to deal with me in the morning, I am part of this one-third.

I've been an insomniac and a restless sleeper for as long as I can remember. Family stories verify I was born not knowing how to sleep.

Unfortunately, I still haven't learned.

![sleep gif](https://media.giphy.com/media/mF4k0YXIHDHzy/giphy.gif)


With the ability to get fairly accurate sleep data from my Apple Watch, accurate enough that Apple Watch data is often used as suppplemental data by medical sleep specialists when patients submit to professional sleep studies, I wanted to track my sleep for one month to try to find trends and correlations between different sleep supplements I use, the different sleep hygeine behaviors I employ, and the indicators for healthy sleep tracked by Watch software: awake time, core sleep, REM sleep, deep sleep, heart rate range, and resiratory rate range.

The questions I want answered are:

1. How much variation is there from night to night in my various sleep metrics?
2. Which supplements work the best at inducing REM and deep sleep? 
3. Which sleep habits and behaviors, collectively known as "sleep hygeine," are best at inducing REM and deep sleep?
4. Is there an easily-reproducible formula of one sleep supplement combined with one sleep hygeine behavior that, done nightly, can increase the amount of time I spend in REM and deep sleep? 

For this particular project, REM and deep sleep will be singled out. Early informal investigations of my sleep tracking data on my Watch showed that I do not spend as much time in REM and deep sleep as other healthy adults my age. According to Healthline, most adults spend 20-25% of their sleep time in REM, or rapid eye movement sleep, and 13-23% in deep sleep, where physical healing, learning, and memory formation takes place. 

Since I am very rarely at those numbers, my focus will be on the supplements and behaviors that correlate with the highest percentages from my Watch data. At this time, I am not over any of the recommended percentages in any recorded metrics.

Data was gathered by wearing my Apple Watch nightly for one month and making sure the Watch was in "Bedtime" mode upon retiring for the night. Each morning, the outputs from the Health app on my phone were entered into the following Google Form used for recording this data in a quick and user-friendly way:

[Sleep Tracking Input Form](https://forms.gle/MngG8s4dmk8k6TRK6)


This Form linked to a Google Sheet containing all the data in a tabular format. This was then converted to a CSV file upon completion of the data gathering stage. That Sheet can be viewed here:

[Sleep Tracking Sheet](https://docs.google.com/spreadsheets/d/1xQZa-SgVZmOvIJ1EnW7v3I0bptejfR9Ju3zafn3GvIk/edit?usp=sharing)

The column headings used in the data analysis correspond to the recorded metrics and to supplements and sleep behaviors. The following labels may help the reader going forward if they are defined and explained:

awake_pct (percentage of recorded sleep time spent in a wakeful state)

rem_pct (percentage of recorded sleep in REM, or Rapid Eye Movement sleep; this is also known as stage 3 sleep)

core_pct (percentage of recorded sleep in core, or stage 1 and stage 2 light sleep)

deep_pct (percentage of recorded sleep in deep stage 4 sleep)

Supplements that were tracked include oral melatonin capsules (3mg), oral magnesium capsules (250mg), Neuriva combination oral supplement capsules (contains melatonin, l-theanine, and ashwagandha), and chamomile tea. These were all taken with a physician's knowledge and consent and I was informed about what could be taken together and what could not. 

Sleep hygeine behaviors tracked included baths, showers, and guided sleep meditation through a meditation app. For the scope of this study, which focuses on behaviors immediately before bedtime, caffeine consumption, exercise, and afternoon naps were not examined. Those are known to impact sleep quality and are certainly worth investigating in a future study. 


### Necessary Installs

The data analysis file, Counting_Sheep.ipynb, can be opened in an IDE that has the necessary extensions to open a Jupyter Notebook. (Visual Studio Code was used for this project.) Google Colab is a free Jupyter Notebook environment that could be used to open and run the project code. 

[Anaconda](https://www.anaconda.com/products/distribution) is recommended as it already has the necessary packages and libraries in this project installed. If you do not have Anaconda installed, you may install the necessary packages individually at your Terminal or Windows Powershell command lines. This project uses pandas, Numpy, and Matplotlib.

python -m pip install -U pip

pip install pandas

pip install numpy

python -m pip install -U matplotlib

A requirements.txt is also included in the repo of this project. To use that file to install all necessary packages and libraries, type the following code into your Terminal or Windows Powershell command lines:

pip install -r requirements.txt

### Potential Error Message in Line 23

On machines without the newest version of pandas, the correlation function at line 23 may not run and may throw a code about the the "numeric_only" parameter. In the newest version of pandas, the default value of "numeric_only" in the corr() function was changed from True to False, and to not include that parameter throws a FutureWarning message. Because I have some non-numeric values in the DataFrame, such as date and day of the week, I opted to put the numeric_only parameter in place and set to True after researching this and looking at other developers' recommendations. If this line of code doesn't run for the tester, it doesn't impact any code later in the project and has little impact upon the overall findings. It was a fishing expedition to search for any interesting correlations to explore. 









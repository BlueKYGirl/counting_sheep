This README is a work in progress and may contain outdated or innaccurate information.

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

According to my clock, my Apple Watch,  and everyone who has to deal with me in the morning, I am one of this one-third.

I've been an insomniac and a restless sleeper for as long as I can remember. My mother told people I was born not knowing how to sleep. 

Unfortunately, I still haven't learned.

With the ability to get fairly accurate sleep data from my Apple Watch, accurate enough the Apple Watch data is often used as suppplemental data by medical sleep specialists when patients submit to professional sleep studies, I wanted to track my sleep for one month to try to find trends and correlations between different sleep supplements I use, the different sleep hygeine behaviors I employ, and the indicators for healthy sleep tracked by Watch software: awake time, core sleep, REM sleep, deep sleep, heart rate range, and resiratory rate range.

The questions I want answered are:

1. How much variation is there from night to night in my various sleep metrics?
2. Which supplements work the best at inducing REM and deep sleep? 
3. Which sleep habits and behaviors, collectively known as "sleep hygeine," are best at inducing REM and deep sleep?
4. Is there an easily-reproducible formula of one sleep supplement combined with one sleep hygeine behavior that, done nightly, can increase the amount of time I spend in REM and deep sleep? 

For this particular project, REM and deep sleep will be singled out. Early informal investigations of my sleep tracking data on my Watch showed that I do not spend as much time in REM and deep sleep as other healthy adults my age. According to Healthline, most adults spend 20-25% of their sleep in REM, or rapid eye movement sleep, and 13-23% in deep sleep, where physical healing and memory formation takes place. 

Since I am very rarely at those numbers, my focus will be on the supplements and behaviors that correlate with the highest percentages from my Watch data. 

Data was gathered from wearing my Apple Watch nightly for one month and making sure the Watch was in "Bedtime" mode upon retiring for the night. Each morning, the outputs from the Health app on my phone were entered into the following Google Form used for recording this data in a quick and user-friendly way:

[Sleep Tracking Input Form](https://forms.gle/MngG8s4dmk8k6TRK6)


This Form linked to a Google Sheet containing all the data in a tabular format. This was then converted to a CSV file upon completion of the data gathering stage. That Sheet can be viewed here:

[Sleep Tracking Sheet](https://docs.google.com/spreadsheets/d/1xQZa-SgVZmOvIJ1EnW7v3I0bptejfR9Ju3zafn3GvIk/edit?usp=sharing)

### Necessary Installs

The data analysis file, Counting_Sheep.ipynb, can be opened in an IDE that has the necessary extensions to open a Jupyter Notebook. (Visual Studio Code was used for this project.) Google Colab is a free Jupyter Notebook environment that could be used to open and run the project code. [Anaconda](https://www.anaconda.com/products/distribution) is recommended as it already has the necessary packages and libraries in this project installed. If you do not have Anaconda installed, you may install the necessary packages individually at your Terminal or Windows Powershell command lines. This project uses pandas, Numpy, and Matplotlib.

pip install pandas

pip install numpy

python -m pip install -U pip

python -m pip install -U matplotlib










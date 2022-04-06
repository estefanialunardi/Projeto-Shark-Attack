
[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Love](https://img.shields.io/badge/Love-pink?style=flat-square&logo=data:image/svg%2bxml;base64,PHN2ZyByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48dGl0bGU+R2l0SHViIFNwb25zb3JzIGljb248L3RpdGxlPjxwYXRoIGQ9Ik0xNy42MjUgMS40OTljLTIuMzIgMC00LjM1NCAxLjIwMy01LjYyNSAzLjAzLTEuMjcxLTEuODI3LTMuMzA1LTMuMDMtNS42MjUtMy4wM0MzLjEyOSAxLjQ5OSAwIDQuMjUzIDAgOC4yNDljMCA0LjI3NSAzLjA2OCA3Ljg0NyA1LjgyOCAxMC4yMjdhMzMuMTQgMzMuMTQgMCAwIDAgNS42MTYgMy44NzZsLjAyOC4wMTcuMDA4LjAwMy0uMDAxLjAwM2MuMTYzLjA4NS4zNDIuMTI2LjUyMS4xMjUuMTc5LjAwMS4zNTgtLjA0MS41MjEtLjEyNWwtLjAwMS0uMDAzLjAwOC0uMDAzLjAyOC0uMDE3YTMzLjE0IDMzLjE0IDAgMCAwIDUuNjE2LTMuODc2QzIwLjkzMiAxNi4wOTYgMjQgMTIuNTI0IDI0IDguMjQ5YzAtMy45OTYtMy4xMjktNi43NS02LjM3NS02Ljc1em0tLjkxOSAxNS4yNzVhMzAuNzY2IDMwLjc2NiAwIDAgMS00LjcwMyAzLjMxNmwtLjAwNC0uMDAyLS4wMDQuMDAyYTMwLjk1NSAzMC45NTUgMCAwIDEtNC43MDMtMy4zMTZjLTIuNjc3LTIuMzA3LTUuMDQ3LTUuMjk4LTUuMDQ3LTguNTIzIDAtMi43NTQgMi4xMjEtNC41IDQuMTI1LTQuNSAyLjA2IDAgMy45MTQgMS40NzkgNC41NDQgMy42ODQuMTQzLjQ5NS41OTYuNzk3IDEuMDg2Ljc5Ni40OS4wMDEuOTQzLS4zMDIgMS4wODUtLjc5Ni42My0yLjIwNSAyLjQ4NC0zLjY4NCA0LjU0NC0zLjY4NCAyLjAwNCAwIDQuMTI1IDEuNzQ2IDQuMTI1IDQuNSAwIDMuMjI1LTIuMzcgNi4yMTYtNS4wNDggOC41MjN6Ii8+PC9zdmc+)
[![GitHub contributors](https://img.shields.io/github/contributors/Naereen/badges.svg)](https://github.com/estefanialunardi/Projeto-Shark-Attack/contributors)
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://github.com/estefanialunardi/)


<img src="https://user-images.githubusercontent.com/101064720/161954804-df227729-227c-4fa8-8b24-963ab173b32f.jpg" width="300" align="right">

# When will I face a shark?
This project is a short analysis of Shark Attacks around the world existing database. My prime objective was to analyse the most probable moments to face an incident with a shark, considering the past repported events.

I focused my work on a quantitative analysis of the data, considering the frequency of attacks depending on the periods of the day, the month and the year.

The results of this very study shall not be used as source of cientific or advanced information on sharks behaviour or risk calculation.

All the steps, opperation and code to reach the final data are avaliable on a Jupyter Notebook for anyone interested in exploring and mining the records.

For the last analysis of this very work, I've used the ".merged()" method.

Thank you!

## How did I do it?
### Cleaning Methods
I used the ".dropna()" for rows that had less then 5 columns filled. 
I also standardized each columns, reassuring that all data found would be using the same patterns (using ".lower()", ".strip().", .etc.).
Then, I checked the values of each column (with ".unique()" or ".value_counts()") to indentify any discrepancy.
Finally, i used the ".loc" method followed by ".replace()" method to reassure that any mispelled or misfilled data were correct.

Mass actions in columns (for all rows) were made using the ".apply()" method.


## The data
I started cleaning some columns, to work only with those which were necessary for my time analyzis. It meant date, country and time. 
I also let the Case Number column available, cause it is filled with important data to the date - and easier to clean then the date column, also. 

After that, I divided that column into three: day, month and year.
<img src="https://user-images.githubusercontent.com/101064720/161955573-3157b2d7-3057-473d-8708-7cbfa9517bc5.PNG" width="800" align="center">

## Day period and the attacks
### Do sharks attack more during twilight?
Researches suggest that shark attacks occur more often at periods when the lower atmosphere is illuminated and the Sun is not directly visible, such as dawn and dusk. 

### Day period and Sun light
Earth's surface is neither completely lit nor completely dark twice a day: dusk and dawn.. The duration of twilight depends on the latitude and the time of the year, by the time the sun rises and when sun sets.

For this study, it will be label as Twilight the periods near the beginning of the morning (4am to 7am) and the ending of the afternoon (5pm to 8pm). 

### Hypothesis
Researchers believe that more attacks occur during the Twilight, due to the fact that sharks are more active searching for food during those periods and the low luminosity may limit their visibility and the animals may mistake humans for prey animals.

To prove this hypothesis it's necessary to analyse the rate of attacks depending on the luminosity when more attacks happen - and another variables related to the same period of time.


### Considerations
<img src="https://user-images.githubusercontent.com/101064720/161961496-aef0c73a-8b9b-490c-a171-97e3e5d51226.PNG" width="210" align="left">
*Dawn lasts 3 hours, corresponding to 12,5% of the day- it corresponds to 4,72% of the amount of attacks*

*Morning lasts 5 hours, corresponding to 20,83% of the day- it corresponds to 28,95% of the amount of attacks.*

*Afternoon lasts 5 hours, corresponding to 20,83% of the day- it corresponds to 47,45% of the amount of attacks.*

*Dawn lasts 3 hours, corresponding to 12,5% of the day- it corresponds to 12,06% of the amount of attacks.*

*Nights, lasts 8 hours, corresponding to 33,33% of the day- it corresponds to 6,8% of the amount of attacks.*

Considering the percentage of the total amount of hours per day in each period (dawn, morning, afternoon, dusk and night) and the rate of attacks during the periods, we will realize that there is an important deviation at mornings and, specially, at afternoons and night.

However, it's known that the luminosity is very much relevant to human activity in the ocean, regardless to it's relevance to shark behaviour. 

People use to go the beach, swim, surf, fish, etc. with day light, which means mornings and afternoons.

<img src="https://user-images.githubusercontent.com/101064720/161975157-9c65aa2e-832c-4b57-affa-e664ad8aff99.PNG" align="right">
So, the deviation could be easily explained by the ocean being crowder with more people baithing, therefor more human exposure to sharks then at the dark periods of the day. 

### Conclusion
The higher number of occurrences at periods with more luminosity of the day, suggests that, despite knowing that sharks prefer to hunt in poor lightning, the level of human activity in the ocean is more important to the amount of attacks then sharks behaviour itself. Or, notwithstanding what researchers may believe, in fact sharks suffer from nyctalopia (night blindness) and can't hunt well in poor lighting.


## Lunar Phases and the attacks

### Do the Lunar Phases interfeer on the attacks?
Researches suggest that shark attacks occur more ore less often depending on phases of the moon. The exact cause remains unclear, but there is reason to believe it's due to the influence of the moon on the sea tides.

### Sea tides and the moon phases
Caused by the moon's (majoritively) and the sun's gravitational forces exerted on the earth, the tidal force generates very long waves that affects the sea level at the coast. When this level is higher, we call it a high tide. When it's lower, the coast is experiencing a low tide.

Every lunar day (or each 24 hours and 50 minutes), there are two low tides and two high tides. Depending on the tidal force, the range between low and high tides are bigger or smaller. 

At new moon or full moon, the tide's range is at its maximum (called spring tide). That mean that high tides are higher and low tides are lower.
At quarter phases, the tide's range is smaller (called neap tide). That mean that high tides are lower and low tides are higher.

Considering this, during the darkest and brightest phases, the tide's variation are much bigger than at the medium luminisoty phases.

### Hypothesis
<img src="https://user-images.githubusercontent.com/101064720/161962754-86a9b3c4-caa5-46dd-b8bd-034bae79a7ff.PNG" width="210" align="left">
Bigger changes on the sea level (higher ranges of sea tides) affect shark behaviour, causing more attacks.

To prove this hypothesis it's necessary to analyze if the rate of attacks depending on the lunar phases are statistically different from the rate of each moon phase on the lunation. 


### Considerations
<img src="https://user-images.githubusercontent.com/101064720/161963073-92326697-d03e-454d-9213-3a5f4c8e4b8a.PNG" width="210" align="right">
Considering that the lunar phase is not relevant to human activity in the ocean (regardless the phase, people will have similar behaviour regarding going to the ocean, swimming, fishing, surfing, etc.).

*New Moon lasts 2 days, corresponding to 6,66% of the month - it corresponds to 9.91 % of the amount of attacks.*

*First Quarter lasts 2 days, corresponding to 6,66% of the month - it corresponds to 7.22% of the amount of attacks.*

*Waxing Crescent lasts 5 days, corresponding to 16.66% of the month - it corresponds to 16.13% of the amount of attacks.*

*Waxing Gibbous lasts 5 days, corresponding to 16,66% of the month - it corresponds to 16.42% of the amount of attacks.*

*Full moon lasts 2 days, corresponding to 6,66% of the month - it corresponds to 6.47% of the amount of attacks.*

*Wanning Gibbous lasts 5 days, corresponding to 16,66% of the month - it corresponds to 20.41% of the amount of attacks.*

*Last Quarter lasts 2 days, corresponding to 6,66% of the month - it corresponds to 6.77% of the amount of attacks.*

*Wanning crescent lasts 5 days, corresponding to 16,66% of the month - it corresponds to 16.44% of the amount of attacks.*

### Conclusion
<img src="https://user-images.githubusercontent.com/101064720/161963073-92326697-d03e-454d-9213-3a5f4c8e4b8a.PNG" width="210" align="left">
Although there is a higher number of occurrences at the darkest and the brightest moon phases, suggesting that a bigger tide variation interferes on how often shark attacks occur, there is no significant difference of the rate of daily attacks during the different phases of the moon.
That mean that the higher frequency of attacks during those phases happens because they last longer and there so there is more occurrences only in absolute terms.

## Seasons and the attacks
### Do sharks attack more during the summer?

Researches suggest shark populations may increase as the thermometers heat up. As the animals are most abundant, it may mean less food available and need to hunt nearer the shore. 

### Defining seasons
<img src="https://user-images.githubusercontent.com/101064720/161963131-51f83b6c-b2e7-42a5-b7d6-2a703acea539.PNG" width="210" align="right">
To define which season it was by the time of attack, it's important to know if the occurrence was in the Northern or Southern hemisphere of the globe. On the months of December, January and February, its summer on the South and winter on the North. On March, April and May, South experiences autumn while North faces spring. Winter stars in the Southern hemisphere on June and stays for July and August, while it's summer in the Northern. Finally, September, October and November are the months when it's spring in the South and autumn in the North.

### Hypothesis
Higher temperatures affect the range of shark population and increases the number of attacks.

To prove this hypothesis it's necessary to analyze the reproduction period of sharks, as well as another variables related to the same period of time, such as higher presence of humans in the ocean.

### Considerations
<img src="https://user-images.githubusercontent.com/101064720/161963215-76c70134-d29d-4dc3-ae52-68220befd3d9.PNG" width="210" align="right">

According to research, usually mature sharks mate in higher temperatures periods, like spring and summer. Most shark species gestation period lasts between 9 and 12 months - which means the increase of the animals population could occur at any season, depending on the month of birth of the baby sharks (tututuru). However, researchers highlight that, on average, most coastal sharks give birth in the summer.

In addition, it's know that warmer seasons attracts more people to the sea. During the summer, humans invade the marine environment and may face greater conflict with animals, as sharks. When it's winter, on the other hand, swimmers are less numerous.

### Conclusion
<img src="https://user-images.githubusercontent.com/101064720/161975406-cbd170e5-e459-47cb-b473-d115b854cf5f.PNG" width="210" align="right">

It's clear that higher temperatures mean more shark attacks. Nevertheless, it's not certain that it occurs only because of the increase of shark populations at this time of the year, once at the same period it's more likely to have more people swimming, bathing, surfing, fishing and living adventures in the sea.


# Let's have some fun!
## Astrology and the attacks
### Do sharks get influeced by the astrology sign season?
According to atrologers, despite of our own sun signs, during a zodiac sign season, every being feels the influence of that very sign. That mean, emulating their most usual traits and personality.
### Sign seasons and their influence on sharks personality
A Zodiac sign season is the time when the sun falls on a particular sign, and, as they say, everyone should act a bit more like the natives of that sun sign.
Signs Seasons
Aries (Ram): March 21 – April 19
Taurus (Bull): April 20 – May 20
Gemini (Twins): May 21 – June 21
Cancer (Crab): June 22 – July 22
Leo (Lion): July 23 – August 22
Virgo (Virgin): August 23 – September 22
Libra (Balance): September 23 – October 23
Scorpius (Scorpion): October 24 – November 21
Sagittarius (Archer): November 22 – December 21
Capricornus (Goat): December 22 – January 19
Aquarius (Water Bearer): January 20 - February 18
Pisces (Fish): February 19 – March 20
### Is there a more fatal season sign?
Now, let's face some facts: regardless what do papers say, aries are not what they say. At least, not considering sharks :rofl:	
<img src="https://user-images.githubusercontent.com/101064720/161963357-099e76b5-7998-476c-ada9-190053200b3b.PNG" align="right">
<img src="https://user-images.githubusercontent.com/101064720/161963374-8d43a4ad-6f94-4681-b7c9-e36e4aa96411.PNG" align="center">




Global Shark Attack File available here 
https://www.kaggle.com/datasets/teajay/global-shark-attacks


# Revolution Prediction Using Thresholds

This project was developed with a group in my Machine Learning and Political Science class (2021). It is based on the model of revolutions presented in the paper "Now Out of Never: The Element of Surprise in the East European Revolution of 1989" by Timur Kuran. In this model, each person has a threshold of how many others have to be part of a revolution before they join it. We iterate through a list of people, sorted in ascending order by threshold, and if their threshold is met, we add them to the revolution. As soon as we reach a person whose threshold is higher than the current number of people revolting, this is the end of the revolution.

This code models, using a Monte Carlo simulation, how many people will join a revolution, based on randomly selected input variables including population size, population distribution (selected from uniform, normal, and mixed distributions), and the starting threshold of people. In addition to these three, we collected data on the time it takes until the revolution ends, and we ran a linear regression to see the strength of the linear relationship between these four variables and the percentage of people that will revolt.

We added another function with a slight twist to make the model more realistic. This was the inclusion of an influential figure, where for each iteration, there was a small probability that the person would have a high influence on others, so they would have the power to increase the count of people in the revolution by more than 1. 

One interesting observation was that as we increase the starting threshold, the R^2 values increase. They are generally lower when the influential figures are added, because this introduces more randomness into the data, and it is thus less predictable. Future steps could include running more extensive regressions and splitting the sample, for more rigorous testing. This model is also not reproducible, due to the randomness in creating the population and introducing influential people, which could be improved. However, for our purposes with this model, we felt this was sufficient.

No shell code provided by professor.

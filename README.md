# Top Streaming Songs Spotify

### Introduction
Our subject domain is the digital music streaming industry, which includes platforms such as Spotify, Apple Music, Deezer, etc. We have decided to specifically explore this data through the lens of Spotify’s metrics that were collected and assembled into our chosen dataset. We are interested in demystifying the top-performing songs on Spotify’s platform in correlation with different attributes of the dataset (i.e. popularity with a particular or combination of attributes, amongst attributes themselves, etc.) The significance of this problem is that Spotify has multitudes of data which can be shared with artists in order to improve their likelihood of creating a top streaming song (which may be different than a song that does well in in-person concert environments) by giving creators valuable insights into how top performing songs are formulated and assembled. This in turn will help growing artists and increase the likelihood of artists who use data-based decision making to create top streaming music.

### Dataset
The dataset we have retrieved is from Kaggle (Elgiriyewithana, 2023) and is in a structured, tabular format (.csv file), with rows representing songs and columns representing different variables of the songs. This dataset was collected for the year of 2023 starting from January 1, 2023 to August 26, 2023.
This dataset was retrieved by the publisher leveraging the digital music streaming platform’s API such as Spotify’s Web API. It is due to this, that the dataset was able to include Spotify proprietary metrics. There is no behind-the-scenes access that would enable us to discover how these metrics were calculated, as it is within the realm of intellectual property and is patented. We have permission to use this dataset in alignment with a Creative Commons License which allows us to use, share, and adapt the dataset for our educational purposes.

### Guiding Questions
##### Data Visualization
Preamble: There are audio-specific features that are quantifiable measures (e.g. bpm, key, mode) and there are spotify-specific features that were generated by Spotify’s proprietary algorithms that provides percentile value (0-100%) for different descriptive ratings of the songs’ valence, danceability, energy, etc.
Focused guiding questions 1 and 2:
1. What proportion of popular songs share the same audio-specific features (e.g. bpm)?
2. Which of these Spotify-specific metrics (e.g. danceability) correlates best with the
number of streams?
Significance: The significance of these two questions lies in how it can provide a valuable business insight for artists and record labels on Spotify’s streaming platform and want to learn how to optimize their product. Essentially every music creator is interested in generating as many streams as possible since it will increase the value of their brand as well as generate revenue per stream. Knowing which dataset features can be repurposed into key performance indicators for top-streaming music will act as a guiding hand in creating a musical recipe that tends towards being highly successful on average.
Preamble & Significance: Spotify, Apple Music and various other platforms all provide music streaming services. Potentially, they are responsible for driving the popularity of any music and likely boost the streams on not just their own platforms but on others as well. Therefore, we aim to analyze the possibility of any synergy between the presence of the music across different platforms, on their charts and playlists as well.
Focused guiding question 3:
3. How are the number of streams on Spotify related to the number of playlists the song has
been added to (Spotify’s own platform vs its competitors like Apple Music)?

##### Statistical Analysis
For our first statistical question we would like to look at two variables, the number of artists and the number of streams. We would like to determine if songs that have multiple artists (2 or more) have more streams than songs with a solo artist on average. Then we would use the student's t-distribution and/or bootstrapping to determine this. Our second statistical question would be to investigate possible linear relationships amongst Spotify proprietary metrics (Ex. Energy (0-100% values) against acousticness (0-100% values)). For this we will use scatter plots/heatmaps to visualize any linear relationships. Then for a pair that demonstrates some reasonably strong linear relationship, we will perform a single-variable linear regression model to further investigate this. Our third statistical question we would like to look at is doing a proportion test between the populations of multiple vs. single artist songs, we then would go ahead and convert the speechiness % column into a categorical variable with songs having a a speechiness % of over 0.50 being labeled with “1” for strong speechiness and the rest being labeled with a “0.” We will then conduct a conventional prop.test and/or bootstrapping simulations in order to get to our final results for this question.
     
### Tasks
We will be performing the following data wrangling; removing missing values, stripping whitespace from strings, dropping columns that do not provide value, converting columns from categorical to numerical data types, changing the datatype of columns (eg.string to numerical conversion), indexing/slicing to retrieve relevant information, and normalizing the values between 0 and 1 into percentages. After a thorough review of this dataset, all of this data wrangling will be necessary in order to retrieve information that is relevant towards the desired analyses.
Some data visualizations we are interested in exploring are bar plots in order to compare difference categories, scatter plots in order to visualize relationships between 2 different variables, correlation matrices with heatmaps to see the correlations of the variables in a more visual way, histograms in order to visualize the distribution of different variables and possibly other plots.
We will be using pandas & numpy to deal with vectorized computation over structured, tabular data, matplotlib in order to visualize data, algebraic operators in order to perform basic mathematical operations to transform the data into more suitable format and datetime in order to work with dates in an easier and more efficient way.

### References
Elgiriyewithana, N. (2023, August 26). Most Streamed Spotify Songs 2023. Kaggle. https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023

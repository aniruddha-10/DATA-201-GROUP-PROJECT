Simple and basic Exploratory data analysis

# Simple and a basic Exploratory Data Analysis using Excel and Tableau 

We intend to explore and analyze the "INFLUENCE OF AGE ON PLAYERS IN THE GAME OF FOOTBALL" by following the simple Data Anaylysis Pipeline.

# Data Analysis Pipeline

Collection of data -> Cleaning of Data -> Analyzing -> Presenting 

# Main Goal of the Project 

TO IDENTIFY HOW AGE AFFECTS THE PERFORMANCE OF THE FOOTBALL PLAYERS.

# Data Collection Process 
We have downloaded a data set from an open web source (Kaggle) for obtaining our data for this project. 

The reason why we have chosen this particular data set as opposed to others is because it provides us with a lot of different and unique types of attributes which can help us in determining performances of players of different age groups. 

It also gives us insights about some of the very important player stats like GPM (goals per match) ratio and APM (assists per match) ratio, in accordance with their age. 

This helps us in coming up with better visualizations to showcase and represent interesting findings. 

This dataset has all the attributes for the players mentioned that can be useful for analyzing the players performance in the game, which helps us to show the link between a respective players performance and age.

The link for our data set can be found below :- 

https://www.kaggle.com/datasets/rishikeshkanabar/premier-league-player-statistics-updated-daily?select=dataset+-+2020-09-24.csv

# Analysis Questions 

Here are the five analysis questions that we have come up with that will enable us to get a better understanding of our project and its main goal.

1.	What is the average age of players in each of the different playing positions?

2.	At what age can we notice the biggest leap in terms of performance of players?

3.	At what age do we start seeing a decline in the performance of players?

4.	Which age group has the best performance and stats in terms of goals, assists, wins, points etc.?

5.	Does the effect of age on player performances vary with different playing positions?

# Cleaning of the Dataset 

We have used Excel to clean the dataset

The dataset we acquired had many attributes, most of them were not completely relevant to the topic we chose or the questions we wanted to answer.

Here we can observe the first couple of attributes that we decided were not necessary for analysis. The first one is jersey number; this number does not represent anything meaningful and as such we have decided to remove it. 

The next attribute is the players club, this once again has no bearing on performance or age, as one doesn’t necessarily perform better or worse because of their club and one certainly doesn’t age more or less because of their club, similarly, nationality was excluded for these reasons too, as it doesn’t really have a bearing on the questions we wanted to answer. 

There were also some attributes that we considered too specific or that were already included in another attribute. Headed goals, goals with right foot and goals with left foot were all too specific and could also simply be aggregated in the goals attribute, which is what we decided to do instead.

In the same vein, shots and shots on target are aggregated into the more advanced metric shooting accuracy, so we decided to analyze that instead as it provides more information than the raw data.

There were also some attributes that were a bit ambiguous and so they had to be removed as well, for instance, penalties and freekicks don’t include the data for the player who actually earned them, only the one who scored them, and since teams often have a specific player that shoots penalties or free kicks this doesn’t give us much information on the player that actually earned the penalty or free kick.

![image](https://user-images.githubusercontent.com/91339174/174402013-82f3a7f2-69ad-4f72-8ddc-30ea576b17f9.png)

This is how the dataset looked after the first bits of cleaning. After this we had to continue selecting the attributes we were going to remove

![image](https://user-images.githubusercontent.com/91339174/174402852-62cbb3a6-d293-4100-b9ec-9a36910e466c.png)

Following from before we have some specific attributes that are included in some other attribute, here we have hit woodwork and big chances missed which is included in the shooting accuracy attribute. 

The next thing to do was to remove data that only really pertains to one position, and as such we have also decide to remove the goalkeepers from our dataset, this was done because a lot of the data for goalkeepers is a bit biased, for example, a goalkeeper could have a lot of goals scored against them without doing anything particularly wrong, as usually a bad defense impacts the game more negatively than a bad goalkeeper, on the other hand a great goalkeeper on a team with a great defense may never have to make many saves and as such could have very little data despite being a great player. 

Similarly, we found that a lot of the data for certain attributes was really only concentrated on some players or positions, as such these were also removed, among them we had clean sheets, goals conceded, tackles, tackle success %, last man tackles, blocked shots, interceptions, clearances and headed clearances.

![image](https://user-images.githubusercontent.com/91339174/174403027-0163ca5d-e601-44e3-911a-1796433d57b4.png)

The next attributes to clean up were mostly the same, attributes that either didn’t provide any meaningful information, such as yellow cards, red cards, fouls and offsides. 

We also removed the remaining attributes that only really apply to goalkeepers and defenders, such as clearances off the line, recoveries, duels won, duels lost, successful 50/50s, aerial battles won, aerial battles lost, own goals, errors leading to goals, passes, big chances missed, passes per match, crosses, pass accuracy %, through balls, saves, penalties saved, punches, high claims, catches, sweeper clearances, throw outs and goal kicks. All of these attributes are either goalkeeper specific or defender specific and as such have been removed.

![image](https://user-images.githubusercontent.com/91339174/174403198-c4c2bd93-6dde-409c-b605-8401e93a5704.png)

![image](https://user-images.githubusercontent.com/91339174/174403237-7375a1ed-742c-484f-9d06-776d09f02419.png)

![image](https://user-images.githubusercontent.com/91339174/174403368-97f264e1-5e90-4a2c-a4df-19516c01a149.png)

With all that done we can take a look at our final 11 attributes, name, position, age, appearances, wins, losses, goals, goals per match, shooting accuracy, assists and assists per match. 

We can observe that there is some missing data in the goals per match, assists per match and shooting accuracy statistics, however we can simply find these by utilizing the other data in the set, for example both goals per match and assists per match are ratios of goals and assists with appearances, so we can deduce them from the present data. Similarly, shooting accuracy can be obtained from shots on target and total shots. 

![image](https://user-images.githubusercontent.com/91339174/174403453-dc1b4d37-3aa2-4921-a29e-4f4561e34f88.png)


                         FINAL LOOK AFTER CLEANING THE DATASET 

![image](https://user-images.githubusercontent.com/91339174/174403604-b9666990-8005-4c48-bb68-4610c6574473.png)

The attributes that we considered clean are name, age, appearance, position, wins, losses, goals and assists, as they had no missing data, were applicable to all positions and there were no misspellings or any other type of wrong data.

# Visualizations and Findings 

**QUESTION 1:  WHAT IS THE AVERAGE AGE IN EACH POSITION?**

![image](https://user-images.githubusercontent.com/91339174/174403818-49dc8844-69f4-427c-af89-0a6ee4e34640.png)

We chose horizontal bar charts in this visualization as they help us tell the average age in each position easily and even compare them with each other.
Based on this visualization, the average age for each position is almost the same age, being 25 years old for Forwards and Midfielders and 26 years old for Defenders. Therefore, there is not a significant age gap between players across different positions.

**QUESTION 2:  AT WHAT AGE DO WE HAVE THE BIGGEST INCREASE IN TERMS OF PERFORMANCE?**

![image](https://user-images.githubusercontent.com/91339174/174403866-d386e58a-d3be-4622-89be-acb9a787aabe.png)

For this question, we chose a line graph since it is the best and most effective graph to see the increases and decreases in performance. 
Based on our dataset, we decided that the best performance would be measured by goals per. The graph above shows us that while 32-year-old Football players have the most goals per match - therefore the best performance -, the biggest increase in terms of performance (goals per match) starts at the age of 19 and continues until the age of 22.

**QUESTION 3:  AT WHAT AGE DO WE START SEEING A DECLINE IN THE PERFORMANCE OF PLAYERS?**

![image](https://user-images.githubusercontent.com/91339174/174403943-3808d26b-a038-4651-a0a7-db27427368ea.png)

To consider a player’s performance we will be considering how player’s goals per match ratio differs in different ages. In order to do that we are using a scatterplot as it seems to be a pretty much useful in visualizing bivariate data.
As mentioned above to analyze the player’s performance we will see the greater the goals per match ratio the better the performance. The age group 20-25 have a high goals per match ratio which basically signifies the players belonging to that age group seem to attain their peak performance. Hence, we see the age group 34-40 seems to have a quite low goals per match ratio and we can say that the performance approximately starts to decline after 30.

**QUESTION 4:  WHICH AGE GROUP HAS THE BEST PERFORMANCE AND STATS IN TERMS OF GOALS, ASSISTS, WINS, POINTS ETC.?**     

Considering the different positions in football we evaluate this question in three parts. Each part devoted to one of three positions (forward, midfielder, defender)

**FORWARDS:**

In this section we focus on two attributes average goals per match and average shoot accuracy because they are the best measures for analysing a forward’s performance and try to find a trend according to age.

AVERAGE GOALS PER MATCH:

![image](https://user-images.githubusercontent.com/91339174/174404510-45e5a91d-a9a9-426a-a0b3-d5629d8cbf9d.png)

The reason for choosing this method of visualization is that line graph is a suitable way of visualizing data when it comes to showing the trend in one aspect. And since we are trying to find a relation between age and goals per match this is the perfect fit for our purpose.
Based on this line graph we have the highest average goals per match at the period between 28 to 32 years of age.

AVERAGE SHOOT ACCURACY:

![image](https://user-images.githubusercontent.com/91339174/174404792-250f99dd-5a31-41bf-b21a-2ca3f4480115.png)

The reason for choosing this method of visualization is that scatter plot is a suitable way of visualizing data when it comes to showing the trend in one aspect. Also, you can have a clear comparison between each age’s average shoot accuracy. And since we are trying to find a relation between age and shoot accuracy this is the perfect fit for our purpose. Based on this line graph we have the highest average shoot accuracy per the period between 28 to 34 years of age.

**FINAL CONCLUSION – FORWARDS**

Interestingly we realize the age for the best performance in the position of forwards is between 28 and 32.

**MIDFIELDERS:**

In this section we focus on two attributes average crosses per match and average assists per match because they are the best measures for analysing a midfielder’s performance and try to find a trend according to age.

Average crosses per match:

![image](https://user-images.githubusercontent.com/91339174/174405063-b209d6dd-65e1-4950-9dc7-db474ea1a496.png)

The reason for choosing this method of visualization is that scatter plot is a suitable way of visualizing data when it comes to showing the trend in a data set. Also, you can have a clear comparison between each age’s average cross per match. And since we are trying to find a relation between age and average cross per match this is the perfect fit for our purpose.

Based on this visualization we can conclude that the highest average for crosses per match has happened in the ages between 28 to 34.

Average assists per match:

![image](https://user-images.githubusercontent.com/91339174/174405151-d7eb3452-f451-481b-9927-062f91b56544.png)

The reason behind choosing line bar is to better visualize the difference of performance.

Between each two ages and since assist per match is an important variable for a midfielder it should be visualized in a way to be easy for the audience to get the average assists per match for each group of age.

Based on this visualization we realize the highest average assist per match has happened in the ages between 31 to 34.

**FINAL CONCLUSION – MIDFIELDERS:**

We can conclude that the best performance for a midfielder happens at the ages between 31 to 34. This can be related to their experience.

**DEFENDERS:**

Win rate :

![image](https://user-images.githubusercontent.com/91339174/174405352-79abec1f-1943-4465-b8b1-f14980a30020.png)

The reason for choosing this method of visualization is that scatter plot is a suitable way of visualizing data when it comes to showing the trend in a data set. Also, you can have a clear comparison between each age’s average cross per match. And since we are trying to find a relation between age and win rate this is the perfect fit for our purpose. Based on the information visualized here we realize when defenders from the age of 19 to 21 are playing the win rate is the highest.

Average goals received :

![image](https://user-images.githubusercontent.com/91339174/174405421-9c475b36-4d4b-41e3-a8e8-cbe0eeae5da7.png)

The reason behind choosing line bar is to better visualize the difference of performance 

Between each two ages and since average goals received per match is an important variable for defenders it should be visualized in a way to be easy for the audience to get the average goals received per match for each group of age.

This visualization shows that when defenders from the age of 19 to 21 are playing for the team the average goals received per match is lower and this indicates that the team performs better when young players are playing as defenders.

**FINAL CONCLUSION – DEFENDERS**

We can conclude that the best performance for a defender happens at the ages between 19 to 21.

**FINAL CONCLUSION:**

    Best performance		Defenders		Midfielders		Forwards  

     Age	                 19 – 21 		 31 – 34   		28 – 32

It seems age is an important aspect when it comes to performance for defenders being young is an advantage this can be due to the physical intensity of this position. In other hand we have midfielders this role doesn’t require high stamina this allows players to gain experience and improve so their best performance happens when they are older. This is not the case with forwards since this role requires stamina and speed so the performance in this position is related to both experience and physique hence the age of best performance is between 28 to 32 lower than midfielders and higher than defenders.

**QUESTION 5: DOES THE EFFECT OF AGE ON PLAYER PERFORMANCES VARY WITH DIFFERENT PLAYING POSITIONS?**

Hence to answer this question we will considering two different age group of players that is (25-30) and (20-24). Also Goals per match ratio will be used as a standard to determine the player’s performance. To visualize this we have used a pareto chart which has the different playing positions mentioned along the x axis and on the Y axis the total goals per match ratio as per the different playing positions. The graph you see below is for age group (25-30)


![image](https://user-images.githubusercontent.com/91339174/174406491-c961ca51-5397-4a07-abaa-bb92be6d8d96.png)

Hence we can see that players who have playing at forward seems to have higher goals per match ratio and then the midfielders having a cumulative goals per match ratio of around 15.24 and at the end we see defenders having the least goals per match ratio. 

This gives us an insight about the game that players who play at forwards generally are much more involved in the game as compared to other playing positions and thereby they seem to score more goals which technically results in higher goals per match ratio. Whereas on the other hand we have defenders, their primary role is to stop attacks during the game and prevent the opposing team from scoring goals which overall results in lower goals per match ratio for them.

Now if we try to visualize the same for age group (20-24) we found this: -

![image](https://user-images.githubusercontent.com/91339174/174406580-2a8516ff-5861-41b4-925e-15dc77f8029e.png)

We see there is a different situation for this particular age group so in this case Midfielders seem to have slightly higher goals per match than the forwards whereas the defenders still have the lowest goals per match ratio. This seemed to have happened as we took age into consideration for analyzing therefore we can conclude on the fact that age kind of affects the player’s performance playing at different position.

For these two visualizations we have chosen to use a pareto chart as it seems to be a perfect visualization for questions like this because it shows a pareto line which represents the cumulative percentage as well which helps to judge the added contribution of each category. Generally in a pareto chart the bars arranged from the largest to smallest which helps to visualize which factors comprise the 20 percent that are most critical.

## Feedback

If you have any feedback, please reach out to us at aniruddhakhan747@gmail.com

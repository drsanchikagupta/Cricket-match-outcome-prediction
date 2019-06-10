# Cricket-match-outcome-prediction
The Indian Premier League is a professional Twenty20 cricket league in India contested during March or April and May of every year by eight teams representing eight different cities in India.  
This is an analysis based project. Given 2 cricket teams, the batting order, bowling order and who bats first. We have to predict the score. The data of IPL matches is available from 2008-2018. So we have to train the model from data from 2008-2016 and test the model for 2018 IPL matches.  
The dataset is stored in HDFS and we are using spark mllib library for doing predictions on the data using 2 methods. 
Simulating the match, given 2 teams, batting order, bowling order and team that bats first. 

- Simulating a match ball by ball using Probability Statistics :
In the first method, we clustered the batsmen and bowlers separately and found the probability of the batsman scoring n runs(0-6) against the bowlers using these clusters. We have used k-means clustering for creating batsmen and bowler clusters.

- Simulating a match over by over with the help of Decision Tree
The next method involved building a decision tree and using its output to determine the output of the match.


Challenges
Challenges : Dealing with debutants:
From the player vs player statistics we compute group vs group statistics.
Using these we deal with 4 cases of debutant pair.
1) Existing bowler, debut batsman : An average statistic of existing bowler
class against all batsmen classes is computed.
2) Existing batsman, debut bowler : An average statistic of existing
batsman class against all bowler classes is computed.
3) Existing batsman , existing bowler (but new combination) : An average
statistic of existing batsman class against existing bowler class is computed.
4) Debut batsman , debut bowler : An average statistic of all batsmen
classes against all bowler classes is computed.

# RPGLite_disseration
## Repository dealing with dissertation on RPGLite, a game created by University of Glasgow for study on game balancing
## Summary of 2022 University of Glasgow MSc Data Science Dissertation

This study deals with quantitative balancing and user segmentation in a competitive video game based on user logs.

Technologies used : MySQL, Python (Scikit-Learn, Pandas, Numpy)
Things to know before reading :
1.	RPGLite
An experimental turn-based PvP game developed by the University of Glasgow as a study on game balancing. Players compete by picking 2 out of 8 classes with unique mechanics. This choice made by the players is referred to as ‘character pairs’. RPGLite had around 300+ players that played around 5800 games, and was serviced for a period of 2 months.
2.	Competitive Balance 
A concept that makes competitive games work. In Rock-Paper-Scissors, all options are valid because they have the equal chance of winning/losing/drawing. When the concepts get more abstract or complex, like ‘Warrior-Mage-Rogue’ (and their trope variations like ‘Warlock’, ’Barbarian’, ’Ninja’, etc.), then there could be many other variables in play. Competitive video games such as League of Legends or DOTA 2 are sensitive about this concept of Competitive Balance, as they must maintain the esports scene fresh and prevent users from dropping out due to repetition.

# Research Questions and Answers:

## RQ1: What are the demotivating factors in a competitive video game?

Quite obvious, but personal taste and some convenience, like most other mobile apps. Out of the 300+ players, around 170 players did not play more than 10 games.(The median of the number of games played was 10) Those players dropped out at the login screen (most likely to have lost login credentials), or at the tutorial. This could be attributed to the nature of gaming that video games tend to cater to a player niche, and players who do not like the aesthetics or turn-based games would have turned away at first sight. Also, this proves the importance of quality-of-life features such as password recovery.

## RQ2: What are the indicators of mastery in a competitive video game?

Users that develop mastery in a video game tend to be more attentive to their in-game performance, and change their choices accordingly. To observe this, players have been divided into two segments. There were players who developed mastery and achieved a win rate of over 50% over the game service period. However, there were also players who could not develop mastery of 50%-win rate and stagnated despite their long playtime. By looking at the data, it was concluded that Expert users tend to be more adventurous when exploring in-game choices. 


## RQ3: Could machine learning be used to predict user success? If so, how could an efficient metric be designed to reflect mastery?

Winners of a RPGLite match can be predicted using machine learning techniques, with the players’ skill metrics and character pair metric as the features. Among the techniques, Gaussian Naïve-Bayes works best. The models work best when the players’ win rates with the specific character pair(strategy) is used as the character metric. Furthermore, a more reflective skill point metric can improve model accuracy. The fact that predictions are not always correct could be attributed to the fact that the game has some elements of luck in it.

## RQ4: Could there be a quantitative way to find patch timings?

Linear regression was attempted, but it failed. As RPGLite does not provide in-depth performance tracking tools such as OpenDota or OP.GG, players could not track their performance in detail. Therefore, players rather rely on intuition or their whims. This research question led to the 5th research question, to attempt and measure intuition in quantitative terms with the data given.

## RQ5: What are the other factors that affect players’ decisions?

Without the tools to track their performance, users would rely on intuition, indicated by game length in this specific case. There were some character pairs which were popular despite low performance, and some pairs that showed good performance but had low preferences. This was attributed to the game length. Some users employed specific character pairs just for the sake of getting quickly done with the game, and due to the news that some characters were ‘buffed’ (made strong). Some strategies, especially the ones including the Healer class (as its name suggests, has mediocre damage output while mitigating some of the damage done, thus extending the gamespan longer by two turns on average) were very unpopular due to long game lengths. 

## Limitations

The biggest limitation was that the game RPGLite was out of service at 2022, and thus first-hand knowledge of the game has become unobtainable. Gameplay could only be hypothesized based on log data, and thus could not be observed firsthand. Furthermore, as user survey has become impossible, so no information about human-computer interaction or competitive gameplay from the users’ perspective was able to be surveyed. 

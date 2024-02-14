# ANOVA-Hypothesis_European-Soccer-Players
European Soccer Players  Analysis By Using ANOVA

DataSource: 
https://www.kaggle.com/code/jocelynallen/starter-european-soccer-database-5bfba1ad-d/data

This is a European Soccer Database, there are 7 tables in total, but we are going to use only two tables: Players and Player_Attributes to conduct our statistical Inference.We chose this data because we found that only these two tables have the same foreign keys  player_api_id and player_fifa_api_id providing a link to two tables, and therefore, we can conduct statistical analysis to see if there are significantly different of heading accuracy, ball control, overall rating and sprint speed over different height and weight categories. Besides, this data is sufficiently large(11060 entries after cleaning and merging)  to do ANOVA analysis.

Analysis or Model:
We conducted an ANOVA  test for each of the following:
1.	THere is a significant difference in heading accuracy over different height categories. 
2.	There is a significant difference in ball control over different height categories.
3.	There is a significant difference in balance over different weight categories. 
4.	There is a significant difference in overall player rating over different age groups.
5.	THere is a significant difference in free kick accuracy over different weight categories.
6.	There is a significant difference in sprint speed over different height categories.

To use ANOVA, the data must satisfy the following conditions (or be sufficiently large):

1.	The observations are independent within and across groups. 
-	Yes, each observation is a different player
2.	The data within each group is nearly normal.
-	Most of the dependent variables(heading_accuracy, ball_control,free_kick_accuracy etc.) are not normally distributed, therefore, a Box-Cox data transformation was conducted doing ANOVA testing. 
3.	Variability across the groups is about equal.
-	 We visually confirmed that this was the case for each hypothesis using boxplots.

Challenges: 
●	We need to make sure the normality of data before doing ANOVA analysis, so transforming skewed data into normally distributed data is a challenge for us
●	We are also  trying to double check normality of residuals after data transformation to ensure our ANOVA assumption.

Conclusions:
Correlation between Height and heading accuracy, Height and ball control
From above testing, we can conclude that taller players don't tend to have higher heading accuracy. The result shows that only those soccer players between 180 cm and 185 cm have significantly less heading accuracy compared with taller players(taller than 185cm), while there is no significant difference between players taller than 185 cm and players shorter than 185 cm.  In terms of ball control, we also can’t say the shorter the better, the same as heading accuracy, the soccer players between 180-185 cm is significantly less than those players taller than 185cm, but there is no significant difference between the rest groups.

Correlation between Weight and Balance
The Correlation between Weight and Balance analysis showed that weight between 163 and 175 lbs have a significant influence on the balance. There is no significant difference for players lighter than 163 lbs and those heavier than 175 lbs. Overall, this analysis of the balance with the attribute weight can indicate there’s an in-between weight that can help players to achieve a certain balance. It would be interesting to observe the correlation with the  attribute height that can affect the balance.

Correlation between Age and Overall rating
Our analysis showed that older players (25 and older) had significantly higher mean overall rating than younger players (under 25),  but there was no other significant differences in the older ages (25-44).  We reasoned that this could be for  a couple of reasons, both based on the assumption that older players have played longer than younger players..  First, the amount of player data would be much less for young, new, players.  This could lead to a lower overall rating.  Also, younger players may be at peak physical condition, but they are inexperienced.  Perhaps playing longer and becoming more familiar with soccer strategy gives the older players an advantage and an increase in overall rating.

Correlation between weight and free kick accuracy
Both the linear regression and the ANOVA analysis demonstrated that weight did not have a significant effect on free kick accuracy.
 Correlation between height and sprint speed
Our result suggested that the players higher than 185cm had a significant difference in sprint speed compared with those height from 180-185cm, but there are no significant difference between other groups, so we reject our hypothesis of taller players will have significantly greater sprint speed.


## 1.	Introduction

In professional football, determining the true impact of a player's actions presents a significant challenge. Most current approaches rely heavily on correlation-based methods, often using supervised learning to identify cause-and-effect relationships. Supervised learning techniques, though powerful in prediction, are typically limited to capturing patterns within the data without addressing the underlying causal mechanisms.

## 2.	Methods

We apply causal inference techniques using player tracking data from the 2024 NFL Big Data Bowl to assess the causal impact of defensive players on the outcomes of tackles. Specifically, we apply a doubly robust framework combining outcome regression and propensity score weighting to compute the Conditional Average Treatment Effect (CATE) for each defensive player. This CATE represents the estimated effect of a player making a tackle on the expected points added (EPA) during a play.

The features used in our models include the location, speed, acceleration, orientation, direction, and distance of all players on the field. This feature set enables the model to capture both the individual movements and interactions between players, allowing the analysis to account for the complex, nonlinear dynamics of football plays and better understand the true impact of each defensive action.


## 3.	Results

The Conditional Average Treatment Effect (CATE) distribution (left figure) shows that most values are negative, with a median CATE of -0.09. This indicates that the model has correctly learned that tackles limit offensive production by reducing the opposing team’s expected points. However, some CATE values are positive, suggesting that in certain instances, another defender may have contributed more positively to the play by having a greater impact on reducing the offensive EPA, possibly due to their positioning or involvement earlier in the play.
The scatter plot (right figure) compares the exp EPA of a tackle with the actual average EPA when tackles are made. The positive correlation (r = 0.66, R² = 0.44) helps validate our causal model's ability to identify the defensive players whose tackles have the most significant impact on limiting offensive gains. 

Figure 2 lists the top 20 defensive tackles based on their Conditional Average Treatment Effect (CATE) in our analysis. Many of the listed players have received accolades such as All-Pro and Pro Bowl selections during the 2022 season. This highlights the accuracy and validity of the model in identifying top-performing players based on the CATE metric.

## 4.	Conclusion

The application of causal inference to tackling in the NFL, as demonstrated in this study, provides an improved method for evaluating defensive player performance. As the field of sports analytics continues to evolve, leveraging models that capture causal relationships rather than relying solely on correlation-based methods will help teams make more informed decisions. We can extend this framework to model other positions.

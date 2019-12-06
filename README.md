# EECS731-The-Oscars
This is the project for the EECS 731 Data Science.

The project contains 2 folder, the 'data' folder with the data used and the 'pic' with one figure used in the notebook.

This project shares the same idea as our semester project, as well as one of the data set.

The general idea of this project is by visualizing the data, we will gain some intuitive knowledge which will give us some hints to choose the approach to solve the problem.
Here I focus on the housing price prediction problem, the most straight-forward way is to apply some regression models, here I use linear regression and MLP, to predict the housing price. But before throwing the data into the model, we might want to know which feature to use, so a heatmap is used to illstrate the correlation of other feature to housing price. The regression result of MLP is surprisingly good.

Then I treat the housing price as time series and the result is not as good as direct application of regression.

Last but not least, by clustering the data only using their geographic info, i.e., lat and lng, I found that the average price of each cluster differs from other cluster, even though some of the clusters are right next to each ohter. I also find that the joint distribution of number of living room and numer of bathroom shows some difference in the price associated with these 2 feature, so it might be possible to predict the housing price using classifier. To do this, we need first discretize the house price into several intervals, and then classify each data into, hopefully correct, interval corresponding to its price. Then predicted the price of that house as the mean of the interval. By doing this, we have more room to adjust the method used to predict the housing price and if we are able to classify all data correctly, we will bound the total error by the size of the interval, but the truth is, it's really hard to do so.

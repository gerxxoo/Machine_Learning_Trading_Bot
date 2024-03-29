# Machine_Learning_Trading_Bot

BACKGROUND

In this Challenge, you’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. Your firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, your firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave your firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. You’re thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, you’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.


PROJECT

This project requires to establish a baseline. After importing the CSV file and setting up the data frame, I generate trading signals using long and short SMA windows of 100 and 4 days, respectively. Whenever the actual return is greater than or equal to zero, I am signaled to buy. When the actual return  is less than zero, I am signaled to sell. Multiplying the actual returns by the trading signals, I am able to calculate the strategy returns. 

Then it is time to split the data into training and testing data sets. I assign my X and y train and test variables and then fit the X train and transform the X train and test variables. The next step is to create my svm model using the SVC calssifier model from SKLearn. I then fit and predict the svm model. 

The classification report is not flattering at all. The model has an accuracy of 0.55. The highest score is the buy signal's recall of 0.96; this means most opportunities to make money (buy) are identified. Conversely, the sell signal's recall of 0.04 tells me that the opportunites to protect the portfolio (sell) are not identified. Precision is more balanced. Buy's precision is 0.56, which means a little more than half of the buy signals were to be heeded. On the other had, sell's precision is 0.43, which lets me know a little less than half of the sell siganls were correct. 

Afterwards, I place the predicted values, actual returns, and strategy returns in one data frame. I finally plot the actual and strategy returns. The strategy returns exceed the actual returns. 

The next section is tuning the baseline trading algorithm. I import Gradient Boosting Classifier. I fit and predict the model. The classification report returns a lower accuracy of 0.46 for the tuned model. The other notable change is recall. Sell's is 0.86 while buy's is 0.14. Once again, I place the predicted values, actual returns, and strategy returns in one data frame and plot the two returns. 


CODE SOURCE

The code was sourced from classwork assignments. 


TECHNOLOGIES

This project uses pandas, numpy, matplotlib, hvplot, and SKLearn. I imported Gradient Boosting CLassifier, svm, StandardScaler, and classification report from SKLearn. I also used DateOffSet from pandas. The project was developed using Python on Visual Studio Code. 
<h1>Analyzing Ethereum's Blockchain - Full Analysis and Gas Price Prediction Models</h1>


<h2>Description</h2>

Welcome to the repository for the project "Predicting Ethereum Transaction Value." This project focuses on the application of machine learning models to predict transaction costs on the Ethereum blockchain by forecasting the average gas used per transaction. As Ethereum grows as a platform for decentralized applications, understanding and predicting transaction costs becomes crucial for users and developers.

### Introduction

In this project, I explore innovative applications of machine learning to predict transaction costs on the Ethereum network. My goal is to provide accurate estimates of transaction costs, which are essential for efficient blockchain operations and cost management. Using a comprehensive dataset of historical Ethereum transactions, I aim to build robust predictive models through backtesting methods commonly used in finance. This approach simulates real-world usage and assesses predictive accuracy, providing valuable insights for network stakeholders.

### Data Processing and Descriptive Analytics

I analyze Ethereum transaction data starting from August 2021, following the implementation of Ethereum Improvement Proposal (EIP) 1559, which introduced a new fee structure. My analysis includes trends in gas usage, average transaction counts, and average block sizes. I observe that gas usage has slightly decreased and stabilized over time, while the average transaction count per block fluctuates significantly but shows a downward trend. Additionally, the increasing average block size suggests higher complexity in transactions.

#### Macroeconomic Data

The macroeconomic landscape plays a crucial role in Ethereum transaction dynamics. I incorporate indicators such as interest rates and Ethereum price and trading volume into my models. These factors help me understand external influences on transaction costs, allowing for more comprehensive and accurate forecasts. For example, fluctuations in interest rates and Ethereum prices can impact transaction volumes and gas fees.

### Modeling Considerations

Several considerations are integral to refining my predictive models. The implementation of EIP-1559 requires adapting my models to incorporate features that capture the new fee dynamics, such as base fee per gas, tip per gas, block fullness ratios, and transaction inclusion priority. Additionally, the increasing number of Ethereum miners and broader market trends, including regulatory changes and macroeconomic conditions, influence transaction costs. These factors must be accounted for to ensure my models remain robust and reliable.

### Backtesting Models Aggregating by Time

I begin by aggregating data by various time intervals, including daily, hourly, 2 hours, 4 hours, and 8 hours. Using models like Linear Regression, XGBoost Regression, and Random Forest Regression, I apply backtesting to evaluate their performance. The Random Forest Regression consistently outperforms other models, particularly at higher aggregation levels, providing more accurate predictions of average gas usage.

### Backtesting Models Aggregating by Block

To further refine my predictions, I aggregate data by block amounts, including individual blocks, 2 blocks, 5 blocks, 10 blocks, and 20 blocks. The Random Forest model continues to demonstrate superior predictive accuracy, especially when aggregating data over more blocks. This approach highlights the importance of choosing appropriate aggregation levels for accurate forecasting.

### Advanced Financial Models

I explore more complex models, such as Prophet and DeepAR, to predict gas fees. Prophet, developed by Meta, excels at handling seasonal data and provides insights into transaction timing. DeepAR, using Long Short-Term Memory (LSTM) recurrent neural networks, shows promise in handling variable data with improved accuracy over traditional models. However, these models also have limitations, particularly in capturing the full complexity and variability of Ethereum transaction data.

#### Transformers

Transformers offer a novel approach to predicting Ethereum gas fees by processing entire sequences of data simultaneously. Their self-attention mechanisms and ability to handle complex patterns make them suitable for time-series forecasting in financial markets. Although initial results indicate underestimation of actual values, further refinement and integration of real-time data feeds could enhance their accuracy.

### Findings and Recommendations

My analysis reveals that the best times to transact on the Ethereum network are during periods of lower gas usage, such as between the end of Monday and the end of Thursday, and between May and August. These insights can help users plan transactions to minimize fees. Additionally, I calculate base fee fluctuations to offer another perspective on model performance, providing users with predictions of base fees for upcoming blocks and time intervals.

### Limitations

While my models provide valuable insights, several limitations need to be addressed. The restricted window frame of data used limits my ability to observe comprehensive trends. Model assumptions and the limited set of variables considered also impact predictive accuracy. Expanding datasets and incorporating more variables, such as the number of users transacting, could improve model performance.

### Conclusion

This study demonstrates the potential of machine learning models in predicting transaction costs on the Ethereum blockchain. By leveraging historical transaction data and advanced modeling techniques, stakeholders can gain actionable insights into cost management strategies, enhancing the efficiency and effectiveness of blockchain interactions. Despite the promising results, further research is needed to address limitations and refine predictive models for real-world applications.

<br />


<h2>Languages and Utilities Used</h2>

- Python</b> 
- SQL</b>
- Libraries: pandas, numpy, scikitlearn, seaborn, keras, tensorflow, pytorch</b>
- Models: Multivariate Regression, Random Forest, XGBoost, Gradient Boosting, Neural Newtowrks (LSTM), Transformers</b>


<h2>Program walk-through:</h2>

<p align="left">
<b>Table of Contents and Intro: <br/>
<img src="https://imgur.com/QHwp44Y.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/otR2BV0.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<b>The Data:  <br/>
<img src="https://imgur.com/svPKpbO.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/tz6r4to.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/Vo7jsXM.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/KkrGmU1.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<b>Models Performance:  <br/>
<img src="https://imgur.com/Q6O0Xbh.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/n0co7aT.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/5pUOQtP.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/Z8gbShS.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/jNlQJqS.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/i3E7tFJ.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/iOuuLuP.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/766SjlC.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/n9RdGv0.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/rYOfWUC.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/3uU1WYh.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/3Xpg15T.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<b>Findings & Recommendations:  <br/>
<img src="https://imgur.com/jCrgyF3.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />
<img src="https://imgur.com/XWgs0UO.png" height="80%" width="80%" alt="Eth Presentation"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

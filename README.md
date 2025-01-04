# Bank-Deposit-Subscription-Predictive-Model
## Business Problem
Term deposits are a reliable and low-risk source of funding for banks. By accurately predicting which customers are more likely to subscribe, the bank can maximize the number of term deposits thereby increasing its overall revenue. On the other hand, marketing campaign can be costly and time-consuming. By focusing on high-potential customers, the bank can allocate marketing resources more efficiently, reducing costs and improving the return on investment (ROI). 
## Business Goals
- Increased revenue
- Efficient Marketing
- Targeting customers efficiently
- Better decision-making regarding pricing, resources, product offerings
- Competitive Advantage
## Introduction
### About Dataset
The dataset contains 21 features, including customer attributes such as age, job type, marital status, education level, and loan status. It also includes campaign-specific details such as the type of contact (e.g., cellular), the month and day of the week when the contact was made, and previous campaign outcomes.
### Data Exploration
![image](https://github.com/user-attachments/assets/87854398-d542-4c07-ad1b-1e4790a98fc0)
Overall, conversion rate is 66%, a strong performance given the 39,00 total contacts. 

**Timing is crucial**. Thursday stands out as the most successful day for conversions, and married individuals, particularly those contacted via cellular phones, respond best. This suggests that targeting the right audience at the right time using the most effective communication method can further improve our success.

**Our audience demographics reveal more opportunities**. The majority of contacts are in administrative or blue-collar jobs, with most people aged between 20 and 50, especially in the 30-40 age range. Additionally, education levels are telling: university graduates and high school-educated individuals dominate our reach. Customizing messages for these groups could make a significant impact.

**Call duration also plays a critical role**. While many calls are short, we observe a clear trend: longer calls have a higher likelihood of converting. This emphasizes the importance of investing in meaningful and engaging interactions. Successful calls average 554 seconds.

**Seasonality is another factor**. Conversion rates peak in May, June, and July, highlighting the influence of seasonal patterns on engagement. Planning our campaigns around these high-performing months could yield better results.

**Timing post-contact** matters significantly. Contacts made within 30 days of the initial reach ouout show much higher success rates, whereas delays severely reduce the chances of conversion. Lastly, we see that economic conditions influence behavior, with a higher employment variation rate correlating positively with subscriptions.

**Client with housing loans** were more likely to subscribe to term deposits.
### Steps
- Data Pre-processing
- Exploratory Data Analysis using PowerBI
- Analysis of Machine Learning Models
- Model Explainability using SHAP framework
## Predictive Models and Evaluation
There are 3 models used for prediction, including tree-based models such as Random Forest, GBoost and linear model Logistic Regression.
![image](https://github.com/user-attachments/assets/0877259e-ea90-4586-800e-a117efedc98b)
Overall, the model (Random Forest Classifier) correctly predicted whether a customer would subscribe to a term deposit 92% of the time on the test data. This means the model is generally reliable in making predictions.
## Model Interpretability
1. Summary Plot
   ![image](https://github.com/user-attachments/assets/c3b0e2a8-ae27-4371-b306-595172d2e377)
The SHAP summary plot shows that duration is the most influential feature, with longer call durations positively impacting the likelihood of a successful outcome.
Economic indicators like nr.employed and euribor3m also have significant effects, where higher values generally decrease the model's output.
Features like pdays and campaign have moderate but varied influences on predictions.
2. Waterfall Plot
   ![image](https://github.com/user-attachments/assets/e6b54bfc-6fba-4dde-b6da-38b2322004f6)

   nr.employed strongly increases the likelihood of a positive outcome ("yes"), suggesting higher employment rates are linked with successful responses. Conversely, features like contact, job, and euribor3m decrease the likelihood, suggesting these factors negatively influence the probability of a successful outcome.
## Recommendation
While the model is highly accurate in predicting non-subscribers, there is a need to focus more on improving the identification of potential subscribers (currently at 44% recall). This could help us better target marketing efforts to increase term deposit subscriptions. 

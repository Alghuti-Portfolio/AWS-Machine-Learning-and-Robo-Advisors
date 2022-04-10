# AWS-Machine-Learning-and-Robo-Advisors
Lambda_Function

## Objective 
Develop a bot that will recommend an investment portfolio.

**Step 1**
- Configure the initial robo advisor: Define an Amazon Lex bot with a single intent that establishes a conversation about requirements to suggest an investment portfolio.

A. Criteria:

- Bot name: RoboAdvisor
- Language: English (US)
- Output voice: Salli
- Session timeout: 5 minutes
- Sentiment analysis: No
- COPPA: No
- Advanced options: No
- All other options: The default value

B. Add a new intent, and name it recommendPortfolio.

C. Configure sample utterances
- I want to save money for my retirement
- I'm {age} and I would like to invest for my retirement
- I'm {age} and I want to invest for my retirement
- I want the best option to invest for my retirement
- I'm worried about my retirement
- I want to invest for my retirement
- I would like to invest for my retirement

D. Create four slots:
![15-4-bot-slots](https://user-images.githubusercontent.com/103196346/162596166-da4cc0f1-d8fa-4566-a357-c12cccaeffd2.png)


**Step 2**
- Build and test the robo advisor: Make sure that your bot works and accurately responds during the conversation with the user.

**Step 3:** Enhance the robo advisor with an Amazon Lambda function: 

- Create an Amazon Lambda function that validates the user's input and returns the investment portfolio recommendation. This includes testing the Amazon Lambda function and integrating it with the bot.
- Develop a new Lambda function from scratch, and name it recommendPortfolio. 
- Add validation rules to recommend_portfolio:
  - The value of age should be greater than zero and less than 65.
  - The value of investment_amount should be greater than or equal to 5000.

- Result: bot should respond with an investment recommendation based on the selected risk level:

  - None: “100% bonds (AGG), 0% equities (SPY)”
  - Low: “60% bonds (AGG), 40% equities (SPY)”
  - Medium: “40% bonds (AGG), 60% equities (SPY)”
  - High: “20% bonds (AGG), 80% equities (SPY)”


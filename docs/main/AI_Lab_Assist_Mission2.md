---
#icon: material/folder-open-outline
icon: material/medal
---
## Feature Description

You can enhance communication efficiency and quality assurance in your contact center with the real-time transcripts feature. It allows agents to access real-time transcriptions of customer interactions directly on their Agent Desktop, enabling them to follow conversations more accurately and respond effectively.

Benefits:

**Accurate communication**: Captures conversations precisely, aiding understanding, especially with diverse accents or non-native speakers. <br/>
**Improved efficiency**: Eliminates manual note-taking, enabling agents to focus and resolve issues faster.<br/>
**Better performance**: Helps agents deliver timely, accurate solutions, boosting customer trust.<br/>
**Higher customer satisfaction**: Reduces misunderstandings, improving CSAT scores and experiences.<br/>
**Training and quality assurance**: Provides reliable references for coaching, evaluations, and compliance checks.<br/>
**Seamless integration**: Easily integrates with systems, optimizing queue-level management.<br/>
**AI support**: Enhances decision-making with complementary AI Assistant features.<br/>


## Mission Details

Your mission is to:

1. Configure a smoth handoff to live human agent from AI Agent.
2. Modify Virtual Agent transcript
3. Configure routing based on last used intent
4. Use AI Assistant

## Build

### Task 1 <span style="color: red;">[READ ONLY]</span>. Order Provisioning & Control Hub Settings

1. You should purchase the new AI Assistant SKU **A-FLEX-AI-ASST** from CCW.

2. Once you purchas the offer, admins with the appropriate profile and access controls will be able to see the AI Assistant menu in Control Hub. Post purchasing the offer, the customer can enable/disable the **Real-time Transcriptions** from the Control Hub.
   ![Profiles](../graphics/Lab1_AI_Agent/3.10.png)


3. The Agent needs to logged in to the Team that is configured with Desktop Layout that has AS 
    <br/>Agents Team:
   ![Profiles](../graphics/Lab1_AI_Agent/3.2.png)    
    <br/>Desktop Layout:
   ![Profiles](../graphics/Lab1_AI_Agent/3.4.png) 
    <br/>Desktop Layout file: Make sure **RT_TRANSCRIPT** widget is configured. 
   ![Profiles](../graphics/Lab1_AI_Agent/3.11.png) 
   <br/>Desktop Layout file: You can download preconfigured desktop layout here.
   [Desktop Layout](https://cisco.box.com/shared/static/o4nrnjengm6od7coql9etz3a3lwzvw1w.json){:target="_blank"}

### Task 2. Test Agent Transfer Summary Feature

1. Login to the Agent Deskopt and make sure you can see Agent Assistant widgit
   ![Profiles](../graphics/Lab1_AI_Agent/3.6.png)

2. Confirm that your Channel is still configured with the flow that includes the Autonomous AI agent, and the "Escalated" output is connected to the Queue node. This configuration is expected to remain the same as in the Autonomous AI Agent lab.
   ![Profiles](../graphics/Lab1_AI_Agent/3.7.gif)
---
#icon: material/folder-open-outline
icon: material/medal
---
## Feature Description

Agent Transfer Summary enhances agent efficiency and elevate customer experiences.

When a customer calls the contact center and interacts with a Virtual Agent (VA), they may request to speak with a live agent at some point during the conversation. Once connected to an agent, it is important for the agent to receive a concise summary of the customer's interaction with the VA. This summary provides the agent with a quick overview of the customer's call reason. The "Virtual Agent Handoff Summary" feature provides this summary, displaying it on the agent's desktop within the AI-Assistant Widget.

## Mission Details

Your mission is to:

1. Configure a smoth handoff to live human agent from AI Agent.
2. Modify Virtual Agent transcript
3. Configure routing based on last used intent
4. Use AI Assistant

## Build

### Task 1 <span style="color: red;">[READ ONLY]</span>. Order Provisioning & Control Hub Settings

1. You should purchase the new AI Assistant SKU **A-FLEX-AI-ASST** from CCW.

2. Once you purchas the offer, admins with the appropriate profile and access controls will be able to see the AI Assistant menu in Control Hub. Post purchasing the offer, the customer can enable/disable the summary features from the Control Hub.
   ![Profiles](../graphics/Lab1_AI_Agent/3.1.png)


3. The Agent needs to logged in to the Team that is configured with Desktop Layout that has AS 
    <br/>Agents Team:
   ![Profiles](../graphics/Lab1_AI_Agent/3.2.png)    
    <br/>Desktop Layout:
   ![Profiles](../graphics/Lab1_AI_Agent/3.4.png) 
    <br/>Desktop Layout file: Make sure **ai-assistant** is configured under the **advancedHeader**
   ![Profiles](../graphics/Lab1_AI_Agent/3.5.png) 

### Task 2. Test Agent Transfer Summary Feature

1. Login to the Agent Deskopt and make sure you can see Agent Assistant widgit
   ![Profiles](../graphics/Lab1_AI_Agent/3.6.png)

2. Confirm that your Channel is still configured with the flow that includes the Autonomous AI agent, and the "Escalated" output is connected to the Queue node. This configuration is expected to remain the same as in the Autonomous AI Agent lab.
   ![Profiles](../graphics/Lab1_AI_Agent/3.7.gif)

3. Place a test call and, for example, mention that you need some flowers for a wedding party. **Allow the AI Agent to complete its response before requesting to transfer the call to a live or human agent**. 

4. Become Available on the Agent Desktop and answer the call. You will see a window with the message **AI agent transfer summary is ready** pops up. You can click on View Summary from the window.
   ![Profiles](../graphics/Lab1_AI_Agent/3.8.png)

5. The **AI agent transfer summary is ready** notification will disappear after a few seconds. However, you can always reopen it by clicking on the AI Assistant widget.
   ![Profiles](../graphics/Lab1_AI_Agent/3.9.png)

<p style="text-align:center"><strong>Congratulations, you have officially completed this mission! 🎉🎉 </strong></p>
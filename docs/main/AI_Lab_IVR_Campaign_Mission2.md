---
#icon: material/folder-open-outline
icon: material/medal
---

## Mission Details

Your mission is to create a new campaign that will deliver call to your cellphone number. When you answer the call, you will be connected to the Blossom AI Agent for interaction.


### Task 1. Create Flow for the Campaign. 

1. Login to [Control Hub](https://admin.webex.com){:target="_blank"}

2. Go to Contact Center > Flows, click on **Creat Flow**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.3.png)

3. Click on **Start Fresh**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.4.png)

4. Name the flow as **<span class="attendee-id-container">OutDial_Flow_2000_<span class="attendee-id-placeholder" data-prefix="OutDial_Flow_2000_">Your_Attendee_ID</span><span class="copy" title="Click to copy!"></span></span>** and click **Create Flow**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.5.png)

6. In the Main Flow, add **End Flow** block and connect **New Phone Contact** block to the **End Flow** block. 
   ![Profiles](../graphics/Lab1_AI_Agent/8.6.gif)

7. Click on the **Event Flows**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.7.png)

8. Add **GoTo** node and connect it to **Outbound Campaign** node. 
   ![Profiles](../graphics/Lab1_AI_Agent/8.8.gif)

9. Click on **GoTo** node and configure it with the Flow that you created in earlier labs for AI agent. It could have the name Flow: **<span class="attendee-id-container">Autonomous_Scripted_Flow_2000_<span class="attendee-id-placeholder" data-prefix="Autonomous_Scripted_Flow_2000_">Your_Attendee_ID</span><span class="copy" title="Click to copy!"></span></span>** and click **Create Flow** if you completed all the previous lab. If you just started from this lab, then you need to create another flow with your Virual Agent. </br></br> Also Validate and Publish the Flow. 
   ![Profiles](../graphics/Lab1_AI_Agent/8.9.gif)

### Task 2. Create Outdial Channel for the Campaign.

1. Click on **Channels** then click on **Create Channel** 
   ![Profiles](../graphics/Lab1_AI_Agent/8.10.png)

2. Name the Channle as **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_2000_Channel_Outdial">Your_Attendee_ID</span>_2000_Channel_Outdial<span   class="copy" title="Click to copy!"></span></span>**. Select **Type** as **Outbound Telephony**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.11.png)

3. Configure **Service Level Threshold** with **300** seconds, select the flow that you have created in the previous Task, add a music on hold and select the Outdial Queue with name **LTRCCT-2000_Campaign_Q**<span class="copy-static" title="Click to copy!" data-copy-text="LTRCCT-2000_Campaign_Q "><span class="copy"></span></span>
   ![Profiles](../graphics/Lab1_AI_Agent/8.12.png)


### Task 3. Configure new Campaign. 

1. Login to [Webex Campaign Manager](https://traininglab.wxcc.webexcampaign.us/nextgen){:target="_blank"}
   ![Profiles](../graphics/Lab1_AI_Agent/8.1.png)

2. Click on **Campaign groups** and select LABCCL_2000 Group. 
   ![Profiles](../graphics/Lab1_AI_Agent/8.2.png)

3. Click on **Creat campaign**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.13.png)

4. Click on Dialer **Configuration**. Select Channel (Entry Point) that you have created in the previous Task. Dialer mode select as **Progressive IVR**. Then **Save changies**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.14.png)

5. Click on **Contact list source**, select **File**. 
   ![Profiles](../graphics/Lab1_AI_Agent/8.15.png)

6. Select preconfigured field mapping with name **2000_Lab**. Select experation value to **30** days. Then click on **Save changies**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.16.png)

7. Select **Daily schedule**. Configure the start day and active hours during the day. Then **Save changies**
   ![Profiles](../graphics/Lab1_AI_Agent/8.17.png)

8. Click on **Schedule exlusion dates** and just **Save changies**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.18.png)

9. Select **Contact attampt strategy** and click on **Configure**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.19.png)

10. Change the Cycle internval to **1** minute and click on **Save**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.20.png)

11. Once the attempts strategy is configurd, click on **Save changies**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.21.png)

12. Click on **Suppression rule sets**. Then select **Suppression rule not require** option. **Save changes**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.22.png)

13. Confirm that you would like to **Continue without supression rules**. 
   ![Profiles](../graphics/Lab1_AI_Agent/8.23.png)

14. Click on **Save & exit** the Campaign configuration. 
   ![Profiles](../graphics/Lab1_AI_Agent/8.24.png)

15. Name the Campaign as **<span class="attendee-id-placeholder">Your_Attendee_ID</span>_2000_Campaign**. For **P&L** from the list select **TrainingAB_PL_17748776940323**. For **Purpose** select from the list **Sales**, and click on **Save campaign**.
   ![Profiles](../graphics/Lab1_AI_Agent/8.26.png)

16. You will see you campaign will show up in the **DRAFT** status. 
   ![Profiles](../graphics/Lab1_AI_Agent/8.27.png)

### Task 4. Upload Contact List. 


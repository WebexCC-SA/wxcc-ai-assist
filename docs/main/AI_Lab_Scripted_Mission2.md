---
#icon: material/folder-open-outline
icon: material/medal
---

### Mission Details

Your mission is to review preconfigured Scripted AI Agent for tracking existing order. If you would like to build it by yourself there are BONUS Missions 3,4,5 and 6 of this lab. 

### Build

#### Task 1. Review the Configurations in AI Studio to track an order. 

1. Go to AI Studio and open AI Agent with name ***180_Scripted_AI_Agent***<span class="copy-static" title="Click to copy!" data-copy-text="180_Scripted_AI_Agent"><span class="copy"></span></span>. Kindly asking not making any changes to this agent, as this lab is for review purposes only for the entire group.
    ![Profiles](../graphics/Lab1_AI_Agent/6.69.png) 


2. Below is the diagram for tracking order flow. If the caller asking to track an order, **track_order** intent should be used as it has utterances like **Can you track my order** and others. This itent is configured to collect required **Entity**, for this the interaction will be moved to the interium response with name **order_number**.  
    ![Profiles](../graphics/Lab1_AI_Agent/6.68.png) 

3. Open up ***180_Scripted_AI_Agent***<span class="copy-static" title="Click to copy!" data-copy-text="180_Scripted_AI_Agent"><span class="copy"></span></span>
 AI agent. Click on **Script > Intents** and then open up **track_order** intent. 
     ![Profiles](../graphics/Lab1_AI_Agent/6.70.png) 

4. If this intent is triggered (customer request match the Utterances), then system will initiate the response **order number** until the required entity is filled or the number of retries is exceeded.
     ![Profiles](../graphics/Lab1_AI_Agent/6.71.png) 

5. Once the entity is filled, the system initiates the final response for this intent. In this case, it is **track_order**.
     ![Profiles](../graphics/Lab1_AI_Agent/6.72.png) 

6. Click on Entities and review **order_number** Entity configuration. 
     ![Profiles](../graphics/Lab1_AI_Agent/6.73.gif) 

#### Task 2. Send the data from AI Agent to Voice Flow​.

1. Click on **Responses** and open up response with name **track_order**
     ![Profiles](../graphics/Lab1_AI_Agent/6.74.png) 

2. Review the response configurations. 
     ![Profiles](../graphics/Lab1_AI_Agent/6.75.png) 

3. Go to [Control Hub](https://admin.webex.com){:target="_blank"} > Contact Center. Click on **Flows** and open up flow with name ***Autonomous_Scripted_Flow_2000_180***<span class="copy-static" title="Click to copy!" data-copy-text="Autonomous_Scripted_Flow_2000_180"><span class="copy"></span></span>.
     ![Profiles](../graphics/Lab1_AI_Agent/6.76.gif) 

4. Click on lower VirtualAgentV2 block. You will see the Activity Output Variables. The Entity value can be found in VirtualAgentV2.MetaData. 
     ![Profiles](../graphics/Lab1_AI_Agent/6.77.png) 

5. Click on the next **SetVariable** block and you can see that we just assigned the value from Activity Output Variable from the previous **VirtualAgentV2** block to the flow variable with name **MetaData_Scripted_Agent**. This is optional step. 
     ![Profiles](../graphics/Lab1_AI_Agent/6.78.png) 

6. Click on **Parse** block. It is configured to parse data from **MetaData_Scripted_Agent** variable using JSON path **$.ordernumber** and assign the respon to the flow variable with name **order_id**.
     ![Profiles](../graphics/Lab1_AI_Agent/6.79.png) 

7. Open up **HTTP Request** block. It is configured to to send **GET** request with the parameter as the order_id value to retrive the resposne specifically for this order. 
     ![Profiles](../graphics/Lab1_AI_Agent/6.80.png) 

8. If I would do the same request from Postman for the order Id 17, here the information I would get. 
     ![Profiles](../graphics/Lab1_AI_Agent/6.81.png) 

9. While on **HTTP Request** node, scorll down and you will see the configurations to parse the data from the response. It is configured to use JSON path **$.[0].status** and assign the response to the variable with name **order_status**.
     ![Profiles](../graphics/Lab1_AI_Agent/6.82.png) 

10. For examle if I would need to parse the status of the order 17 using this JSON path, the result would be "new".
     ![Profiles](../graphics/Lab1_AI_Agent/6.83.png) 

#### Task 3. Send the data from Voice Flow to AI Agent. 

1. To send data back to AI Studio we need to use one more VirtualAgentV2 block. Click on it to review configurations. You can see that we use the same Scripted AI agent **180_Scripted_AI_Agent**, but we also configured the State Event. The **Evant Name** will refare to the response on AI Studio. And the **Evant Data** contains the result of the **order_status** that can be retrived from the AI Studio.  
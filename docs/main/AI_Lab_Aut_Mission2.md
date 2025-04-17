---
#icon: material/folder-open-outline
icon: material/medal
---



# Mission 2: Configure Action to create an order.

 **<details><summary>What is Action? <span style="color: orange;">[Optional]</span></summary>**
An action is a functionality that lets your AI agent connect with external systems so it can perform more
complex tasks, such as bookings or finding information. 

For more information visit [Webex Documentation](https://help.webex.com/en-us/article/ncs9r37/Webex-AI-Agent-Studio-Administration-guide#concept-template_5ea99e1f-a679-4cf9-8e33-7a4f83d9f66a){:target="_blank"}


</details>
---


## Mission overview
Your mission is to:

Configure an action to collect order details from the customer and send them to a third-party application via APIs.

---

## Build

### Task 1. Create Service and AI Agent Flow in Webex Connect. 

1. From Control Hub, go to Contact Center and open up Webex Connect Portal. 
    ![Profiles](../graphics/Lab1_AI_Agent/2.9.gif)



2. Create new Service with name **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_2000_Service">Your_Attendee_ID</span>_2000_Service<span   class="copy" title="Click to copy!"></span></span>**
    ![Profiles](../graphics/Lab1_AI_Agent/2.10.gif)


3. Click on Flows and create new flow with the name <b>Create_Ordedr_Flowers.</b>
    ![Profiles](../graphics/Lab1_AI_Agent/2.11.gif)

4. From the Integrations list select AI Agent. 
    ![Profiles](../graphics/Lab1_AI_Agent/2.12.gif)

5. For now, save the flow and make it live. We will return to configuring this flow later. Creating it now is necessary to complete configurations in the AI Studio Portal.
    ![Profiles](../graphics/Lab1_AI_Agent/2.13.gif)
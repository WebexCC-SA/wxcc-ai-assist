---
#icon: material/folder-open-outline
icon: material/medal
---

### Mission Details

In the previous **Mission 4**, you configured a fulfillment flow that executes an API call in the WxCC Voice flow based on the order number and parses the order status. In this mission, you will configure the flow to return this status to **AI Studio** so that the Scripted AI agent can deliver the result back to the caller.


### Build

#### Task 1. Add VirtualAgentV2 block to bring data back to AI Studio.

1. To deliver the call back to AI Studio, you need to add an additional **VirtualAgentV2** block to the flow. Open **<span class="attendee-id-container">Autonomous_Scripted_Flow_2000_<span class="attendee-id-placeholder" data-prefix="Autonomous_Scripted_Flow_2000_">Your_Attendee_ID</span><span class="copy" title="Click to copy!"></span></span>** and click **Create Flow** flow. Click on **Edit** the flow. 
    ![Profiles](../graphics/Lab1_AI_Agent/6.56.gif)

2. Delete the **Disconnect Contact** node and add **VirtualAgentV2** node. Connect **HttpRequest** block to **VirtualAgentV2** block. 
    ![Profiles](../graphics/Lab1_AI_Agent/6.57.gif)

3. Click on **VirtualAgentV2**. In the Contact Center AI Config serach for scripted and select **Webex AI Agent (Scripted)**. Under the Virtual Agent option, search for the Scripted AI Agent with name **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_Scripted_AI_Agent">Your_Attendee_ID</span>_Scripted_AI_Agent<span class="copy" title="Click to copy!"></span></span>**.
    ![Profiles](../graphics/Lab1_AI_Agent/6.58.gif)

4. Connect Escalated output from the **VirtualAgentV2** node to the **Queue** node.
    ![Profiles](../graphics/Lab1_AI_Agent/6.59.gif)

5. Add **Disconnect Contact** node and connect **Handled** output to the **Disconnect Contact** node.
    ![Profiles](../graphics/Lab1_AI_Agent/6.60.gif)

6. You can publish the flow at this point. 
    ![Profiles](../graphics/Lab1_AI_Agent/6.61.gif)

#### Task 2. Add VirtualAgentV2 block to bring data back to AI Studio.
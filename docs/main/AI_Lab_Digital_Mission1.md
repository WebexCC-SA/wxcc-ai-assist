---
#icon: material/folder-open-outline
icon: material/medal
---
## Introduction

#### Mission Objective

In this mission, you can review the tasks required to complete the basic web chat configuration. All the configurations shown in this mission are preconfigured for you in this lab. This serves as a reference guide in case you wish to build this integration for your customer in the future.


### Task 1. Find your Service.
1. Login to Webex Connect Portal.
Go to **Services** and look for the service that you have created earlier. The name should be **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_2000_Service">Your_Attendee_ID</span>_2000_Service<span   class="copy" title="Click to copy!"></span></span>**
   ![Profiles](../graphics/Lab1_AI_Agent/4.1.png)

### Task 2. Configure and Register Chat Asset.

1. While on Webex Connect portal, go to ***Assets*** -> ***Apps***, press ***Configure New App*** and select ***Mobile / Web*** option.
   ![Profiles](../graphics/Lab1_AI_Agent/4.2.png)


2.  Input ***Name*** as Agent Name: **Chat_App_<span class="attendee-id-placeholder">Your_Attendee_ID</span>_2000**

3.  Toggle/enable ***Live Chat / In-AppMessaging*** to ***ON*** and choose ***Primary Transport Protocol*** as **`MQTT`** & ***Secondary Transport Protocol*** as **`Web Socket`** then tick ***Use Secured Port*** checkbox and press ***Save*** button.
   ![Profiles](../graphics/Lab1_AI_Agent/4.3.png)
>**Note**: If there is an error that your request cannot be processed, please press ***Save*** button one more time.



4.  Once asset is saved, press ***Register To Webex Engage*** at the top. 
   ![Profiles](../graphics/Lab1_AI_Agent/4.4.png)

5. Choose **<span class="attendee-id-placeholder">Your_Attendee_ID</span>_2000_Service** from the drop-down list and press ***Register*** button.
   ![Profiles](../graphics/Lab1_AI_Agent/4.5.png)

6.  Check and make sure the asset has been succesfully registered to the service and  ***Register To Webex Engage*** button has been greyed out.
   ![Profiles](../graphics/Lab1_AI_Agent/4.6.png)


7.  Return to ***Assets*** -> ***Apps***, find ***ChatAsset***, copy ***App ID***, paste it into the text file and save. We will use it when configuring chat flow later.
   ![Profiles](../graphics/Lab1_AI_Agent/4.7.png)


## Task 3. Create Entry Point for Chat

1. Login to Control Hub and go to Channels and click on **Create Channel**.
   ![Profiles](../graphics/Lab1_AI_Agent/4.8.png)


2.  Input ***Name*** as **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_2000_Chat_Channel">Your_Attendee_ID</span>_2000_Chat_Channel<span   class="copy" title="Click to copy!"></span></span>**
   ![Profiles](../graphics/Lab1_AI_Agent/4.9.png)

3. Select **`Chat`** from the ***Channel Type*** drop-down list. Select **Chat_App_<span class="attendee-id-placeholder">Your_Attendee_ID</span>_2000** as an ***Asset Name***. Set ***Service Level Threshold*** as **`360`** and click on **Save**.
   ![Profiles](../graphics/Lab1_AI_Agent/4.10.png)




## Task 4. Create Queue for Chat

1.  While on the **Control Hub** portal go to Queues and click on **Create a queue**.
   ![Profiles](../graphics/Lab1_AI_Agent/4.11.png)



2. Input ***Name*** as **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_2000_Chat_Queue">Your_Attendee_ID</span>_2000_Chat_Queue<span   class="copy" title="Click to copy!"></span></span>**. Also select **`Chat`** in the ***Channel Type*** section.
   ![Profiles](../graphics/Lab1_AI_Agent/4.12.png)

3. Scroll down to **Chat Distribution** click on ***Add Group*** and select **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_2000_Team">Your_Attendee_ID</span>_2000_AutoAI_Lab<span   class="copy" title="Click to copy!"></span></span>**
   ![Profiles](../graphics/Lab1_AI_Agent/4.13.gif)

4. Set ***Service Level Threshold*** as **`7200`** seconds (2 hours). Set ***Maximum Time in Queue*** as **`10800`** seconds (3 hours). Click on ***Save*** after comparing your values with the screenshot below.
   ![Profiles](../graphics/Lab1_AI_Agent/4.14.png)


## Task 5. Website Widget Configuration

-  Login to WxCC Management Portal access the menu and cross launch Engage Portal by choosing ***New Digital Channels***.



-  Go to ***Assets*** -> search and edit ***Chat_Asset*** which you have created in Connect Portal.



-  Scroll down and click on ***Save Changes*** button.
-  Scroll to top of the page and choose ***Websites*** tab.
-  Click on ***ADD Website***.



-  Fill in the respective fields as per the table below:

| **Parameter Name**                | **Parameter Value**            |
| ----------------------------- | -------------------------- |
| Chat Widget Language          | English-US                 |
| Display Name                  | Webex CC Chat Demo         |
| Byline Text                   | Web chat of the future     |
| Button Text                   | Start Chat                 |
| First message                 | Hello! Welcome to the chat |
| PCI Compliance Banner Message | This chat is PCI compliant |
| Domain                        | www.w3schools.com          |
| Set wait time                 | Disabled                   |
| Set Chat Announcement         | Enabled                    | 

-  Scroll down and click on ***Save changes*** button after comparing your values with the screenshot below.


-  Scroll up, select ***Appearance*** and change the settings:
	- \[Optional\] Widget Color
	- \[Optional\] Widget Button Type
	- \[Optional\[ Logo
	- Enable Emojis
	- Enable Attachments
-  Press ***Save changes*** button at the bottom of the page.


 
-  Scroll up, select ***Widget Visibility*** tab and make sure that ***Force Turn Off Widget*** switch is disabled.  Then select ***Widget Visibility*** as ***Show without any restrictions*** and save changes.



-  Now click on ***<*** arrow near ***Website Settings*** and go-back to edit your chat asset.



- Select ***Installation*** then click on ***Copy*** to copy the chat script to clipboard.




 
-  Paste copied script into a text editor and save it. We will paste it on web site later.

## 7. Create Chat Inbound Flow

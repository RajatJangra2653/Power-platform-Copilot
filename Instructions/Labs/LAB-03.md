## Lab-03: Build a basic Power Automate flow in Microsoft Copilot Studio.

### Task-01: Create a new topic.

1. Login to **https://copilotstudio.microsoft.com/** and get started login with the **<inject key="AzureAdUserEmail"></inject>** and choose the **Region** and enter the **dummy phone number**

   ![screenshot of the prompt ](../Media/getstarted.png)

2. Choose the **Copilot** Environment .

   ![screenshot of the prompt ](../Media/copilot-env.png)

   
3. Create a new copilot named **User 1 Contoso Customer** 

   ![screenshot of the prompt ](../Media/newcopilot.png)

   ![screenshot of the prompt ](../Media/03/login-2.png)
	
3. Select the **New Topic** drop down at the top of the page and **choose the From Blank** 
  option. Enter **Check Weather** as the name of your topic.

   ![screenshot of the prompt ](../Media/fromblk.png)

5. Click on edit Phrases then enter simple trigger phrases, such as **What is the weather** and **What is the temperature today**, until you have at least five trigger phrases. Select the **Edit** button within the node to open a pane to the right of the screen where you can add the trigger phrases.

   ![screenshot of the prompt ](../Media/03/phrases.png)

6. Create a **new Question node** below the trigger phrase node and then enter text, such as: `Of course, I can share the weather with you! Can you tell me the name of the region where you want to know the weather?`

   ![screenshot of the prompt ](../Media/3.1/question.png)

7. Rename the variable to **Region**. To do so, select the name of the variable within the node. Within a pane that appears to the right of the screen.

   ![screenshot of the prompt ](../Media/3.1/phraese1.png)

8. Within the top right corner of the screen, select the **Save** button to ensure that your work is saved.

 ## Task-02: Create your Power Automate flow

1. Select the **Add node button** below the question node to add a new node to the topic. Select **Call an action > Create a flow**. Power Automate opens in a new browser window 

   ![screenshot of the prompt ](../Media/get-flow.png)

2. Click on In the first node **Run a flow from copilot** new flow window that opens, select the **Add an input** within the first scaffolded action. Then, select **Text**.

   ![screenshot of the prompt ](../Media/3.1/2.png)
       
   ![screenshot of the prompt ](../Media/3.1/3.png)

3. Within the first column, enter `Region` (leaving the second column empty).

   ![screenshot of the prompt ](../Media/3.1/4.png)

4. Then, select the **Insert new step** button to **add a new action**.

5. Select the **Add an action** option from the menu.

6. Enter `weather` in the search bar and then select **Get current weather by MSN Weather**.
    
   ![screenshot of the prompt ](../Media/3.1/weather.png)

7. A new node appears, where you can enter the location , from the Dynamic content drop-down menu, select **Region** and then keep units as **Imperial**.

   ![screenshot of the prompt ](../Media/3.1/getcurrent.png)

8. Select the **Return value(s) to Microsoft Copilot Studio** node at the end of the flow, then select **Add an output > Number** . Place your cursor in the **Enter a value to respond** text box. Select **Temperature** from dynamic data to add it to the response text box. Then, enter **Temperature** in the Title field.

   ![screenshot of the prompt ](../Media/03/temperature.png)

9. The flow is almost complete, select the template title and rename it to `Get Temperature`.

10. Select **Save** on the flow in Power Automate to ensure that it saves. Wait a moment until the green banner appears, indicating success then Select **Publish** .

## Task-03 : Connect a Power Automate flow with Microsoft Copilot Studio.

1. In this task, you connect a Power Automate flow with Microsoft Copilot Studio `https://web.powerva.microsoft.com`

2. Open your existing topic in Microsoft Copilot Studio, entitled **Weather**, and return to the bottom of your flow, as shown in the following screenshot. Select **Call an action**. Your new Power Automate flow displays in the list. From the list, select **Get Temperature**.

   ![screenshot of the prompt ](../Media/get-tem-last.png)

   >**Note**: If the flow does not show up, save the Check Weather topic and refresh the page.

3. Select **Enter or select a value** and then select the **Region** variable that you created in previous steps of this lab. 

   ![screenshot of the prompt ](../Media/last-3s.png)

4. Add a Condition node so that you can check if the **Temperature** variable is greater than 75.

5. For the true branch, if the Temperature is greater than 75, add the following text within the 
   Message node:
   `For {Topic.Region} the temperature is {Topic.Temperature} and that is getting warm! Consider cooling off with one of our cold brew coffees.`

      >**Note**: The braces { } are variables to display dynamic data. To enter variables into the node, use the {X} button on the Message node and then select a variable from the list.

6. For the All other conditions branch, add the following text within the message node: `The temperature for {Topic.Region} is {Topic.Temperature}`. Where the braces { } are variables to display dynamic data.
   
   ![screenshot of the prompt ](../Media/last-ss.png)

   ![screenshot of the prompt ](../Media/last.png)

7. To end the conversation, select the **Add node** button below the condition. Select **Topic management** and then choose **End conversation**.


   ![screenshot of the prompt ](../Media/3.1/endcon.png)

8. **Save** your topic using the button found in the top right corner of the screen and then Click on **test your copilot** and test it out 

   ![screenshot of the prompt ](../Media/3.1/endotput.png)
	
9. You successfully created a Power Automate flow and a new topic in Microsoft Copilot Studio that used the flow to provide real-time data from an external service to the user.


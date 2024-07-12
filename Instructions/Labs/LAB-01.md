# Lab-01: Create a canvas app with Copilot in Power Apps.

### Task 1 – Create environment
 
1. Open a new browser tab and navigate to the Power Platform admin center `https://aka.ms/ppac` 

2. Log in using the following Username **<inject key="AzureAdUserEmail" enableCopy="true"></inject>** and Password **<inject key="AzureAdUserPassword" enableCopy="true"></inject>**.
 
3. Skip the welcome tour by closing the prompt, or select **Get Started** to begin the tour and select **Next** through each prompt. At the end, select **Done** to finish the tour.
 
4. Select **Environments** from the site navigation and select **+ New** from the toolbar.

   ![screenshot of the prompt ](../Media/new11.png) 

5. For **Name**, enter **Copilot**

6. For **Type**, select **Sandbox**.

7. Change the toggle on **Add a Dataverse data store?** to **Yes**. Leave all other selections as default and select **Next**.

   ![screenshot of the prompt ](../Media/coco.png) 
 
8. On the **Add Dataverse** tab, under **Security group** use the **+ Select** button, and under **Open access**, select **None**.

   ![screenshot of the prompt ](../Media/sel.png)

   ![screenshot of the prompt ](../Media/non.png)

9. Select **Done** and select **Save**.
 
10. In the list of environments, your **Copilot** environment should now show as **Preparing**.

11. Your practice environment will take a few minutes to provision. Refresh the **Environments** list if needed.
 
12. When your environment shows as **Ready**, select your **Copilot** environment by selecting the ellipses next to the name to expand the drop-down menu and select **Settings**.
 
13. Explore the different areas in **Settings** that you are interested in but do not make any changes.

## Task–02: Create an app with Copilot.

1. On the Home page in Power Apps `https://make.powerapps.com`

2. Make sure you in the environment you previously created, in the center text field, enter the following prompt to search for an AI-generated table **build an app to manage real estate showings** , Select the Send button.

   ![screenshot of the prompt ](../Media/01/copilot-chat-prompt-1.png) 

3. After Copilot AI generates a table based on your prompt, look through the table to view the columns that are created for the start of your table.

   ![screenshot of the prompt ](../Media/01/copilot-table-1.png)

4. In the text box, in the lower part of the Copilot pane to the right of the screen, enter the following text: **add a column to track client full name**.Select the Send button.

   ![screenshot of the prompt ](../Media/01/copilot-table-new-column-1.png)

    >**Note**: Copilot notifies you that the table is updated, and the new column should show as being added to the table.

4. In the text box, in the lower part of the Copilot pane to the right of the screen, enter the following text: **add a column to track client email**. Select the Send button.

    ![screenshot of the prompt ](../Media/copilot-table-new-column-email-1-2.png)

    >**Note**:
    > - The data that's generated in your table might vary from the data that's shown in the table in the screenshots for this lab.
    > - The Suggestions section in the lower-left corner of the screen provides you with different suggestions on how you can add to and modify your table.

5. In the text box, in the lower part of the Copilot pane to the right of the screen, enter the following text:	**add an option for “Completed” to the Status column**. Select the Send 
   button.

   ![screenshot of the prompt ](../Media/01/edit-table-1.png)


6. The system might take a minute to load. When it does, the Status column shows as updated and includes the option for Completed.

7. Select the Status column name dropdown menu and then select View column where you can view the columns’ properties and the current status details and data.

8. The status choices should be Pending, Confirmed, Cancelled, and Completed,Select the X in the upper-right corner of the pane to close it.

9. Next, you'll add more data to your table and the existing columns. In the Copilot pane text box, enter and send the following text: **add 5 more rows of data** Five more rows of data are added for each existing column in the table.

    ![screenshot of the prompt ](../Media/copilot-table-new-rows-1-1.png)

10. In the text box, in the lower part of the Copilot pane to the right of the screen, enter the following text: **add a column to track Client Address**. Select the Send button
(2), To create the app, select the Create app button in the lower-right corner of the screen.(3)

    ![screenshot of the prompt ](../Media/01/client-address-1.png)

    > **Note**: Your table should have several columns. However, to continue following the modules in this learning path, try to remove some columns that you won't use:The list of columns that you need are: ID ,	Address , Date , Time , Status , Agent Name, Client Full Name, Client Email.

11. When the app first loads, a dialog might appear stating Welcome to Power Apps Studio. If so, select the Skip button.

12. The app that has been built for you should show in Edit mode.

    ![screenshot of the prompt ](../Media/01/reordsgallery-1.png)


## Task–03: Make edits using Copilot to edit your app.

1. Within the **Data** pane To the right of the table, select the **ellipsis** From the menu select **Edit data**.

   ![screenshot of the prompt ](../Media/copilot-edit-data.png)

2. Select the ID column header from the table.	From the dropdown menu, select the Edit column option.
   
   ![screenshot of the prompt ](../Media/01/copilot-edit-column-1.png)
  
3. In this example, you don't want the Data type to be a Single line of text. To change that value, go to the Edit column pane, and then from the Date type dropdown menu, select # 
     Autonumber,Select Save.Select the Close button in the lower-right corner of the Edit table dialog.

   ![screenshot of the prompt ](../Media/01/save-column-1.png)

4. The table should now show as Refreshed in the Data pane.

   ![screenshot of the prompt ](../Media/01/copilot-refreshed-table-1.png)

5. Modify the gallery in the application so that it displays the relevant data. Select the Tree view icon to return to the Tree view.

6. On the app's main screen, select RecordsGallery1 to display Real Estate Showings and then select the edit button to put the gallery in edit mode.

   ![screenshot of the prompt ](../Media/01/editing-1.png)

7. Select the Title and then set the Text value to the following formula: **ThisItem.'client Address'**
  
8. Select the Subtitle and then set the Text value to the following formula: **ThisItem.'Client Email'**
    
9. Select the Body and then set the Text value to the following formula: **ThisItem.Status**

10. A single record in the gallery should now resemble the following image.

    ![screenshot of the prompt ](../Media/01/copilot-checkmark-2.png)

11. On the app's main screen, select the Form control.

    ![screenshot of the prompt ](../Media/copilot-checkmark-1-1.png)

12. On the Properties pane on the right, under the Fields property, select Edit fields.

    ![screenshot of the prompt ](../Media/01/copilot-edit-fields-1.png)

13. In the Fields pane, expand the ID field.

14. From the Control type dropdown menu, change the type to View text.

    ![screenshot of the prompt ](../Media/01/copilot-view-text-1.png)

    >**Note**:previously changed the ID field to Autonumber, you don’t want users entering their own number; Dataverse automatically enters the numbers for you.

15. In the Fields pane, select the X in the upper-right corner to close the pane.

16. Make a new request for a property that shows in the app by selecting the **Play** button from the upper part of the screen.

    ![screenshot of the prompt ](../Media/01/copilot-play-1.png)

17. In the left pane, select the +New button.

    ![screenshot of the prompt ](../Media/01/copilot-new-1.png)

18. Though you could modify the form to automatically fill in the fields for you, for this lab, you'll complete this step manually to observe how the app works.

    ![screenshot of the prompt ](../Media/copilot-checkmark-1-1.png)

19. Fill in the fields with the following information:

    - Agent Name - < Your name >

    - Client Full Name - < Your name >

    - Client Email - < Your email >

    - Date - < Any future date >

    - Time - < Any future time >

    - Status - Pending

    - Address - 210 Pine Road, Portland, OR 97204

  > **Note** : This address is one of the addresses from the Microsoft Excel file in Module 1, and it's the same file that you uploaded and turned into the Real Estate Properties 
   table.Though you'd usually have a lookup field to the Real Estate Properties table, this lab doesn't provide one to keep it simple.

20. Select the check mark in the upper-right corner of the screen.

21. Screenshot of the completed form, showing the check mark that you select to save your changes.

22. Select the X in the upper-right corner to close out of the app.

23. If a dialog appears saying Did you know?, select OK.

24. The new request is added to the left of the list of requests.

25. From the upper part of your screen, select the Save button to save the new app that you created.

    ![screenshot of the prompt ](../Media/copilot-save.png)

26. If the system prompts you, save the app name as Real Estate Showings.

27. Exit the app to return to the Power Apps home page.

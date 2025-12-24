<!-- suite
id: @Sa8d7faeb
emoji: 
-->
# Product Retail

### Requirements

<!-- test
id: @T333af346
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Access the Product Retail application on DM Platform

### Description
Accessing the Product Retail application from the welcome page

### Requirements
The Product Retail Model is already deployed on the DM Staging QA Platform.
You can use the following Github workflow to deploy the two tutorials models
https://github.com/semarchy/platform-designer-xdm-test/actions/workflows/build-deploy-QA.yml
- Click on Run workflow top open the input selection
- Select a datasource not used for ProductRetail and CustomerB2C
- Click on Run workflow
- Wait until the end of the workflow to see the link of the deployed applications
If there is an error in the workflow, it is very likely that the datasource you selected is already used. In that case, either select another datasource or ask other QAs if you can delete the data location.

### Steps
1. Make sure you use a user with **semarchyAdmin** role in an incognito windows - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users
2. Locate the Data products widget.
    *Expected:* The Data product widget is visible 

3. Click on the deployed Product Retail application to access it's features.
    *Expected:* The application opens on the Global Search page

<!-- test
id: @T979fe186
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Import data

### Description
Follow the "Import, fix and delete data" of the Semarchy Product Retail Demo

### Requirements 
The xslx files in the Attachments section of this test have been downloaded
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
1. Access the Product Retail MDM application in the QA tenant in Staging environment
2. Click on “Start Here” to begin the data import process
    *Expected:* Cards are displayed to import different kind of objects

3. Click on Import Brands
    *Expected:* A file picker component is displayed

4. Select the file 3-import-data-1-brand.xlsx
    *Expected:* A preview of the data is displayed

5. Click Continue
    *Expected:* On the Define mappings step, the columns from the Excel file are correctly mapped to the Brand columns

6. Click Continue
    *Expected:* A summary of the data to be imported is provided

7. Click Finish
    *Expected:* The data are imported to DM but only visible to you

8. Click Finish in the lower-right corner to submit the data to the hub
    *Expected:* Wait until the confirmation messages "New data submitted" and "Changes successfully applied" appear in the pop-up toaster menu located at the lower-left corner of your screen

9. Redo the import operations for Families, Subfamilies, Sizes using the appropriate xlsx files
    *Expected:* All the imports should be successful

10. Click on Import Products
    *Expected:* A file picker component is displayed

11. Select the 3-import-data-5-product.xlsx file
    *Expected:* A preview of the data is displayed

12. Click Continue
    *Expected:* On the Define mappings step, the columns from the Excel file are correctly mapped to the Product columns

13. Click Continue
    *Expected:* A summary of the data to be imported is provided

14. Click Finish
    *Expected:* The data are imported to DM but only visible to you

15. Click Finish in the lower-right corner.
    *Expected:* You will encounter a Found data validation issues pop-up that alerts you to errors in the recently imported spreadsheet

16. Click Proceed anyway to close the window and save the records
    *Expected:* Wait until the confirmation messages "New data submitted" and "Changes successfully applied" appear in the pop-up toaster menu located at the lower-left corner of your screen

17. Redo the import operations for Items and Item images using the appropriate xlsx files
    *Expected:* All the imports should be successful

18. In the left menu, click on Product Catalog
    *Expected:* 5 cards are displayed : All Products, By Family, By Brand, All items and All item images

19. Click on All Item images
    *Expected:* You should see records

<!-- test
id: @T55ccedd9
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Fix Data

### Description
Follow the "Rectify and Delete records" of the Semarchy Product Retail Demo

### Requirements 
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
1. Access the Product Retail MDM application in the QA tenant in Staging environment
2. Click on “Browse Errors” in the left navigation panel
    *Expected:* 7 cards are displayed for errors related to all types of objects. A 5 is displayed in Product Errors card

3. Click on Product Errors
    *Expected:* 5 records should be displayed

4. Select the first product in the list. : Airstrides Contrails Speedy Cross-trainers
5. Click on the tab "Error Details" to view the reason, the customer record was rejected
    *Expected:* The error message, "Brand MANDATORY", indicates that this customer record is missing a brand

6. Rectify the error, open the option menu in the upper right corner and click on "Edit"
    *Expected:* A stepper interface opens and provides step-by-step guidance for editing the customer record

7. Select the brand from the icon picker
8. Choose the first option, Air Strides
9. Click Continue
10. Click Finish on the Additional Attributes step

    *Expected:* The toaster messages in the lower-left corner pops up with the message "New data submitted" and "Changes successfully applied" are displayed

11. Click "click to Refresh"
12. Return to the Product Errors
    *Expected:* You should notice fewer errors in the list, as one has been corrected

13. Repeat the process to rectify other erroneous records
14. Navigate to Browse errors > Products Errors
    *Expected:* You should see no error now

<!-- test
id: @Tf12446b8
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Delete Data

### Description
Follow the "Rectify and Delete records" of the Semarchy Product Retail Demo

### Requirements 
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
1. Access the Product Retail MDM application in the QA tenant in Staging environment
2. Click on Reference Data in the left menu panel (More section)
    *Expected:* 3 cards should be displayed : Family hierarchy, Brand details and Sizes

3. Click on Sizes
    *Expected:* Records should be displayed

4. Select the first two sizes under the Boys clothing product family (Sizes 00 and 0 are not valid)
5. Open the Options menu
6. Select the Delete option
    *Expected:* A confirmation message will appear, reminding you that this action cannot be undone once completed

7. Click Delete
    *Expected:* You will receive a confirmation toaster message in the lower-left corner stating "2 record(s) sent for deletion."

8. Open the Options menu and select Refresh to refresh the data
    *Expected:* The 2 sizes just deleted should not be there anymore

<!-- test
id: @T435da7d1
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Browse Data

### Description
Follow the "Browse data" of Semarchy Product Retail Demo

### Requirements
You are logged-in using Business user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+2@semarchy.com
password : TXXE#GKCET76ALiM

### Steps
1. Access the Product Retail MDM application in the QA tenant in Staging environment
2. In the left navigation panel, click on Search to access the Global Search
3. Type "pencil" in the Search text field.
    *Expected:* You should see one result

4. Select the result, Blackberry Slim Pencil Skirt
    *Expected:* You should see product details like Brand name, Product family, Product subfamily, Sales unit, Material and country of origin

5. Click on the items tab
    *Expected:* You should see the variety of sizes and colors in which the product is offered

6. Click on All Products in the left navigation menu (Quick Access section)
7. Click on the Filter icon in the upper-right corner
    *Expected:* The filter menu appears

8. Keep the default search type on Full-text
9. In the search Text field, type "skirt"
10. Click Apply at the top of the filter to execute the search
    *Expected:* The search should return 6 product records

11. Click on "Save as" in the lower-right corner of the filter menu to save this search
12. In the Save filter as field, enter "Skirt"
    *Expected:* After clicking Save, the app takes you to the Filters menu where you can see all the saved filters you or your coworkers created previously and shared with you

13. To share the Skirt filter, click on the Options button next to the Skirt filter
14. Select Share
    *Expected:* You should see the confirmation message "Filter ‘Skirt' is now shared with all users."

15. Click New Filter
16. In the Search Text field, type "casual"
17. Press Enter on your keyboard
    *Expected:* The filter should be applied and the search should return only one record called Leslie Styles Women Contrast Color Stripes T-shirt, because both the Skirt and casual filters are enabled

18. Save this new filter with the name Casual
19. In the Filters tab, disable the Skirt filter and click Apply
    *Expected:* You should observe that only the product results from the Casual filter are displayed

20. In the Quick Access section of the navigation drawer, click on By Family
    *Expected:* You will see product data categorized by product families using a hierarchy view

21. Click on the Men's shoes product family in the tree view.
    *Expected:* You will find the subfamily categories listed under this product family

22. Click on the arrow icon next to Men's shoes to expand the hierarchy
23. Continue to drill down the Sub Families hierarchy
24. Expand the Business node
    *Expected:* You see a list of all the men's business shoes

25. Select the product called Murphy's Classic Leather Shoe in the tree view
    *Expected:* This action opens a detailed form view for this product

26. Click on the Items tab
    *Expected:* You will see a list of the different sizes the Murphy's Classic Leather Shoe product comes in

27. Click on the item with a size 6
    *Expected:* You can see the item information for this particular size of the Murphy's Classic Leather Shoe

28. Click on the Images tab
    *Expected:* You will find three images associated with this item

29. In the Quick Access section of the navigation drawer, click on All Products
30. Click on the second column's header, which should be labeled ID
    *Expected:* The arrow should be pointing upwards to sort the records by ascending order based on their ID number

31. Click on the first product in the table, which should be Simmi Professional Suits from the brand Giorgio for Men
32. Open the Options menu in the upper-right corner of the application
33. Select Graph View
    *Expected:* A graph has been generated

<!-- test
id: @T6907d831
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Author Data

### Description
Follow the "Author" of Semarchy Product Retail Demo

### Requirements 
You are logged-in using Business user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+2@semarchy.com
password : TXXE#GKCET76ALiM

### Steps
1. Access the Product Retail MDM application in the QA tenant in Staging environment
2. Click on “Add Product” in the left navigation panel
    *Expected:* A workflow is initiated to add a new product
3. Enter the following data on the General Information step:
        ID: 10011
        Name: Polka Power
        Brand: Rainbow Scout (click the picker button and select Rainbow Scout from the list)
        Family: Girls clothing (select this option from the drop-down menu)
        SubFamily: Dresses & Skirts (type dress into the field and select the option in the drop-down menu)
        Description: Polka Power is a polka dotted sleeveless dress with a frill hem and puffy skirt. This is a fashionable and affordable dress for all girls.
        Image: https://s3.amazonaws.com/semarchy-tutorials/10011-MAIN.jpg

4. Click Next and, on the Additional Attributes step, enter the following data:
        Sales Unit: Piece
        Material: 60% Cotton, 35% Linen, 5% Spandex
        Made in: Vietnam
        Care Instructions: Machine wash gentle cycle, hang to dry.

5. Click Next and, on the Item step, enter the following data:
        UPC: 31234568090
        Size: 6 (type in the number 6)
        Color: Red (select this option from the drop-down menu)
        Color Description: Polka dot red and white
        Primary Image: https://s3.amazonaws.com/semarchy-tutorials/10011-MAIN.jpg

6. Click Next and, on the Item Image step, enter the following data:
        Label: Front view - Polka dot red and white
        Image URL: https://s3.amazonaws.com/semarchy-tutorials/10011-MAIN.jpg

7. Click on Go to list
    *Expected:* You are now back to the list of images.

8. Click Add another
9. Enter the following data for the second item:
        UPC: 31234568091
        Size: 8 (select this option from the drop-down menu)
        Color: Red (select this option from the drop-down menu)
        Color Description: Polka dot red and white
        Primary Image: https://s3.amazonaws.com/semarchy-tutorials/10011-MAIN.jpg

10. Click Continue and add the image information to the Polka Power in size 8 item.
        Label: Front view - Polka dot red and white
        Image URL: https://s3.amazonaws.com/semarchy-tutorials/10011-MAIN.jpg

11. Click Go to list
    *Expected:* The item image you just added is now saved, and you will be redirected to the Items step

12. Click Go to list again
    *Expected:* The item information is now saved, and you will be redirected to the Products step

13. Click Send to review
    *Expected:* You will receive a confirmation toaster message in the lower-left corner stating "Changes successfully applied"
14. Add a comment "ready for review" and click OK
    *Expected:* You will receive a confirmation toaster message in the lower-left corner stating "Workflow in progress"
15. Logout from the Business user account and login using Data steward account in a new incognito window (pierrick.tassery+1@semarchy.com / TyXSqr7zcS#Acnsj )
16. Access the Product Retail MDM application in the QA tenant in Staging environment
17. Click My Tasks in the navigation drawer
    *Expected:* Under the To Do category, notice there is one pending Approve Product workflow that is assigned to you    
18. Select the checkbox next to the task in the table view, then select Start from the action menu to initiate the workflow
19. Make any edits you deem necessary
20. Click Continue to proceed to the next step of the stepper
21. Click the Save to xDM button once you are ready to save and publish this new product to the hub
22. On the final screen, enter the comment "review approved" and click OK
    *Expected:* A toaster notification in the bottom-left corner of the screen indicating "Workflow completed"

<!-- test
id: @T5072d58e
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# About Box

### Description
Review the product version and build type in the about box.

### Requirements 
Make sure you use a user with semarchyAdmin role - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
1. Access the Product Retail MDM application in the QA tenant in Staging environment
2. Navigate to the top-right corner of the Product Retail MDM application interface
3. Click on the User avatar icon (or the profile circle showing the user’s initial)
4. In the dropdown menu that appears, click About
    *Expected:* The “About” dialog should appear and display details about Product Version, Build information, Git commit and two links "Learn more about Semarchy" and "Manage license"

<!-- test
id: @Tc1196706
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Application Localization - French

### Description
Open an Application with the Language set to French


### Requirements 
Make sure you use a user with semarchyAdmin role - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
1. Access the Product Retail MDM application in the QA tenant in Staging environment
2. Click on the User icon on the top right of the screen
3. Click on Profile
4. Go to the Preferences tab
5. Update Language from English to French
6. Click on Save
7. Navigate through several screens and check buttons, labels, and tooltips to make sure they are translated in French
8. Update Language from French to English for the next tests

<!-- test
id: @Te8720d1d
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Import ProductRetail Dashboard

### Description
Import ProductRetail dashboard and check that there is no error

### Requirements
Download the zip file in the Attachments section of this test
Make sure you use a user with semarchyAdmin role in an incognito windows - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
1. Go to the welcome page of QA tenant in Staging https://dm-qa.na.staging.semarchy.net/welcome
2. Open the Dashboard builder in the Tools section
3. Hover the + symbol and click on import application
4. Select the file ProductRetailDashboard.zip downloaded earlier
5. Click on Create
    *Expected:* The Dashboard should be imported and displayed in the list of applications

6. Click on ProductRetailDashboard
7. Toggle the Visible Parameter
8. Go to the datasources tab
9. For ProductRetail, make sure the datasource selected is the one where your NRT model has been deployed
10. Come back to the welcome page
    *Expected:* You should see the Dashboard imported (Product Retail Dashboard)

11. Click on the Dashboard logo corresponding to your dashboard
    *Expected:* You should see no error and the Product Metrics dashboard should be displayed

12. Go to the Data Quality tab
    *Expected:* You should see no error and data should be displayed

<!-- test
id: @Tf6724d38
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Check that deployed ProductRetail model works fine

### Description
Check that ProductRetail model that was already deployed works correctly 

### Requirements
Make sure you use a user with semarchyAdmin role in an incognito windows - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
1. Access the Welcome page in the QA Staging environment
2. Click on the deployed Product Retail application called "0 Product Retail (do not delete)" with a hand stop sign logo
    *Expected:* The application opens on the Global search page

3. Go to the different parts of the app to make sure there is no issue
4. Create a Product from the All Products tab
    *Expected:* There should be no error

<!-- test
id: @T05e807dd
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Check that deployed ProductRetail dashboard works fine

### Description
Check that ProductRetail dashboard that was already deployed works correctly

### Requirements
Make sure you use a user with semarchyAdmin role in an incognito windows - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
- Access the Welcome page in the QA Staging environment
- Click on the deployed Product Retail dashboard called "0 Product Retail Dashboard_DoNotDelete" with a hand stop sign logo
    Expected: The dashboard opens without any error
- Go to the different parts of the dashboard to make sure there is no error

<!-- test
id: @T06310b01
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Dashboard Localization - French

### Description
Open a Dashboard with the Language set to French


### Requirements 
Make sure you use a user with semarchyAdmin role - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
1. Access the Product Retail Dashboard you have deployed earlier in the QA tenant in Staging environment
2. Click on the User icon on the top right of the screen
3. Click on Profile
4. Go to the Preferences tab
5. Update Language from English to French
6. Click on Save
7. Navigate through several screens and check buttons, labels, and tooltips to make sure they are translated in French

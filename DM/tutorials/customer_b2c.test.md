<!-- suite
id: @S6360151e
emoji: 
-->
# Customer B2C

### Requirements

<!-- test
id: @T591e787c
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Access the Customer B2C application on DM Platform

### Description
Accessing the Customer B2C application from the welcome page

### Requirements
The Customer B2C Model is already deployed on the DM Staging QA Platform.
You can use the following documentation to deploy the model https://semarchy.atlassian.net/wiki/spaces/QA/pages/4217667586/DM+-+Deploy+a+model+using+Design+CLI

### Steps
1. Make sure you use a user with semarchyAdmin role in an incognito windows - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users
2. Locate the Data products widget.
    *Expected:* The Data product widget is visible 

3. Click on the deployed Product Retail application to access it's features.
    *Expected:* The application opens on the Global Search page

<!-- test
id: @Tf95bc480
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Import data

### Description
Follow the "Import data" section of the Semarchy Customer B2C Demo
https://semarchy.com/tutorials-content/customer-b2c-demo/#3

### Requirements 
The xslx files in the Attachments section of this test have been downloaded
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
1. Access the Customer B2C MDM application in the QA tenant in Staging environment
2. Click on “Start Here” to begin the data import process
    *Expected:* Cards are displayed to import different kind of objects

3. Click on Import Nicknames
    *Expected:* A file picker component is displayed

4. Select the file 3-import-data-1-Nicknames.xlsx
    *Expected:* A preview of the data is displayed

5. Click Continue
    *Expected:* On the Define mappings step, the columns from the Excel file are correctly mapped to the Brand columns

6. Click Continue
    *Expected:* A summary of the data to be imported is provided

7. Click Finish
    *Expected:* The data are imported to DM but only visible to you

8. Click Finish in the lower-right corner to submit the data to the hub
    *Expected:* Wait until the confirmation messages "New data submitted" and "Changes successfully applied" appear in the pop-up toaster menu located at the lower-left corner of your screen

9. Click on Import Customers
    *Expected:* A file picker component is displayed

10. Select the 3-import-data-2-Customers.xlsx file
    *Expected:* A preview of the data is displayed

11. Click Continue
    *Expected:* On the Define mappings step, the columns from the Excel file are correctly mapped to the Product columns

12. Click Continue
    *Expected:* A summary of the data to be imported is provided

13. Click Finish
    *Expected:* The data are imported to DM but only visible to you

14. Click Finish in the lower-right corner.
    *Expected:* You will encounter a Found data validation issues pop-up that alerts you to errors in the recently imported spreadsheet

15. Click Proceed anyway to close the window and save the records
    *Expected:* Wait until the confirmation messages "New data submitted" and "Changes successfully applied" appear in the pop-up toaster menu located at the lower-left corner of your screen

16. Redo the import operations for Products, Communications andCustomers' Products and Item images using the appropriate xlsx files
    *Expected:* All the imports should be successful

17. In the left menu, click on Customers
    *Expected:* Records should be displayed

18. Click on the Antonia Mattos record
19. Click on the Communications tab
    *Expected:* You should see Communications records
20. Click on the Products tab
    *Expected:* You should see Products records

<!-- test
id: @T982058c8
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Fix data

### Description
Follow the "Rectify and Delete records" of the Semarchy Customer B2C Demo
https://semarchy.com/tutorials-content/customer-b2c-demo/#4

### Requirements
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
1. Access the Customer B2C MDM application in the QA tenant in Staging environment
2. Click on “Browse Errors” in the left navigation panel
    *Expected:* 5 cards are displayed for errors related to all types of objects. A 5 is displayed in Customer Errors card and a 3 on COmmunication Channel Errors card

3. Click on Customer Errors
    *Expected:* 5 records should be displayed

4. Select the first record in the list : Winnie Gouker
5. Click on the tab "Error Details" to view the reason, the customer record was rejected
    *Expected:* The error message, "SourceEmail MANDATORY", indicates that this customer record is missing an email address

6. Rectify the error, open the option menu in the upper right corner and click on "Edit"
    *Expected:* A stepper interface opens and provides step-by-step guidance for editing the customer record

7. Click Next to proceed to the Contact info step
8. Add the email address winnie@gouker.com in the second step
9. Click Finish to submit your changes

    *Expected:* The toaster messages in the lower-left corner pops up with the message "New data submitted" and "Changes successfully applied" are displayed

10. Click "click to Refresh"
11. Return to the Customer Errors
    *Expected:* You should notice fewer errors in the list, as one has been corrected

12. Repeat the process to rectify other erroneous records using the following information
Hanna Waetzig: hanna@waetzig.com
Mikel Pete: mikel@pete.com
Marlon Gouker: marlon@gouker.com
Jack Guzzetta: jack@guzzetta.com
13. Navigate to Browse errors > Customers Errors
    *Expected:* You should see no error now

<!-- test
id: @T4e72b441
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Delete data

### Description
Follow the Delete records section of "Rectify and Delete records" of the Semarchy Customer B2C Demo. 
https://semarchy.com/tutorials-content/customer-b2c-demo/#4

### Requirements 
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
1. In the Browse Data section of the navigation drawer, click on Customers
2. Click on the Filter icon in the upper-right corner of the application
    *Expected:* The filter menu appears

3. Keep the default Search type on Full-text
4. In the Search Text field, type "Marquis"
5. Click Apply at the top of the filter to execute the search
    *Expected:* The search should return one customer record: Marquis Barayuga

6. Select the checkbox next to Marquis Barayuga's record
7. Click the Options button
8. Select the Delete option
    *Expected:* A confirmation message will appear, reminding you that this action cannot be undone once completed

9. Click Delete
    *Expected:* You will receive a confirmation toaster message in the lower-left corner stating "1 record(s) sent for deletion."

10. Open the Options menu and select Refresh to refresh the data
    *Expected:* You should see no records

<!-- test
id: @T42646652
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Review matches and merges

### Description
Follow the "Review matches and merges" section of the Semarchy Customer B2C Demo
https://semarchy.com/tutorials-content/customer-b2c-demo/#5

### Requirements 
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
- In the Quick Actions section of the navigation drawer, click Confirm Matches
    *Expected:* Here, you can find all the customer and prospect records that DM merged together based on the defined match rules

- Examine the Confirmation Status, Confidence Scores, and Masters Count columns.
    *Expected:* You can see some records are NOT_CONFIRMED or PARTIALLY_CONFIRMED. These records require manual confirmation because their confidence scores did not meet the Auto-Confirm threshold in the matcher.

- Click on the Last Name column header until the arrow points upwards to sort all customer records in alphabetical order (from A to Z) based on the Last Name value
- Select the Select All checkbox to mark all records for review in a duplicate manager
- Open the Options menu
- Click Review And Confirm Matches
    *Expected:* A duplicate manager opens

- Hover your mouse over the golden-colored display tile to view information about the golden record
    *Expected:* Information about the golden record are displayed (status, confidence score, masters numbers)

- Click on the golden tile
    *Expected:* The Record details side panel appears on the right side of your screen and provides detailed information on the golden record

- Click on the eye icon on the upper-right side of the side panel
    *Expected:* A comparison table explains the golden record, detailing how the underlying master records match and contribute data to the golden record

- Click Close in the lower-right corner
- Once you are back to the duplicate manager again, click Next to go to the next golden record
- The next golden record to review is Mary-Ann Markes, Open the record in a duplicate manager
- Examine the record details for Mary-Ann Markes
    *Expected:* → Note discrepancies in birth dates across the six master records, while contact information remains consistent. Consulting with the Marketing team confirms that Dec 31, 1899, is a placeholder birth date used when the field is blank. This indicates erroneous data entry into DM.

- Go back to the duplicate manager
- Select Modify to edit this record and rectify it
- Click on the pencil icon on the golden record tile
- Click on the pencil icon to override the Date Of Birth value in the golden record
- Click on the Select value from another Master icon
- Select any record with the correct birth date in 1993
- Click Apply to apply the changes in the duplicate manager
    *Expected:* You successfully modified a golden record and confirmed a match

- Examine the golden record for Toni Mattos to determine the reason for the master record matches
- Review the record details and then click the eye icon to view the master records
- Analyze this golden record to determine whether you can confirm it as correctly matched.
    *Expected:*
        Notice the following:
        The golden record was flagged for review because the name "Toni," standardized address, phone, and emails are identical.
        However, two out of three master records are missing a date of birth.
        There is no member ID to ascertain if this is the same individual.

- Click Confirm to accept DM's decision to merge these three master records
- Proceed to the next golden record to be reviewed: Ken Robaina
- Examine the golden record for Ken Robaina to determine the reason for the master record matches.
    *Expected:* Ken Robaina is an interesting golden record because xDM merged several master records to form it. There are three master records under Kenneth Robaina and two under Ken Robaina, which contribute to this golden record. The master record tiles are color-coded: red indicates the CRM system, while blue signifies the Marketing Automation system.

- Click on the Show Matches icon to reveal the relationships between the master records.
- Examine the match rules that formed this match group.
    *Expected:* The match scores are aggregated to generate the confidence score. Since the confidence score exceeds the merge threshold set in the matcher, the Ken Robaina and Kenneth Robaina records matched and merged.

- Look at the Explain Record view of this suggestion and note the following:
    *Expected:*
        The master records share the same date of birth, member ID, address, email, and phone number, except for null values.
        This is likely the same individual, with a difference in first names due to Kenneth commonly being referred to as Ken as a nickname.

- Confirm this match is correct.
- Click Finish to save your confirmations.

<!-- test
id: @T7bc7357b
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Review suggestions

### Description
Follow the "Review suggestions" section of the Semarchy Customer B2C Demo
https://semarchy.com/tutorials-content/customer-b2c-demo/#6

### Requirements 
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
1. In the Quick Actions section of the navigation drawer, click Review Suggestions
    *Expected:* You will see a view of all customer and prospect records identified by DM as potential matches, but not yet merged

2. Click on the Filter icon to start creating a filter that only displays customers with value status HIGH
3. In the Search type menu, select Customer Value Status
4. In the Value Status, select HIGH
    *Expected:* This creates a filter to show customers with a value status HIGH
5. Click Save as in the lower-right corner of the filter menu
6. In the Save filter as field, enter "Value Status"
7. Click Save
    *Expected:* DM takes you to the Filters menu where you can see all the saved filters you or your coworkers created previously and shared with you
8. Click on the Options button next to the Value Status filter
9. Select Share
    *Expected:* You should see the confirmation message "Filter 'Value Status' is now shared with all users."
10. Click Apply
    *Expected:* Notice there are seven customer records that have been merged and deduplicated
11. Click on the First Name column until the arrow is pointing down to sort the records in reverse alphabetical order (from Z to A) based on the First Name value
12. Select the Select All checkbox to mark all the records for review in a duplicate manager
13. Open the Options menu
14. Select Review Suggestions
    *Expected:* You enter the duplicate manager with five suggestions to review
15. The first suggestion is Toni Mattos : In the duplicate manager, click on Show matches and transitive matches
    *Expected:* The solid lines indicate match rules that have merged specific master records successfully. Dotted lines represent suggested matches. Gray lines represent transitive matches, which can be solid if merged or dotted if resulting from suggestions
16. Click on one of the solid lines
    *Expected:* The side panel shows documentation details about the match rule
17. Review the suggested match for Toni Mattos in the Explain Record view using the eye icon (Click on the Toni Mattos card at the top to see the eye icon)
    *Expected:* The master records contain numerous conflicting details and null values, including varying addresses and a potential date of birth discrepancy (07-01-1973 versus 01-07-1973). Additionally, there are two different email addresses, but one Antonia master record (CRM.1469708) shares an email address with the other Toni master records.
18. Accept this suggestion to merge the golden records of Toni Mattos and Antonia Mattos to form a new golden record
19. Click on Next to review the next golden record suggestion for Lynda Bamfield
20. Accept this suggestion to merge the Linda Bamfield and Lynda Bamfield master records into the Lynda Bamfield golden record
21. Click on Next to review the next golden record suggestion Louis Kyle
22. Reject the suggestion
    *Expected:* DM will remove the suggestion and display the individual golden records along with the associated master records
23. Click on Next to review the next golden record suggestion Emilio Michaels
24. Reject the suggestion
25. Click on Next to review the next golden record suggestion Anthony Roberts
26. Reject this suggestion
27. Click Finish to submit your actions in the duplicates manager
    *Expected:* A toast message "Duplicate changes submitted (if any)" is displayed

<!-- test
id: @T2a2a51f2
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Browse data and explore an audit trail

### Description
Follow the "Browse data and explore an audit trail" section of the Semarchy Customer B2C Demo

### Requirements
The xls files in the Attachments section has been dowloaded
You are logged-in using Data steward user in an incognito window (to avoid cookies issues)
username : pierrick.tassery+1@semarchy.com
password : TyXSqr7zcS#Acnsj

### Steps
1. Click Global Search in the navigation drawer
2. Search for "mary-ann"
    *Expected:* You should see one result

3. Select the result, Mary-Ann Markes, to learn more about this customer
4. Click the Master records tab
    *Expected:* This view displays the various master records that contributed to the golden record. Values highlighted in blue indicate those that "survived" to the golden record

5. Click on the Person tab
6. Hover your mouse over the Date Of Birth information
    *Expected:* An information icon appears

7. Click the information icon
    *Expected:* The Field tab details appear in the side panel

8. Click on the Value tab
    *Expected:* You can see the values from source systems as well as see the current value you entered to "override" DM's chosen value in the duplicate manager

9. Search for a customer called Adele Mackson using the Global Search
10. Select Adele Mackson's record
    *Expected:* Note that this customer's last name is Mackson

11. In the Quick Actions section of the navigation drawer, select Update Customers
12. Import the 3-import-data-6-Customers.xlsx Excel spreadsheet
13. Click the refresh button when the toaster message appears
    *Expected:* Once refreshed, note that Adele's last name has changed from Mackson to Richardson

14. Click the information icon on the Last Name field to reveal the field details
15. Click on the Timeline tab
    *Expected:* DM shows that it has recorded the data change from Mackson to Richardson, identifying the source system (CRM) and the time of change

<!-- test
id: @T4d9f22e6
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Model documentation

### Description
Check that the model documentation is generated.


### Steps
1. Access the Customer B2C MDM application in the QA tenant in Staging environment
2. Navigate to the top-right corner of the Customer B2C MDM application interface
3. Click on the User avatar icon (or the profile circle showing the user’s initial)
4. In the dropdown menu that appears, click Documentation
5. Click Customer B2C Diagram
    *Expected:* A diagram is displayed with the entities, their attributes and the links between them

<!-- test
id: @Ta6697f1f
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Import Customer B2C Dashboard

### Description
Import Customer B2C dashboard and check that there is no error

### Requirements
Download the zip file in the Attachments section of this test
Make sure you use a user with semarchyAdmin role in an incognito windows You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
1. Go to the welcome page of QA tenant in Staging https://dm-qa.na.staging.semarchy.net/welcome
2. Open the Dashboard builder in the Tools section
3. Hover the + symbol and click on import application
4. Select the file CustomerB2CDashboard.zip downloaded earlier
5. Click on Create
    *Expected:* The Dashboard should be imported and displayed in the list of applications

6. Click on CustomerB2CDashboard
7. Toggle the Visible Parameter
8. Go to the datasources tab
9. For CustomerB2C, make sure the datasource selected is the one where your NRT model has been deployed
10. Come back to the welcome page
    *Expected:* You should see the Dashboard imported (Customer B2C Dashboard)

11. Click on the Dashboard logo corresponding to your dashboard
    *Expected:* You should see no error and the Customer Metrics dashboard should be displayed

12. Go to the Data Quailty tab
    *Expected:* You should see no error and data should be displayed
13. Go to the Data Matching analysis tab
    *Expected:* You should see no error and data should be displayed

<!-- test
id: @T970ae691
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Check that deployed Customer B2C model works fine

### Description
Check that CustomerB2C model that was already deployed works correctly 

### Requirements
Make sure you use a user with semarchyAdmin role in an incognito windows - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
1. Access the Welcome page in the QA Staging environment
2. Click on the deployed Customer B2C application called "0 Customer B2C (do not delete)" with a hand stop sign logo
    *Expected:* The application opens on the Global search page

3. Go to the different parts of the app to make sure there is no issue
4. Create a Product from the Products tab
    *Expected:* There should be no error

<!-- test
id: @T9bde4a0c
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Check that deployed Customer B2C dashboard works fine

### Description
Check that Customer B2C dashboard that was already deployed works correctly

### Requirements
Make sure you use a user with semarchyAdmin role in an incognito windows - You can check roles in https://dm-qa.na.staging.semarchy.net/dm/admin/users

### Steps
- Access the Welcome page in the QA Staging environment
- Click on the deployed Product Retail dashboard called "0 Customer B2C Dashboard_DoNotDelete" with a hand stop sign logo
    Expected: The dashboard opens without any error
- Go to the different parts of the dashboard to make sure there is no error

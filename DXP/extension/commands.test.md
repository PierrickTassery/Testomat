<!-- suite
id: @S214911ed
emoji: 
-->
# Commands

### Requirements

<!-- test
id: @T6a5e9ff3
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Initiate Project

### Requirements
Your VSCode workspace is configured (See https://semarchy.atlassian.net/wiki/spaces/QA/pages/4194533383/DXP+-+Testing+environment)
The extension is installed on VSCode (See https://semarchy.atlassian.net/wiki/spaces/QA/pages/4193746966/DXP+Extension+-+Installation+guide+for+a+specific+version)

### Steps
1. Click on File, and then Add Folder to Workspace.
2. Create a Folder called "DXP NRT" and add it to your workspace
3. Right click on the folder added to your workspace
4. Go to Semarchy > Semarchy : Initiate Project
    *Expected:* You should be asked if you want to create the full structure of the project

5. Answer yes
    *Expected:* The following files / folders should be created ![](/attachments/NwtJSzXvxT.png)

<!-- test
id: @T478e6d77
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Create Model

### Requirements
The Initiate Project step has been executed successfully 

### Steps
1. Right click on the src folder
2. Go to Semarchy > Semarchy : Create Model
3. Enter the model name : TestModel
4. Answer yes to the question regarding the creation of all default folders
    *Expected:* The following folders / files should be created ![](/attachments/SNWqJIszOM.png)

<!-- test
id: @Tce85eb0a
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Create Entity

### Requirements
The Initiate Project & Create Model steps have been executed successfully 


### Steps
1. Right click on entities folder inside the TestModel model
2. Go to Semarchy > Semarchy : Create Entity
3. Enter the name of the Entity : BasicEntity
4. Answer yes to the question regarding the creation of all default folders
5. Select the type of the entity : Basic
    *Expected:* The following file / folders should be created ![](/attachments/hpmI2BvQ85.png)

6. Right click on entities folder inside the TestModel model
7. Go to Semarchy > Semarchy : Create Entity
8. Enter the name of the Entity : FuzzyEntity
9. Answer yes to the question regarding the creation of all default folders
10. Select the type of the entity : Fuzzy Matched
    *Expected:* The following files / folders should be created ![](/attachments/KHYuk5Q8YF.png)

11. Right click on entities folder inside the TestModel model
12. Go to Semarchy > Semarchy : Create Entity
13. Enter the name of the Entity : TestIDEntity
14. Answer yes to the question regarding the creation of all default folders
15. Select the type of the entity : ID Matched
    *Expected:* The following files / folders should be created ![](/attachments/3asAwWpPTc.png)

<!-- test
id: @T10f41884
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Create Application Components

### Requirements
The Initiate Project, Create Model and Create Entity steps have been executed successfully 


### Steps
1. Open BasicEntity folder
2. Right click on BasicEntity.Entity.seml file
3. Go to Semarchy > Create application components
    *Expected:* The following files should be created ![](/attachments/lE4dNiGAYK.png)

4. Open FuzzyEntity folder
5. Open FuzzyEntity.Entity.seml file and add "1=1" in matcher > matchRules > condition attribute
6. Right click on FuzzyEntity.Entity.seml file
7. Go to Semarchy > Create application components
    *Expected:* The following files should be created ![](/attachments/URzNRLWZg9.png)

8. Open TestIDEntity folder
9. Right click on TestIDEntity.Entity.seml file
10. Go to Semarchy > Create application components
    *Expected:* The following files should be created ![](/attachments/DBJOMPsx31.png)

<!-- test
id: @Td455ce3f
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Build Data Management Model

### Requirements
The Initiate Project, Create Model, Create Entity and Create Application components steps have been executed successfully
There is no error in the PROBLEMS section (You might need to use the Semarchy > refresh workspace command to remove errors.)
To run the refresh workspace command, use CTRL (or CMD on Mac) + P and then type > Semarchy : Refresh workspace


### Steps
1. Use CTRL (or CMD on Mac) + P to open the Command panel
2. Type "> Build" and Select Semarchy > Build Data Management Model
3. Select DXP NRT model (the model you have created in the previous test cases)
    *Expected:* A message "Building OK" should be displayed at the bottom right of the screen and in the OUTPUT section ![](/attachments/sZjju8jaGo.png)

<!-- test
id: @T589b3d59
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Build and Deploy Data Management Model

### Requirements
The Initiate Project, Create Model, Create Entity and Create Application components steps have been executed successfully
There is no error in the PROBLEMS section (You might need to use the Semarchy > refresh workspace command to remove errors.)
To run the refresh workspace command, use CTRL (or CMD on Mac) + P and then type > Semarchy : Refresh workspace

### Steps
1. Go to the extension settings, in the User section
2. For the DM Api Key, use the value stored in https://drive.google.com/open?id=1W-5SGOhtLyPOOEEoo5wXC90GBgj6QY3Q&usp=drive_fs (See https://semarchy.atlassian.net/wiki/spaces/QA/pages/4295426075/Guide+for+Keepass+Password+manager)
3. For Data Location, type TEST_DXP
4. For Datasource, use a data source not used in your instance. (See https://semarchy.atlassian.net/wiki/spaces/QA/pages/4295917583/DM+-+Find+available+datasources+in+an+instance)
5. For DM Instance URL, make sure the value is https://dm-qa.na.staging.semarchy.net/dm
6. Use CTRL (or CMD on Mac) + P to open the Command panel
7. Type "> Deploy" and Select Semarchy > Build and Deploy Data Management Model
8. Select DXP NRT model (the model you have created in the previous test cases)
    *Expected:* A message "Deploying OK" should be displayed at the bottom right of the screen and in the OUTPUT section ![](/attachments/4vVVbOlu6p.png)

9. Access the welcome page in the QA tenant https://dm-qa.na.staging.semarchy.net/welcome
10. Click on Default Application which is the one you just deployed
    *Expected:* You should be able to access the application on the root folder

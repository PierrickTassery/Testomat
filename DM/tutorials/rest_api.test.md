<!-- suite
id: @S6c1dcbdc
emoji: 
-->
# REST API



<!-- test
id: @T04677962
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Documentation

### Description
Check that the REST API documentation can be viewed.

### Steps
1. Access the Welcome page of the QA tenant in Staging https://dm-qa.na.staging.semarchy.net/welcome
2. Click on DM REST API in the Tools section at the bottom
3. Click on the dropdown selection "Getting started" at the top right corner of the page
4. Select NRT_ProductRetail_XXX (XXX being your trigram) in the Data Management - Data location section
    *Expected:* Check that the documentation is interactive and readable

5. Select NRT_ProductRetail_XXX (XXX being your trigram) in the Data Management - Data location (advanced) section
    *Expected:* Check that the documentation is interactive and readable

6. Select NRT_CustomerB2C_XXX (XXX being your trigram) in the Data Management - Data location section
    *Expected:* Check that the documentation is interactive and readable

7. Select NRT_CustomerB2C_XXX (XXX being your trigram) in the Data Management - Data location (advanced) section
    *Expected:* Check that the documentation is interactive and readable

<!-- test
id: @T84972212
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Query Data

### Description
Execute the tests in https://github.com/semarchy/platform-designer-xdm-test

### Steps
1. Access https://github.com/semarchy/platform-designer-xdm-test/actions/workflows/run-bruno-tests.yml
2. Click on Run workflow to open the input selection
3. Type the data location name for both models
4. Click on run worflow to run the tests
    *Expected:* At the end, the results should be displayed in the workflow summary and you should see no error

<!-- test
id: @T77127b31
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Publish Data



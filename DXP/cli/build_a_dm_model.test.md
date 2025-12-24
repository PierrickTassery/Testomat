<!-- suite
id: @S1008b851
emoji: 
-->
# Build a DM model



<!-- test
id: @Tf382cb36
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Build ProductRetail model with design CLI

### Requirements
Read https://semarchy.atlassian.net/wiki/spaces/QA/pages/4194762755/DXP+CLI+-+Installation+guide+for+a+specific+version to install the last version successfully built for the version you test. 
Read https://semarchy.atlassian.net/wiki/spaces/QA/pages/4194533383/DXP+-+Testing+environment to set up your testing environment if it is not done yet.

### Steps
- In a terminal, run the following command : (Change the path according to your environment)
sem-design dm model build --root-folder /Users/pierricktassery/Projects/DXP/platform-designer-xdm-test/data-solution-productretail/src/ProductRetail/
    *Expected:*
        You should see the following lines displayed :
        Building...
        Build successful

<!-- test
id: @T6c2596f2
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Build Customer B2C model with design CLI

### Requirements
Read https://semarchy.atlassian.net/wiki/spaces/QA/pages/4194762755/DXP+CLI+-+Installation+guide+for+a+specific+version to install the last version successfully built for the version you test. 
Read https://semarchy.atlassian.net/wiki/spaces/QA/pages/4194533383/DXP+-+Testing+environment to set up your testing environment if it is not done yet.

### Steps
- In a terminal, run the following command : (Change the path according to your environment)
sem-design dm model build --root-folder /Users/pierricktassery/Projects/DXP/platform-designer-xdm-test/data-solution-customerb2c/src/CustomerB2C/
    *Expected:*
        You should see the following lines displayed :
        Building...
        Build successful

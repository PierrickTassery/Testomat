<!-- suite
id: @S5b01f269
emoji: 
-->
# Deploy a DM model



<!-- test
id: @Ta7b584ca
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Deploy ProductRetail & CustomerB2C models with design CLI using API key

### Requirements
Being able to access the repository https://github.com/semarchy/platform-designer-xdm-test

### Steps
1. Go to build-deploy-QA action https://github.com/semarchy/platform-designer-xdm-test/actions/workflows/build-deploy-QA.yml
2. Click on Run workflow
3. Select available datasources for CustomerB2C and ProductRetail models (See https://semarchy.atlassian.net/wiki/spaces/QA/pages/4295917583/DM+-+Find+available+datasources+in+an+instance)
4. Select the CLI version you are currently testing
5. Click on Run Workflow
6. Wait until the action is done
    *Expected:* The action should be executed with no error. You should see in the Action summary the links of the two deployed apps. Make sure you can access the home page for both applications.

<!-- test
id: @T5f557e57
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Execute ProductRetail tutorial on DM on a model deployed with design CLI



<!-- test
id: @T289a7046
priority: normal
creator: pierrick.tassery@semarchy.com
-->
# Execute Customer B2C tutorial on DM on a model deployed with design CLI



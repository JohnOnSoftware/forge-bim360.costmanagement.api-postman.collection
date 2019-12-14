# BIM360 Cost Management Step-by-Step Tutorial

![Platforms](https://img.shields.io/badge/Web-Windows|MacOS-lightgray.svg)
[![oAuth2](https://img.shields.io/badge/Authentication-v1-green.svg)](http://developer.autodesk.com/)
[![Data-Management](https://img.shields.io/badge/Data%20Management-v2-green.svg)](http://developer.autodesk.com/)
[![BIM360-CostManagement](https://img.shields.io/badge/BIM360%20Cost%20Management-v1-green.svg)](http://developer.autodesk.com/)

[![Postman](https://img.shields.io/badge/Postman-v7-orange.svg)](https://www.getpostman.com/)

![Beginner](https://img.shields.io/badge/Level-Beginner-green.svg)
[![License](https://img.shields.io/:license-MIT-blue.svg)](http://opensource.org/licenses/MIT)

This folder contains a Postman Collection that contains the requests cover the current main workflow of BIM360 Cost Management. The collection together with the environment shows you how to create a new budget with contract, create a cost item, and create different change orders then attach to the cost item, you can also use the available "Action" applied on the change order to change the status of the change order.


## Instructions to run the Postman tutorial are as below:

### Preparation before you begin:
- [Create Forge App, get access to a BIM 360 Account](https://forge.autodesk.com/en/docs/bim360/v1/tutorials/getting-started/get-access-to-account/)
- [Create BIM360 project, activate Cost Management module, setup project for Cost Management](https://help.autodesk.com/view/BIM360D/ENU/?guid=BIM360D_Cost_Management_getting_started_with_cost_management_html);

### Setup Postman environment and Authorization:
- Import Postman environment & collection, please setup the following environment vialables, 
    - client_id:     Forge App Id.
    - client_secret: Forge App Secrect. 
    - project_name:  The project name that you want to operate on.

- Please add the Authorization for the collection, click "Edit Collection", go to "Authorization" tab, make sure to use "OAuth 2.0" to get a 3 legged token, use it in the "Request Headers".
![3leggedToken](./Img/3leggedToken.png)
    - Callback URL: https://www.getpostman.com/oauth2/callback
    - Auth URL: https://developer.api.autodesk.com/authentication/v1/authorize 
    - Access Token URL: https://developer.api.autodesk.com/authentication/v1/gettoken

### Tutorials of BIM360 Cost Management workflow
![Collection](Img/collection.png)

1. 


Follow step 1 to step 5 to create a budget which assigned to a contract, also create a cost item that will be attached to change orders in the following step.

4. Iterate to do step 6 ~ step 11 to get different change order types, and create the different orders then perform action on that based on your workflow.
	- PCO -> RFQ -> SCO
	- PCO -> RCO -> OCO -> SCO
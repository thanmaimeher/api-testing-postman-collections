# api-testing-postman-collections-for-serviceNow
This project demonstrates API testing with Postman by interacting with a ServiceNow Developer Instance. It includes collections that perform full CRUD operations (Create, Read, Update, Delete) on ServiceNow records through the Table API. The workflow covers authentication, request setup, JSON payload handling, and automated test scripts to validate responses. This repository serves as a practical example of using Postman for comprehensive REST API testing in real‑world QA scenarios.

Test Case ID: API_TC_Incident_001
Title: Validate if GET request is fetching all incidents from instance in default json format
Feature: ServiceNow – Incident API
Objective: Verify retrieval of all incidents via API
Preconditions: Valid ServiceNow instance and credentials
Test Steps: Send GET request to incident endpoint with Basic Auth
Expected Result: Response body returns all incidents in JSON format, status code 200, status text OK, response time ≤ 5000 ms
Postconditions: No data modification, only retrieval
Priority: High
Status: Pass

Test Case ID: API_TC_Incident_002
Title: Validate if GET request is fetching all incidents from instance in xml format on changing request header
Feature: ServiceNow – Incident API
Objective: Verify retrieval of all incidents via API
Preconditions: Valid ServiceNow instance and credentials
Test Steps: Send GET request to incident endpoint with Basic Auth and in headers add Accept as "application/xml".
Expected Result: Response body returns all incidents in XML format, status code 200, status text OK, response time ≤ 5000 ms
Postconditions: No data modification, only retrieval
Priority: Medium
Status: Pass

Test Case ID: API_TC_Incident_003
Title: Validate if retrive a record feature is working using sys_id value only one record is getting fetched
Feature: ServiceNow – Incident API
Objective: Verify retrieval of a incident via API
Preconditions: Valid ServiceNow instance, credentials 
Test Steps: Send GET request to incident endpoint with Basic Auth and in param add sys_id in path param
Expected Result: Response body returns single incident record with respect to sys_id in json format, status code 200, status text OK, response time ≤ 5000 ms
Postconditions: No data modification, only retrieval
Priority: Medium
Status: Pass

Test Case ID: API_TC_Incident_004
Title: Validate if query param is fetching all records related to that key vlaue pair
Feature: ServiceNow – Incident API
Objective: Verify retrieval of specific incidents via API
Preconditions: Valid ServiceNow instance, credentials 
Test Steps: Send GET request to incident endpoint with Basic Auth and in param add category key and its value as 'Hardware' in query param
Expected Result: Response body returns all incident records with respect to category as Hardware in json format, status code 200, status text OK, response time ≤ 5000 ms
Postconditions: No data modification, only retrieval
Priority: Medium
Status: Pass

Test Case ID: API_TC_Incident_005
Title: Validate if user is bale to create an incident using post method in servicenow
Feature: ServiceNow – Incident API
Objective: Verify creation of incident via API
Preconditions: Valid ServiceNow instance, credentials
Test Steps:  Send POST request to endpoint with Basic Auth and shot_discription in body.
Expected Result: Response body returns an incident record created with shot_discription in json format, status code 201, status text Created, response time ≤ 5000 ms
Postconditions: No data modification, only retrieval
Priority: Medium
Status: Pass


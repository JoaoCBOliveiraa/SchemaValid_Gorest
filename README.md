GoRest API Testing and DevOps Exercise
This repository contains an exercise focused on API testing and DevOps practices using the GoRest public API. The exercise includes selecting a test automation tool, implementing various API test cases, schema validation, interpreting date values, and explaining CI/CD and load testing strategies.


1. Tool Selection for API Testing
For this exercise, Postman was chosen as the tool for API test automation. The reasons for selecting Postman include:

Ease of Use: Provides an intuitive interface for creating, managing, and executing API requests.
Scriptable Tests: Allows writing tests in JavaScript to validate responses, making it flexible for different testing scenarios.
Automation: Supports automated test runs via Newman, Postman's command-line tool, which can be integrated into CI/CD pipelines.

2. Test Use Cases
The main use cases covered in this exercise include:

Schema Validation: Ensuring that the API response adheres to the expected JSON schema.
Status Validation: Verifying that all items in the response have the completed status.
Date Validation: Interpreting and validating the format of the due_on field to ensure it follows ISO 8601 standards.

3. Automated Testing Implementation
Schema Validation
Uses the tv4 library in Postman to validate the structure of each todo item against a predefined JSON schema.
Ensures that the response includes all necessary fields with correct data types.
Status Validation
Checks if all todo items in the response have the status set to "completed".
Provides an assertion to confirm that the API data is consistent with expected business logic.
Due Date Validation
Verifies that the due_on field for each todo item is in the correct ISO 8601 date format.
Ensures that date values are properly formatted and can be used reliably in further processing.

4. DevOps and CI/CD
Load Testing
Explanation: Load testing was proposed to simulate high traffic on the API, identifying performance bottlenecks and ensuring the system's reliability under stress.
Implementation Justification: Suggested using tools like JMeter or Locust to create a controlled environment for load testing. Emphasized the importance of obtaining permission before performing such tests to avoid potential legal and ethical issues, as load testing can resemble a DDoS attack if done improperly.
Continuous Testing
Explanation: Continuous Testing involves integrating automated tests into the CI/CD pipeline to ensure consistent quality and immediate feedback on code changes.
Implementation Justification: Proposed using tools like Postman/Newman for automated API testing in the pipeline, coupled with scheduled load testing to maintain performance standards. Continuous Testing helps catch defects early, ensures consistent quality, and reduces the risk of introducing regressions.

5. How to Use
Clone the Repository: Clone this repository to your local machine.
Postman Collection: Import the provided Postman collection to test the /public/v2/todos endpoint.
Run Tests: Execute the tests in Postman or use Newman for command-line execution.
Review DevOps Documentation: Review the included documentation for the proposed load testing and continuous testing strategies.

6. Requirements
Postman installed for API testing.
Newman (optional) for running Postman tests via command line.
Basic understanding of API testing, JSON schema validation, and DevOps principles.

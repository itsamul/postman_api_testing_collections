# API Testing Postman + Newman + newman-reporter-htmlextra reporter
API testing is an essential part of software development to ensure that your application's APIs (Application Programming Interfaces) are functioning correctly. **Postman**, **Newman**, and **newman-reporter-htmlextra** are powerful tools that work together to streamline API testing, automate test execution, and generate detailed HTML reports for test results. 

**Postman**: Postman is a popular API testing tool that allows you to create, manage, and execute API requests and collections. It provides a user-friendly interface for designing requests, setting up test scripts, and organizing tests into collections. Postman also enables manual testing, which is valuable during initial API development and exploration.

**Newman**: Newman is a command-line collection runner for Postman. It allows to automate the execution of Postman collections, making it suitable for continuous integration and continuous deployment (CI/CD) pipelines. 

**newman-reporter-htmlextra**: newman-reporter-htmlextra is a custom Newman reporter that extends the default HTML reporter. It generates comprehensive HTML reports that provide a detailed summary of the API test runs. These reports include information such as request-response details, test script results, environment variables, and even screenshots. This reporter enhances the visibility of the test results, making it easier to identify issues and communicate test outcomes.

# Prerequiste and Installation:

1. Install Node.js:
Node.js is required for both Newman and the newman-reporter-htmlextra reporter.
Visit the official Node.js website: Node.js Downloads.
Download the LTS (Long Term Support) version and install.

2. Verify Node.js and npm Installation:
After installing Node.js, open terminal or command prompt and run the following commands to verify the installation:
```
node -v
npm -v
```
These commands should display the installed Node.js and npm versions.

3. Install Postman:
Visit the official Postman website: Postman Download.
Download the appropriate version and install postman.

4. Install Newman:
Newman is a command-line tool for running Postman collections. It is installed using npm (Node Package Manager).
Open terminal or command prompt and run the following command:
```
npm install -g newman
```
This command installs Newman globally on the system.

5. Install newman-reporter-htmlextra:
The newman-reporter-htmlextra reporter provides detailed HTML reports for Newman test runs.
Open terminal or command prompt and run the following command to install it globally using npm:
```
npm install -g newman-reporter-htmlextra
```

6. Verify Newman and newman-reporter-htmlextra Installation:
To verify that Newman and the HTML Extra reporter are installed, run the following commands:
```
newman -v
newman-reporter-htmlextra -v
```
These commands should display the installed versions of Newman and the HTML Extra reporter.


# Application under Test:

Application: **Reqres project**

Reqres is a popular public API that provides a mock server for testing purposes. It's an excellent resource for practicing and learning API testing with tools like Postman and Newman. Reqres can be used to simulate various HTTP request-response scenarios.<br>

Here are some of the common Reqres endpoints used for testing:

1. List of Users:<br>
Endpoint: GET /api/users<br>
Description: Retrieve a list of users<br>
Example: https://reqres.in/api/users?page=2<br>

1. Single User:<br>
Endpoint: GET /api/users/:id<br>
Description: Retrieve information about a single user, identified by their id.<br>
Example: https://reqres.in/api/users/2<br>

1. Create User:<br>
Endpoint: POST /api/users<br>
Description: Create a new user by sending a POST request with user data in the request body.<br>
Example: https://reqres.in/api/users<br>

1. Update User:<br>
Endpoint: PUT /api/users/:id<br>
Description: Update user information for the user identified by their id. Send user data in the request body.<br>
Example: https://reqres.in/api/users/2<br>

1. Delete User:<br>
Endpoint: DELETE /api/users/:id<br>
Description: Delete a user based on their id.<br>
Example: https://reqres.in/api/users/2<br>

1. List Resources:<br>
Endpoint: GET /api/unknown<br>
Description: Retrieve a list of resources. This endpoint has a delay in the response to simulate real-world conditions.<br>
Example: https://reqres.in/api/unknown<br>

1. Single Resource:<br>
Endpoint: GET /api/unknown/:id
Description: Retrieve information about a single resource, identified by its id. This endpoint also has a delay in the response.<br>
Example: https://reqres.in/api/unknown/2<br>

1. Register:<br>
Endpoint: POST /api/register<br>
Description: Simulate user registration by sending a POST request with user registration data in the request body. This endpoint does not perform actual user registration.<br>
Example: https://reqres.in/api/register<br>

# How use Postman, Newman, and newman-reporter-htmlextra together for API testing:

1. Create and Organize API Tests in Postman:<br>
   Used Postman to design the API requests and organized them into collections.<br>
   Added test scripts to validate the responses and ensure the correctness of the APIs.<br>

1. Export the Postman Collection/Enviornment/Global as json file:<br>
   Export the Postman Collection/Enviornment/Global as a JSON file. These files will be used by Newman for test execution.<br>

1. Run API Tests with Newman and Generate HTML Reports:<br>
   Executed the API tests using Newman from the command line. Specified the Postman collection and used the newman-reporter-htmlextra reporter.<br>
   ```
   newman run your-collection.json -r htmlextra
   ```
   This command will rund tests and generates HTML reports using newman-reporter-htmlextra.<br>

1. Review and Share HTML Reports:<br>
   Open the generated HTML reports in your web browser to review the test results.<br>

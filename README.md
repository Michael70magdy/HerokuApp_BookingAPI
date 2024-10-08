
# Booking API Automation with REST Assured

This project is a test automation suite for the Booking API using Java, Rest Assured, and TestNG. The project automates three key scenarios: token generation, booking creation, and retrieval of booking lists.

Run Demo : https://drive.google.com/file/d/1IwkMAuorC7v-TFnz91II4j1axi9vFDva/view?usp=sharing 


## Project Structure

- **`src/test/java`**: Contains the test classes for each scenario.
- **`resources`**: Includes any test data files in Excel format.
- **`reports`**: Holds the generated test execution reports (Allure).
- **`pom.xml`**: Maven configuration file for managing project dependencies.

## Scenarios Covered

### Scenario 1: Verify Token Generation
- **Description**: Validates that a token is successfully generated when authenticating with the Booking API.
- **API Endpoint**: `POST /auth`
  
  **Request Payload**:
  ```json
  {
    "username": "admin",
    "password": "password123"
  }
  ```

  **Validations**:
  - Ensure the response is not empty.
  - Verify that the token is generated successfully.

### Scenario 2: Verify Booking Creation
- **Description**: Verifies that a booking is created successfully in the Booking API.
- **API Endpoint**: `POST /booking`
  
  **Request Payload**:
  ```json
  {
    "firstname": "Jim",
    "lastname": "Brown",
    "totalprice": 111,
    "depositpaid": true,
    "bookingdates": {
      "checkin": "2018-01-01",
      "checkout": "2019-01-01"
    },
    "additionalneeds": "Breakfast"
  }
  ```

  **Validations**:
  - Verify that the booking is added successfully by comparing the response data.

### Scenario 3: Verify List of Bookings
- **Description**: Checks that the list of bookings returned by the API contains more than zero entries.
- **API Endpoint**: `GET /booking`

  **Validations**:
  - Assert that the list of booking IDs is greater than zero.

## Tools and Technologies Used

- **Java**: Programming language used for writing the test scripts.
- **Rest Assured**: Library for automating REST APIs.
- **TestNG**: Testing framework for managing and running tests.
- **Extent Reports/Allure**: Tools for generating test execution reports.
- **Maven**: Build automation tool for managing dependencies and running the project.


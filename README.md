## Go Developer Take Home Test
### Objective
* To create a RESTful API for calculating Scope-2 carbon emissions using provided formulas.
* Additionally, implement NATS for asynchronous processing of emission data.
* This test will evaluate your skills in Test-Driven Development (TDD), REST API creation, messaging queue integration, authentication, coding structure, and database design.

* Scope-2 Emission Calculation Formula
* Scope-2 Emissions (kg CO2) = Electricity Consumption (kWh) × Emission Factor (kg CO2/kWh)
* Example Emission Factor: 0.417 kg CO2/kWh (this can vary based on location and should be configurable)

### Requirements
#### Project Setup
* Use Go (Golang) for development.
* Use a version control system (preferably Git) and provide a repository link.
* Use NATS for message queuing.
* Use Gin as the HTTP web framework.
* Use SQLBoiler for ORM.
#### API Endpoints
* GET /emissions: Retrieves the calculated Scope-2 carbon emissions data. Requires API key authentication.
*  POST /emissions: Accepts electricity consumption data and triggers emission calculation via NATS. Requires API key authentication.
#### Authentication
* Implement API key authentication for securing API endpoints.
#### Data Model
* Design a data model to store emissions data. Each record should include:

#### Timestamp
* Electricity Consumption (kWh)
* Emission Factor (kg CO2/kWh)
* Calculated Emissions (kg CO2)
* Location (optional)
#### Database
* Use PostgreSQL for the database.
* Design and implement the necessary tables to store emission data using SQLBoiler.
#### NATS Integration
* Implement a producer to send electricity consumption data to a NATS topic.
* Implement a consumer to process the topic, calculate emissions, and store the results in the database.
#### Testing
* Use Test-Driven Development (TDD) practices.
* Provide unit tests for the API endpoints and NATS integration.
* Include integration tests for end-to-end scenarios.
#### Documentation
* Provide clear instructions on how to set up and run the project, including NATS and PostgreSQL setup.
* Document the API endpoints, authentication method, and their usage.
#### Bonus
* Implement data validation for electricity consumption inputs.
* Handle errors gracefully and provide meaningful error messages in the API responses.
* Implement structured logging for API requests, errors, and NATS message processing.
* Use Docker to containerize the application, including NATS and PostgreSQL setup.
#### Evaluation Criteria
* Code quality and structure
* Adherence to TDD practices
* REST API and NATS integration
* API authentication implementation
* Database design and implementation using SQLBoiler
* Documentation clarity and completeness
#### Submission
* Create a Private GitHub repository.
* Add Calvin Cheng (@calvinchengx),  Subhransu Behera (@subhransu), Le Thanh Son (thsonvt) as collaborators so they can review your code.

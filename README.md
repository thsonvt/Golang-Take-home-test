Take-Home Test: Full-Stack Developer (Go & Angular)**

**Objective:**
The purpose of this take-home test is to evaluate your ability to implement authentication flows using

**Ory** in a full-stack application built with **Go** for the backend and **Angular** for the frontend.
The test assesses your skills in **authentication, API development, secure token handling, and
frontend integration**.

Requirements

You are required to implement the following features:

**Custom Login Page (MUST)**

Implement a login page using **Angular**, integrating with Ory for authentication.

Capture and store **access tokens** securely in the frontend.

Support refresh tokens for maintaining user sessions.

**Custom Registration Page (MUST)**
Implement a user registration page using **Angular**, integrating with Ory’s identity management.

Store new user credentials securely.

**Backend in Go (MUST)**

Implement authentication API endpoints in Go using Ory's SDK.

Handle user sessions securely using **access tokens** and **refresh tokens**.

Implement a middleware to **protect private routes**.

**Secure API Route (SHOULD)**

Implement a protected API endpoint ( `/api/protected` ) that can be accessed only by
authenticated users.

**Frontend Token Handling (SHOULD)**

Store tokens securely in memory or HttpOnly cookies.

Implement automatic token refresh.

**Unit and Integration Tests (COULD)**

Write tests for the authentication API in Go.

Write frontend tests for login and registration components.

Method

**Backend (Go)**

Use the **Ory Kratos SDK** for authentication.

Implement API endpoints:

`POST /api/register` → Handles user registration.

`POST /api/login` → Handles authentication.

`GET /api/protected` → Example protected route.

Use **JWT** for authentication, supporting refresh tokens.

Middleware to validate and extract the user from tokens.

Use **Fiber** or **Echo** for the API framework.

**Frontend (Angular)**
Build a login and registration UI using **Angular Material**.

Use the **HttpClient** module to communicate with the Go API.

Store tokens securely in **HttpOnly cookies**.

Implement an Angular **Auth Guard** to protect private routes.

Implement an **interceptor** to attach tokens to API requests.

**Database**
Use **PostgreSQL** or **SQLite** to store user data if required.

Store user sessions securely.

Use an ORM such as **GORM**.

**Security Considerations**
Secure token storage using **HttpOnly cookies**.

Implement **CORS** to allow frontend-backend communication securely.

Use **rate limiting** to prevent brute force attacks.

Ensure **password hashing** using bcrypt.

Implementation Steps

1. **Setup Ory Kratos**

Configure Ory for self-hosted authentication.

Set up user schemas in Ory.

2. **Backend Implementation (Go)**

Create authentication APIs with login and registration.

Implement JWT-based access and refresh token handling.

Secure endpoints with middleware.

3. **Frontend Implementation (Angular)**

Build login and registration pages.

Implement token storage and API authentication.

Protect routes using Angular Guards.

4. **Testing**

Write backend unit tests.

Write frontend component tests.

Deliverables & Submission Instructions

To evaluate your implementation, ensure that:

The login and registration flow work correctly with Ory.

Tokens are stored and used securely.

Secure API routes are accessible only when authenticated.

Basic unit tests pass.

The code follows clean architecture and best practices.

**Submission Requirements:**

A **GitHub repository** containing the full implementation (backend in Go & frontend in Angular).

**Instructions to run the project** ( `README.md` ).

API documentation ( `swagger.yaml` or equivalent).

Any assumptions or design decisions should be documented.

**GitHub Access:**
Please create a **private GitHub repository** and add the following users as collaborators so that they
can review your code:

**Calvin Cheng (@calvinchengx)**

**Subhransu Behera (@subhransu)**

****Le Thanh Son** (@thsonvt)**

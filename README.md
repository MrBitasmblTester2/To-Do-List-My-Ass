# To-Do-List-My-Ass

Description
---
Create a web-based to-do-list app where users can add, edit, and delete daily objectives. Front-end is handled by Angular and back-end by ASP.NET Core.

## Tech Stack

- ASP.NET Core
- Angular

## Requirements

- Design RESTful API endpoints for ToDo operations (Refer to ASP.NET Core Web API docs)
- Implement CRUD operations in both API and Angular (Use Angular HttpClient for HTTP requests)
- Manage UI state in Angular using component properties or RxJS (Use RxJS BehaviorSubject or component state variables)
- Validate user input in Angular forms (Import ReactiveFormsModule in AppModule)
- Handle and display errors from HTTP requests (Use RxJS catchError in services and show error messages in UI)
- Write unit tests for API controllers and Angular components (Use xUnit for .NET and Jasmine/Karma for Angular)
- Follow best practices like dependency injection and logging (Inject ILogger<T> via constructor)

## Installation

### Backend (ASP.NET Core)
bash
# Navigate to the backend project folder
cd backend

# Restore dependencies and build the project
dotnet restore
dotnet build

# Configure environment variables
# Example for Linux/macOS
export ConnectionStrings__DefaultConnection="YourConnectionStringHere"

# Run migrations (if EF Core used)
dotnet ef database update


### Frontend (Angular)
bash
# Navigate to the Angular project folder
cd client-app

# Install dependencies
npm install


## Usage

1. Start the backend API:
bash
cd backend
dotnet run

2. Start the Angular development server:
bash
cd client-app
ng serve --open

3. The application will open in your default browser at http://localhost:4200.

## Implementation Steps

1. Scaffold a new ASP.NET Core Web API project.
2. Create a `ToDo` model and configure `DbContext` for EF Core.
3. Define RESTful CRUD endpoints in a `ToDosController`.
4. Implement dependency injection for services and configure logging with `ILogger<T>`.
5. Write unit tests for API controllers using xUnit.
6. Use Angular CLI to generate a new project (`ng new client-app`).
7. Generate ToDo components and a ToDo service (`ng generate service todo`).
8. Implement CRUD operations in the Angular service using `HttpClient`.
9. Manage UI state with RxJS `BehaviorSubject` in the ToDo service.
10. Set up reactive forms in Angular for input validation (import `ReactiveFormsModule`).
11. Handle HTTP errors using `catchError` and display error messages in the UI.
12. Write unit tests for Angular components and services using Jasmine and Karma.
13. Configure environment variables and command scripts for seamless development.

## API Endpoints

- GET `/api/todos` : Retrieve all to-dos
- GET `/api/todos/{id}` : Retrieve a to-do by ID
- POST `/api/todos` : Create a new to-do
- PUT `/api/todos/{id}` : Update an existing to-do
- DELETE `/api/todos/{id}` : Delete a to-do
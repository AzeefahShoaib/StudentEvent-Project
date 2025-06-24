# Student Event Management System API

A comprehensive backend solution for managing student events, built on ASP.NET Core 9.0. This RESTful API provides a full suite of features for event coordination, participant registration, and feedback collection, all structured according to Clean Architecture principles.

---

## Key Features

-   **Event Management**: Full CRUD (Create, Read, Update, Delete) capabilities for events.
-   **Participant Registration**: Allows students to register for events through a dedicated endpoint, handling many-to-many relationships.
-   **Feedback System**: Enables students to submit ratings and comments for events they have attended.
-   **Dynamic Querying**: Supports searching for events by name/venue and sorting the results.
-   **Robust Architecture**: Utilizes a layered architecture (Domain, Application, Infrastructure, API) for maintainability and scalability.

---

## Core Technologies

-   **Backend Framework**: ASP.NET Core 9.0
-   **Data Access**: Entity Framework Core
-   **Database**: Microsoft SQL Server
-   **API Specification**: OpenAPI (Swagger)

---

## Getting Started

Follow these instructions to get a local copy of the project up and running for development and testing.

### Prerequisites

*   [.NET 9.0 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0)
*   [Visual Studio 2022](https://visualstudio.microsoft.com/vs/)
*   [SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) (or any other SQL Server edition)

### Installation & Setup

1.  **Clone the Repository**
    ```sh
    git clone https://github.com/AzeefahShoaib/StudentEvent-Project.git
    ```

2.  **Configure the Database Connection**
    -   Open the solution file (`.sln`) in Visual Studio 2022.
    -   In the `Solution Explorer`, navigate to the `StudentEventManagement.API` project.
    -   Open the `appsettings.Development.json` file.
    -   Update the `DefaultConnection` string to match your local SQL Server instance name. The default is `Server=localhost\\SQLEXPRESS;...`.

3.  **Apply Database Migrations**
    -   In Visual Studio, open the **Package Manager Console** (`Tools > NuGet Package Manager > Package Manager Console`).
    -   Set the **Default project** dropdown to `StudentEventManagement.Infrastructure`.
    -   Run the following command to create the database and its tables:
        ```powershell
        Update-Database
        ```

4.  **Run the Application**
    -   Ensure `StudentEventManagement.API` is set as the startup project.
    -   Press **F5** or the green "Play" button to launch the API.
    -   The application will start, and a browser window will open to the Swagger UI, where all API endpoints can be tested.

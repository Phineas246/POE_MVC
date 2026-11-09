# POE_RaceDay_MVC
# RaceDay – Part 3

## Project Overview

RaceDay is an online event management system developed to make it easier to organise and manage running events. Part 3 focuses on building an ASP.NET Core MVC application that connects to the Web API developed in Part 2.

The system has two primary user groups : Organisers and Participants. Each user has access to different features depending on their role. Organisers can manage events and participants, while Participants can browse events, enrol in races and view their results.

## Main Features

### 1. Authentication and Navigation

The system allows set an accounts and log in securely. Once logged in, users can access features and tools based on their assigned roles.

The application also includes:
- User registration and login.
- Session management to keep users logged in.
- Different navigation options for Organisers and Participants.
- A secure logout feature.
- Protection of pages that should only be accessed by logged-in users.

### 2. Organiser Interface

Organisers have access to a dashboard where they can manage running events and keep track of participant activities.

The main features include:
- Viewing event information and enrolment summaries.
- Creating, editing and deleting events.
- Managing event categories based on age groups and race distances.
- Viewing participants who have enrolled in specific events.
- Checking the enrolment status of participants.
- Recording participants' finishing times and positions.
- Uploading banner images for events.

### 3. Participant Interface

Participants can use the system to find running events, enrol in races and keep track of their participation.

The main features include:
- Viewing upcoming running events.
- Filtering events to find suitable races.
- Viewing event details and available categories.
- Enrolling in events and selecting a category.
- Viewing personal enrolments and their statuses.
- Checking personal race results.
- Updating personal information and uploading profile pictures.

## Technologies Used

The following technologies and tools are used to develop the RaceDay application:

- C#
- ASP.NET Core MVC
- ASP.NET Core Web API (Part 2)
- HTML and CSS
- Bootstrap
- Azure Blob Storage
- Docker
- GitHub Actions

## System Architecture

The RaceDay MVC application communicates with the Web API developed in Part 2. The API is responsible for handling requests and managing all data operations.

The MVC application does not connect directly to the database. Instead, it sends requests to the API whenever it needs to retrieve, add, update or delete information.

The application follows the Model-View-Controller (MVC) design pattern:

- **Models:** Store and represent the data used by the application.
- **Views:** Display the pages and information that users see.
- **Controllers:** Handle user requests and communicate with the API to perform the required operations.

This structure helps keep the application organised and makes it easier to maintain and update.

## Azure Blob Storage Integration

RaceDay uses Azure Blob Storage to store images uploaded by users.

Organisers can upload banner images for their events, while Participants can upload profile pictures to their accounts.

The MVC application sends the images to the Part 2 API, which handles the uploading and storage process using Azure Blob Storage. The stored images can then be displayed in the application when needed.

## How to Run the Application Locally

### Requirements

Before running the application, make sure you have the following:

- Visual Studio 2022 or another compatible development environment.
- The .NET SDK required by the project.
- Access to the Part 2 Web API.
- SQL Server and the correct database configuration for the API.

### Steps to Run

1. Clone or download the RaceDay GitHub repository.
2. Open the MVC project in Visual Studio.
3. Make sure the Part 2 API is running.
4. Check that the API base URL is correctly configured in the MVC application.
5. Build the solution to check for any errors.
6. Run the MVC application.
7. Open the local URL provided by Visual Studio in your browser.

## GitHub and CI/CD

GitHub is used to store the project's source code and keep track of changes made during development.

GitHub Actions is also included to automate the build process and help identify possible errors when changes are pushed to the repository.

The project repository contains:

- The MVC application source code.
- A Dockerfile for running the application in a container.
- A GitHub Actions workflow for automated builds.
- README documentation explaining the project and how to run it.

As part of the Part 3 requirements, at least 20 meaningful commits must be made to show the progress of development.

## Error Handling and User Interface

The application is designed to provide users with a simple and consistent experience when using the system.

Different navigation options are displayed depending on whether the user is an Organiser or a Participant.

Other interface and error-handling features include:

- Different colours to show enrolment statuses.
- Validation to prevent users from submitting incorrect information.
- Clear error messages when something goes wrong.
- Consistent fonts, colours and spacing throughout the application.
- Bootstrap to make the application responsive and easier to use on different screen sizes.

## Conclusion

The RaceDay Part 3 project completes the MVC side of the RaceDay event management system. It allows Organisers to manage running events and Participants to browse events, enrol in races and view their results.

By connecting the MVC application to the Part 2 Web API, the system can manage information without directly accessing the database. Azure Blob Storage is used to handle event banners and profile pictures, while Docker provides support for containerisation.

GitHub and GitHub Actions also help manage the source code and automate the build process. Overall, the project brings the different parts of RaceDay together into one system that is easier for both Organisers and Participants to use.

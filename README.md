**PetPals - The Pet Adoption Platform**


PetPals is a software system designed to facilitate the adoption of pets from shelters and rescue organizations. This platform enables potential adopters to browse available pets, shelters to list adoptable pets, and donors to contribute to animal welfare efforts.

**Features**:
        1.Pet Management:
          -List available pets for adoption, including details like name, age, and breed.
          -Add or remove pets from the list of available pets.
          
        2.Donation System:
          -Handle both cash and item donations.
          -Record donation details and provide options for donors to contribute.
          
        3.Adoption Event Management:
          -Manage adoption events, including registration of participants (shelters and adopters).
          -List and retrieve upcoming events from the database.
          
        4.Database Connectivity:
          -Retrieve, update, and manage data for pets, donations, and events using SQL.
          
        5.Exception Handling:
          -Handle invalid inputs, null references, insufficient funds, file handling errors, and custom exceptions.


**Project Structure**

The project follows an organized directory structure:

  -**entity/model**: Contains entity classes representing real-world objects like Pet, Dog, Cat.
  -**dao**: Contains service interfaces and their implementations for database interaction.
  -**exception**: Defines custom exceptions to handle various error conditions.
  -**util**: Contains utility classes for database connection and configuration.
  -**main**: Contains the main application module with a menu-driven approach to showcase all functionalities.
  
**Classes Overview**

Pet Class
Attributes: Name, Age, Breed
Methods: Constructor, Getters, Setters, toString()

Dog and Cat Classes (Inherit from Pet)
Attributes: DogBreed (Dog), CatColor (Cat)
Methods: Constructor, Getters, Setters

PetShelter Class
Manage a list of available pets for adoption.
Donation System
CashDonation and ItemDonation (derived from an abstract Donation class) handle cash and item donations, respectively.
Adoption Event
Manage and host adoption events, including participant registration.
Database Connectivity
The application interacts with a database to store and retrieve data for pets, donations, and events.
SQL scripts generate tables based on entity classes (Pet, User, etc.).
Requirements
Java 8 or above
SQL Database (e.g., MySQL, PostgreSQL)
JDBC driver for database connectivity
Setup Instructions
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/PetPals.git
Import the project into your IDE.
Configure the database connection in the DBPropertyUtil class.
Run the SQL schema scripts to create the necessary tables in your database.
Run the MainModule class to start the application.
Exception Handling
The application implements robust exception handling for:

Invalid pet age input
Null reference handling for pet properties
Insufficient donation amounts
File handling errors for missing data
Custom exceptions for adoption-related errors

# PROG6212 Part 1
 1. Project Overview 
RaceDay is a database system designed to manage running events. The system stores information about users, organisers, events, event categories, participants, enrolments and race results. The Entity Relationship Diagram (ERD) shows how these entities are related to one another. 
2. Entity Relationship Diagram (ERD) in UML 
The ERD is used to plan the structure of the RaceDay database before creating it in Microsoft SQL Server. Each entity represents a table in the database, while primary keys and foreign keys are used to create relationships between the tables. 
3. Entities in the RaceDay System 
Users 
keeps the details of every user in the RaceDay system, like user ID, full name, email address, phone number, password and user role. 
Organisers 
Stores event organiser information. Each organiser is linked to a user through userID. 
Events 
Stores race event information, like the event name, description, date, location, distance and event type. Each event is managed by an organiser (Microsoft 2026). 
Categories 
saves categories for each event. Categories can be based on age, distance and start time. Each category belongs to an event. 
Participants 
merges users to events as participants. 
Enrolments 
saves information when a participant enrols for an event, including the enrolment date. 
Results 
Stores race results, including finish time and finish position. Each result is linked to an enrolment. 
4. Primary Keys are
Each table has a primary key that uniquely identifies every record: 
•	Users - userID 
•	Organisers - organiserID 
•	Events - eventID 
•	Categories - categoryID 
•	Participants - participantID 
•	Enrolments - enrolmentID 
•	Results - resultID 

5. Relationships Between Entities.
•	A User can be an Organiser. The Organisers table has userID as a foreign key. 
•	An Organiser can manage one or more Events. Each Event is linked to an organiser using organiserID. 
•	An Event can have one or more Categories. Each Category is linked to an Event using eventID. 
•	A User can participate in an Event. The Participants table links a user to an event. 
•	A Participant can enrol for an Event. The Enrolments table stores the enrolment information. 
•	A single Enrolment can have one Result. The Results table stores the finish time and finish position. 

6. Database Constraints 
•	PRIMARY KEY – uniquely identifies each record in a table (Microsoft 2026a).
•	FOREIGN KEY – creates relationships between tables and maintains referential integrity. 
•	NOT NULL – ensures that important fields cannot be left empty. 
•	UNIQUE – prevents duplicate values, like the duplicate email addresses. 
•	DEFAULT – provides a default value when no value is supplied. 

7. Database Implementations
The RaceDay database is implemented using Microsoft SQL Server and SQL Server Management Studio (SSMS). The SQL script creates the RaceDayDB database, creates all 
tables from the ERD, defines primary keys and foreign keys, and inserts realistic sample data including organisers, participants, events, categories, enrolments and results. 
8. Design Note 
The relationship between Events and Categories is created using eventID in the Categories table. This means that one event can have many categories. This design avoids unnecessary duplication and keeps the relationship simple. 
9. Technologies Used (Microsoft 2026):
•	Microsoft SQL Server 
•	SQL Server Management Studio (SSMS) 
•	Structured Query Language (SQL) 

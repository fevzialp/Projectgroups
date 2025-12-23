# Projectgroups
PROJECT SUBMISSION REPORT: EVENT MANAGEMENT SYSTEM
1. Project Overview
The Event Management System (EMS) is a robust C# Windows Forms application developed to streamline event organization and ticket sales. The project aims to provide a reliable platform for admins to manage event data and for customers to browse and purchase tickets in a user-friendly environment. The system utilizes modern database technologies and data serialization techniques to ensure data integrity and portability.
2. User Guide
•	Authentication: Users log in via the LoginForm. Enter credentials and select either "Admin" or "Customer" role to access specific panels.
•	Admin Operations: Admins can add new events by specifying the title, price, and capacity. They can also remove specific records or clear the entire database for maintenance.
•	Customer Operations: Customers can search for events by keyword. Clicking "Buy Ticket" updates the database by decreasing the event's capacity and increasing the sold ticket count in real-time.
•	Data Backup: Use the JSON "Export" and "Import" buttons in the Admin panel to create backups or restore event lists from external files.
3. GitHub Repository Link  https://github.com/fevzialp/Projectgroups.git
4. Short Code Explanation
The application is built using a UserControl-based architecture managed by a central main form.
•	Logic & Routing: LoginForm handles role-based routing, dynamically loading UC_Admin or UC_Customer into the main container based on successful authentication.
•	Data Handling (EF Core & SQLite): We used Entity Framework Core as an ORM to communicate with a local SQLite database (EventDatabase.db).
•	Database Automation: The AppDbContext class uses this.Database.EnsureCreated() to automatically generate the database file and table schema if they do not exist.
•	Serialization: The Newtonsoft.Json library is used to transform C# object lists into readable JSON strings for data portability.
5. Division of Responsibilities
Our team collaborated effectively by dividing the technical workload into specialized domains:
•	Fevzi Alp Aydın - Database & Architectural Lead:
o	Designed the database schema and implemented Entity Framework Core integration.
o	Developed the AppDbContext and ensured data persistence with SQLite.
•	Eren Tunç - UI/UX Specialist:
o	Constructed the visual layout using UserControls for a seamless navigation experience.
o	Managed front-end feedback mechanisms, including professional message boxes and data grid formatting.
•	Uğur Bıyıklıoğlu- Data Integration (JSON Export/Import):
o	Developed the logic for exporting and importing data using JSON serialization.
o	Integrated file system dialogs to facilitate data backup and recovery processes.
•	Shared Responsibility - Error Handling & Quality Assurance:
o	The entire team cooperated on implementing robust Exception Handling (try-catch blocks) to prevent system crashes during database or file operations.
o	Collaborative testing was performed to ensure the language was consistently professional (English) and the logic was bug-free.


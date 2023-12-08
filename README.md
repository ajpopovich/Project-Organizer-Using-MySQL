# Project-Organizer-Using-MySQL
The Project Organizer is a Java-based project management tool that utilizes MySQL and DBeaver to create a project database. It implements CRUD (Create, Read, Update, Delete) functionalities, allowing users to manage projects efficiently.

Project Description: 
The Project Organizer serves as a comprehensive tool for managing projects with the fundamental CRUD operations:

Add a Project: Easily add new projects to the database.

List Projects: View a list of existing projects.

Select a Project: Select and view details of a specific project.

Update Project Details: Modify and update project information.

Delete a Project: Remove projects from the database.

Key Features: 
CRUD Operations: The ability to perform all CRUD operations on project data, offering full control and management capabilities.
Database Integration: Leveraging MySQL and DBeaver, ensuring robust and scalable storage and management of project data.
Technologies Used
Java
MySQL
DBeaver
Maven 
Favorite Features:
Feature 1: CRUD Operations
Implementing the complete set of CRUD functionalities was crucial. It involved creating a seamless user interface and ensuring database synchronization with user actions.

Feature 2: Database Integration
Integrating MySQL with the application was a significant challenge. Establishing proper connections, managing schemas, and handling queries were key aspects that required meticulous attention.

Code Snippets: 
	private Scanner scanner = new Scanner (System.in);
	private ProjectService projectService = new ProjectService();
	private Project curProject;
	
        // @formatter:off
       private List<String> operations = List.of(
        		"1) Add a project",
    		   	"2) List projects",
    		   	"3) Select a project",
    		   	"4) Update project details",
    		   	"5) Delete a project"
        );
        // @formatter:on
  
       public static void main(String[] args) {
    new ProjectsApp().processUserSelections();
    }


       private void processUserSelections() {
           boolean done = false;
           
           while (!done) {
               try {
                   int selection = getUserSelection();
                   
                   switch(selection) {
                   case -1:
                	   done = exitMenu();
                	   break;
                	   
                   case 1:
                	   createProject();
                	   break;
                	   
                   case 2:
                	   listProjects();
                	   break;
                	   
                   case 3:
                	   selectProject();
                	   break;
                	   
                   case 4:
                	   updateProjectDetails();
                	   break;
                	   
                   case 5:
                	   deleteProject();
                	   break;
                	   
                	   default:
                		   System.out.println("\n" + selection + " is not a valid selection. Try again.");
                		   break;
                   }
               } 
               catch (Exception e) {
                   System.out.println("\nError: " + e + " Try again.");
               }
           }
       }
Installation & Usage
Install Dependencies:

Install Java, MySQL, and DBeaver on your system if not installed already.
Set up the MySQL database and tables according to the project's requirements.
Clone the Repository:

bash
Copy code
git clone https://github.com/ajpopovich/Project-Organizer-Using-MySQL.git

Run the Application:

Open the project in your preferred Java IDE (like Eclipse or IntelliJ IDEA).
Configure database connection settings in the code.
Compile and run the main application file.

Contributions to the project are welcome! If you'd like to contribute:

Submit bug reports, feature requests, or pull requests via Github @ajpopovich

Contact Information
For any inquiries or feedback, feel free to reach out:

Email: popovich2614@gmail.com
@ajpopovich on Instagram!

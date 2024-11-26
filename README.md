E-votng System React SpringBoot Mysql
---


This is a complete e-voting application built with Angular for the frontend and Spring Boot for the backend. The backend connects to a MySQL database to manage data. Follow the steps below to set up and run the project on your local machine.
---

## Prerequisites

### Frontend Prerequisites
1. Install [Node.js](https://nodejs.org/) (v20.10.0 or above).
   - Verify installation:
     ```bash
     node -v
     npm -v
     ```
   - Expected output:
     - Node.js version: `v20.10.0`
     - npm version: `10.9.1`
2. Install Angular CLI globally:
   ```bash
   npm install -g @angular/cli
   ```

### Backend Prerequisites
1. Install MySQL Server and MySQL Workbench:
   - Follow this tutorial: [Install MySQL Server and Workbench](https://youtu.be/YSOY_NyOg40?si=DsszBShtN1j7BHl9).
2. Create a new MySQL database:
   - Open MySQL Workbench.
   - Run the following query to create a database:
     ```sql
     CREATE DATABASE voting_system;
     ```

3. Install IntelliJ IDEA or any preferred Java IDE.
4. Ensure you have Java 17+ installed.

---

## Steps to Run the Project

### 1. Run the Frontend
1. Navigate to the frontend folder:
   ```bash
   cd Voting_FrontEnd
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the development server:
   ```bash
   ng serve
   ```

4. Open your browser and go to:
   ```
   http://localhost:4200
   ```


### 2. Run the Backend
1. Open the `VotingServer` folder in IntelliJ IDEA.
2. Configure the `application.properties` file located in:
   ```
   src/main/resources/application.properties
   ```
   Update the following fields with your MySQL database credentials:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/voting_system
   spring.datasource.username=YOUR_USERNAME
   spring.datasource.password=YOUR_PASSWORD
   ```

3. Build and run the Spring Boot project:
   - Click on the **Run** button in IntelliJ.
   - The backend server will start on `http://localhost:8080`.

---

## Expected Behavior
- Frontend (Angular): Accessible at `http://localhost:4200`.
- Backend (Spring Boot): Accessible at `http://localhost:8080`.
- Ensure both servers are running simultaneously for full functionality.

---

## Notes
- If you encounter issues with MySQL, ensure the MySQL server is running and that the credentials in `application.properties` are correct.
- Customize the project settings in IntelliJ and Angular as per your system configuration.




**Improvements:**
- Conduct multiple elections simultaneously.
- Enhanced UI with Angular in the frontend.
- Improved security with Spring Security.

The system recognizes two main user types: Voters and Administrators. Each has its own tailored set of functionalities, catering to their specific needs in the voting process.

**Tools Used:**
- **IntelliJ IDEA:** Used as the primary development environment, ensuring a consistent and efficient coding practice.
- **VS Code:** Assists in designing intuitive user interfaces, enhancing the user experience.
- **MySQL Workbench:** Ensures stable database management and web services, allowing for secure data storage and retrieval.


**User Types:**
- **Voters:** Regular users with the privilege to cast votes.
- **Admin:** Responsible for managing the voting process, candidates, and voter verification.

## Functionalities:</br>

### Voter:
- **Election:** A clear and concise space where voters can quickly choose their preferred candidate and cast their vote in the election.
- **Voting Result:** Provides transparency, allowing voters to view real-time and final election results.
- **Profile:** A personalized space for each user:
  - Displays relevant personal details (e.g., name, location, etc).
  - Ensures security by allowing users to change their login credentials.

### Admin:
- **Election:** A place where you can manage the Elections. Admins can:
  - View and update election details.
  - Monitor live updates on election status.
  - Can see election result once the election ends.
  - Can conduct multiple elections at once.
- **Candidate Details:** A dedicated space to manage candidate profiles. Admins can:
  - Add fresh faces to the election.
  - Update candidate details as required.
  - Remove candidates if needed.
- **Voting Result:** A summarized view of the results, giving admins the data they need to ensure fair elections.
- **Voters Details:** Maintains voter integrity by showing a list of verified voters and relevant details.
- **Verify Voter:** Ensuring the legitimacy of the voting process:
  - Every new account undergoes admin scrutiny.
  - Accounts stay inactive until verified, ensuring only legitimate votes count.


This system is a step towards more transparent and efficient electoral processes, combining modern technology with the time-honored practice of voting.

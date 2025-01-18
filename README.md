# E-commerce Web App (Spring Boot)

## Overview
This is a simple **E-commerce Web Application** built with **Java** and **Spring Boot**, using **HTML** and **CSS** for the front end. It was developed as part of my **Java III** class to demonstrate the creation of a basic e-commerce system where users can browse products, add them to their cart, and proceed to checkout.

## Features
- **Product Display**: View a list of products with basic details like name, description, and price.
- **Shopping Cart**: Add products to the cart and view the cart summary.
- **Checkout Process**: Display cart contents and total price.
- **Basic UI**: Simple HTML and CSS to provide a user-friendly experience.
- **User Authentication**: Implement login and registration functionality for users.
- **Database Integration**: Use a database MySQL to persist product information, cart details, and user orders.

## Technologies Used
- **Backend**: Java, Spring Boot
- **Frontend**: HTML, CSS
- **Build Tool**: Maven (for dependency management and build automation)
- **Database**: MySQL

## Installation & Setup

Follow these steps to get the project running locally on your machine:

### 1. Set Up the MySQL Database

1. **Open MySQL Workbench** and create a new schema:
   ```sql
   CREATE SCHEMA cst_339_milestone;
   ```

2. **Run the SQL Script** from the GitHub repository to create the database structure in your MySQL instance:
   - Download the SQL script from the GitHub repository.
   - Execute it within the `cst_339_milestone` schema in MySQL Workbench to create tables, relationships, and other necessary structures for the app.

3. **Start MySQL Server** on **port 3306** to allow the application to connect to the database.

### 2. Clone the Repository

Clone this repository to your local machine:
```bash
git clone https://github.com/batyrrasulov/e-commerce-web-app.git
```

### 3. Navigate to the Project Directory
```bash
cd e-commerce-web-app
```

### 4. Open the Project in Eclipse

1. Open **Eclipse** IDE.
2. Import the project as a **Maven project** if it's not already in your workspace.
3. Navigate to `src/main/java/com/gcu` and open the `SampleMilestoneApplication.java` file.

### 5. Configure the Database Connection

Make sure that your application is set to connect to the local MySQL server running on **port 3306**. You might need to modify `application.properties` (or `application.yml` depending on your configuration) to set the correct database credentials. Here’s an example of what the `application.properties` file might look like:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/cst_339_milestone
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.database-platform=org.hibernate.dialect.MySQL5Dialect
```

### 6. Run the Application

1. In Eclipse, select the dropdown arrow next to the **Run** button.
2. Choose **Run As** > **Spring Boot Application**.

The application will now start and be accessible on your browser at:
```
http://localhost:8080
```

### 7. Verify the Application

After starting the server, you can open a browser and navigate to `http://localhost:8080` to view and interact with the e-commerce application.

## Screenshots


## Future Improvements
- **Payment Gateway**: Add payment processing integration using Stripe or PayPal.
- **Responsive Design**: Improve the user interface to be mobile-friendly using frameworks like Bootstrap or custom media queries.

## Challenges Faced
- **Front-End Design**: Creating a clean and minimalistic UI with HTML and CSS was challenging but a valuable learning experience.
- **Cart Management**: Implementing cart functionality to handle adding/removing products and calculating the total was a key feature.
- **Session Management**: (Optional: If you implemented session-based cart functionality, mention the challenge of managing user sessions here.)
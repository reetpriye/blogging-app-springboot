# Blogging Application

## About
The Blogging Application is a simple and scalable web application built using Spring Boot. It allows users to create, read, update, and delete blog posts. The application is designed to demonstrate the core concepts of web development, REST APIs, and the integration of a backend server with a database.

---

## Features

- **User Management**
  - User registration and login functionality.
  - Role-based access control (e.g., Admin, User).

- **Blog Management**
  - Create, update, and delete blog posts.
  - View all blogs or individual blogs.
  
- **Category Management**
  - Organize blogs by categories.
  - CRUD operations for categories.

- **Comment System**
  - Add comments to blog posts.
  - Manage comments as an admin.

- **Search Functionality**
  - Search blogs by title or content.

---

## Technologies Used

- **Backend:** Spring Boot, Spring MVC, Spring Data JPA
- **Database:** MySQL (or any RDBMS of your choice)
- **Build Tool:** Maven
- **Languages:** Java

---

## Getting Started

### Prerequisites

1. **Java Development Kit (JDK):** Ensure you have JDK 8 or higher installed.
2. **Maven:** Install Apache Maven for building and managing dependencies.
3. **Database:** Set up MySQL or any preferred database.
4. **IDE:** Use an IDE like IntelliJ IDEA, Eclipse, or VS Code for development.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/reetpriye/blogging-app-springboot.git
   cd blogging-app-springboot
   ```

2. Set up the database:
   - Create a database named `blog_app` (or any preferred name).
   - Update the database configurations in the `application.properties` file located in `src/main/resources`:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/blog_app
     spring.datasource.username=your_username
     spring.datasource.password=your_password

     spring.jpa.hibernate.ddl-auto=update
     spring.jpa.show-sql=true
     ```

3. Build the project:
   ```bash
   mvn clean install
   ```

4. Run the application:
   ```bash
   mvn spring-boot:run
   ```

5. Access the application at:
   ```bash
   http://localhost:8080
   ```

---

## Usage

### API Endpoints

#### Authentication
- `POST /api/auth/register` - Register a new user.
- `POST /api/auth/login` - Log in and retrieve a token.

#### Blog Management
- `GET /api/blogs` - Get all blog posts.
- `GET /api/blogs/{id}` - Get a specific blog post by ID.
- `POST /api/blogs` - Create a new blog post.
- `PUT /api/blogs/{id}` - Update an existing blog post.
- `DELETE /api/blogs/{id}` - Delete a blog post.

#### Category Management
- `GET /api/categories` - List all categories.
- `POST /api/categories` - Add a new category.

#### Comment Management
- `POST /api/blogs/{id}/comments` - Add a comment to a blog post.

### Testing the Application
You can test the APIs using tools like:
- **Postman:** For API testing.
- **Swagger UI:** If integrated (accessible at `/swagger-ui.html`).

---

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature/bugfix.
3. Commit your changes.
4. Push your branch and create a pull request.

---

## License

This project is open-source and available under the [MIT License](LICENSE).

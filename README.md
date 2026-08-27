# Online Quiz and Exam Platform

A production-quality backend for an online quiz and exam platform built with Spring Boot.

## Technology Stack

- **Backend**: Java 21, Spring Boot 3.x, Maven
- **Database**: PostgreSQL (via Supabase)
- **ORM**: Spring Data JPA / Hibernate
- **Validation**: Jakarta Bean Validation
- **Tools**: Lombok, Spring Boot DevTools

## Prerequisites

- Java 21 or higher
- Apache Maven 3.8+
- Git
- Supabase account (for PostgreSQL database)

## Setup Instructions

### 1. Clone the repository

```bash
git clone <repository-url>
cd quiz-project
```

### 2. Configure environment variables

Create a `.env` file in the project root based on `.env.example`:

```bash
cp .env.example .env
```

Edit `.env` and provide your Supabase PostgreSQL credentials:

```
DB_URL=jdbc:postgresql://db.<your-project-ref>.supabase.co:5432/postgres
DB_USERNAME=your_database_username
DB_PASSWORD=your_database_password
```

**Important**: Never commit the `.env` file to version control.

### 3. Build the project

```bash
mvn clean install
```

## Running the Application

```bash
mvn spring-boot:run
```

The application will start on `http://localhost:8080`.

## Testing the API

### Health Check Endpoint

**Request:**
```
GET http://localhost:8080/api/v1/health
```

**Expected Response:**
```json
{
  "status": "UP",
  "message": "Quiz Platform API is running"
}
```

**HTTP Status:** `200 OK`

## Project Structure

```
com.quizplatform
├── config          # Configuration classes (future)
├── controller      # REST controllers
├── service         # Business logic services (future)
├── repository      # Data access layer (future)
├── entity          # JPA entities (future)
├── dto             # Data Transfer Objects
└── security        # Security configuration (future)
```

## Environment Variables

| Variable | Description |
|----------|-------------|
| `DB_URL` | Supabase PostgreSQL JDBC connection string |
| `DB_USERNAME` | Database username |
| `DB_PASSWORD` | Database password |

## Phase 1 Status

✅ Project foundation complete
✅ Database connection configured
✅ Health check API implemented
✅ Environment-based configuration

## Future Phases

- User authentication (Spring Security + JWT)
- User management
- Exam and question management
- Quiz attempts and evaluation
- Analytics and leaderboard
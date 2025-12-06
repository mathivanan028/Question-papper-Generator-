# Question Paper Generator (Minimal)

This archive contains a minimal Java-based Question Paper Generator project with:

- backend/ — Spring Boot application (uses H2 in-memory DB and Apache PDFBox to generate PDF).
- frontend/ — Simple JavaFX application that calls backend API and saves the generated PDF.

## How to run

### Backend
1. Install JDK 17+ and Maven.
2. Open a terminal in `backend/` and run:
   ```
   mvn spring-boot:run
   ```
   Server starts on port 8080. H2 console at `http://localhost:8080/h2-console` (jdbc url: `jdbc:h2:mem:qpgdb`).

### Frontend
1. In a separate terminal (after backend is running), open `frontend/` and run:
   ```
   mvn compile exec:java -Dexec.mainClass=com.qpg.frontend.MainApp
   ```
   Or run the JavaFX app from your IDE. Enter subject (e.g., `Math`) and count, click Generate.


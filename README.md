## **HeadlineAI: AI-Powered News Application**

### 1. **Project Overview**
- **Project Name**: HeadlineAI
- **Purpose**: HeadlineAI is an AI-powered news application with a conversational user interface (CUI), designed to help users query news efficiently. It pulls information from multiple sources using APIs, offering users accurate and relevant news articles.
- **Technology Stack**:
  - **Frontend**: Next.js
  - **Backend**: FastAPI
  - **Database**: PostgreSQL
  - **API Integration**: NewsAPI + Tavily API for web search
  - **ORM**: SQLModel
  - **Testing**: Pytest
  - **Dependency Management**: Poetry
  - **Containerization**: Docker, Docker Compose
  - **Cloud Native Development**: Dev containers for consistent development environments

### 2. **Features**
- Fetches news articles based on user queries using NewsAPI and Tavily API for extended web search capabilities.
- Advanced search options (keywords, AND/OR logic, language filters, date filters).
- Planned voice input/output functionality for a more natural user interaction.
- Users’ news query histories will be maintained and managed in future iterations.

### 3. **Development Approach**
- **Cloud-Native Development**: The project is being developed using a cloud-native style to ensure scalability and portability. Dev containers are used for consistent development environments.
- **Containerization**: Docker and Docker Compose will be used for deployment and local development, ensuring consistency between environments.

### 4. **Installation & Setup**
   - **Prerequisites**:
     - Docker & Docker Compose installed
     - NewsAPI and Tavily API keys
   - **Steps**:
     1. Clone the project repository.
     2. Set up development containers:
        ```bash
        docker-compose up
        ```
     3. Set up environment variables:
        - Create a `.env` file in the root directory:
          ```bash
          NEWS_API_KEY=your_news_api_key
          TAVILY_API_KEY=your_tavily_api_key
          ```
     4. Access the development environment using the dev containers.
     5. Run the application locally:
        ```bash
        docker-compose run app
        ```

### 5. **API Integrations**
- **NewsAPI**: For fetching news articles based on user queries.
- **Tavily API**: Used to extend news search by performing web searches beyond traditional news articles.

### 6. **Architecture**

- **Frontend**: The conversational UI built with Next.js interacts with the backend API to handle user queries and display results.

  #### **Main Pages**:

  1. Landing Page

     :

     - About the app
     - Signup
     - Login
     - Introductory content

  2. Login Page

     :

     - Email/username input
     - Password input
     - Login button

  3. Signup Page

     :

     - Username, email, and password input fields
     - Signup button

  4. Main App Page (Conversational UI)

     :

     - Input text box (bottom)
     - Send button (end of text box)
     - User profile icon (top right)
     - Log out button (bottom left)

- **Backend**:

  1. **Authentication**: Handles user signup and login requests.
  2. **API Interaction**: Receives search queries from the frontend, processes them, and queries external APIs (NewsAPI, Tavily API).
  3. **Response Handling**: Formats the API results and returns them to the frontend for display in the conversational UI.
  4. **User Management**: Handles user data for profile and session management.

- **Database**: PostgreSQL stores user information (login data, profiles), with plans to store user history in future iterations

### 7. **Future Enhancements**
- **Voice Input/Output**: Enabling users to interact with HeadlineAI using voice commands.
- **More Search Tools**: Integration with additional news sources and APIs to enhance search functionality.
- **User History Management**: Maintaining and retrieving individual user histories to provide personalized news recommendations.

### 8. **Minimal Version**
   - **Initial Features**: The first draft will focus on basic text-based search with a minimalistic UI.
   - **Planned Enhancements**: After launching the minimal version, the focus will be on improving the user interface, integrating voice interaction, and adding support for managing user histories.

### 9. **Testing**
   - **Unit Tests**: Written using Pytest to ensure the application functions as expected.
   - **Test Environment**: Ensure consistency using Docker to run tests in an isolated environment.

### 10. **Contributing**
   - **Fork and Clone**: Collaborators can fork the repository, clone it, and work on feature branches.
   - **Branch Naming**: Use descriptive names like `feature/voice-input`.
   - **Pull Requests**: Submit PRs for review before merging into the main branch.

---

This first draft will help your collaborators understand the project's structure and goals. Over time, you can expand sections such as **API Integrations** and **Architecture** as more features are implemented.

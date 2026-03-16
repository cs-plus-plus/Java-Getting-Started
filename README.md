# Introduction to Git, GitHub, JUnit, Maven, GitHub Classroom, and GitHub Codespaces

## What is Git?

Git is a version control system that tracks changes in code and files. It allows multiple developers to collaborate on a project efficiently and helps manage code history, branches, and merges.

### Key Features of Git
- **Version Control**: Tracks changes in files, allowing you to revert to previous versions if needed. Provides a clear history of who made changes, what changes were made, and when.
- **Branching and Merging**: Branches allow you to work on new features or bug fixes without affecting the main codebase. Merging integrates changes from different branches, enabling collaborative development.
- **Commit and Push**: A commit saves your changes locally with a message describing what was done. Push sends your commits to a remote repository, like GitHub, for others to access.

## What is GitHub?

GitHub is a web-based platform that hosts Git repositories. It provides tools for version control, collaboration, and project management, allowing developers to share code, contribute to open-source projects, and work together on private or public repositories.

### Core Features of GitHub
- **Repositories**: Central location for all your project files and history.
- **Pull Requests**: A way to propose changes to a project; allows for code review and discussion before merging.
- **Issues and Project Boards**: Tools for tracking bugs, feature requests, and project tasks.

## What is GitHub Codespaces?

GitHub Codespaces is a cloud-based development environment that runs directly in your browser. It gives you a full VS Code editor with all the tools you need — no local installation required.

### Why Use Codespaces?
- **No setup required**: Everything is pre-configured — Java, Maven, extensions, and dependencies are ready to go.
- **Works anywhere**: All you need is a web browser. Works on Chromebooks, school computers, tablets, etc.
- **Consistent environment**: Every student gets the exact same setup, eliminating "it works on my machine" issues.
- **Fast start**: Click a button and you're coding in under a minute.

### How to Open a Codespace
1. Go to the assignment repository on GitHub
2. Click the green **"Code"** button at the top
3. Select the **"Codespaces"** tab
4. Click **"Create codespace on main"**
5. Wait for the environment to load (this may take a few minutes the first time)

> **Note:** If the Java extension shows errors on first load, press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows/Chromebook) and run **"Developer: Reload Window"**. This is a one-time setup step.

## What is Maven?

Maven is a build automation and project management tool primarily used for Java projects. It helps manage project dependencies, build lifecycle, and documentation, simplifying the build process and project setup.

### Key Features of Maven
- **Dependency Management**: Automatically downloads required libraries and dependencies from a central repository and handles version conflicts.
- **Project Structure and Build Lifecycle**: Enforces a standard project layout and manages the complete build lifecycle, including compiling, testing, packaging, and deploying.
- **Plugins**: Uses plugins to perform tasks such as compiling code, testing, packaging, and deploying applications.

## What is JUnit?

JUnit is a popular testing framework for Java. It is used for writing and running repeatable automated tests, helping ensure that code behaves as expected by validating the correctness of the code through tests.

### Key Features of JUnit
- **Annotations**:
  - `@Test`: Marks a method as a test case.
  - `@DisplayName`: Gives a test a human-readable name.
  - `@BeforeEach` / `@AfterEach`: Setup and cleanup code that runs before/after each test.
- **Assertions**:
  - `assertEquals(expected, actual)`: Checks if two values are equal.
  - `assertTrue(condition)`: Checks if a condition is true.
  - `assertAll(...)`: Runs multiple assertions and reports all failures (not just the first one).

## What is GitHub Classroom?

GitHub Classroom is a tool designed to help educators manage coding assignments using GitHub.

### How It Works
1. Your instructor posts an assignment link in Google Classroom
2. Click the link to accept the assignment
3. GitHub Classroom creates a **personal copy** of the repository just for you
4. You write your code and push (save) it to GitHub
5. **Autograding** runs automatically when you push — tests check your code and assign points
6. Check the **Actions** tab on GitHub to see your score

### Checking Your Score
1. Go to your assignment repository on GitHub
2. Click the **Actions** tab at the top
3. Click on the most recent workflow run
4. Each test shows as a separate step with its point value
5. Green checkmarks = passing, red X = failing

## Running Tests

### In Codespaces / VS Code
- Click the **Testing** icon (flask/beaker) in the left sidebar
- Click **Run All Tests** to run everything
- Or right-click individual tests to run them one at a time
- Green checkmark = passing, red X = failing

### From the Command Line
```bash
# Run all tests
mvn test

# Run a specific test method
mvn -Dtest=TestClassName#testMethodName test
```

## GitHub Desktop (Alternative to Codespaces)

If you prefer to work locally instead of using Codespaces:

1. Download and install [GitHub Desktop](https://desktop.github.com/)
2. Open GitHub Desktop and sign in with your GitHub account
3. Click **File** > **Clone Repository**
4. Select the **URL** tab and paste your assignment repository URL
5. Choose a local path and click **Clone**
6. Open the project in VS Code or IntelliJ IDEA

### Local Requirements
- Java 17 or newer ([Download](https://adoptium.net/))
- Maven 3.x ([Download](https://maven.apache.org/download.cgi))
- VS Code with Java extensions, or IntelliJ IDEA

## Benefits of These Tools in Computer Science Classes

- **Industry-standard tools**: Git, GitHub, Maven, and JUnit are used by professional software developers worldwide.
- **Collaboration skills**: Learn how to manage code contributions from multiple people.
- **Automated testing**: Get instant feedback on your code through autograded tests.
- **Cloud development**: Codespaces lets you code from anywhere without installing anything.

## Next Steps

Navigate to the [Workflow Repo](https://github.com/cs-plus-plus/Java-Workflow) for a step-by-step guide on accepting assignments, writing code, and submitting your work.

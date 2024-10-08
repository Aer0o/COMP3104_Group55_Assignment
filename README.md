# COMP3104 Group 1 Assignment

![GitHub last commit](https://img.shields.io/github/last-commit/Aer0o/COMP3104_Group55_Assignment)
![GitHub contributors](https://img.shields.io/github/contributors/Aer0o/COMP3104_Group55_Assignment)

## 👥 Group Members

| Role | Name                    | Student ID | GitHub                                                |
|------|-------------------------|------------|-------------------------------------------------------|
| **Leader** | Oleg Chystieiev         | 101447469  | [Aer0o](https://github.com/Aer0o)                   |
| Member 2 | Mo Harry Bandukda       | 101451857  | [harrybandukda](https://github.com/harrybandukda)     |
| Member 3 | Teimur Terchyyev        | 101412670  | [cozimo-davinci](https://github.com/cozimo-davinci)   |
| Member 4 | Fredrich Tan            | 101318950  | [Cloudtemplar26](https://github.com/Cloudtemplar2615) |
| Member 5 | Akorede Daniel Osunkoya | 101477407  | [Kodex-Baba](https://github.com/Kodex-Baba)           |
| Member 6 | Samuel Gallego Rivera   | 101435708  | [SamuelGallegoR](https://github.com/SamuelGallegoR)   |

## 📝 Project Description

This repository is dedicated to Group 55's Assignment 1 for COMP3104. The main objectives of this project are:

- Learn the fundamentals of Git commit practices
- Understand and implement merging strategies
- Set up and maintain a CI/CD integration

Through this project, we aim to gain practical experience in collaborative software development and version control.

## 🚀 Setup Instructions

1. Clone the repository:
   ```
   git clone https://github.com/Aer0o/COMP3104_Group55_Assignment.git
   ```
2. Navigate to the project directory:
   ```
   cd COMP3104_Group55_Assignment
   ```
3. Create Switch to your Branch:
   
   git check out -b STUDENTID-Name
4. Push the branch to Github

   git push -u origin STIDENTID-Name

## 🔄 CI/CD Pipeline

Our CI/CD pipeline is set up to ensure the smooth and efficient development, testing, and deployment of our project. This pipeline automates the process of verifying code quality, running tests, and ensuring that all changes pushed to the repository meet the required standards. Below is a breakdown of the tools, stages, and setup for the CI pipeline.

### 🛠️ Tools and Technologies

- **GitHub Actions**: We use GitHub Actions for Continuous Integration (CI). It helps us automate our workflows by running tests and other checks whenever code is pushed or a pull request is made.
- **YAML Configuration**: The pipeline is configured through a `.github/workflows/ci.yml` file, which contains instructions for the CI process.

### 🔄 Pipeline Stages

1. **Trigger**: 
   - The CI pipeline is triggered automatically whenever changes are pushed to any branch in the repository or when a pull request is opened. This ensures that all code contributions are validated before being merged into the `main` branch.


2. **Setup Node.js**: 
   - The workflow sets up the required environment, specifically the Node.js version needed for the project. The configuration file includes:
     
     ```yaml
     jobs:
       build:
         runs-on: ubuntu-latest
         steps:
           - uses: actions/checkout@v2
           - name: Set up Node.js
             uses: actions/setup-node@v2
             with:
               node-version: '14'
     ```


3. **Install Dependencies**:
   - The workflow installs all project dependencies using `npm install`. This ensures that the environment has all the necessary libraries and tools.
     
     ```yaml
           - name: Install Dependencies
             run: npm install
     ```


4. **Run Tests**:
   - Once the dependencies are installed, the pipeline runs the project's tests to verify that everything is working as expected. This is crucial for catching errors early in the development process.
     
     ```yaml
           - name: Run Tests
             run: npm test
     ```


5. **Build and Lint**:
   - The pipeline also builds the project and performs linting to ensure the code follows coding standards. Any issues with the build or code quality will cause the pipeline to fail, alerting developers to address the problems before merging.
     
     ```yaml
           - name: Lint Code
             run: npm run lint
     ```


6. **Notification**:
   - The pipeline is configured to notify the team of the build status, whether successful or failed. This ensures timely communication of issues.
   
### 🔁 Continuous Integration (CI) Flow

The CI pipeline ensures that:

- Every push and pull request is validated.
- Code quality is maintained through linting and testing.
- Only passing code is merged into the `main` branch to avoid breaking the project.

By automating these processes, we ensure a more efficient and reliable workflow, reducing the chances of introducing bugs or issues into the project.


## 🌿 Branching Strategy

Our team will follow a structured branching strategy for efficient and organized collaborative development. Here's our approach:

### Main Branch
- **Name**: `main`
- **Description**: Contains a stable, production-ready version of the project. Only approved and tested changes are merged here.

### Individual Contribution Branches
- **Naming Convention**: `{studentID}-{name}`
- **Description**: Each member has their own branch for personal work and smaller tasks.
- **Example**: `101447469-Oleg`

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

© 2024 COMP3104 Group 55. All Rights Reserved.

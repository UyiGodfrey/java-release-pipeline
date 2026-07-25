# Java Release Pipeline

A hands-on Release Engineering project demonstrating how to build, test, package, and automatically release a Java application using Maven and GitHub Actions.

The project follows modern Continuous Integration (CI) and Release Engineering practices by automatically compiling the application, executing unit tests, packaging it into a JAR file, and publishing official versioned releases whenever a Git tag is pushed.

---

## Project Objectives

* Build a Java application using Maven.
* Automate builds with GitHub Actions.
* Execute unit tests during every build.
* Package the application into a JAR file.
* Automatically create GitHub Releases.
* Upload release artifacts automatically.
* Learn modern Release Engineering workflows.

---

## Technologies Used

* Java 21
* Apache Maven 3.9
* Git
* GitHub
* GitHub Actions
* JUnit 5

---

## Project Structure

```text
java-release-pipeline/
│
├── .github/
│   └── workflows/
│       ├── maven.yml
│       └── release.yml
│
├── src/
│   ├── main/
│   └── test/
│
├── pom.xml
└── README.md
```

---

## Continuous Integration (CI)

Every push to the `main` branch automatically triggers a GitHub Actions workflow that:

1. Checks out the source code.
2. Installs Java 21.
3. Restores Maven dependencies.
4. Builds the project.
5. Executes unit tests.
6. Packages the application into a JAR file.
7. Uploads the generated build artifact.

---

## Automated Release Process

Whenever a Git tag beginning with `v` is pushed (for example `v1.0.2`), GitHub Actions automatically:

1. Builds the project.
2. Runs all tests.
3. Packages the application.
4. Creates a GitHub Release.
5. Uploads the generated JAR file as a release asset.

This removes the need for manual release creation and provides a consistent, repeatable release process.

---

## Running the Project Locally

Clone the repository:

```bash
git clone https://github.com/UyiGodfrey/java-release-pipeline.git
```

Navigate into the project:

```bash
cd java-release-pipeline
```

Build the application:

```bash
mvn clean package
```

Run the tests:

```bash
mvn test
```

---

## Creating a New Release

Create a Git tag:

```bash
git tag v1.0.3
```

Push the tag:

```bash
git push origin v1.0.3
```

GitHub Actions will automatically build the application, create a GitHub Release, and upload the generated JAR file.

---

## Skills Demonstrated

* Java Development
* Maven Build Automation
* Continuous Integration (CI)
* GitHub Actions
* Release Engineering
* Git Versioning
* Git Tags
* Build Artifact Management
* Automated Software Releases

---

## Lessons Learned

This project demonstrates the complete journey from source code to an official software release. It highlights how Continuous Integration and Release Engineering work together to automate software delivery, improve consistency, reduce manual effort, and produce versioned release artifacts suitable for deployment.

---

## Future Improvements

Future versions of this project will include:

* Docker image creation
* Docker image publishing
* Nexus Repository integration
* Helm chart publishing
* Kubernetes deployments
* Semantic version automation
* Multi-stage Docker builds
* Container registry publishing
* Continuous Deployment (CD)

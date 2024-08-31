# COSC2759 Assignment 1
## Notes App - CI Pipeline
- Full Name/Names: **Khalif Pirtondi Siregar** / **Azfar Syed**
- Student ID/IDs: **s3895242** / **s4014872**

### Guidance (remove this section before final submission)

1. Refer for assignment specification `Marking Guide` for details of what should appear in this README.

2. If you do not see an `Actions` tab in your GitHub, email matthew.cullen@rmit.edu.au with URL to your repository, so that it can be enabled.

3. Implement your CI pipeline in the directory `.github/workflows`.

4. Refer to [src/README.md](/src/README.md) for important details on building and testing the application.

5. Commit images to the `img` directory and add them like 
    ```html
    <img src="/img/md.png" style="height: 70px;"/>
    ```
    <img src="/img/md.png" style="height: 70px;"/>

6. Only edit THIS README.md - not the src/README.md

## Description

The following repository integrates a Continuous Integration (CI) pipeline via Github Actions to automate the build and testing processes for the Notes Application.

### Running the Pipeline

The CI pipeline is automatically triggered by GitHub Actions under the following conditions:

- A new commit is pushed to any branch.
- A pull request is opened or updated.

### Expected Output

Once the pipeline is activated, Github Actions will execute the following steps:
1. **Checkout Code:** Using the latest version, the code will be checked out from the repository.
2. **Install Dependencies:** The necessary Node.js packages will be installed.
3. **Lint Code:** The code is checked for quality and style issues.
4. **Run Tests:** Execution of unit and integration tests to ensure code functionality and correctness.
5. **Build Application:** If applicable, the application will be built (e.g. if a build step is defined).

### Viewing Pipeline Results
1. Navigate to the "Actions" tab in the GitHub Repository.
2. Select the workflow run. This will enable viewing detailed logs and results of each step.

### Manual Trigger (Optional)
While the pipeline is automatically triggered by the conditions mentioned above, you can also manually trigger it:
1. Navigate to the "Actions" tab in the GitHub Repository.
2. Seclect the workflow you wish to run.
3. Click the "Run workflow" button to start the pipeline manually.

## Troubleshooting 

If the pipeline fails, check the logs in the "Actions" tab for details on the errors. Common issues include:

- **Dependency Errors:** Update package versions in package.json if needed.
- **Linting Issues:** Follow the linting rules and fix any issues reported.
- **Test Failures:** Review test logs to identify and fix any issues.

## Contributing

To contribute to the CI pipeline or the project, please follow the GitFlow branching strategy:

1. Create a feature branch from 'develop':
Branch naming convention: feature/add-your-feature.

2. Make your changes and commit them:
Ensure your commit messages are clear and descriptive.

3. Open a pull request against the 'develop' branch for review:
Include a summary of the changes and any relevant context in the pull request description.

4. Ensure your changes pass the CI pipeline:
The CI pipeline will automatically run tests and checks on your feature branch. All checks must pass before merging.

5. Merge the feature branch into 'develop' after approval:
Once your changes are reviewed and approved, merge the feature branch into 'develop'.

6. When the 'develop' branch is stable and ready for release, it will be merged into 'main':
The 'main' branch should always reflect the production-ready state of the project.

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

The Notes Application's Continuous Integration (CI) pipeline configuration is stored in this repository. The pipeline's automated linting, testing, and deployment procedures ensure code quality and maintains stability across various branches.

### Running the Pipeline

The CI pipeline is automatically triggered when either of the following occurs:
1. Push Events: The pipeline runs on any push to any branch within the repository.
2. Pull Request Events: The pipeline runs on any pull request targeting any branch within the repository.

The pipeline is automatically initiated by the events mentioned above. Developers do not need to manually trigger the pipeline; it will run as part of the standard development workflow. However, manual triggers can be initiated by pushing changes to any branch or by updating a pull request.

### Manual Trigger (Optional)
While the pipeline is automatically triggered by the conditions mentioned above, you can also manually trigger it:
1. Navigate to the "Actions" tab in the GitHub Repository.
2. Select the workflow you wish to run.
3. Click the "Run workflow" button to start the pipeline manually.

### Expected Output

Upon triggering, the pipeline executes a series of jobs that ensure the codebase maintains high quality standards. 

- Linting Results: Identification and reporting of any code style or syntax issues.
- Unit Test Results: Pass or fail status of the unit tests along with logs.
- Code Coverage Reports: Information indicating the percentage of code covered by tests.
- Artifacts: Generated test reports available for download.
- Deployment Status: Confirmation of successful deployment to GitHub Pages when applicable.

### Viewing Pipeline Results
1. Navigate to the "Actions" tab in the GitHub Repository.
2. Select the workflow run. This will enable viewing detailed logs and results of each step.


## Troubleshooting 

If the pipeline fails, check the logs in the "Actions" tab for details on the errors. Common issues include:

- **Dependency Errors:** Update package versions in package.json if needed.
- **Linting Issues:** Follow the linting rules and fix any issues reported.
- **Test Failures:** Review test logs to identify and fix any issues.

### Branching Strategy (GitFlow)

- Main Branch ("main"): The main branch that has code that is suitable for production. Merges into main are only modifications that have successfully completed all CI tests. Artifacts and deployments are limited to this branch.
- Develop Branch ("develop"): Functions as a feature construction integration branch, prior to merging into main.
- Feature Branches ("feature/*"): Used to create specific features or fixes. Before these branches are pulled into develop or main via pull requests, the continuous integration pipeline runs on them to guarantee code quality.


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

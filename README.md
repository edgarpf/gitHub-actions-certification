# gitHub-actions-certification
* You can include the version of the action in several ways including specifying a Git ref, SHA, tag, or branch.
  * - uses: actions/checkout@8f4b7f84864484a7bf31766abe9204da3cbe65b3
  * - uses: actions/checkout@v4
  * - uses: actions/checkout@v4.2.0
  * - uses: actions/checkout@main
* You can choose to disable GitHub Actions for all organizations in your enterprise, or only allow specific organizations. You can also limit the use of public actions and reusable workflows, so that people can only use local actions and reusable workflows that exist in your enterprise.
* The on keyword is used to specify the events that should trigger a workflow. It allows you to define the events, such as pushes, pull requests, or other GitHub activities, that should initiate the execution of the workflow.
* The "Choose a workflow" page shows a selection of recommended starter workflows. Find the starter workflow that you want to use, then click Configure. To help you find the starter workflow that you want, you can search for keywords or filter by category.
* Semantic versioning (SemVer) provides a systematic approach to versioning, enabling users to quickly understand the significance of updates, maintain compatibility with existing workflows, and adhere to the MAJOR.MINOR.PATCH format allows for clear communication of backward-incompatible changes, feature enhancements, and bug fixes.
* Workflow templates are a great way to ensure automation is reused and maintained in your enterprise. Both in Enterprise Cloud and Enterprise Server, users with write access to an organization's .github repository can create workflow templates that will be available for use to the other organization's members with the same write access.
* You can use the if conditional to prevent a step from running unless a condition is met. You can use any supported context and expression to create a conditional.
* In GitHub Actions, workflow files are stored in the .github/workflows directory within the code repository.
* To access an environment variable corresponding to an input in a Docker container action, you must pass the input using the args keyword in the action metadata file. This ensures that the input is correctly passed to the Docker container environment.
* In an organization where teams manage their own infrastructure costs, utilizing runner groups in GitHub Actions can help segregate runners based on team-specific expenses.
* GitHub Actions use the Checks API to output statuses, results, and logs for a workflow.
* Files required to create a custom action for GitHub Actions: JavaScript files (main.js or index.js) for JavaScript actions and an action metadata file (action.yml or action.yaml) to define the action's configuration and behavior or Dockerfile.
* It is recommended that you use the default environment variables to reference the filesystem rather than using hard-coded file paths.
* By default, self-hosted runners will automatically perform a software update whenever a new version of the runner software is available. Turning off automatic updates allows you to update the runner version on the container image directly on your own schedule.
* 

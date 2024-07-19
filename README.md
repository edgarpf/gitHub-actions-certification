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
* One way to ensure that a script file is executable in a workflow job is to manually grant execute permission to the script file on the runner. This can be done using commands like chmod +x within the workflow steps.
* To filter on all failed runs, you can set the Status filter to specify failure status.
* A composite action allows for consolidating multiple workflow steps into a single action.
* Dependent jobs allow you to specify the order in which jobs should run, ensuring that one job completes before another starts.
* Workflow badges in a private repository are not accessible externally to prevent embedding or linking from unauthorized sources.
* You should select a category for the action when publishing to Github Marketplace. This will help people find your action more easily.
* To effectively manage and collaborate on your organization's diverse reusable components in GitHub Actions workflows, enforce a standardized naming convention across all teams.
* Creating a release strategy for a GitHub Action involves defining a structured approach to managing updates and versioning. This strategy ensures clear communication with users regarding changes, major updates, critical fixes, and security patches.
* Caching dependencies helps reduce network utilization, runtime, and cost by avoiding the need to download dependencies for every workflow run.
* GitHub provides a token that you can use to authenticate on behalf of GitHub Actions. GitHub automatically creates a unique GITHUB_TOKEN secret to use in your workflow. You can use the GITHUB_TOKEN to authenticate in the workflow job.
* By using GitHub-hosted runners for common tasks and self-hosted runners for resource-intensive ones, you can balance cost-effectiveness and performance.
* If you want a self-hosted runner to communicate through a proxy server, you can configure the proxy settings in the following environment variables: https_proxy: <proxy URL for traffic>. Additionally, you can also include basic authentication credentials, if necessary.
* The primary purpose of custom labels for self-hosted runners is to route jobs to specific types of runners based on the labels assigned to those runners.
* In addition to the steps configured in the workflow file, GitHub adds two additional steps to each job to set up and complete the job's execution. These steps are logged in the workflow run with the names "Set up job" and "Complete job".
* Steps represent individual tasks within a job.
* GitHub allows you to run scheduled workflows once every five minutes. It is the shortest interval that is allowed, meaning that the minimum time granularity available would be minutes.
* To facilitate the secure downloading of actions from internal or private repositories, GitHub issues scoped installation tokens to runners. These tokens have read access to the repository containing the actions and automatically expire after one hour.
* While a job is awaiting approval, it has a status of "Waiting". If a job is not approved within 30 days, it will automatically fail.
* The outputs key in the action's metadata syntax is used to declare the outputs produced by the action. These outputs can then be consumed by subsequent steps in the workflow.
* While enhancing security with an IP address allowlist is important, the operations team may find the task of constantly updating it for GitHub-hosted runners to be burdensome due to the potential for errors and time consumption. This balance between security and operational efficiency is crucial for maintaining smooth CI/CD workflows.
* If you're developing a Node.js project, the GitHub Actions Toolkit provides packages that you can use in your project to speed up development.
* Custom retention periods can be configured for individual artifacts using the actions/upload-artifact action in a workflow.
* You cannot overwrite the value of the default environment variables named GITHUB_* and RUNNER_*.
* Unlike Python, however, YAML doesn’t allow literal tab characters for indentation.

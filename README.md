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
* Custom labels in GitHub Actions operate cumulatively, meaning a self-hosted runner must have all assigned labels to be eligible to process a job
* To set a custom environment variable for a single workflow, you can define it using the ‘env’ key in the workflow file. The scope of a custom variable set by this method is limited to the element in which it is defined.
* Utilizing large runners with static IP address ranges and adding these ranges to the allowlist offers a secure and manageable solution because larger runners provide increased flexibility and isolation compared to standard hosted runners.
* You can add the action you've created to the GitHub Marketplace by tagging it as a new release and then publishing it.
* Enabling debug logging in the GitHub repository settings increases the verbosity of the job's logs, providing more detailed information that can help troubleshoot issues with the JavaScript action.
* The GITHUB_TOKEN expires either when a job finishes or after a maximum of 24 hours.
* The expiration date of an artifact can be confirmed using the API, specifically by checking the expires_at value returned by the “Actions” API.
* To store secrets larger than 48 KB, you have to use encryption with GPG. The encrypted file is stored in the repository, and the decryption passphrase is stored as a secret on GitHub.
* Docker container actions can only be executed on runners with a Linux operating system. Self-hosted runners must use a Linux operating system and have Docker installed to run Docker container actions.
* JavaScript actions in GitHub repositories differ from traditional Node.js projects in their development and distribution processes. They include dependent packages alongside the code and support tagged releases for direct publication to GitHub Marketplace.
* If a newly registered self-hosted runner is not visible in the assigned runner group, it is likely because the runner has not yet been assigned to any runner group. Runner visibility in groups is determined by assignment, so if the runner has not been explicitly assigned to a group, it will not appear in any group, even if it has been successfully registered with the organization.
* Service containers are Docker containers that offer a simple and portable way to host services needed for testing or operating applications
* Workflow commands are used to interact with the runner during the execution of a step, providing a way to pass information, set environment variables, or perform other actions related to the workflow.
* GitHub ensures the security of secrets printed to workflow logs within GitHub Actions by automatically redacting them.
* Treating environment variables as case-sensitive is good practice to avoid issues and maintain consistency in the workflow.
* The RUNNER_OS environment variable provides the operating system of the runner executing the job. Possible values are Linux, Windows, or macOS.
* In GitHub Actions, the exit code of an action determines its success or failure status. A zero exit code indicates success.
* In scenarios where cost-effectiveness and minimal management are priorities, GitHub-hosted runners provided by GitHub are the most suitable option for GitHub Actions. These runners are maintained and managed by GitHub, eliminating the need for organizations to handle infrastructure setup, maintenance, and costs, thereby providing a hassle-free and economical solution for CI/CD workflows.
* The continue-on-error keyword in a step allows the workflow to continue even if a step fails.
* When a workflow job references an environment, the job won't start until all of the environment's protection rules pass.
* The run directive uses the echo "/tmp" >> $GITHUB_PATH command to add /tmp to the PATH on the Ubuntu runner.
* If there is a cache miss and the job completes successfully, the cache action automatically creates a new cache with the specified key and contents.
* The setOutput command is used to set an output variable that can be used in subsequent steps or even in the parent workflow.
* By default, the artifacts and log files generated by workflows are retained for 90 days before they are automatically deleted. You can adjust the retention period depending on the type of repository.
* You can use the GITHUB_TOKEN by using the standard syntax for reference secrets: ${{ secrets.GITHUB_TOKEN }}.
* GitHub Actions workflows allow you to execute commands directly on the runner using the run keyword. You can specify the location of the script within the repository and execute it with this keyword
* The GITHUB_REPOSITORY default environment variable provides the owner and repository name (in the format owner/repository) for the repository where the workflow is running.
* restore-keys allows you to specify a list of alternative restore keys. These keys are used sequentially in the order provided to find and restore a cache in case of a cache miss.
* To get a link to a specific line in the logs, click on the step's line number. You can then copy the link from the address bar of your web browser.
* Default environment variables are set by GitHub and are available at every step in a workflow. They provide information about the workflow run and repository.
* If the targeted environment is configured to prevent self-approvals, the user initiating the workflow run cannot approve the deployment.
* One common use of environment variables is to store sensitive information like API keys without hardcoding them in the code, making the code more secure.
* When troubleshooting connectivity issues with a self-hosted runner and validating its access to GitHub services, the development team must use the --check feature alongside the runner's URL and authentication token.
* To enable step debug logging, set the following secret or variable in the repository that contains the workflow: ACTIONS_STEP_DEBUG to true. If both the secret and variable are set, the value of the secret takes precedence over the variable.
* All actions require a metadata file. The metadata filename must be either action.yml or action.yaml. The data in the metadata file defines the inputs, outputs, and runs configuration for your action.
* The jobs.<job_id>.runs-on configuration is used to specify the type of runner and the operating system on which the job should be executed.
* The URL for the GitHub Container Registry is ghcr.io.
* To publish an action, the action’s metadata file must be in the root directory of the repository.
* GitHub limits the maximum number of jobs generated by a matrix to 256 jobs per workflow run.
* Tags are useful and widely used, but one downside to using tags is that they can be deleted or moved. With Git, each commit receives a calculated SHA value, which is unique and cannot be modified.
* In GitHub Actions, debug messages printed using workflow commands are not displayed in the logs by default.
* Composite run steps actions allow you to reuse actions by using shell scripts.
* Secrets are variables that you create in an organization, repository, or repository environment.
* You can delete a workflow run that has been completed or is more than two weeks old.
* Users should not be referencing an action's default branch with the action because the default branch is likely to contain the latest code (which might or might not be stable) and could break your workflow.
* Workflow template and metadata files must reside in the workflow-templates directory of the .github repository.
* the using: keyword is used to specify the type of the action being executed, such as docker, node12, composite, etc.
* In GitHub Actions, you can use the group workflow command to create expandable groups in the workflow logs.
* To trigger a workflow when a comment is created on an issue within a GitHub repository, you should use the issue_comment event.
* Workflow commands prefixed with the :: can be used to customize the runner environment, such as setting environment variables or modifying the working directory.
* Outputs are Unicode strings, and can be a maximum of 1 MB. The total of all outputs in a workflow run can be a maximum of 50 MB.
* The GITHUB_ACTIONS variable is always set to true when GitHub Actions is running the workflow.
* To enable step debug logging, set the following secret or variable in the repository that contains the workflow: ACTIONS_STEP_DEBUG to true. If both the secret and variable are set, the value of the secret takes precedence over the variable.
* In GitHub Actions, runner labels can be used to categorize different types of runners provisioned in an organization for various workloads.
* GitHub Actions does not dictate or even propose a naming convention for workflow files.
* read, write, none provide fine-grained permissions for individual actions. {} disables permissions for all of the available scopes. write-all defines write access for all of the available scopes.
* The status "Running" does not exist. The status that indicates a running workflow is "In Progress".
* You can add self-hosted runners at various levels in the management hierarchy:
  * Repository-level runners are dedicated to a single repository.
  * Organization-level runners can process jobs for multiple repositories in an organization.
  * Enterprise-level runners can be assigned to multiple organizations in an enterprise account.
* The github.run_number property is a unique number for each run of a particular workflow in a repository. This number begins at 1 for the workflow's first run, and increments with each new run. This number does not change if you re-run the workflow run.
* A reusable workflow can be used by another workflow if any of the following is true:
  * Both workflows are in the same repository.
  * The called workflow is stored in a public repository, and your organization allows you to use public reusable workflows.
  * The called workflow is stored in a private repository and the settings for that repository allow it to be accessed.
* You can use GitHub Actions Importer to plan and automatically migrate your CI/CD pipelines to GitHub Actions from Azure DevOps, CircleCI, GitLab, Jenkins, and Travis CI.
* All actions require a metadata file. The metadata filename must be either action.yml or action.yaml
* When an action fails, all concurrent actions are canceled and future actions are skipped.
* When you plan to publish your action to GitHub Marketplace, you'll need to ensure that the repository only includes the metadata file, code, and files necessary for the action.
* You can use the CODEOWNERS feature to control how changes are made to your workflow files.
* You can access the artifacts produced by a completed workflow run from the GitHub UI by using the "Artifacts" section in the GitHub Actions UI. The UI does not offer an "Artifacts" tab.
* You can use pre-entrypoint: to run a prerequisite setup script.
* Workflow runs can restore caches created in either the current branch or the default branch (usually main). If a workflow run is triggered for a pull request, it can also restore caches created in the base branch, including base branches of forked repositories.
* The branding section in the action.yml file is used to provide branding information for the custom action, including icons and colors.
* Artifacts allow you to persist data after a job has completed, and share that data with another job in the same workflow.
* You can download the detailed log output of a specific job within a GitHub Actions workflow run from the GitHub UI.
* There's no direct "pause" feature for workflows.
* The name in the action's metadata file must be unique.

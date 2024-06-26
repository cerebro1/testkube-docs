import SimpleGradle from "../../workflows/simple-gradle-workflow.md"
import SimpleGradleFromTemplate from "../../workflows/simple-gradle-workflow-from-template.md"

# Basic Gradle Example

Below is a simple workflow for executing tests in a Gradle project stored on GitHub. You can paste this directly into the
YAML of an existing or new test, just make sure to update the `name` and `namespace` for your environment as needed.

- The `spec.content` property defines the path to the Gradle project on GitHub.
- The `spec.container` property defines default constraints for any container created in this workflow.
- The `spec.steps` property defines a single step that runs the `gradle --no-daemon` test command.

<SimpleGradle/>

After execution, you can see the log output from the test executions under the executions panel tabs:

![Gradle Log Output](images/basic-gradle-log-output.png)

## Basic Gradle from Template
Below is an example workflow for executing the Gradle project using an official Testkube Template.

<SimpleGradleFromTemplate/>

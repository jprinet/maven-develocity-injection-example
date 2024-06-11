## Maven Develocity Injection example

This repo contains a Maven project, and demostrates how a GitHub Actions workflow can inject the required configuration 
to connect to Develocity before executing the build.

Key pieces:
- ["Inject Develocity" workflow step](https://github.com/bigdaz/maven-develocity-injection-example/blob/main/.github/workflows/build.yml#L31-L35)
  - This step copies the Develocity configuration files into the `.mvn` directory
- [Develocity configuration files](https://github.com/bigdaz/maven-develocity-injection-example/tree/main/.github/resources/.mvn)
  - These example files connect to the Develocity instance at `https://ge.solutions-team.gradle.com`. This URL should be changed as required.

Each resulting workflow run will produce a Develocity Build Scan®. [The link is visible at the end of the build step](https://github.com/bigdaz/maven-develocity-injection-example/actions/runs/9470336821/job/26090987469#step:6:77).

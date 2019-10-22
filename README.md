# Sample workflows for Logtalk repos

To use a workflow in your own repo, copy its file to the `.github/workflows` directory on your repo and edit the workflow to match your application requirements. Don't forget to sign up for the GitHub Actions beta program. See the [`demo`](https://github.com/logtalk-actions/demo) repo for usage examples of some of these workflows.

##### [`testing.yml`](https://github.com/logtalk-actions/workflows/blob/master/testing.yml)

This workflow runs tests and makes available a TAP report and a code coverage report as build artifacts. 

##### [`coverage.yml`](https://github.com/logtalk-actions/workflows/blob/master/coverage.yml)

This workflow is a variant of the `testing.yml` workflow that also publishes the code coverage report to `gh-pages`. It uses a third-party action that requires creating a personal access token. You will also need to create the `gh-pages` branch. See [https://github.com/maxheld83/ghpages](https://github.com/maxheld83/ghpages) for details.

##### [`diagrams.yml`](https://github.com/logtalk-actions/workflows/blob/master/diagrams.yml)

This workflow generates and uploads as a build artifact the application diagrams in SVG format.

##### [`documenting.yml`](https://github.com/logtalk-actions/workflows/blob/master/documenting.yml)

This workflow generates HTML documentation using Sphinx making it available as a build artifact.

##### [`doclet.yml`](https://github.com/logtalk-actions/workflows/blob/master/doclet.yml)

This workflow runs the `logtalk_doclet` script to generate documentation assuming that the project defines a doclet.

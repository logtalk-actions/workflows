# Sample workflows for Logtalk repos

To use a workflow in your own repo, copy its file to the `.github/workflows` directory on your repo and edit the workflow to match your application requirements, notably to choose and configure the Prolog compiler backend that you want to use. Don't forget to [sign up](https://github.com/features/actions) for the [GitHub Actions](https://help.github.com/en/github/automating-your-workflow-with-github-actions/about-github-actions) beta program. See the [`demo`](https://github.com/logtalk-actions/demo) and [`spider`](https://github.com/logtalk-actions/spider) repos for usage examples of some of these workflows.

##### [`testing.yml`](https://github.com/logtalk-actions/workflows/blob/master/testing.yml)

This workflow runs tests on push events and makes available a TAP report and a code coverage report as build artifacts. To generate instead a xUnit report, change the `logtalk_tester` option `-f tap` to `-f xunit` and `tap-report` to `xunit-report` in the upload action.

##### [`testing_for_pull_requests.yml`](https://github.com/logtalk-actions/workflows/blob/master/testing_for_pull_requests.yml)

This workflow run tests on pull request events without generating any reports. It also uses a minimal Logtalk setup without installing third-party dependencies, which are not required in this case. Merging the pull request requires this workflow to succeed.

##### [`coverage.yml`](https://github.com/logtalk-actions/workflows/blob/master/coverage.yml)

This workflow runs on push events and is a variant of the `testing.yml` workflow that also publishes the code coverage report to [GitHub Pages](https://pages.github.com/). It uses a third-party action that requires creating a personal access token. You will also need to create the `gh-pages` branch before running the workflows. See [https://github.com/maxheld83/ghpages](https://github.com/maxheld83/ghpages) for details.

##### [`diagrams.yml`](https://github.com/logtalk-actions/workflows/blob/master/diagrams.yml)

This workflow runs on push events and generates and uploads as a build artifact the application diagrams in SVG format.

##### [`documenting.yml`](https://github.com/logtalk-actions/workflows/blob/master/documenting.yml)

This workflow runs on push events and generates HTML documentation using Sphinx making it available as a build artifact.

##### [`doclet.yml`](https://github.com/logtalk-actions/workflows/blob/master/doclet.yml)

This workflow runs on push events and calls the `logtalk_doclet` script to generate documentation assuming that the project defines a doclet.

##### [`embedding.yml`](https://github.com/logtalk-actions/workflows/blob/master/embedding.yml)

This workflow runs on push events and illustrates how to embed a Logtalk application and generate an executable. For more on embedding support see [https://github.com/LogtalkDotOrg/logtalk3/tree/master/scripts/embedding](https://github.com/LogtalkDotOrg/logtalk3/tree/master/scripts/embedding).

## License

This project is released under the [Apache License 2.0](LICENSE).

## Current Status

These workflows are in active development.

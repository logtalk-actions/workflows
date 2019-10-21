# Sample workflows for Logtalk repos

##### [`testing.yml`](https://github.com/logtalk-actions/workflows/blob/master/testing.yml)

This workflow runs tests and makes available a TAP report and a code coverage report as build artifacts. 

##### [`coverage.yml`](https://github.com/logtalk-actions/workflows/blob/master/coverage.yml)

This workflow is a variant of the `testing.yml` workflow that also publishes the code coverage report to gh-pages.

##### [`diagrams.yml`](https://github.com/logtalk-actions/workflows/blob/master/diagrams.yml)

This workflow generates and uploads to gh-pages the application SVG diagrams.

##### [`documenting.yml`](https://github.com/logtalk-actions/workflows/blob/master/documenting.yml)

This workflow runs the `logtalk_doclet` script to generate documentation assuming that the project defines a doclet.

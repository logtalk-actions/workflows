# workflows

Sample workflows for Logtalk repos.

## `testing.yml`

This workflow runs tests and makes available a TAP report and a code coverage report as build artifacts. 

## `coverage.yml`

This workflow is a variant of the `testing.yml` workflow that also publishes the code coverage report to gh-pages.

## `documenting.yml`

This workflow runs the `logtalk_doclet` script to generate documentation assuming that the project defines a doclet.

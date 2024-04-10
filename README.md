# Documentation as Code

This repository contains an example of how to release crucial documentation with every version of your software.

## How it works

You can edit the operations manual and arc42.adoc with chapters. Commits tagged in semver.org schema will be built and released on Github.

- .github/workflows/main.yml calls build_docs.yml
- build_docs.yml runs dtcw, which is configured by docToolchainConfig.groovy
- once docs are built and uploaded as Artifacts, main.yml calls release.yml
- release.yml creates releases with downloadable documentation on Github

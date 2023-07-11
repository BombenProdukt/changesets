# Changesets

Changesets is a tool for managing versioning and changelogs with a focus on agnosticism. This tool was inspired by [changesets](https://github.com/changesets/changesets) from [Atlassian](https://www.atlassian.com/), which focuses on mono repositories and JavaScript projects. Changesets is designed to be language-agnostic and work with any repository structure or project type, as it only concerns itself with the changelog and versioning.

## Guiding Principles

- **Agnostic**: Changesets should work with any repository structure or project type.
- **Simple**: Changesets should be easy to create and understand.
- **Flexible**: Changesets should be flexible enough to work with any workflow.

## Data Model

Each changeset is stored in a [YAML](https://yaml.org/) file in the `.changesets` directory. The file's name is used to identify the changeset, and the contents of the file are used to generate the changelog. The file's name is a randomly generated string and is not meant to be human-readable. The file's contents are a [YAML](https://yaml.org/) document with the following structure:

```yaml
packageName: "laravel-lighty"
versionBump: patch
description: "FIXED: compatibility with laravel 10"
```

- The **packageName** refers to the name of the package undergoing modification. It groups changesets together in the changelog.
- The **versionBump** specifies the type of version bump to be applied to the package. It can be either `major`, `minor`, or `patch` as per [Semantic Versioning](https://semver.org/) guidelines, and aids in generating the version number.
- The **description** provides a human-readable explanation of the changeset, facilitating the generation of the changelog.

## Format

Changesets can be used to generate changelogs and versioning information for any project. It does this by generating a `CHANGELOG.md` file in a repository. This file contains a changelog for the project, and is generated from a set of changesets. This changelog adheres to the [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) format and is designed to be human-readable.

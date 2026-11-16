# Contributing to CoCreateJS

This is CoCreateJS’s default contribution guide; repository-specific guides take precedence. CoCreateJS is developed across multiple repositories in the [CoCreateJS organization](https://github.com/CoCreateJS). Choose the repository that owns the code or documentation you want to change, and check that repository's contribution guide and release configuration first.

## Before you start

- Search existing issues and pull requests, or open an issue to discuss a substantial change.
- Keep changes focused on one repository and one purpose.
- Follow the conventions already used by that repository.

## Make and submit a change

1. Fork or clone the relevant repository.
2. Create a topic branch from its default development branch.
3. Make the change and run the repository's relevant checks.
4. Update documentation or examples when behavior changes.
5. Open a pull request describing the reason for the change and how you verified it.

Use Conventional Commit messages where the repository uses Semantic Release. For example, `fix: handle empty socket responses` describes a patch, while `feat: add organization-level releases` describes a feature. For a breaking change, include a `BREAKING CHANGE:` footer in the commit message.

## CoCreateJS workspace releases

The CoCreateJS workspace repository uses Semantic Release on `main` to create Git tags, update `CHANGELOG.md`, and publish GitHub releases. This workflow does not publish an npm package. Other repositories may have their own release workflows and package publishing rules.

# Maintaining consistency in your project

Because the API and/or UI that your project provides forms the user-experience, you should aim for a consistent approach across

- Code layout
- Testing approaches
- UI patterns
- Naming

The most effective way to achieve this is to automate using GitHub status checks (or checks for equivalent platforms like BitBucket). Contributions can only
be accepted once they pass all of the tests.

For this process to be well-maintained and consistent, it needs to apply to the core contributors **and** to community contributors, see [Protecting branches](#protecting-branches) for guidance on
completing this.

## Choosing a linter

There are linters available for every language https://github.com/showcases/clean-code-linters

Your linter should ideally have

- The project-specific preferences stored inside the root of the project directory (e.g. .pylintrc files) in a way that the linter runs project practice
- Integration into your CI system, so when pull-requests are raised (see [Managing pull-requests](managing pull-requests.md))

It is up to you to decide the line between

- A restrictive toolset and a highly-consistent codebase
- A leniant toolset and a more approachable

The goal of your project is both consumption and contribution so decide on the appropriate mix. Remember, everyone has their own unique coding-style, there
are best-practices and there is code style, try not to mix concerns. 

## Using GitHub status checks

In an ideal workflow, a contributor and a core committer would

1. Fork the repository to a working repository
2. Clone the personal copy
3. Branch for their change (incase they later want to work on >1 change in parallel)
4. Make their changes
5. Push new branch to their personal repository
6. Request that new branch be merged into central repository (pull-request)
7. Code is automatically reviewed, tested and validated
8. Code is then manually reviewed and voted to merge
9. Code is merged.


### Protecting branches

With a linter, test automation and (potentially) automated integration tests, you want to ensure that someone can't just push code directly onto your master or develop branch. GitHub has a feature to protect
branches, used in combination with the required status checks feature.

Refer to this [GitHub guide](https://help.github.com/articles/working-with-protected-branches-and-required-status-checks/) on how to protect branches from those with git access to push directly to master.

Now everyone must follow the same process, you should ALWAYS have a secondary person review and merge your code contributions. There are plenty of ways to test forked repositories without it blocking you, don't setup
your process so that merging a PR into develop "just this once I'll do it myself" is ever an excuse.

### Requiring status checks

See [this guide](https://help.github.com/articles/enabling-required-status-checks/) on how to ensure that status checks pass before pull-requests can be merged.

https://help.github.com/articles/types-of-required-status-checks/

# Checklist

- [ ] - Project has a linter
- [ ] - Code linting is automated and integrated into GitHub
- [ ] - Status checks are enabled
- [ ] - master/develop/trunk branch is protected to stop individuals pushing direct
- [ ] - Status checks are restricted to ensure passing before merge


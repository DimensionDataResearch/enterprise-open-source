# Maintaining consistency in your project

Because the API and/or UI that your project provides forms the user-experience, you should aim for a consistent approach across

- Code layout
- Testing approaches
- UI patterns
- Naming

The most effective way to acheive this is to automate

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

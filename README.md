![hello](/assets/hello.png)

# Adventures in Git

Welcome to the world of [pull requests][GitHub-PrOverview]! Pull requests (or PRs) are how we propose changes to a codebase that allows for discussion, collaboration, and peer review. In this repository, we'll practice submitting and reviewing PRs in a way that is thoroughly Sparkbox.

## Getting Started

### Cloning the repository

To start, clone this repository to your local machine by running the following:

```sh
git clone git@github.com:sparkbox/apprenticeship-adventures-in-git.git
```

### Branching

Now that you have the repository, you can branch off into a [feature branch]. But what to name the branch? We'll need to name your feature branch something unique. Let's start by coming up with a prefix for the branch. Since we're adding some features to the repository, we can prefix it with `feat--` so developers who look at the branch know that this [adds a feature][Standard-NamingBranches]. But it's still not unique, so we're going to use both the current year and your first name. So, for example, if the current year was 2022 and your name was Jordan, your branch might be named `feat--2022-jordan`.

like this:

```sh
git checkout -b feat--2022-jordan
```

This command will tell git that you want to branch off of the current branch and name it `feat--2022-jordan`. But we need to link it to the remote, so we'll run the following command:

```sh
git push --set-upstream origin feat--2022-jordan
```

This is telling git that we want to push (`git push`) to a new upstream (`--set-upstream`) with the name of the remote (`origin`) and the name of the remote branch (`feat--2022-jordan`).

### Making your changes

Now that you're branched off of `main`, you can make all the changes you want! As you commit changes to this branch and push them up to the remote via `git push`, your changes will be isolated to your branch. This allows for easy peer review via opening pull requests. Now that you're branched off, let's talk challenges!

## Challenges

### Make changes on a feature branch

1. Your first challenge is to create a new markdown file under the current year directory in `about-the-apprentices`. The name of the file should be your first name (like `Jordan.md`). Copy the contents of `about-me.md` into this newly created file.
1. Fill out the sections that are currently encapsulated in backticks as a way to introduce yourself. Note that the backticks are there just to identify the sections you need to fill in and can be removed afterward.
1. Commit your changes using the Conventional Commits spec [we used at Sparkbox][Standard-CommitMessage]. This means that your commit message has to start with an appropriate subject (and optional emoji). If it doesn't the PR will fail its status checks.

### Submit a PR

1. [Open a PR][GitHub-OpenPR] on GitHub and [assign yourself to it][GitHub-AssignPr]. Find another apprentice who is available to review your PR and [request a review][GitHub-RequestReview] from them. During this process, your reviewer might ask for changes (if there are spelling mistakes, incorrectly named files, etc).
1. Once all issues are resolved and your PR has been approved, [squash your commits][To Squash or Not to Squash] into a single commit and push back up to the remote using the `--force-with-lease` option.
1. Once you push up your squashed branch, let your reviewer know so they can merge in your code.

### Review a PR

1. Review another apprentice's PR. Leave [review comments][GitHub-Reviews] as part of your review. Learn something new about a fellow apprentice? Have questions about their introduction? Posting review comments is a powerful collaboration style that we'll be using for the rest of the apprenticeship.
1. [Finish your PR review][GitHub-ReviewApprove] by either approving it or requesting changes. Let the reviewee know that the review has been completed.
1. If the PR is approved, wait for the reviewee to squash their commits (if necessary). Once the commits are ready to be merged into `main`, merge their code into `main` using the `--ff-only` flag (this is the [Sparkbox way][Standard-Merging] of merging code).

[GitHub-AssignPr]: https://docs.github.com/en/issues/tracking-your-work-with-issues/assigning-issues-and-pull-requests-to-other-github-users
[GitHub-ReviewApprove]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/approving-a-pull-request-with-required-reviews
[GitHub-OpenPR]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request
[GitHub-PrOverview]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests
[GitHub-RequestReview]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review
[GitHub-Reviews]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews
[To Squash or Not to Squash]: https://sparkbox.com/foundry/to_squash_or_not_to_squash
[feature branch]: https://docs.github.com/en/get-started/quickstart/github-flow
[forking repositories]: https://docs.github.com/en/get-started/quickstart/fork-a-repo
[Standard-CommitMessage]: https://github.com/sparkbox/standard/tree/main/code-style/git#the-art-of-the-commit-message
[Standard-NamingBranches]: https://github.com/sparkbox/standard/tree/main/code-style/git#naming-branches
[Standard-Merging]: https://github.com/sparkbox/standard/tree/main/code-style/git#the-sparkbox-git-flow

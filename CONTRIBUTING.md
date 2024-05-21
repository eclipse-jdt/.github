# Contributing to Eclipse JDT

Thanks for your interest in this project.

## Project description

The Eclipse JDT™ project provides plug-ins that implement a Java IDE supporting 
the development of any Java application, including Eclipse plug-ins. It adds a Java 
project nature and Java perspective to the Eclipse Workbench as well as a number of views, 
editors, wizards, builders and code merging and refactoring tools. The JDT project allows 
Eclipse to be a development environment for itself.

* https://projects.eclipse.org/projects/eclipse.jdt

## Developer resources

Information regarding source code management, builds, coding standards, and
more.

* https://projects.eclipse.org/projects/eclipse.jdt/developer

The project issues and source code are maintained in GitHub int the following projects: 
* https://github.com/eclipse-jdt/eclipse.jdt.core Java compiler, builder, etc.
* https://github.com/eclipse-jdt/eclipse.jdt.ui Java related UI components
* https://github.com/eclipse-jdt/eclipse.jdt.debug Java debugger implementation
* https://github.com/eclipse-jdt/eclipse.jdt JDT feature and releng stuff
* https://github.com/eclipse-jdt/eclipse.jdt.core.binaries used for performance tests only


Be sure to search for existing issues before you create a new one. Remember that
contributions are always welcome!

## Setting up GitHub account

Create an account at GitHub.com using the same email address used for eclipse account. 
In case you already have an Eclipse account add the email to your GitHub account using https://github.com/settings/emails

Add the GitHub account id to your eclipse account under social media links section. 
If you are already a commiter in any of the projects in the GitHub org, a mail containing invite to join 
that project's GitHub organisation will be sent within 2 hours. You need to accept the invite 
to gain committer status in the GitHub organisation

## Create an Eclipse Development Environment

[![Create Eclipse Development Environment for JDT](https://download.eclipse.org/oomph/www/setups/svg/JDT.svg)](https://www.eclipse.org/setups/installer/?url=https://raw.githubusercontent.com/eclipse-jdt/eclipse.jdt/master/org.eclipse.jdt.releng/JDTConfiguration.setup&show=true "Click to open Eclipse-Installer Auto Launch or drag onto your running installer's title area")

See also https://wiki.eclipse.org/Platform/How_to_Contribute

## Contributing a change

We generally use the [Fork and pull model](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/about-collaborative-development-models#fork-and-pull-model) for JDT development. 

Here are the steps:

1. If it is a new issue, create it in the appropriate repository (e.g. [here](https://github.com/eclipse-jdt/eclipse.jdt.core/issues) for compiler and [here](https://github.com/eclipse-jdt/eclipse.jdt.ui/issues) for UI)
2. Create a [fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository) of the repository in your GitHub account. 
3. Clone the original Eclispe project repo to your local machine
4. Add your fork as a remote on the local repo.
5. Create a **dedicated** local branch for your changes (like "issue_123")
6. Develop your changes and commit them to your newly created branch, **do not commit on master!**
7. For compiler fixes **regression test is mandatory**, for other fixed highly recommended.
8. Before opening PR, fetch latest changes from master and rebase your branch on latest master commit.
9. Open a pull request.  

    * Push the local branch from step 5 to your fork  
    * Go to the GitHub repo page (for example, https://github.com/eclipse-jdt/eclipse.jdt.ui). GitHub will detect that
you have pushed to your fork and will show a button offering you to "Compare & pull request". Alternatively, you 
can navigate to the repo's pull request page (https://github.com/eclipse-jdt/eclipse.jdt.ui/pulls) and 
press "New pull request"  
    * Request a review from one or more reviewers.

10. Address any review comments and commit any further changes to the branch from step 5 and 
push the branch to your fork. This will update the PR with those changes. Generally, you should add 
additional changes in separate PRs. It makes it easier to review just those new changes.

Sometimes a PRs cannot be automatically merged into master. In this case, a reviewer might ask you to rebase your 
PR branch and force-push it to your fork again.

### Commit message recommendations

The commit message should provide a concise description of the change and a link to the ticket. If a commit resolves an issue, 
the issue should be mentioned in the commit message like this:

> Check variable `foo` for null. Fixes \#27
  
GitHub picks it up when this commit is merged and will auto-close the issue being mentioned. If multiple commits are used in a PR, you can still autoclose the issue by mentioning the issue in the description of the PR see https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword
You should make sure that your PR description includes an issue reference anyway, since this will automatically link the
PR to the issue.

### Reviewing a change

1. You can look at a PR on the Github web site itself or fetch the PR using egit menu "Fetch github PR"
2. You can finish a review in three ways: 
    1. Approve: this means you are O.K. to merge this PR as is
    2. Comment: you neither approve nor reject the PR
    3. Request changes: changes need to be made before the PR can be merged. This blocks the merging of the PR.
3. Before approving and merging a PR make sure it passes any relevant PR checks (i.e. the ECA check CI build succeeds)
4. Once the PR is approved there two options to merge. You can select either of these based on the requirement the following are recommendations only. Need to select based on the requirement
    * Rebase and Merge (retains commit history from PR useful in developing a feature)
    * Squash and Merge (All commits in PR gets squashed in to a single commit useful in bug fixes)

### JDT.Core General Practices
In JDT.Core, committers follow a few additional general practices
 
Whenever there are mass cleanup commits please adhere to the following:
 
1. Please have [cleanup] in the subject of the issue and pr.
2. Please assign reviewers to these PRs [look at the code neighbourhood to “find” a committer who has changed/added code]
3. Please restrict the mass cleanups to only M1 milestone.
 
These are nothing new but just adapted to the github world.

## Eclipse Contributor Agreement

Before your contribution can be accepted by the project team contributors must
electronically sign the Eclipse Contributor Agreement (ECA).

* https://www.eclipse.org/legal/ECA.php

Commits that are provided by non-committers must have a Signed-off-by field in
the footer indicating that the author is aware of the terms by which the
contribution has been provided to the project. The non-committer must
additionally have an Eclipse Foundation account and must have a signed Eclipse
Contributor Agreement (ECA) on file.

For more information, please see the Eclipse Committer Handbook:
https://www.eclipse.org/projects/handbook/#resources-commit

## Contact

Contact the project developers via the project's "dev" list.

* https://dev.eclipse.org/mailman/listinfo/jdt-dev

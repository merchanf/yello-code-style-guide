# Git guidelines

## Workflow

1. We use the workflow designed by Vincent Driessen. This workflow is based on giving branches a role and each role has its own rules and ways to be pushed, modified, etc. Check the following links with further and better explained information.

- [Atlassian blog](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Original article](https://nvie.com/posts/a-successful-git-branching-model/)

2. Create or use one branch for one ticket. Never use a branch to develop more than one task.
   
3. Always squash your commits before pushing them.

### Naming

At the moment of a branch creations use the following conventions:

``` bash
git branch [ticket number]_[brief description]
```

the characters must be lowercase (except when needed i.e. acronyms), and the spaces replaced by hypens.

Examples.

``` bash
# bad
git branch feature/oc-399/awesome-feature-creation

# bad
git branch OC-399_AwesomeFeatureCreation

# good
git branch OC-399_awesome-feature-creation
```


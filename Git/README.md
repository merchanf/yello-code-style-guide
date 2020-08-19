# Git guidelines

## Workflow

We use the workflow designed by Vincent Driessen. This workflow is based on giving branches a role and each role has its own rules and ways to be pushed, modified, etc. Check the following links with further and better explained information.

- [Atlassian blog](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Original article](https://nvie.com/posts/a-successful-git-branching-model/)

### Scope

Create or use one branch for one ticket. Never use a branch to develop more than one task.

### Naming

At the moment of a branch creations use the following conventions:

      git branch [ticket number]-[brief description]

the name must be lowercase, and the spaces replaced by hypens.

Examples.

      # bad
      git branch feature/oc-399/awesome-feature-creation

      # bad
      git branch feature-OC-399-AwesomeFeatureCreation

      # good
      git branch oc-399-awesome-feature-creation

### Merging and pushing

Always squash your commits before pushing them.

# Ephemeral Environments

## Definition

Temporary deployments that have self-contained versions of your application, generally every feature branch.

**Uses**: Slack/ heroku / LayerCI

**Ephemeral environments are lined to github pull request**

## Benefits

1. Accelerate software development lifecycle
2. Allows developers to share changes with designers,
   managers and other stakeholders

# How do databases work in ephemeral environment

- Pre-populated Data
- Un-doable
- Migrated

# Ephemeral environment lifecycle management

1. Option A: Tie the lifecycle to the life of a pull request or merge request

2. Option B: create a chatOps bot that allows creating a new environment for specific branch with a small timeout

3. Option C: create a ephemeral environment for every commit and hibernate them the second they are provisioned, then wake them up as they are required

## Continuos Staging definition

CI/CD + Ephemeral Environment = unified CI/CD amd review process for every commit

## DIY ephemeral Environments

Budget 6-12 months of engineering time for setup, then dedicated person for managing these environment

Will need **cloud service provider**

Create a slackbot that responds to /env-created-for-mybranch with a link

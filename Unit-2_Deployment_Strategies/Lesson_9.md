# Blue / green deployments

## Definition

Strategy to deploy a new version of an application. They work by **starting an entirely new instance of the application and then routing traffic over to it**.

## Benefits

- Easy to understand
- Powerful
- Extendable to workflows

## Cons

- Difficult to make hotfixes
- Resource allocation is not convenient
- Clusters can affect each other

## Rainbow deployments

- Have more than the two deployment clusters.
- Old clusters would only be shut off after all of their long-running jobs are done processing.

## Acceptance Tests

- Useful for longer running releases like desktop app, mobile app
- New version is tested against the production database in the very environment which will be soon become production

- QA and stakeholders can choose to "accept" the developers team's latest release

## Canary Deployments

- Would be to route around 5% of users at random to the new clusters and check that those users do not have negative feedback.

## B/G Deployment

- **Fit**: deploying a few times per day
- **Unfit**: many services are being deployed many times per day

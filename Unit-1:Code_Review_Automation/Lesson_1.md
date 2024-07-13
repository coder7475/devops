## DevOps Definition

A methodology that helps engineering teams build products by continuosly getting user feedback.

---

### Stages in DevOps

- Plan
- Code
- Build
- Test
- Release
- Deploy
- Operate
- Monitor
- **Do it again!**

---

## DevOps Engineering Pillars

1. Pull Request Automation
2. Deployment Automation
3. Application Performance Management

---

### Pull Request Automation

- Developers share code changes using **git** tools like GitHub, GitLab and BitBucket
- A set of code changes in git tools is called a **"pull reques"** or **"merge request"**
- If pull requests are approved, the code changes can go into the main codebase

#### Git Definition

Git is used for cloud-based code chage collaboration. See the full history of code changes, review developer changes, and store code in files called repositories.

#### What can you automate?

- Continuous Integration (CI)
- Per change ephemeral environments
- Automated security scanning
- Notification to reviews

#### Goal as DevOps Engineer

Help developer change proposals get reviewed and merged within 24 hours of when they are made.

### Deployment Automation

- Deploy a feature to a certain set of users as a final test before rolling it out publically
- Starting new versions of services without causing downtime
- Rolling back to the prior version in case something does go wrong
- Some Off the selves solutions: Spinnaker, harness

### Application Performance Management

- Metrics: numeric measurements of key numbers in production
- Logging: text descriptions of what is happening during processing
- Monitoring: take metrics and logs to convert them into health metrics
- Alerting: If monitoring detects a problem, it notifies developer

## Examples of DevOps Engineering

**Scenario 1**: new startup with no users building a web application.

_Recomanded free stack:_

> GitHub  
>  Netifly/Vercel  
>  LayerCI

**Scenario 2**: Team building an application for 10 enterprise customers.

_Recomanded stack:_

> GitHub  
> Sentry  
> PagerDuty  
> CodeCov
> Bitrise/CircleCI

**Scenario 3**: Heavy traffic social media application like Reddit.

_Recomanded stack:_

> GitHub Enterprise  
> Sentry  
> ElasticSearch/Logstash/Kibana  
> Pingdom  
> Launch Darkly  
> Terraform
